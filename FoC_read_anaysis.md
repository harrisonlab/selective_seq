# Selective sequencing. Analysis FoC genomes 

### Extract mapped reads and read headers

```bash
screen -a
srun --partition long --mem-per-cpu 20G --cpus-per-task 10 --pty bash

    for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new 15-074 Straw465 AJ516 AJ520 4287_chromosomal 4287_v2 Stocks4 FON129 FON_63 FON77 FON81 fo47 fo47_tgac_filtered FON89 N139_ncbi F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3 Stat10; do
        for file in $(ls genome_alignment/minimap2/filtered/*/*/vs_"$Strain"/*_aligned_sorted.bam ); do
            Data=$(echo $file | rev | cut -f4 -d '/' | rev)
            Org=$(echo $file | rev | cut -f3 -d '/' | rev)
            echo "$Data"_"$Org"
            echo $file
            samtools view -F4 $file -o $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads.bam
            samtools view $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads.bam | cut -f1 | LC_ALL=C sort | uniq > $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_read_ID.txt
        done
    done
```
```bash
    for file in */*/barcode*mapped_reads.bam; do
        echo $file
        samtools view -F4 $file | cut -f1 | LC_ALL=C sort | uniq | wc -l
    done

for file in */*/*vs*read_ID.txt; do
echo $file
less $file | wc -l
done
# Sanity check. All good
```

### Extract unique reads of FoC Fus2


```bash
# barcode11
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal 4287_v2 Stocks4 FON129 FON_63 FON77 FON81 fo47 fo47_tgac_filtered FON89 N139_ncbi F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3 Stat10; do
    for file in $(ls genome_alignment/minimap2/filtered/barcode11/*/vs_"$Strain"/*vs*_read_ID.txt); do
        Data=$(echo $file | rev | cut -f4 -d '/' | rev)
        Org=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Data"_"$Org"
        echo $file
        OutDir=genome_alignment/minimap2/filtered/Fus2_uniq_reads/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 genome_alignment/minimap2/filtered/barcode11/FoC/vs_Fus2_canu_new/barcode11_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
    done
done
# barcode12
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal 4287_v2 Stocks4 FON129 FON_63 FON77 FON81 fo47 fo47_tgac_filtered FON89 N139_ncbi F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3 Stat10; do
    for file in $(ls genome_alignment/minimap2/filtered/barcode12/*/vs_"$Strain"/*vs*_read_ID.txt); do
        Data=$(echo $file | rev | cut -f4 -d '/' | rev)
        Org=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Data"_"$Org"
        echo $file
        OutDir=genome_alignment/minimap2/filtered/Fus2_uniq_reads/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 genome_alignment/minimap2/filtered/barcode12/FoC/vs_Fus2_canu_new/barcode12_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
    done
done
# S3D6-2_filtered
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal 4287_v2 Stocks4 FON129 FON_63 FON77 FON81 fo47 fo47_tgac_filtered FON89 N139_ncbi F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3 Stat10; do
    for file in $(ls genome_alignment/minimap2/filtered/S3D6-2_filtered/*/vs_"$Strain"/*vs*_read_ID.txt); do
        Data=$(echo $file | rev | cut -f4 -d '/' | rev)
        Org=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Data"_"$Org"
        echo $file
        OutDir=genome_alignment/minimap2/filtered/Fus2_uniq_reads/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 genome_alignment/minimap2/filtered/S3D6-2_filtered/FoC/vs_Fus2_canu_new/S3D6-2_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
    done
done
# S3D6_readfish_filtered
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal 4287_v2 Stocks4 FON129 FON_63 FON77 FON81 fo47 fo47_tgac_filtered FON89 N139_ncbi F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3 Stat10; do
    for file in $(ls genome_alignment/minimap2/filtered/S3D6_readfish_filtered/*/vs_"$Strain"/*vs*_read_ID.txt); do
        Data=$(echo $file | rev | cut -f4 -d '/' | rev)
        Org=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Data"_"$Org"
        echo $file
        OutDir=genome_alignment/minimap2/filtered/Fus2_uniq_reads/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 genome_alignment/minimap2/filtered/S3D6_readfish_filtered/FoC/vs_Fus2_canu_new/S3D6_readfish_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
    done
done
```

```bash
    for d in $(ls genome_alignment/minimap2/filtered/Fus2_uniq_reads/*/*uniq.txt); do
        echo $d
        less $d | wc -l
    done
```

```bash
# Create file with file name and number of reads
    for f in *uniq.txt ; do 
    { echo "$f" ; cat $f | wc -l ; } > $f.tmp
    done
    paste *.tmp > final_S3D6_readfish.txt
```

### Count shared read IDs

```bash
# for S3D6-2, barcode 11 and S3D6-readfish
comm -12 Fus2_vs_FoC_A28_ncbi_uniq.txt Fus2_vs_FoF_Straw465_uniq.txt | comm -12 - Fus2_vs_FoN_FON129_uniq.txt | comm -12 - Fus2_vs_FoP_F81_uniq.txt | comm -12 - Fus2_vs_FoC_55_uniq.txt | comm -12 - Fus2_vs_FoP_PG3_uniq.txt | comm -12 - Fus2_vs_FoC_125_ncbi_uniq.txt | comm -12 - Fus2_vs_FoC_CB3_ncbi_uniq.txt | comm -12 - Fus2_vs_FoL_AJ516_uniq.txt | comm -12 - Fus2_vs_FoN_FON_63_uniq.txt | comm -12 - Fus2_vs_FoP_FOP1-EMR_uniq.txt | comm -12 - Fus2_vs_FoS_Stat10_uniq.txt | comm -12 - Fus2_vs_FoC_PG_ncbi_uniq.txt | comm -12 - Fus2_vs_FoL_AJ520_uniq.txt | comm -12 - Fus2_vs_FoN_FON77_uniq.txt | comm -12 - Fus2_vs_FoP_FOP1_uniq.txt | comm -12 - Fus2_vs_FoF_15-074_uniq.txt | comm -12 - Fus2_vs_FoLy_4287_chromosomal_uniq.txt | comm -12 - Fus2_vs_FoN_FON81_uniq.txt | comm -12 - Fus2_vs_FoP_FOP2_uniq.txt | comm -12 - Fus2_vs_FoC_A13_ncbi_uniq.txt | comm -12 - Fus2_vs_FoLy_4287_v2_uniq.txt | comm -12 - Fus2_vs_FoN_FON89_uniq.txt | comm -12 - Fus2_vs_FoP_FOP5_uniq.txt | comm -12 - Fus2_vs_FoC_A23_ncbi_uniq.txt | comm -12 - Fus2_vs_Fo_fo47_uniq.txt | comm -12 - Fus2_vs_FoM_Stocks4_uniq.txt | comm -12 - Fus2_vs_FoN_N139_ncbi_uniq.txt | comm -12 - Fus2_vs_FoP_PG18_uniq.txt
# for barcode12
comm -12 Fus2_vs_FoC_A28_ncbi_uniq.txt Fus2_vs_FoF_Straw465_uniq.txt | comm -12 - Fus2_vs_FoN_FON129_uniq.txt | comm -12 - Fus2_vs_FoP_F81_uniq.txt | comm -12 - Fus2_vs_FoC_55_uniq.txt | comm -12 - Fus2_vs_FoP_PG3_uniq.txt | comm -12 - Fus2_vs_FoC_125_ncbi_uniq.txt | comm -12 - Fus2_vs_FoC_CB3_ncbi_uniq.txt | comm -12 - Fus2_vs_FoL_AJ516_uniq.txt | comm -12 - Fus2_vs_FoN_FON_63_uniq.txt | comm -12 - Fus2_vs_FoP_FOP1-EMR_uniq.txt | comm -12 - Fus2_vs_FoC_PG_ncbi_uniq.txt | comm -12 - Fus2_vs_FoL_AJ520_uniq.txt | comm -12 - Fus2_vs_FoN_FON77_uniq.txt | comm -12 - Fus2_vs_FoP_FOP1_uniq.txt | comm -12 - Fus2_vs_FoF_15-074_uniq.txt | comm -12 - Fus2_vs_FoLy_4287_chromosomal_uniq.txt | comm -12 - Fus2_vs_FoN_FON81_uniq.txt | comm -12 - Fus2_vs_FoP_FOP2_uniq.txt | comm -12 - Fus2_vs_FoC_A13_ncbi_uniq.txt | comm -12 - Fus2_vs_FoLy_4287_v2_uniq.txt | comm -12 - Fus2_vs_FoN_FON89_uniq.txt | comm -12 - Fus2_vs_FoP_FOP5_uniq.txt | comm -12 - Fus2_vs_FoC_A23_ncbi_uniq.txt | comm -12 - Fus2_vs_Fo_fo47_uniq.txt | comm -12 - Fus2_vs_FoM_Stocks4_uniq.txt | comm -12 - Fus2_vs_FoN_N139_ncbi_uniq.txt | comm -12 - Fus2_vs_FoP_PG18_uniq.txt
```

## fsp analysis

### List of all reads per fsp

```bash
mv FoC/vs_55_tgac_filtered/ FoC/Unknown_vs_55_tgac_filtered/
cat FoC/vs*/*vs*_read_ID.txt > FoC/all_FoC_reads.txt
cat FoC/all_FoC_reads.txt | LC_ALL=C sort | uniq > FoC/all_FoC_reads.uniq.txt
cat FoL/vs*/*vs*_read_ID.txt > FoL/all_FoL_reads.txt
cat FoL/all_FoL_reads.txt | LC_ALL=C sort | uniq > FoL/all_FoL_reads.uniq.txt
cat FoN/vs*/*vs*_read_ID.txt > FoN/all_FoN_reads.txt
cat FoN/all_FoN_reads.txt | LC_ALL=C sort | uniq > FoN/all_FoN_reads.uniq.txt
cat FoP/vs*/*vs*_read_ID.txt > FoP/all_FoP_reads.txt
cat FoP/all_FoP_reads.txt | LC_ALL=C sort | uniq > FoP/all_FoP_reads.uniq.txt
cat FoF/vs*/*vs*_read_ID.txt > FoF/all_FoF_reads.txt
cat FoF/all_FoF_reads.txt | LC_ALL=C sort | uniq > FoF/all_FoF_reads.uniq.txt
cat FoLy/vs*/*vs*_read_ID.txt > FoLy/all_FoLy_reads.txt
cat FoLy/all_FoLy_reads.txt | LC_ALL=C sort | uniq > FoLy/all_FoLy_reads.uniq.txt

cp barcode11/FoM/vs_Stocks4/barcode11_vs_FoM_Stocks4_read_ID.txt barcode11/FoM/all_FoM_reads.uniq.txt
cp barcode11/Fo/vs_fo47/barcode11_vs_Fo_fo47_read_ID.txt barcode11/Fo/all_Fo_reads.uniq.txt
cp barcode11/FoS/vs_Stat10/barcode11_vs_FoS_Stat10_read_ID.txt barcode11/FoS/all_FoS_reads.uniq.txt
cp barcode12/FoM/vs_Stocks4/barcode12_vs_FoM_Stocks4_read_ID.txt barcode12/FoM/all_FoM_reads.uniq.txt
cp barcode12/Fo/vs_fo47/barcode12_vs_Fo_fo47_read_ID.txt barcode12/Fo/all_Fo_reads.uniq.txt
cp barcode12/FoS/vs_Stat10/barcode12_vs_FoS_Stat10_read_ID.txt barcode12/FoS/all_FoS_reads.uniq.txt
cp S3D6-2_filtered/FoM/vs_Stocks4/S3D6-2_filtered_vs_FoM_Stocks4_read_ID.txt S3D6-2_filtered/FoM/all_FoM_reads.uniq.txt
cp S3D6-2_filtered/Fo/vs_fo47/S3D6-2_filtered_vs_Fo_fo47_read_ID.txt S3D6-2_filtered/Fo/all_Fo_reads.uniq.txt
cp S3D6-2_filtered/FoS/vs_Stat10/S3D6-2_filtered_vs_FoS_Stat10_read_ID.txt S3D6-2_filtered/FoS/all_FoS_reads.uniq.txt
cp S3D6_readfish_filtered/FoM/vs_Stocks4/S3D6_readfish_filtered_vs_FoM_Stocks4_read_ID.txt S3D6_readfish_filtered/FoM/all_FoM_reads.uniq.txt
cp S3D6_readfish_filtered/Fo/vs_fo47/S3D6_readfish_filtered_vs_Fo_fo47_read_ID.txt S3D6_readfish_filtered/Fo/all_Fo_reads.uniq.txt
cp S3D6_readfish_filtered/FoS/vs_Stat10/S3D6_readfish_filtered_vs_FoS_Stat10_read_ID.txt S3D6_readfish_filtered/FoS/all_FoS_reads.uniq.txt
```


### Extract unique reads of FoC

```bash
    for file in $(ls barcode11/*/*_reads.uniq.txt); do
        Org=$(echo $file | rev | cut -f2 -d '/' | rev)
        Data=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Org"
        echo $file
        OutDir=Fus2_uniq_reads/fsp_analysis/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 barcode11/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
    done

    for file in $(ls barcode12/*/*_reads.uniq.txt); do
        Org=$(echo $file | rev | cut -f2 -d '/' | rev)
        Data=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Org"
        echo $file
        OutDir=Fus2_uniq_reads/fsp_analysis/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 barcode12/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
    done

    for file in $(ls S3D6_readfish_filtered/*/*_reads.uniq.txt); do
        Org=$(echo $file | rev | cut -f2 -d '/' | rev)
        Data=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Org"
        echo $file
        OutDir=Fus2_uniq_reads/fsp_analysis/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 S3D6_readfish_filtered/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
    done

    for file in $(ls S3D6-2_filtered/*/*_reads.uniq.txt); do
        Org=$(echo $file | rev | cut -f2 -d '/' | rev)
        Data=$(echo $file | rev | cut -f3 -d '/' | rev)
        echo "$Org"
        echo $file
        OutDir=Fus2_uniq_reads/fsp_analysis/$Data
        mkdir -p $OutDir
        LC_ALL=C comm -23 S3D6-2_filtered/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
    done
```


```bash
    for d in $(ls Fus2_uniq_reads/*/*/*uniq.txt); do
        echo $d
        less $d | wc -l
    done
```

```bash
# Create file with file name and number of reads
for f in *uniq.txt ; do 
{ echo "$f" ; cat $f | wc -l ; } > $f.tmp
done
paste *.tmp > barcode11_unique.txt

for f in *uniq.txt ; do 
{ echo "$f" ; cat $f | wc -l ; } > $f.tmp
done
paste *.tmp > barcode12_unique.txt

for f in *uniq.txt ; do 
{ echo "$f" ; cat $f | wc -l ; } > $f.tmp
done
paste *.tmp > S3D6-2_filtered_unique.txt

for f in *uniq.txt ; do 
{ echo "$f" ; cat $f | wc -l ; } > $f.tmp
done
paste *.tmp > S3D6_readfish_filtered_unique.txt
```


```bash
# Create a list with FoC unique reads ID on each seq run
cd genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode11
comm -12 FoC_vs_FoF_uniq.txt FoC_vs_FoL_uniq.txt | comm -12 - FoC_vs_FoLy_uniq.txt | comm -12 - FoC_vs_FoM_uniq.txt | comm -12 - FoC_vs_FoN_uniq.txt | comm -12 - FoC_vs_FoP_uniq.txt | comm -12 - FoC_vs_FoS_uniq.txt | comm -12 - FoC_vs_Fo_uniq.txt > FoC_unique_reads.txt

cd genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3D6-2_filtered
comm -12 FoC_vs_FoF_uniq.txt FoC_vs_FoL_uniq.txt | comm -12 - FoC_vs_FoLy_uniq.txt | comm -12 - FoC_vs_FoM_uniq.txt | comm -12 - FoC_vs_FoN_uniq.txt | comm -12 - FoC_vs_FoP_uniq.txt | comm -12 - FoC_vs_FoS_uniq.txt | comm -12 - FoC_vs_Fo_uniq.txt > FoC_unique_reads.txt

cd genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3_D6_readfish1
comm -12 FoC_vs_FoF_uniq.txt FoC_vs_FoL_uniq.txt | comm -12 - FoC_vs_FoLy_uniq.txt | comm -12 - FoC_vs_FoM_uniq.txt | comm -12 - FoC_vs_FoN_uniq.txt | comm -12 - FoC_vs_FoP_uniq.txt | comm -12 - FoC_vs_FoS_uniq.txt | comm -12 - FoC_vs_Fo_uniq.txt > FoC_unique_reads.txt

cd genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode12
comm -12 FoC_vs_FoF_uniq.txt FoC_vs_FoL_uniq.txt | comm -12 - FoC_vs_FoLy_uniq.txt | comm -12 - FoC_vs_FoM_uniq.txt | comm -12 - FoC_vs_FoN_uniq.txt | comm -12 - FoC_vs_FoP_uniq.txt | comm -12 - FoC_vs_Fo_uniq.txt > FoC_unique_reads.txt
```

```bash
# Extract FoC unique reads on each seq run
/scratch/software/seqtk/seqtk subseq raw_data/S3D6-2_filtered.fq genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3D6-2_filtered/FoC_unique_reads.txt > genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3D6-2_filtered/S3D6-2_filtered_FoC_unique.fq
/scratch/software/seqtk/seqtk subseq raw_data/S3_D6_readfish1/S3D6_readfish.fastq genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3D6_readfish_filtered/FoC_unique_reads.txt > genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/S3D6_readfish_filtered/S3D6_readfish_filtered_FoC_unique.fq
/scratch/software/seqtk/seqtk subseq raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode11/FoC_unique_reads.txt > genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode11/barcode11_FoC_unique.fq
/scratch/software/seqtk/seqtk subseq raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode12/FoC_unique_reads.txt > genome_alignment/minimap2/filtered/Fus2_uniq_reads/fsp_analysis/barcode12/barcode12_FoC_unique.fq
```



```bash
for Bam in $(ls genome_alignment/minimap2/filtered/*/FoC/vs_Fus2_canu_new/*aligned_sorted.bam); do
Strain=$(echo $Bam | rev | cut -f2 -d '/' | rev)
Organism=$(echo $Bam | rev | cut -f3 -d '/' | rev)
Reads=$(echo $Bam | rev | cut -f3 -d '/' | rev)
echo "$Organism - $Strain - $Reads"
OutDir=$(dirname $Bam)/coverage
mkdir -p $OutDir
samtools depth -aa $Bam > $OutDir/${Organism}_${Strain}_vs_${Reads}_depth.tsv
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
$ProgDir/cov_by_window.py --cov $OutDir/${Organism}_${Strain}_vs_${Reads}_depth.tsv > $OutDir/${Organism}_${Strain}_vs_${Reads}_depth_10kb.tsv
sed -i "s/$/\t$Strain/g" $OutDir/${Organism}_${Strain}_vs_${Reads}_depth_10kb.tsv
done


less genome_alignment/minimap2/filtered/S3D6-2_filtered/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb.tsv | sed 's/vs_Fus2_canu_new/S3D6-2_vs_Fus2/g' > genome_alignment/minimap2/filtered/S3D6-2_filtered/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb_edited.tsv 

less genome_alignment/minimap2/filtered/S3D6_readfish_filtered/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb.tsv | sed 's/vs_Fus2_canu_new/S3D6_readfish_vs_Fus2/g' > genome_alignment/minimap2/filtered/S3D6_readfish_filtered/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb_edited.tsv 

less genome_alignment/minimap2/filtered/barcode11/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb.tsv | sed 's/vs_Fus2_canu_new/barcode11_vs_Fus2/g' > genome_alignment/minimap2/filtered/barcode11/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb_edited.tsv 

less genome_alignment/minimap2/filtered/barcode12/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb.tsv | sed 's/vs_Fus2_canu_new/barcode12_vs_Fus2/g' > genome_alignment/minimap2/filtered/barcode12/FoC/vs_Fus2_canu_new/coverage/FoC_vs_Fus2_canu_new_vs_FoC_depth_10kb_edited.tsv 

OutDir=genome_alignment/minimap2/filtered/Fus2coverage/grouped
mkdir -p $OutDir
cat genome_alignment/minimap2/filtered/*/FoC/vs_Fus2_canu_new/coverage/*_depth_10kb_edited.tsv  > $OutDir/Fus2_grouped_depth.tsv
```

```r
#Plot coverage of each isolate against the R0905 reference genome.
library(readr)
df_R0905 <- read_delim("Fus2_grouped_depth.tsv", "\t", escape_double = FALSE, col_names = FALSE, col_types = cols(X4 = col_factor(levels = c("S3D6-2_vs_Fus2", "S3D6_readfish_vs_Fus2", "barcode11_vs_Fus2", "barcode12_vs_Fus2"))), trim_ws = TRUE)
myFun <- function(x) {
c(min = min(x), max = max(x),
mean = mean(x), median = median(x),
std = sd(x))
}
colnames(df_R0905) <- c("contig","position", "depth", "strain")
df_R0905$treatment <- paste(df_R0905$strain , df_R0905$contig)
tapply(df_R0905$depth, df_R0905$treatment, myFun)
df2 <- cbind(do.call(rbind, tapply(df_R0905$depth, df_R0905$treatment, myFun)))
write.csv(df2, 'Fus2_contig_coverage.csv')
df_R0905$depth <- ifelse(df_R0905$depth > 100, 100, df_R0905$depth)
# install.packages("ggplot2")
library(ggplot2)
require(scales)
for (i in 1:50){
contig = paste("contig", i, sep = "_")
p0 <- ggplot(data=df_R0905[df_R0905$contig == contig, ], aes(x=`position`, y=`depth`, group=1)) +
geom_line() +
labs(x = "Position (bp)", y = "Coverage") +
scale_y_continuous(breaks=seq(0,100,25), limits=c(0,100)) +
facet_wrap(~strain, nrow = 28, ncol = 1, strip.position = "left")
outfile = paste("R0905_contig", i, "cov.jpg", sep = "_")
ggsave(outfile , plot = p0, device = 'jpg', path = NULL,
scale = 1, width = 500, height = 500, units = 'mm',
dpi = 150, limitsize = TRUE)
}


library(ggplot2)
require(scales)
for (i in 1:50){
contig = paste("contig", i, sep = "_")
p0 <- ggplot(data=df_Hg199[df_Hg199$contig == contig, ], aes(x=`position`, y=`depth`, group=1)) +
geom_line() +
labs(x = "Position (bp)", y = "Coverage") +
scale_y_continuous(breaks=seq(0,100,25), limits=c(0,100)) +
facet_wrap(~strain, nrow = 28, ncol = 1, strip.position = "left")
outfile = paste("Hg199_contig", i, "cov.jpg", sep = "_")
ggsave(outfile , plot = p0, device = 'jpg', path = NULL,
scale = 1, width = 500, height = 500, units = 'mm',
dpi = 150, limitsize = TRUE)
}