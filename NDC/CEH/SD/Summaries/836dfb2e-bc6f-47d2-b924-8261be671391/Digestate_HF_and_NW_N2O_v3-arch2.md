# Details of data structure to 'Digestate_HF_and_NW_N2O_v2.csv'

## Overview
- Supplement to supporting documentation for data series related to the Digestate_HF_and_NW_N2O_v2.csv dataset.
- 8-column, 2800-row dataset from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW) with collaboration between Bangor University and Rothamsted Research.
- Captures N2O flux measurements across different digestate treatments to support environmental monitoring and policy performance assessments over time.

## Dataset scope and origin
- Sites: HF (Henfaes) and NW (North Wyke).
- Year: 2017.
- Experimental context: digestate applications in wheat; N2O fluxes measured to evaluate treatment effects.
- Treatments represented by codes: C (zero nitrogen control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).

## Dataset structure
- Columns total: 8 (with associated explanations and units provided in metadata not fully listed here).
- Core columns:
  - Site: HF or NW.
  - Treatment: C, D, AD, DNI, ADNI.
  - Block: 1–5 (randomised block design).
  - Plot: Plot identifier from which yield measurements were derived (specific plots noted; some plots used for monthly samplings for the 150 kg N ha-1 treatment are 1, 19, 25, 31, 47).
  - Date: Date of measurement.
  - N2O_qa1: All N2O flux data for each chamber/plot across the experimental period used to derive cumulative values.
  - N2O_qa2: Cumulative N2O flux data after removing fits with R^2 < 0.6 and replacing with zero flux.
  - N2O_qa3: Cumulative N2O flux data after removing fits with R^2 < 0.6 and replacing all negative flux values with zero.

## Columns in detail
- Site: Identifies the research site (HF or NW).
- Treatment: Indicates the nitrogen/digestate treatment category (C, D, AD, DNI, ADNI).
- Block: Blocking factor in the randomised design (1–5).
- Plot: Plot number; the source from which yield measurements are derived.
- Date: Date when the measurement was conducted.
- N2O_qa1: Raw or primary N2O flux data per chamber/plot for the full experimental period.
- N2O_qa2: Cumulative N2O flux after quality control (R^2 threshold applied; low-fit values replaced with zero).
- N2O_qa3: Further curation of cumulative N2O flux (applies same R^2 threshold; negative flux values also set to zero).

Note: Units are specified in the dataset metadata for each column; not all units are listed in this excerpt.

## Data processing and quality assurance
- N2O_qa2: Data fits with R^2 < 0.6 are removed and replaced with zero flux.
- N2O_qa3: Further curation removes fits with R^2 < 0.6 and replaces all negative N2O flux values with zero.
- R^2 threshold is noted as arbitrary and configurable for qa2 and qa3.

## Experimental design and sampling details
- Plot sizes differ between sites:
  - HF: 1.2 m × 6.5 m harvest area for nitrogen addition rate plots; 1.2 m × 14 m harvest area for C, D, AD, DNI, ADNI plots.
  - NW: 2 m × 4.5 m harvest area for nitrogen addition rate plots; 2 m × 9 m harvest area for C, D, AD, DNI, ADNI plots.
- Some plots (1, 19, 25, 31, 47) were used for monthly samplings specifically for the 150 kg N ha-1 treatment.
- NA stands for Not Assessed where applicable.

## Purpose and application for environmental monitoring
- The dataset supports standardized, longitudinal assessment of soil N2O flux responses to different digestate treatments.
- Aims to enable scrutiny of environmental health and policy performance over time by providing a consistent, quality-assured data structure.
- Facilitates data integration with other monitoring datasets by clearly defined fields (site, treatment, block, plot, date, and curated flux metrics).

## Notes for use
- Data quality is controlled via qa2 and qa3 steps, with explicit handling of low-quality fits and negative flux values.
- The R^2 threshold is acknowledged as adjustable, allowing researchers to tailor QA stringency.
- The document is a supplement to broader CINAg experiments documentation, intended to support reproducible monitoring and analysis in environmental research.