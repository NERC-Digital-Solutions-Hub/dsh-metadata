# Details of data structure to ' Digestate_HF_and_NW_N2O_v2.csv '

## Overview
- 8 columns and 2800 rows of N2O flux data from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Measurements come from plots receiving different nitrogen treatments: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Experimental context: a randomized block design with blocking factor 'Block' (1–5) and multiple plots per treatment.
- Some plots (1, 19, 25, 31, 47) were used for monthly samplings for the 150 kg N ha⁻¹ treatment.

## Dataset scope and experimental design
- Sites: HF (Henfaes) and NW (North Wyke).
- Treatments: C, D, AD, DNI, ADNI.
- Design: Randomised block with Block values 1–5; Plot numbers indicate derivation of yield measurements (except the listed monthly-sampling plots).
- Plot sizes (harvest area) differ by site:
  - HF: 1.2 m × 6.5 m (nitrogen addition rates) and 1.2 m × 14 m (C, D, AD, DNI, ADNI).
  - NW: 2 m × 4.5 m (nitrogen addition rates) and 2 m × 9 m (C, D, AD, DNI, ADNI).

## Variables and data columns
- Site: HF or NW.
- Treatment: C, D, AD, DNI, ADNI.
- Block: 1–5.
- Plot: plot identifier.
- Date: date of measurement.
- N2O_qa1: All N2O flux data for each chamber/plot across the experimental period used to derive cumulative values.
- N2O_qa2: Cumulative N2O flux data with poor-quality fits removed; fits with R² < 0.6 replaced by zero flux. The R² threshold is adjustable for qa2.
- N2O_qa3: Cumulative N2O flux data with poor-quality fits removed; all negative Flux_N2O values replaced with zero. The R² threshold is adjustable for qa3.
- NA: Not Assessed (indicative placeholder in the dataset).

## Data quality and processing
- Data cleaning includes removing data with poor cumulative-fit quality (R² < 0.6) and substituting zero flux for those instances.
- qa2 and qa3 processing steps are adjustable via the R² threshold.
- Documentation notes potential adjustments to the fit criteria and handling of negative flux values.

## Data governance, sharing, and provenance
- This document is supplementary to supporting documentation for the data series and accompanies the Digestate_HF_and_NW_N2O_v2.csv file.
- The dataset structure and QA steps are described to aid data discovery, reuse, and governance.
- Notation includes explicit references to how data are stored and updated, and how limitations (e.g., data replacements) should be interpreted in downstream analyses.

## Notes and caveats
- Some plots were repurposed for monthly samplings, which may affect temporal resolution for certain treatments.
- The R²-based QA thresholds are described as adjustable, indicating the need for provenance-traceable parameter settings during reprocessing.
- The document uses “NA = Not Assessed” for unspecified fields, signaling areas where metadata may be incomplete or awaiting future documentation.