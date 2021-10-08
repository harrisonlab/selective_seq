# Amplicon seq analysis

## Potato cyst nematode

### Remove adapters

```bash
# Run fastq-mcf
    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210720_M04543_0009_000000000-DBN4W/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
        sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
        echo $sampleID
        OutDir=qc_dna/paired/PCN/Plate1/$sampleID
        mkdir -p $OutDir
        Read_F=$fastq
        Read_R=$(echo $Read_F | sed 's/_R1_/_R2_/g')
        echo $Read_F;
        echo $Read_R;
        IluminaAdapters=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/illumina_full_adapters.fa
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
        sbatch -p himem $ProgDir/fastq-mcf.sh $Read_F $Read_R $IluminaAdapters DNA $OutDir
    done

    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210728_M04543_0011_000000000-DC78R/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
        sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
        echo $sampleID
        OutDir=qc_dna/paired/PCN/Plate2/$sampleID
        mkdir -p $OutDir
        Read_F=$fastq
        Read_R=$(echo $Read_F | sed 's/_R1_/_R2_/g')
        echo $Read_F;
        echo $Read_R;
        IluminaAdapters=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/illumina_full_adapters.fa
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
        sbatch -p himem $ProgDir/fastq-mcf.sh $Read_F $Read_R $IluminaAdapters DNA $OutDir
    done
```

### Classification using centrifuge (nt database)

Plate 1

```bash
    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210720_M04543_0009_000000000-DBN4W/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
    sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
    echo $sampleID
    mkdir -p analysis/Centrifuge/$sampleID
        for Read1 in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210720_M04543_0009_000000000-DBN4W/Data/Intensities/BaseCalls/"$sampleID"_*R1_001.fastq.gz); do
            Read2=$(echo $Read1 | sed 's/_R1_/_R2_/g')
            echo $Read1
            echo $Read2
            #Sample=$(echo $Read1 | rev | cut -f1 -d '/' | rev | sed 's/_S37_L001_R1_001.fastq.gz//g')
            #echo $Sample
            Database=../../../scratch/public_data/nt-centrifuge_12jan2021/nt
            OutDir=analysis/Centrifuge/$sampleID
            ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
            sbatch -p short $ProgDir/centrifuge.sh $Database $OutDir $Read1 $Read2
        done
    done
```

Plate 2 

```bash
    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210720_M04543_0009_000000000-DBN4W/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
    sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
    echo $sampleID
    #mkdir -p analysis/Centrifuge/$sampleID
        for Read1 in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210720_M04543_0009_000000000-DBN4W/Data/Intensities/BaseCalls/"$sampleID"_*R1_001.fastq.gz); do
            Read2=$(echo $Read1 | sed 's/_R1_/_R2_/g')
            echo $Read1
            echo $Read2
            #Sample=$(echo $Read1 | rev | cut -f1 -d '/' | rev | sed 's/_S37_L001_R1_001.fastq.gz//g')
            #echo $Sample
            Database=../../../scratch/public_data/nt-centrifuge_12jan2021/nt
            OutDir=analysis/Centrifuge/$sampleID
            ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
            sbatch -p short $ProgDir/centrifuge.sh $Database $OutDir $Read1 $Read2
        done
    done
```

