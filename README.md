# STAT 3660 Project: LGG Tumor Subtype Classification

## Overview
This project was completed as part of STAT 3660: Data Visualization and Mining.

The goal is to analyze gene expression data from the TCGA Lower Grade Glioma (LGG) dataset and build a complete data analysis workflow, including data loading, cleaning, validation, and preprocessing for further analysis and modelling.

---
```
## Project Structure

STAT3660_Project/
│
├── STAT3660_Project.Rproj
├── README.md
├── .gitignore
│
├── report/
│   └── STAT_PROJECT.Rmd
│
├── data/
│   └── lgg_tcga_pan_can_atlas_2018/
│       ├── data_clinical_patient.txt
│       ├── data_clinical_sample.txt
│       └── data_mrna_seq_v2_rsem.txt
│
├── output/        
├── R/             

```

---

## Dataset

Source: cBioPortal for Cancer Genomics  
Dataset: Brain Lower Grade Glioma (TCGA, PanCancer Atlas)

## Data Source

The dataset used in this project is from cBioPortal:

Brain Lower Grade Glioma (TCGA, PanCancer Atlas)

To reproduce the analysis:

1. Go to: https://www.cbioportal.org/
2. Search: "Brain Lower Grade Glioma (TCGA, PanCancer Atlas)"
3. Download the full dataset (.tar.gz)
4. Extract it into the `data/` folder

Expected structure:
data/lgg_tcga_pan_can_atlas_2018/

File used:
lgg_tcga_pan_can_atlas_2018.tar.gz

The dataset includes:
- Clinical patient data
- Clinical sample data
- mRNA expression data (RSEM normalized expected counts)

---

## Methods

### Data Cleaning
- Removed redundant variables (e.g., Entrez_Gene_Id)
- Removed rows with missing gene identifiers (Hugo_Symbol)
- Checked and corrected data types
- Verified valid data ranges

### Data Validation
- Checked for missing values
- Checked for duplicate entries
- Verified expression values are non-negative

### Preprocessing
- Structured dataset for analysis
- Prepared data for downstream dimension reduction and modelling

---

## Required Libraries

```r
library(dplyr)
library(ggplot2)
library(readr)
library(knitr)
library(rmarkdown)
