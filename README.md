# BAMSE Proteogenomic pQTL Analysis Framework

[![License: EUPL-1.2](https://img.shields.io/badge/License-EUPL--1.2-blue.svg)](LICENSE)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

The **BAMSE-pQTL-analysis** framework contains the analytical pipeline, statistical models, and command-line scripts used for genome-wide protein quantitative trait loci (pQTL) mapping, meta-analysis, and functional characterization in the BAMSE cohort.

---


> **Proteogenomic pQTL Analysis in the BAMSE Cohort**  
> **Authors:** Annika Bendes1#, Sophia Björkander2#, Maura M. Kere2, Simon Kebede Merid2, **Ashish Kumar**2, Leo Dahl1, Zhebin Yu2, Amelie Vogt1, Changil Kim3, Qiang Pan-Hammarström4, Anna Bergström56, Inger Kull26, Anne-Sophie Merritt6, Sandra Ekström267, Alexandra Lövquist7, Ben Murrell3, Niclas Roxhed89, Erik Melén26* and Jochen M. Schwenk16*

> **Affiliations:** 1. Department of Protein Science, SciLifeLab, KTH Royal Institute of Technology, Solna, Sweden
2. Department of Clinical Science and Education, Södersjukhuset, Karolinska Institutet, Stockholm, Sweden
3. Department of Microbiology, Tumor and Cell Biology, Karolinska Institutet, Stockholm, Sweden
4. Division of Immunology, Department of Medical Biochemistry and Biophysics, Karolinska Institutet, Stockholm, Sweden
5. Institute of Environmental Medicine, Karolinska Institute, Stockholm, Sweden
6. Sachs’ Children and Youth Hospital, Södersjukhuset, Stockholm, Sweden
7. Centre for Occupational and Environmental Medicine, Region Stockholm, Stockholm, Sweden
8. Department of Intelligent Systems, KTH Royal Institute of Technology, Stockholm, Sweden
9. MedTechLabs, BioClinicum, Karolinska University Hospital, Solna, Sweden

↵*Corresponding authors: erik.melen@ki.se and jochen.schwenk@scilifelab.se

↵# Contributed equally

> **Preprint:** [medRxiv (10.64898/2026.01.16.26344184v1)](https://www.medrxiv.org/content/10.64898/2026.01.16.26344184v1)

---

## Author & Maintainer Details

* **Lead Analyst & Author:** Ashish Kumar ([ashish.kumar@ki.se](mailto:ashish.kumar@ki.se))
* **Institution:** Department of Clinical Science and Education, Södersjukhuset, Karolinska Institutet, Stockholm, Sweden
* **Repository Maintainer:** Ashish Kumar ([@kumar-ashish](https://github.com/kumar-ashish))

*(For questions regarding code execution, methodology, or analysis replication, please write to the lead analyst directly.)*

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
    └── 04_gcta_cojo.R             # Post-GWAS GCTA-COJO conditional analysis
    └── 05_annotation.py           # Cis/trans classification criteria

```

---
## Workflow Summary

Phenotype Preprocessing: Inverse normal transformation (INT) applied to ProtPQN-standardized Olink protein levels.

Genome-Wide Mapping: Primary association testing across 365 target proteins using PLINK2 task arrays on HPC clusters.

Quality Control & Meta-Analysis: Output diagnostic checks and multi-cohort summary statistics integration via METAL.

Post-GWAS Fine Mapping: Signal decomposition using GCTA (COJO) and functional variant classification (cis vs trans loci).

---
## **Software Requirements**
PLINK2 (v2.00-alpha)

R (v4.3.1)

METAL (Release 2020-05-05)

GCTA (v1.94.1)

---
Data Availability
Individual-level clinical and genomic data from the BAMSE cohort are subject to ethical and legal restrictions under GDPR to protect participant confidentiality. Data access requests for validation purposes may be submitted to the BAMSE steering committee.

---
## Manuscript & Citation

If you use or adapt these analytical parameters and methods, please cite our study:

> **Proteogenomic pQTL Analysis in the BAMSE Cohort**  
> Annika Bendes, Sophia Björkander et al.  
> *medRxiv* (2026). DOI: [10.64898/2026.01.16.26344184v1](https://www.medrxiv.org/content/10.64898/2026.01.16.26344184v1)

License
This project is licensed under the European Union Public Licence v1.2 (EUPL-1.2) - see the LICENSE file for details.
