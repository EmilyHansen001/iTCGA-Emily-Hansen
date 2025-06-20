# iTCGA-Emily-Hansen
This project is a part of the Summer 2025 ITCGA: Integrated Training in Computational Genomics and Data Sciences. We studied the effect of MNP AMF (magnetic nanoparticle with alternating magnetic field) therapy on Ovarian Cancer Cells. We performed differential gene expression analysis to determine which genes were upregulated and downregulated after recieving treatment. The scripts included in this repository were used to run the RNA sequence data in bash to allow us to anlayze and form conclusions about the therapy on Ovarian Cancer Cells. 

Project Overview
- Magnetic hyperthermia (MHT) is a thermal cancer treatment using magnetic nanoparticles (MNPs)
- When exposed to an alternating magnetic field (AMF), MNPs generate heat to:
  - Destroy cancer cells via apoptosis (programmed cell death)
  - Minimize damage to surrounding healthy tissue
- Effectiveness depends on:
  - High accumulation of MNPs within tumors
  - Tumors’ poor heat dissipation due to abnormal vasculature
- This study explores the genomic effects of MHT in ovarian cancer cells.
  - Focused on how the intracellular microenvironment impacts MHT outcomes
  - Cancer cells' disorganized cytoskeleton enhances MNP heat generation compared to normal cells

---
RNA-seq Analysis Pipeline on Chimera Cluster

- Download FastQ Files
  - Used sratoolkit and a custom fastq-dump.sh script to download sequencing data from SRA

- Quality Control
  - Assessed read quality using FastQC

- Adapter Trimming
  - Removed Illumina adapters and low-quality bases using cutadapt
  - Employed SLURM scripts for batch trimming

- Data Alignment & Expression Analysis
    - Aligning reads to a reference genome
    - Quantifying gene expression
    - Identifying differentially expressed genes between treatment groups
