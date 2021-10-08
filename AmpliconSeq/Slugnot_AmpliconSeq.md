# Amplicon seq analysis

## Slugbot analysis

### Remove adapters

```bash
    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210624_M04543_0008_000000000-DBMTB/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
        sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
        echo $sampleID
        OutDir=qc_dna/paired/Slugbot/$sampleID
        mkdir -p $OutDir
        Read_F=$fastq
        Read_R=$(echo $Read_F | sed 's/_R1_/_R2_/g')
        echo $Read_F;
        echo $Read_R;
        IluminaAdapters=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/illumina_full_adapters.fa
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
        sbatch -p short $ProgDir/fastq-mcf.sh $Read_F $Read_R $IluminaAdapters DNA $OutDir
    done

# Run fastqc
    for Strain in 16S-AA01 16S-AA02 16S-AA03 16S-AA04 16S-AA05 16S-AA06 16S-AA07 16S-AA08 16S-AA09 16S-AA10; do
    #for Strain in 16S-AJ01 16S-AJ02 16S-AJ03 16S-AJ04 16S-AJ05 16S-AJ06 16S-AJ07 16S-AJ08 16S-AJ09 16S-AJ10 16S-AJ11 16S-AJ12 16S-AJ13 16S-AJ14 16S-AJ15 16S-AJ16; do
    #for Strain in 16S-ASLUG01 16S-ASLUG02 16S-ASLUG03 16S-ASLUG04 16S-ASLUG05 16S-ASLUG06 16S-ASLUG07 16S-ASLUG08 16S-ASLUG09 16S-ASLUG10 16S-ASLUG11 16S-ASLUG12 16S-ASLUG13 16S-ASLUG14 16S-ASLUG15 16S-ASLUG16 16S-ASLUG17 16S-ASLUG18 16S-ASLUG19 16S-ASLUG20 16S-ASLUG21 16S-ASLUG24; do
    #for Strain in 16S-DIN01 16S-DIN02 16S-DIN03 16S-DIN04 16S-GF01 16S-GF02 16S-GF03 16S-GF04 16S-GF05; do
    #for Strain in CO-AJ11 COI-AA03 COI-AJ04 COI-AJ05 COI-AJ09 COI-AJ10 COI-AJ12 COI-AJ13 COI-AJ14; do
    #for Strain in COI-ASLUG16 COI-ASLUG3 COI-ASLUG6 COI-ASLUG8 COI-DIN04 COI-GF01 COI-GF02 COI-GF03 COI-GF04 COI-GF05; do
        RawData=$(ls qc_dna/paired/Slugbot/$Strain/F/*trim.fq.gz)
        echo $RawData;
        OutDir=$(dirname $RawData)
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
        sbatch $ProgDir/fastqc.sh $RawData $OutDir
    done
```

```bash
# Remove adapters and smaller than 60bp reads
    for fastq in $(ls ../../../archives/2021_camb_miseq/ANALYSIS/210624_M04543_0008_000000000-DBMTB/Data/Intensities/BaseCalls/*R1_001.fastq.gz); do
        sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
        echo $sampleID
        OutDir=qc_dna/paired/Slugbot_vTrim/$sampleID
        mkdir -p $OutDir
        Read_F=$fastq
        Read_R=$(echo $Read_F | sed 's/_R1_/_R2_/g')
        echo $Read_F;
        echo $Read_R;
        IluminaAdapters=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/illumina_full_adapters.fa
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
        sbatch -p short $ProgDir/fastq-mcf_edited.sh $Read_F $Read_R $IluminaAdapters DNA $OutDir
    done
```

```bash
# Test trimmomatic to remove adapters. Not used.
    for Strain in COI-ASLUG16 COI-ASLUG3 COI-ASLUG6 COI-ASLUG8 COI-DIN04 COI-GF01 COI-GF02 COI-GF03 COI-GF04 COI-GF05; do
    Read_F=qc_dna/paired/Slugbot/$Strain/F/*trim.fq.gz
    Read_R=qc_dna/paired/Slugbot/$Strain/R/*trim.fq.gz
    echo $Read_F;
    echo $Read_R;
    IluminaAdapters=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/illumina_full_adapters.fa
    ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc
    sbatch $ProgDir/trimmomatic.sh $Read_F $Read_R $IluminaAdapters qc_dna/paired/noprimers_trimmomatic/$Strain
    done
```

### Classification using centrifuge (nt database)


```bash
    for fastq in $(ls qc_dna/paired/Slugbot/16S-ASLUG07/*/*R1_001_trim.fq.gz); do
    sampleID=$(echo $fastq | rev | cut -f1 -d '/' | rev | sed 's/_S.*//g')
    echo $sampleID
    OutDir=analysis/Centrifuge/Slugbot/$sampleID
    mkdir -p $OutDir
        for Read1 in $(ls qc_dna/paired/Slugbot/*/*/"$sampleID"_*R1_001_trim.fq.gz); do
            Read2=qc_dna/paired/Slugbot/*/R/"$sampleID"_*R2_001_trim.fq.gz
            echo $Read1
            echo $Read2
            #Sample=$(echo $Read1 | rev | cut -f1 -d '/' | rev | sed 's/_S37_L001_R1_001.fastq.gz//g')
            #echo $Sample
            Database=../../../scratch/public_data/nt-centrifuge_12jan2021/nt
            ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
            sbatch -p himem $ProgDir/centrifuge.sh $Database $OutDir $Read1 $Read2
        done
    done

    for kraken in $(ls analysis/Centrifuge/Slugbot/*/centrifuge_krakened.txt); do
        ID=$(echo $kraken | rev | cut -f2 -d '/' | rev )
        echo $ID
        echo $ID > "$ID".txt
        cat $kraken | awk '$4 == "S" { print $0 }' | head -1 > analysis/Centrifuge/Slugbot/stat_"$ID".txt
        paste analysis/Centrifuge/Slugbot/stat_"$ID".txt "$ID".txt > analysis/Centrifuge/Slugbot/"$ID"_stats.txt
        rm analysis/Centrifuge/Slugbot/stat_"$ID".txt
        rm "$ID".txt
    done

    cat analysis/Centrifuge/Slugbot/*_stats.txt > analysis/Centrifuge/Slugbot/Slug_top_hits.txt
```


### Cut primers

Tools to remove primers were tested here

```bash
python /home/gomeza/git_repos/scripts/bioinformatics_tools/SEQdata_qc/cutPrimers.py -r1 16S-AA01/F/16S-AA01_S42_L001_R1_001_trim.fq.gz -r2 16S-AA01/R/16S-AA01_S42_L001_R2_001_trim.fq.gz -pr15 16SAR.fasta -pr25 16SBR.fasta -tr1 1_r1_trimmed.fastq.gz -tr2 1_r2_trimmed.fastq.gz -utr1 1_r1_untrimmed.fastq.gz -utr2 1_r2_untrimmed.fastq.gz -t 2 -err 30

cutadapt -a "TCGTCGGCAGCGTCAGATGTGTATAAGAGACAGCGCCTGTTTAWCAAAAACATX;max_error_rate=0.2;min_overlap=5" -A "GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAGCCGGTYTGAACTCAGATCAGATCAYGTX;max_error_rate=0.2;min_overlap=5" -o out.1.fastq -p out.2.fastq 16S-AA01/F/16S-AA01_S42_L001_R1_001_trim.fq.gz 16S-AA01/R/16S-AA01_S42_L001_R2_001_trim.fq.gz

cutadapt -a TCGTCGGCAGCGTCAGATGTGTATAAGAGACAGCGCCTGTTTAWCAAAAACATX -A GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAGCCGGTYTGAACTCAGATCAGATCAYGTX -o out.1.fastq -p out.2.fastq 16S-AA01/F/16S-AA01_S42_L001_R1_001_trim.fq.gz 16S-AA01/R/16S-AA01_S42_L001_R2_001_trim.fq.gz

cutadapt -u 30 -U 30 -o out.1.fastq -p out.2.fastq 16S-AA01/F/16S-AA01_S42_L001_R1_001_trim.fq.gz 16S-AA01/R/16S-AA01_S42_L001_R2_001_trim.fq.gz
```