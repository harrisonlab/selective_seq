## Minimap2 

This analysis was repeated using the latest version of mimimap2 (2.22) and to fix some errors found in the stats

#### S3D6_readfish_filtered

```bash
# Fo
for Strain in fo47; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/Fo/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in 55; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp..cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp fragariae
for Strain in 15-074 Straw465; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoF/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoL/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoLy/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoM/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoP/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp statice
for Strain in Stat10; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3_D6_readfish1/S3_D6_readfish_filtered2.fastq.gz
R1=S3D6_readfish_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoS/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### S3D6-2

```bash
# Fo
for Strain in fo47; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/Fo/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/edited_contigs_repmask/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in 55; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoF/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoL/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoLy/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoM/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-2_filtered.fq.gz
R1=S3D6-2_filtered
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoP/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoS/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### barcode11

```bash
# Fo
for Strain in fo47; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/Fo/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/edited_contigs_repmask/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in 55; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoF/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoL/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoLy/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoM/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode11_filtered.fq.gz
R1=barcode11
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoP/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoS/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```

#### barcode12

```bash
# Fo
for Strain in fo47; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/ncb*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/Fo/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo cepae
for Strain in 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in Fus2_canu_new; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_cepae/$Strain/edited_contigs_repmask/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in 55; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_f.sp.cepae/$Strain/nc*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoC/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoF/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lactucae
for Strain in AJ516 AJ520; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoL/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo lycopersici
for Strain in 4287_chromosomal; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoLy/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# Fo mathioli
for Strain in Stocks4; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoM/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum narcissi
for Strain in FON129 FON_63 FON77 FON81 FON89; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/filtered_contigs/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

for Strain in N139_ncbi; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/F.oxysporum_fsp_narcissi/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoN/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done

# F.oxysporum fsp pisi
for Strain in F81 FOP1 FOP2 FOP5 PG18 PG3; do
for Reference in $(ls ../oldhome/groups/harrisonlab/project_files/fusarium/repeat_masked/*/$Strain/*/*_contigs_unmasked.fa); do
echo $Reference
Read=raw_data/S3D6-BC11_BC12_No_Selection/barcode12_filtered.fq.gz
R1=barcode12
echo $R1
ProgDir=/home/gomeza/git_repos/scripts/bioinformatics_tools/Genome_aligners
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoP/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
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
OutDir=genome_alignment/minimap2/filtered_VP/$R1/FoS/vs_"$Strain"
sbatch -p short $ProgDir/minimap2.sh $Reference $Read $OutDir
done
done
```


#### Alignment statistics

```bash
for alignment in $(ls genome_alignment/minimap2/filtered_VP/barcode11/F*/vs*/*aligned_sorted.bam); do
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

for alignment in $(ls genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/F*/vs*/*aligned_sorted.bam); do
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

for alignment in $(ls genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/F*/vs*/*aligned_sorted.bam); do
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

for alignment in $(ls genome_alignment/minimap2/filtered_VP/barcode11/F*/vs*/*aligned_sorted.bam); do
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

for alignment in $(ls genome_alignment/minimap2/filtered_VP/barcode12/F*/vs*/*aligned_sorted.bam); do
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

tail -n +1 genome_alignment/minimap2/filtered_VP/barcode11/*/*/*_results.txt > genome_alignment/minimap2/filtered_VP/barcode11/barcode11_all.txt
tail -n +1 genome_alignment/minimap2/filtered_VP/barcode12/*/*/*_results.txt > genome_alignment/minimap2/filtered_VP/barcode12/barcode12_all.txt
tail -n +1 genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/*/*/*_results.txt > genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/S3D6-2_filtered_all.txt
tail -n +1 genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/*/*/*_results.txt > genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/S3D6_readfish_filtered_all.txt
```


# Selective sequencing. Analysis FoC genomes 

### Extract mapped reads and read headers

```bash
screen -a
srun --partition long --mem-per-cpu 20G --cpus-per-task 10 --pty bash

for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi Fus2_canu_new 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/barcode12/*/vs_"$Strain"/*_aligned_sorted.bam ); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
#samtools view -F4 $file -o $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads.bam
#samtools view -F260 $file -o $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_primarly_reads.bam
#samtools view $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads.bam | cut -f1 | LC_ALL=C sort | uniq > $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_read_ID.txt
#samtools view $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_primarly_reads.bam | cut -f1 | LC_ALL=C sort | uniq > $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_read_ID_primarly.txt
samtools view -F4 $file -q 30 -o $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads_Q30.bam
samtools view $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_mapped_reads_Q30.bam | cut -f1 | LC_ALL=C sort | uniq > $(dirname $file)/"$Data"_vs_"$Org"_"$Strain"_read_ID_Q30.txt
done
done


for file in genome_alignment/minimap2/filtered_VP/*/*/vs_Fus2*/*vs*read_ID_Q30.txt; do
echo $file
less $file | wc -l
done
```






```bash
# S3D6_readfish_filtered
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/*/vs_"$Strain"/*vs*_read_ID.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/FoC/vs_Fus2_canu_new/S3D6_readfish_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# barcode11
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/barcode11/*/vs_"$Strain"/*vs*_read_ID.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/barcode11/FoC/vs_Fus2_canu_new/barcode11_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# barcode12
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/barcode12/*/vs_"$Strain"/*vs*_read_ID.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/barcode12/FoC/vs_Fus2_canu_new/barcode12_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# S3D6-2_filtered
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/*/vs_"$Strain"/*vs*_read_ID.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/FoC/vs_Fus2_canu_new/S3D6-2_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done

for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/S3D6_readfish_filtered/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/S3D6-2_filtered/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/barcode11/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads/barcode12/*txt;do echo $f ; less $f | wc -l ; done



# S3D6_readfish_filtered
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/*/vs_"$Strain"/*vs*_read_ID_Q30.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/S3D6_readfish_filtered/FoC/vs_Fus2_canu_new/S3D6_readfish_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# barcode11
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/barcode11/*/vs_"$Strain"/*vs*_read_ID_Q30.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/barcode11/FoC/vs_Fus2_canu_new/barcode11_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# barcode12
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/barcode12/*/vs_"$Strain"/*vs*_read_ID_Q30.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/barcode12/FoC/vs_Fus2_canu_new/barcode12_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done
# S3D6-2_filtered
for Strain in 55 125_ncbi A13_ncbi A23_ncbi A28_ncbi CB3_ncbi PG_ncbi 15-074 Straw465 AJ516 AJ520 4287_chromosomal Stocks4 FON129 FON_63 FON77 FON81 fo47 FON89 N139_ncbi F81 FOP1 FOP2 FOP5 PG18 PG3 Stat10; do
for file in $(ls genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/*/vs_"$Strain"/*vs*_read_ID_Q30.txt); do
Data=$(echo $file | rev | cut -f4 -d '/' | rev)
Org=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Data"_"$Org"
echo $file
OutDir=genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 genome_alignment/minimap2/filtered_VP/S3D6-2_filtered/FoC/vs_Fus2_canu_new/S3D6-2_filtered_vs_FoC_Fus2_canu_new_read_ID.txt $file > $OutDir/Fus2_vs_"$Org"_"$Strain"_uniq.txt
done
done

for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/S3D6_readfish_filtered/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/S3D6-2_filtered/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/barcode11/*txt;do echo $f ; less $f | wc -l ; done
for f in genome_alignment/minimap2/filtered_VP/Fus2_uniq_reads_Q30/barcode12/*txt;do echo $f ; less $f | wc -l ; done
```



## fsp analysis

### List of all reads per fsp

```bash
cat Fo/vs*/*vs*_read_ID.txt > Fo/all_Fo_reads.txt
cat Fo/all_Fo_reads.txt | LC_ALL=C sort | uniq > Fo/all_Fo_reads.uniq.txt
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
cat FoS/vs*/*vs*_read_ID.txt > FoS/all_FoS_reads.txt
cat FoS/all_FoS_reads.txt | LC_ALL=C sort | uniq > FoS/all_FoS_reads.uniq.txt
```


### Extract unique reads of FoC

```bash
for file in $(ls barcode11/*/*_reads.uniq.txt); do
Org=$(echo $file | rev | cut -f2 -d '/' | rev)
Data=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Org"
echo $file
OutDir=fsp_analysis/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 barcode11/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
done

for file in $(ls barcode12/*/*_reads.uniq.txt); do
Org=$(echo $file | rev | cut -f2 -d '/' | rev)
Data=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Org"
echo $file
OutDir=fsp_analysis/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 barcode12/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
done

for file in $(ls S3D6_readfish_filtered/*/*_reads.uniq.txt); do
Org=$(echo $file | rev | cut -f2 -d '/' | rev)
Data=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Org"
echo $file
OutDir=fsp_analysis/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 S3D6_readfish_filtered/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
done

for file in $(ls S3D6-2_filtered/*/*_reads.uniq.txt); do
Org=$(echo $file | rev | cut -f2 -d '/' | rev)
Data=$(echo $file | rev | cut -f3 -d '/' | rev)
echo "$Org"
echo $file
OutDir=fsp_analysis/$Data
mkdir -p $OutDir
LC_ALL=C comm -23 S3D6-2_filtered/FoC/all_FoC_reads.uniq.txt $file > $OutDir/FoC_vs_"$Org"_uniq.txt
done
```


```bash
for d in $(ls fsp_analysis/*/*uniq.txt); do
echo $d
less $d | wc -l
done
```