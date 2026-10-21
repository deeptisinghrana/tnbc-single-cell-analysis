# Single-cell Transcriptomic Profiling of TNBC Treatment Response
## Overview 
This repository contains a high-level computational pipeline for analyzing a massive single-cell RNA- sequencing clinical atlas (**427,823 cells across 101 donors**) to investigate tumor microenvironment dynamics in Triple-Negative Breast Cancer (TNBC).
## Methodology & Tech Stack
- **Language & Frameworks:** Python, Scanpy ('backed='r'' mode for memory optimization), Pandas, SciPy, Seaborn, Matplotlib.
- **Key Steps:**
  1. Memory-efficient data loading and indexing of large-scale H5AD single-cell matrices.
  2. Automated cohort-wide metadata aggregation, cell-type proportion normalization, and grouping by treatment response ('pCR' vs. 'RD').
  3. High-resolution distribution visualization via overlaid boxplots and strip plots to capture inter-patient heterogeneity.
  4. Non-parametric statistical validation using the **Mann-Whitney U test** across macro-compartments and specialized immune functional states.
## Key Findings
- -**Macro-Infiltration Trends:**Global proportion analysis indicated T-cell and B-lineage enrichmentin responders ('pCR'), though bulk total T-cell comparison yielded a non-significant global trend ($p=0.1775$).
- -**Immune Exhaustion Signatures:** High-resolution deconvolution of fine-grained'cell_state' annotations revealed that exhausted CD8+ T cells ('CD8-TEXH') approached statistical significance ($p = 0.0583$), underscoring microenvironmental immunosuppression as a critical barrier to therapeutic response in non-responders ('RD').
## Dataset Reference
- Clinical single-cell TNBC atlas and metadata annotations sourced andretrieved from **CZ CELLxGENE Discover**.
