# Digestate_HF_and_NW_N2O_v2.csv

## Overview
- Supplement to the supporting documentation for data series detailed in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Details the data structure for the N2O flux dataset from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW), involving Bangor University and Rothamsted Research.

## Dataset scope
- 8 columns and 2800 rows.
- Two sites: HF and NW.
- Treatments: C (control with no nitrogen), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Measurements derive cumulative N2O flux values from plot/chamber data over the experimental period.
- Data reflect N2O fluxes for plots under different nitrogen treatments.

## Column definitions
- Site: HF or NW (Henfaes or North Wyke).
- Treatment: C, D, AD, DNI, ADNI with defined meanings as above.
- Block: 1–5, blocking factor of the randomized block design.
- Plot: Plot number; note that plots 1, 19, 25, 31, and 47 were used for monthly samplings for the 150 kg N ha−1 treatment.
- Date: Date of measurement.
- N2O_qa1: All N2O flux data for each chamber/plot during the entire experimental period (used for deriving cumulative values).
- N2O_qa2: Cumulative N2O flux data; fits with R² < 0.6 removed and replaced with zero flux. The R² threshold is adjustable for both qa2 and qa3.
- N2O_qa3: Cumulative N2O flux data; fits with R² < 0.6 removed and all negative N2O flux values replaced with zero.
- NA = Not Assessed.

## Experimental design and plot details
- Plot sizes:
  - HF: 1.2 m × 6.5 m harvest area for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: 2 m × 4.5 m harvest area for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI.

## Data handling and quality considerations
- N2O data are filtered for cumulative values using R² thresholds (qa2 and qa3; threshold 0.6, adjustable).
- Poor fits and all negative flux values are replaced with zero to produce robust cumulative values.
- Data structure and processing steps are described to support transparency and reproducibility.

## Metadata and references
- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Originates from the 2017 digestate wheat trial conducted at HF and NW by Bangor University and Rothamsted Research.