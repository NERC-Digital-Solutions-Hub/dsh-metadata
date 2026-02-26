# Digestate_HF_and_NW_N2O_v2.csv

## Overview
- Supplement to the supporting documentation for CINAg experiments detailing the data structure of Digestate_HF_and_NW_N2O_v2.csv.
- Data come from a digestate wheat trial conducted in 2017 at two sites: Henfaes Research Center (HF) and North Wyke (NW).
- Measurements focus on N2O fluxes under different nitrogen/digestate treatments to derive cumulative values.

## Dataset structure
- 8 columns, 2800 rows.
- Columns and meanings:
  - Site: HF or NW.
  - Treatment: C (zero nitrogen control), D (digestate), AD (acidified digestate), DNI (digestate + nitrification inhibitor DMPP), ADNI (acidified digestate + DMPP).
  - Block: 1–5 (randomised block design).
  - Plot: plot identifier.
  - Date: date of measurement.
  - N2O_qa1: all N2O flux data for each chamber/plot across the entire experimental period, used to derive cumulative values.
  - N2O_qa2: cumulative N2O flux data after quality filtering; data with model fit R^2 < 0.6 are removed and replaced with zero flux (R^2 threshold is adjustable).
  - N2O_qa3: cumulative N2O flux data after quality filtering; data with R^2 < 0.6 are removed and all negative Flux_N2O values replaced with zero (R^2 threshold adjustable).
- Notation: NA = Not Assessed.

## Experimental design and sites
- Digestate wheat trial conducted in 2017 at:
  - HF: Henfaes Research Center, Bangor University.
  - NW: North Wyke, Rothamsted Research.
- Design: randomized blocks (Block 1–5) with plots assigned to treatments C, D, AD, DNI, ADNI.
- Monthly samplings were conducted on plots 1, 19, 25, 31, and 47 specifically for the 150 kg N ha^-1 treatment.

## Plot sizes and measurement scope
- Plot/habitat sizes (harvest area) vary by site and treatment:
  - HF: 1.2 m × 6.5 m for nitrogen addition-rate plots; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: 2 m × 4.5 m for nitrogen addition-rate plots; 2 m × 9 m for C, D, AD, DNI, ADNI.
- Date indicates when each N2O measurement was taken; unit details for N2O flux are not specified in the excerpt.

## Data processing and quality assurance
- N2O_qa1: raw flux data used to derive cumulative values.
- N2O_qa2: cumulative flux with low-quality fits removed (R^2 < 0.6); removed values replaced with zero; R^2 threshold is configurable.
- N2O_qa3: cumulative flux with low-quality fits removed and negative flux values replaced with zero; R^2 threshold configurable.
- Emphasis on transparent QA steps to ensure robust cumulative estimates.

## Data usage notes
- The dataset is a structured data component of the CINAg experiments and linked to broader supporting documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Data provenance and metadata are important for discovery and reuse; datasets may be uploaded to data portals with accompanying metadata.

## Limitations and caveats
- Some data points may be NA (Not Assessed).
- Access to and standardisation of data across sites can be challenging due to differing plot sizes and QA criteria.
- R^2-based filtering thresholds are adjustable, which can affect the derived cumulative N2O values.