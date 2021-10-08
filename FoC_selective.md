# EPI2ME WIMP

## Selective seq FoC

#### Data organization

```bash
srun --partition himem --mem 10G --cpus-per-task 10 --pty bash

# First dataset
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode09/*.fastq | gzip > barcode09_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode10/*.fastq | gzip > barcode10_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode08/*.fastq | gzip > barcode08_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode07/*.fastq | gzip > barcode07_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode06/*.fastq | gzip > barcode06_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode05/*.fastq | gzip > barcode05_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode04/*.fastq | gzip > barcode04_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode03/*.fastq | gzip > barcode03_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode02/*.fastq | gzip > barcode02_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test2_S4/20200928_1648_X1_FAO37117_0347a639/fastq_pass/barcode01/*.fastq | gzip > barcode01_pass.fastq.gz

cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode01/*.fastq | gzip > barcode01_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode02/*.fastq | gzip > barcode02_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode03/*.fastq | gzip > barcode03_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode04/*.fastq | gzip > barcode04_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode05/*.fastq | gzip > barcode05_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode08/*.fastq | gzip > barcode08_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode09/*.fastq | gzip > barcode09_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode10/*.fastq | gzip > barcode10_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode11/*.fastq | gzip > barcode11_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/barcode12/*.fastq | gzip > barcode12_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/FOC-test1/20200914_1602_X1_FAN52950_a37c17d4/fastq_pass/unclassified/*.fastq | gzip > unclassified.fastq.gz
```

```bash
srun --partition himem --mem 10G --cpus-per-task 10 --pty bash

# Second dataset

cat  /archives/2020_niabemr_nanopore/S3D6/20201215_1453_X1_FAO27987_9702022c/fastq_pass/*.fastq | gzip > raw_data/S3D6_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-2/20201215_1645_X1_FAO27987_b2861159/fastq_pass/*.fastq | gzip > raw_data/S3D6-2_pass.fastq.gz

cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode01/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode01_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode02/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode02_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode03/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode03_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode04/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode04_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode05/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode05_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode06/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode06_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode07/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode07_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode08/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode08_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode09/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode09_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode10/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode10_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode11/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode11_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/barcode12/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/barcode12_pass.fastq.gz
cat  /archives/2020_niabemr_nanopore/S3D6-BC11_BC12_No_Selection/20201217_1441_X2_FAO27999_57821556/fastq_pass/unclassified/*.fastq | gzip > raw_data/S3D6-BC11_BC12_No_Selection/unclassified_pass.fastq.gz

cat  /archives/2020_niabemr_nanopore/S3_D6_readfish1/20201216_1220_X1_FAO27987_4cc4da2e/fastq_pass/*.fastq | gzip > raw_data/S3_D6_readfish1/S3_D6_readfish_pass.fastq.gz
```

## Count number of reads

```bash
# Count number of reads. Count all lines and divide it by 4.
for d in raw_data/*.fastq.gz ;do 
echo $d
echo $(zcat $d |wc -l)/4|bc
done
```

```
raw_data/S3D6-BC11_BC12_No_Selection/barcode01_pass.fastq.gz
10
raw_data/S3D6-BC11_BC12_No_Selection/barcode02_pass.fastq.gz
9
raw_data/S3D6-BC11_BC12_No_Selection/barcode03_pass.fastq.gz
43
raw_data/S3D6-BC11_BC12_No_Selection/barcode04_pass.fastq.gz
9
raw_data/S3D6-BC11_BC12_No_Selection/barcode05_pass.fastq.gz
8
raw_data/S3D6-BC11_BC12_No_Selection/barcode06_pass.fastq.gz
26
raw_data/S3D6-BC11_BC12_No_Selection/barcode07_pass.fastq.gz
14
raw_data/S3D6-BC11_BC12_No_Selection/barcode08_pass.fastq.gz
11
raw_data/S3D6-BC11_BC12_No_Selection/barcode09_pass.fastq.gz
15
raw_data/S3D6-BC11_BC12_No_Selection/barcode10_pass.fastq.gz
2
raw_data/S3D6-BC11_BC12_No_Selection/barcode11_pass.fastq.gz
910153
raw_data/S3D6-BC11_BC12_No_Selection/barcode12_pass.fastq.gz
1322587
raw_data/S3D6-BC11_BC12_No_Selection/unclassified_pass.fastq.gz
29044
raw_data/S3_D6_readfish1/S3_D6_readfish_pass.fastq.gz
9764274
raw_data/S3D6-2_pass.fastq.gz
11003176
raw_data/S3D6_pass.fastq.gz
125373
```

## Fusarium genomes db

```bash
# F.oxysporum
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum/fo47/ncbi_edits_repmask/fo47_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum/fo47/broad_repmask/fo47_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum/fo47_tgac_filtered/ncbi_edits_repmask/fo47_tgac_filtered_contigs_unmasked.fa

# F.oxysporum fsp cepae
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/55/ncbi_edits_repmask/55_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/55_tgac_filtered/ncbi_edits_repmask/55_tgac_filtered_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/125_ncbi/ncbi_submission/125_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/A13_ncbi/ncbi_submission/A13_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/A23_ncbi/ncbi_submission/A23_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/A28_ncbi/ncbi_submission/A28_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/CB3_ncbi/ncbi_submission/CB3_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/PG_ncbi/ncbi_submission/PG_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/Fus2_canu_new/edited_contigs_repmask/Fus2_canu_contigs_unmasked.fa

../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae_old/A1-2/filtered_contigs_repmask/A1-2_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae_old/D2/filtered_contigs_repmask/D2_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae_old/HB6/filtered_contigs_repmask/HB6_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae_old/HB17/filtered_contigs_repmask/HB17_contigs_unmasked.fa

# F.oxysporum fsp fragariae
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_fragariae/15-074/filtered_contigs/15-074_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_fragariae/Straw465/filtered_contigs/Straw465_contigs_unmasked.fa

# F.oxysporum fsp lactucae
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lactucae/AJ516/filtered_contigs/AJ516_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lactucae/AJ516/filtered_ncbi/AJ516_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lactucae/AJ520/filtered_contigs/AJ520_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lactucae/AJ520/filtered_ncbi/AJ520_contigs_unmasked.fa

# F.oxysporum fsp lycopersici
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lycopersici/4287_chromosomal/ensembl_repmask/4287_chromosomal_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lycopersici/4287_v2/fungidb_repmask/4287_v2_contigs_unmasked.fa

# F.oxysporum fsp mathioli
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_mathioli/Stocks4/filtered_contigs/Stocks4_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_mathioli/Stocks4/filtered_ncbi/Stocks4_contigs_unmasked.fa

# F.oxysporum narcissi
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/FON129/filtered_contigs/FON129_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/FON_63/filtered_contigs/FON_63_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/FON77/filtered_contigs/FON77_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/FON81/filtered_contigs/FON81_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/FON89/filtered_contigs/FON89_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/N139_ncbi/ncbi_submission/N139_contigs_unmasked.fa

# F.oxysporum fsp pisi
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/F81/filtered_contigs/F81_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/FOP1/filtered_contigs_repmask/FOP1_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/FOP1-EMR/filtered_contigs/FOP1-EMR_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/FOP2/filtered_contigs_repmask/FOP2_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/FOP5/filtered_contigs_repmask/FOP5_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/PG18/filtered_contigs_repmask/PG18_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/PG3/filtered_contigs_repmask/PG3_contigs_unmasked.fa
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_pisi/PG3/filtered_contigs_repmask/PG3_contigs_unmasked.fa

# F.oxysporum fsp statice
../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_statice/Stat10/filtered_contigs/Stat10_contigs_unmasked.fa
```

## Quast and BUSCO of ref genomes

```bash
for Strain in 55; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in fo47; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in N139_ncbi; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in Fus2_canu_new; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/edited_contigs_repmask/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in 15-074 Straw465 AJ516 AJ520 Stocks4 FON129 FON_63 FON77 FON81 FON89 F81 R2 Stat10; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in 4287_chromosomal; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lycopersici/$Strain/ensembl_repmask/4287_chromosomal_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
for Strain in FOP1 FOP2 FOP5 PG18 PG3; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs_repmask/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev)
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) 
echo $Assembly
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain
sbatch -p himem $ProgDir/quast.sh $Assembly $OutDir
done
done
```

```bash
for Strain in 55; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p short $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p short $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in fo47; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p short $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in N139_ncbi; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/ncb*/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p short $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in Fus2_canu_new; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/edited_contigs_repmask/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p long $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in 15-074 Straw465 AJ516 AJ520 Stocks4 FON129 FON_63 FON77 FON81 FON89 F81 R2 Stat10; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p long $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in 4287_chromosomal; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_lycopersici/$Strain/ensembl_repmask/4287_chromosomal_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p long $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
for Strain in FOP1 FOP2 FOP5 PG18 PG3; do
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Assembly_qc
for Assembly in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs_repmask/*_contigs_unmasked.fa); do
Strain=$(echo $Assembly| rev | cut -d '/' -f3 | rev) # Edit to set your ouput directory
Organism=$(echo $Assembly | rev | cut -d '/' -f4 | rev) # Edit to set your ouput directory
echo "$Organism - $Strain"
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Gene_prediction
BuscoDB=$(ls -d /projects/dbBusco/sordariomycetes_odb10)
OutDir=gene_pred/BUSCO/F.oxysporum_REF/$Organism/$Strain/busco_sordariomycetes_obd10
sbatch -p long $ProgDir/busco.sh $Assembly $BuscoDB $OutDir
done
done
```



## S3D6_readfish run (unblocked file test)

Reads from the unblocked_reads_id.txt file were extracted from the fastq reads

```bash
# Extract reads from fastq using a list of read IDs
/scratch/software/seqtk/seqtk subseq raw_data/S3_D6_readfish1/S3D6_readfish.fastq /archives/2020_niabemr_nanopore/S3_D6_readfish1/20201216_1220_X1_FAO27987_4cc4da2e/unblocked_read_ids.txt > WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads.fq
# Count number of reads
echo $(cat WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads.fq |wc -l)/4|bc
9381818
# Read lenght
awk '{if(NR%4==2) print length($1)}' WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads.fq | sort -n | uniq -c > WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_read_length.txt
```
```r
# Plot histogram read lenght
reads<-read.csv(file="WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")
```

```bash
/scratch/software/seqkit/seqkit seq -m 1000 WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads.fq > WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads_filtered.fq
echo $(cat WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads_filtered.fq |wc -l)/4|bc

gzip WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads_filtered.fq
for Read1 in $(ls WIMP_analysis/S3D6_readfish/S3D6_readfish_unblocked_reads_filtered.fq.gz); do
Database=Foxysporum
OutDir=analysis/Kraken/filtered_1kb/S3D6_readfish_unblocked
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
sbatch $ProgDir/kraken_long_reads.sh $Read1 $Database $OutDir
done
```

## S3D6_readfish run

```bash
awk '{if(NR%4==2) print length($1)}' raw_data/S3_D6_readfish1/S3_D6_readfish_pass.fastq.gz | sort -n | uniq -c > WIMP_analysis/S3D6_readfish/S3D6_readfish_read_length.txt
reads<-read.csv(file="WIMP_analysis/S3D6_readfish/S3D6_readfish_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")

/scratch/software/seqkit/seqkit seq -m 1000 raw_data/S3D6-2_pass.fastq.gz  > raw_data/S3D6-2_filtered.fq
echo $(cat raw_data/S3D6-2_filtered.fq |wc -l)/4|bc

/scratch/software/seqkit/seqkit seq -m 1000 raw_data/S3_D6_readfish1/S3_D6_readfish_pass.fastq.gz > raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
echo $(cat raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz|wc -l)/4|bc
awk '{if(NR%4==2) print length($1)}' raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz | sort -n | uniq -c > WIMP_analysis/S3D6_readfish/S3D6_readfish_read_length.txt
reads<-read.csv(file="WIMP_analysis/S3D6_readfish/S3D6_readfish_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")

gzip filtered.fq
mv filtered.fq.gz raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz



awk '{if(NR%4==2) print length($1)}' raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz | sort -n | uniq -c > WIMP_analysis/S3D6_readfish/S3D6_readfish_filtered_read_length.txt
reads<-read.csv(file="WIMP_analysis/S3D6_readfish/S3D6_readfish_filtered_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")

gzip filtered.fq
mv filtered.fq.gz raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz

# Number of reads and bases
gzip -dc raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number of reads: "c; 
                print "Number of bases in reads: "l
              }' 

Number of reads: 8599
Number of bases in reads: 40259061

gzip -dc raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number input bases"
                print l
              }' > raw_data/S3_D6_readfish1/S3D6_readfish_filtered_numberbases.txt
```

#### Kraken2

```bash
for Read1 in $(ls raw_data/S3_D6_readfish1/S3D6_readfish_filtered.fg.gz); do
Database=Foxysporum
OutDir=analysis/Kraken/filtered_1kb/S3D6_readfish
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
sbatch -p long $ProgDir/kraken_long_reads.sh $Read1 $Database $OutDir
done
```

#### Minimap2

```bash
# Fo
for Strain in fo47 fo47_tgac_filtered; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/Fo/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ed*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp fragariae
for Strain in 15-074 Straw465; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoF/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoL/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal 4287_v2; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoLy/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoM/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89 N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoP/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp statice
for Strain in Stat10; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=filtered.fq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/$R1/FoS/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

mv genome_alignment/minimap2/S3D6_readfish_filtered/ genome_alignment/minimap2/filtered/
```

#### Alignment statistics

```bash
srun --partition long --mem-per-cpu 6G --cpus-per-task 10 --pty bash

for alignment in $(ls genome_alignment/minimap2/filtered/S3D6_readfish_filtered/F*/vs*/*aligned_sorted.bam); do
R1=$(echo $alignment | rev | cut -f2 -d '/' | rev | sed 's/vs_//g')
echo $R1
Org=$(echo $alignment | rev | cut -f3 -d '/' | rev)
echo $Org
picard CollectAlignmentSummaryMetrics -AS -I $alignment -O $(dirname $alignment)/"$Org"_"$R1".stats.txt
for h in $(ls $(dirname $alignment)/*.stats.txt); do
less $h | tail -n +7 | head -2 | cut -f 3,6,8,9,10,11 > $(dirname $alignment)/"$Org"_"$R1".stats_values.txt
done
# total number of bases mapped (how many times a base is mapped)
bedtools genomecov -ibam $alignment -d > $(dirname $alignment)/"$Org"_"$R1"_depth.txt
for i in $(ls $(dirname $alignment)/*_depth.txt); do
awk '{s+=$3}END{print s}' $i > $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
done
# total number of bases in ref that have been mapped
bedtools genomecov -ibam $alignment -bg > $(dirname $alignment)/"$Org"_"$R1"_BedGraph.txt
for f in $(ls $(dirname $alignment)/*_BedGraph.txt); do
awk '{ s+=($3-$2) } END { print s }' $f > $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_REF_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
done
paste $(dirname $alignment)/"$Org"_"$R1".stats_values.txt $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt raw_data/S3_D6_readfish1/S3D6_readfish_filtered_numberbases.txt > $(dirname $alignment)/"$Org"_"$R1"_results.txt
echo ""$R1" done"
done
```

## S3D6-2 run

```bash
# Read lenght
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-2_pass.fastq.gz | sort -n | uniq -c > WIMP_analysis/S3D6-2/S3D6-2_read_length.txt


/scratch/software/seqkit/seqkit seq -m 1000 raw_data/S3D6-2_pass.fastq.gz  > raw_data/S3D6-2_filtered.fq
echo $(cat raw_data/S3D6-2_filtered.fq |wc -l)/4|bc
25436
# Read lenght
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-2_filtered.fq | sort -n | uniq -c > WIMP_analysis/S3D6-2/S3D6-2_filtered_read_length.txt
```
```r
# Plot histogram read lenght
reads<-read.csv(file="WIMP_analysis/S3D6-2/S3D6-2_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")

reads<-read.csv(file="WIMP_analysis/S3D6-2/S3D6-2_filtered_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")
```


```bash
gzip S3D6-2_filtered.fq
mv S3D6-2_filtered.fq.gz raw_data/S3D6-2_filtered.fq.gz

# Number of reads and bases
gzip -dc raw_data/S3D6-2_filtered.fq.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number of reads: "c; 
                print "Number of bases in reads: "l
              }' 

Number of reads: 25436
Number of bases in reads: 99678044

gzip -dc raw_data/S3D6-2_filtered.fq.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number input bases"
                print l
              }' > raw_data/S3D6-2_filtered_numberbases.txt
```


#### Kraken

```bash
for Read1 in $(ls raw_data/S3D6-2_filtered.fq.gz); do
     Out=$(echo $Read1 | rev | cut -f1 -d '/' | rev | sed 's/_filtered.fq.gz//g')
     echo $Out
     Database=Foxysporum
     OutDir=analysis/Kraken/filtered_1kb/$Out
     mkdir -p $OutDir
     ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
     sbatch $ProgDir/kraken_long_reads.sh $Read1 $Database $OutDir
done
```

#### Minimap2

```bash
# Fo
for Strain in fo47 fo47_tgac_filtered; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/Fo/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoC/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp fragariae
for Strain in 15-074 Straw465; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoF/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoL/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal 4287_v2; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoLy/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoM/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89 N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoN/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoP/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp statice
for Strain in Stat10; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoS/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### Alignment statistics

```bash
srun --partition long --mem-per-cpu 6G --cpus-per-task 10 --pty bash
conda activate SNP_calling_v2

for alignment in $(ls genome_alignment/minimap2/filtered/S3D6-2_filtered/F*/vs*/*aligned_sorted.bam); do
R1=$(echo $alignment | rev | cut -f2 -d '/' | rev | sed 's/vs_//g')
echo $R1
Org=$(echo $alignment | rev | cut -f3 -d '/' | rev)
echo $Org
picard CollectAlignmentSummaryMetrics -AS -I $alignment -O $(dirname $alignment)/"$Org"_"$R1".stats.txt
for h in $(ls $(dirname $alignment)/*.stats.txt); do
less $h | tail -n +7 | head -2 | cut -f 3,6,8,9,10,11 > $(dirname $alignment)/"$Org"_"$R1".stats_values.txt
done
# total number of bases mapped (how many times a base is mapped)
bedtools genomecov -ibam $alignment -d > $(dirname $alignment)/"$Org"_"$R1"_depth.txt
for i in $(ls $(dirname $alignment)/*_depth.txt); do
awk '{s+=$3}END{print s}' $i > $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
done
# total number of bases in ref that have been mapped
bedtools genomecov -ibam $alignment -bg > $(dirname $alignment)/"$Org"_"$R1"_BedGraph.txt
for f in $(ls $(dirname $alignment)/*_BedGraph.txt); do
awk '{ s+=($3-$2) } END { print s }' $f > $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_REF_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
done
paste $(dirname $alignment)/"$Org"_"$R1".stats_values.txt $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt raw_data/S3D6-2_filtered_numberbases.txt > $(dirname $alignment)/"$Org"_"$R1"_results.txt
echo ""$R1" done"
done
```


## No selection run

```bash
# Read lenght
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-BC11_BC12_No_Selection/barcode11_pass.fastq.gz  | sort -n | uniq -c > WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode11_raw_read_length.txt
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-BC11_BC12_No_Selection/barcode12_pass.fastq.gz | sort -n | uniq -c > WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode12_raw_read_length.txt

# Filter read smaller than 1kb

/scratch/software/seqkit/seqkit seq -m 1000 raw_data/S3D6-BC11_BC12_No_Selection/barcode11_pass.fastq.gz  > raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq
echo $(cat raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq |wc -l)/4|bc
689768

/scratch/software/seqkit/seqkit seq -m 1000 raw_data/S3D6-BC11_BC12_No_Selection/barcode12_pass.fastq.gz  > raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq
echo $(cat raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq |wc -l)/4|bc
933468

# Read lenght
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq | sort -n | uniq -c > WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode11_filtered_read_length.txt
awk '{if(NR%4==2) print length($1)}' raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq | sort -n | uniq -c > WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode12_filtered_read_length.txt
```
```r
# Plot histogram read lenght
reads<-read.csv(file="WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode11_raw_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")
reads<-read.csv(file="WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode12_raw_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")

# Plot histogram read lenght
reads<-read.csv(file="WIMP_analysis/S3D6-BC11_BC12_No_Selection/barcode12_filtered_read_length.txt", sep="", header=FALSE)
plot (reads$V2,reads$V1,type="l",xlab="read length",ylab="occurences",col="blue")
```

```bash
gzip raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq 
gzip raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq

# Number of reads and bases
gzip -dc raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz  |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number of reads: "c; 
                print "Number of bases in reads: "l
              }' 

Number of reads: 689768
Number of bases in reads: 4049766750

gzip -dc raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz  |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number of reads: "c; 
                print "Number of bases in reads: "l
              }' 

Number of reads: 933468
Number of bases in reads: 5302619831

gzip -dc raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number input bases"
                print l
              }' > raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered_numberbases.txt

gzip -dc raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz |
     awk 'NR%4==2{c++; l+=length($0)}
          END{
                print "Number input bases"
                print l
              }' > raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered_numberbases.txt
```

#### Kraken

```bash
    for Read1 in $(ls raw_data/S3D6-BC11_BC12_No_Selection/barcode1*_filtered.fq.gz); do
        Out=$(echo $Read1 | rev | cut -f1 -d '/' | rev | sed 's/_filtered.fq.gz//g')
        echo $Out
        Database=Foxysporum
        OutDir=analysis/Kraken/filtered_1kb/$Out
        mkdir -p $OutDir
        ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Metagenomics
        sbatch $ProgDir/kraken_long_reads.sh $Read1 $Database $OutDir
    done
```

### barcode11

```bash
# Fo
for Strain in fo47 fo47_tgac_filtered; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/Fo/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoC/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp fragariae
for Strain in 15-074 Straw465; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoF/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoL/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal 4287_v2; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoLy/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoM/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89 N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoN/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoP/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# F.oxysporum fsp statice
for Strain in Stat10; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoS/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### Alignment statistics

```bash
srun --partition long --mem-per-cpu 6G --cpus-per-task 10 --pty bash
conda activate SNP_calling_v2

for alignment in $(ls genome_alignment/minimap2/filtered/barcode11/F*/vs*/*aligned_sorted.bam); do
R1=$(echo $alignment | rev | cut -f2 -d '/' | rev | sed 's/vs_//g')
echo $R1
Org=$(echo $alignment | rev | cut -f3 -d '/' | rev)
echo $Org
picard CollectAlignmentSummaryMetrics -AS -I $alignment -O $(dirname $alignment)/"$Org"_"$R1".stats.txt
for h in $(ls $(dirname $alignment)/*.stats.txt); do
less $h | tail -n +7 | head -2 | cut -f 3,6,8,9,10,11 > $(dirname $alignment)/"$Org"_"$R1".stats_values.txt
done
# total number of bases mapped (how many times a base is mapped)
bedtools genomecov -ibam $alignment -d > $(dirname $alignment)/"$Org"_"$R1"_depth.txt
for i in $(ls $(dirname $alignment)/*_depth.txt); do
awk '{s+=$3}END{print s}' $i > $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
done
# total number of bases in ref that have been mapped
bedtools genomecov -ibam $alignment -bg > $(dirname $alignment)/"$Org"_"$R1"_BedGraph.txt
for f in $(ls $(dirname $alignment)/*_BedGraph.txt); do
awk '{ s+=($3-$2) } END { print s }' $f > $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_REF_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
done
paste $(dirname $alignment)/"$Org"_"$R1".stats_values.txt $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered_numberbases.txt > $(dirname $alignment)/"$Org"_"$R1"_results.txt
echo ""$R1" done"
done
```

### barcode12

```bash
# Fo
for Strain in fo47 fo47_tgac_filtered; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/Fo/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 55 55_tgac_filtered 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoC/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp fragariae
for Strain in 15-074 Straw465; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoF/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoL/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal 4287_v2; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoLy/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoM/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89 N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoN/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP1-EMR FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoP/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done


# F.oxysporum fsp statice
for Strain in Stat10; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered/$R1/FoS/vs_"$Strain"
sbatch -p long $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### Alignment statistics

```bash
srun --partition long --mem-per-cpu 6G --cpus-per-task 10 --pty bash
conda activate SNP_calling_v2

for alignment in $(ls genome_alignment/minimap2/filtered/barcode12/F*/vs*/*aligned_sorted.bam); do
R1=$(echo $alignment | rev | cut -f2 -d '/' | rev | sed 's/vs_//g')
echo $R1
Org=$(echo $alignment | rev | cut -f3 -d '/' | rev)
echo $Org
picard CollectAlignmentSummaryMetrics -AS -I $alignment -O $(dirname $alignment)/"$Org"_"$R1".stats.txt
for h in $(ls $(dirname $alignment)/*.stats.txt); do
less $h | tail -n +7 | head -2 | cut -f 3,6,8,9,10,11 > $(dirname $alignment)/"$Org"_"$R1".stats_values.txt
done
# total number of bases mapped (how many times a base is mapped)
bedtools genomecov -ibam $alignment -d > $(dirname $alignment)/"$Org"_"$R1"_depth.txt
for i in $(ls $(dirname $alignment)/*_depth.txt); do
awk '{s+=$3}END{print s}' $i > $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt
done
# total number of bases in ref that have been mapped
bedtools genomecov -ibam $alignment -bg > $(dirname $alignment)/"$Org"_"$R1"_BedGraph.txt
for f in $(ls $(dirname $alignment)/*_BedGraph.txt); do
awk '{ s+=($3-$2) } END { print s }' $f > $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
sed -i '1s/^/BEDTOOLS_REF_BASES_MAPPED\n/' $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt
done
paste $(dirname $alignment)/"$Org"_"$R1".stats_values.txt $(dirname $alignment)/"$Org"_"$R1"_bases_aligned.txt $(dirname $alignment)/"$Org"_"$R1"_ref_bases_aligned.txt raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered_numberbases.txt > $(dirname $alignment)/"$Org"_"$R1"_results.txt
echo ""$R1" done"
done
```


for filename in S3D6_readfish_filtered/*/*/*results.txt; do
echo "$filename"
cat "$filename"
done > S3D6_readfish_filtered.temp.txt
