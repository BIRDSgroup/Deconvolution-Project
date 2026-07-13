# Deconvolution_Main_Code

Scripts for cell-type deconvolution of bulk RNA-seq data from the MSBB and ROSMAP cohorts, including preprocessing, differential expression analysis, and pseudobulk generation from matched snRNA-seq data.

## Repository Structure

```
Deconvolution_Main_Code/
├── README.md
├── data/
├── MSBBBulk_preprocessing.R
├── ROSMAPBulk_preprocessing.R
├── runDEGs.R
├── celltype_deconvolution.R
├── runCIBERSORT.R
├── runDtangle.R
├── process_SCE_data.R
├── generate_celltype_pseudobulk_countmatrix.R
├── generate_simulatedbulk_countmatrix.R
├── ROSMAP24_pseudobulk_countmatrix_metadata.R
└── ROSMAP24_actual_celltype_proportions.R
```

## Requirements

The libraries required to run each script are mentioned within the scripts themselves.
R Version 4.2.2
RStudio 2022.07.1

##Data

A data/ folder contains some of the files used by the scripts in this repository. Other files can be downloaded from the synapse IDs mentioned in the manuscript. 

## Script Descriptions

### Preprocessing

- **`MSBBBulk_preprocessing.R`** — Preprocesses and classifies bulk RNA-seq samples as AD and CTL obtained from the MSBB cohort on the Synapse portal.
- **`ROSMAPBulk_preprocessing.R`** — Preprocesses and classifies bulk RNA-seq samples as AD and CTL obtained from the ROSMAP cohort on the Synapse portal.

### Differential Expression

- **`runDEGs.R`** — Identifies differentially expressed genes between AD and CTL samples across all cohorts.

### Cell Type Deconvolution

- **`celltype_deconvolution.R`** — Computes estimates of cell type proportions from an expression matrix and the MultiBrain signature matrix. Calls the `runCIBERSORT` and `runDtangle` methods.
- **`runCIBERSORT.R`** — CIBERSORT-based deconvolution method used by `celltype_deconvolution.R`.
- **`runDtangle.R`** — dtangle-based deconvolution method used by `celltype_deconvolution.R`.

### snRNA-seq Processing & Pseudobulk Generation (ROSMAP, 24 matched samples)

The following scripts process the snRNA-seq data from ROSMAP for the 24 samples matched to the bulk RNA-seq data, and generate pseudobulk count matrices:

- **`process_SCE_data.R`** — Processes the single-cell/single-nucleus experiment (SCE) data.
- **`generate_celltype_pseudobulk_countmatrix.R`** — Generates cell-type-level pseudobulk count matrices.
- **`generate_simulatedbulk_countmatrix.R`** — Generates simulated bulk count matrices.
- **`ROSMAP24_pseudobulk_countmatrix_metadata.R`** — Generates the pseudobulk count matrix and associated metadata for the 24 matched ROSMAP samples.
- **`ROSMAP24_actual_celltype_proportions.R`** — Actual cell type proportions for the 24 matched ROSMAP samples.
