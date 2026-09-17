You can copy the code block below and paste it directly into your README.md editor on GitHub:

Markdown
# BAMSE Proteogenomic pQTL Analysis Framework

[![License: EUPL-1.2](https://img.shields.io/badge/License-EUPL--1.2-blue.svg)](LICENSE)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

This repository contains the analytical workflow, statistical thresholds, and computational code used for genome-wide proteogenomic pQTL mapping, meta-analysis, and functional characterization in the BAMSE cohort.

For full study methodology and clinical context, please refer to our manuscript:
> **Proteogenomic pQTL Analysis in the BAMSE Cohort**  
> medRxiv Preprint: [https://www.medrxiv.org/content/10.64898/2026.01.16.26344184v1](https://www.medrxiv.org/content/10.64898/2026.01.16.26344184v1)

---

## Repository Structure

```text
BAMSE-pQTL-analysis/
├── README.md
├── LICENSE
├── CITATION.cff
├── config/
│   └── analysis_params.yaml       # Statistical thresholds and parameter bounds
└── scripts/
    ├── 01_phenotype_prep.R        # Rank-based INT transformation logic
    ├── 02_gwas_association.sh     # Primary PLINK2 association mapping setup
    ├── 03_meta_analysis.sh        # Summary statistics integration logic
    └── 04_annotation.py           # Cis/trans classification criteria
Workflow Summary
Phenotype Preprocessing: Inverse normal transformation (INT) applied to ProtPQN-standardized Olink protein levels.

Genome-Wide Mapping: Primary association testing across 365 target proteins using PLINK2 task arrays on HPC clusters.

Quality Control & Meta-Analysis: Output diagnostic checks and multi-cohort summary statistics integration via METAL.

Post-GWAS Fine Mapping: Signal decomposition using GCTA (COJO) and functional variant classification (cis vs trans loci).

Software Requirements
PLINK2 (v2.00-alpha)

R (v4.3.1)

METAL (Release 2020-05-05)

GCTA (v1.94.1)

Data Availability
Individual-level clinical and genomic data from the BAMSE cohort are subject to ethical and legal restrictions under GDPR to protect participant confidentiality. Data access requests for validation purposes may be submitted to the BAMSE steering committee.

## Author & Citation

**Ashish Kumar**  
Karolinska Institutet  
Email: ashish.kumar@ki.se  

If you use this workflow or cite the underlying analysis, please cite our preprint:

> **Proteogenomic pQTL Analysis in the BAMSE Cohort**  
> Annika Bendes, Sophia Björkander et al.  
> *medRxiv* (2026). DOI: [10.64898/2026.01.16.26344184v1](https://www.medrxiv.org/content/10.64898/2026.01.16.26344184v1)

License
This project is licensed under the European Union Public Licence v1.2 (EUPL-1.2) - see the LICENSE file for details.
