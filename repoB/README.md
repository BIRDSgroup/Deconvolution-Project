# Deconvolution_Downstream analyses
This repository contains code used to investigate the downstream effects of applying cell-type deconvolution methods to brain transcriptomic data in Alzheimer's disease.

The project systematically evaluates how cell-type correction influences differential gene expression analyses and downstream biological interpretation across multiple brain regions and independent cohorts.

# Code and corresponding analysis overview

The repository includes code for the following analyses:

- Cell-type proportion represention across brain regions
- Differential gene expression before and after deconvolution
- Concordance between correction methods
- Marker gene enrichment analysis
- Functional enrichment analysis (GSEA)
- Cross-region DEG consistency analysis
- Alzheimer’s disease GWAS risk gene enrichment
- Cross-cohort comparison between **MSBB and ROSMAP**


# Requirements

The analysis was performed in RStudio Version 2022.07.1+554 (2022.07.1+554)

Required packages are mention in the scripts

Install missing packages using:

install.packages("package_name")


# Running the Analysis

Clone the repository:

git clone https://github.com/mitra-sanga/Deconvolution_Downstream.git

Open the project in RStudio and run the analysis scripts located in:

scripts/

All file paths are handled using the here() package, allowing the project to run without modifying file paths.


# Data Sources

Mount Sinai Brain Bank (MSBB) RNA-seq dataset

ROSMAP RNA-seq dataset

Open Targets GWAS risk loci for Alzheimer’s disease

Brain cell-type marker gene sets from published studies

# Author

Dr. Sanga Mitra
Senior Research Scientist
Department of Computer Science and Engineering
Indian Institute of Technology Madras

# License

This repository is provided for academic research purposes.
