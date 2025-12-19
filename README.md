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
