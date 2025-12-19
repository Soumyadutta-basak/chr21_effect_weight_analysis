###################-----------------------------------------------------------------ASSIGNMENT 1 -----------------------------------------------------------------------------------------

##### Overview
This repository contains the data preprocessing and exploratory analysis performed on the polygenic score (PGS) dataset **PGS001298** related to obesity.  
The analysis includes chromosome-specific data extraction, effect weight visualization, and insights derived from exploratory data analysis (EDA).

**Dataset Source:**  
- File: `PGS001298_hmPOS_GRCh38.txt.gz`

## Data Preprocessing

The original PGS scoring file contains metadata lines starting with `#` and variants from all chromosomes.

The following preprocessing steps were performed:

1. Removed all metadata/header lines starting with `#`.
2. Filtered variants mapped to chromosome 21 using the harmonized chromosome column (`hm_chr`).
3. Extracted only the required columns for analysis:
   - `effect_weight`
   - `hm_chr`
   - `hm_pos`
4. Saved the processed data into a clean TSV file for downstream analysis.

####Exploratory Data Analysis 

It was performed to understand the distribution and characteristics of effect weights for variants mapped to chromosome 21.

After preprocessing, the dataset contained only harmonized variants from chromosome 21 along with their corresponding effect weights and genomic positions. The primary focus of the exploratory analysis was the effect_weight column, as it represents the contribution of each genetic variant to the polygenic score.

A histogram was generated to visualize the distribution of effect weights.

###################---------------------------------------------------------------------ASSIGNMENT 2--------------------------------------------------------------------------------------

gsutil -m cp -r gs://BucketA/P21 gs://BucketB/

-m → enables parallel (multi-threaded/multi-processing) transfer.
cp -r → recursively copies the folder P21 and all its contents.
The destination bucket BucketB will have the same folder structure (P21).


