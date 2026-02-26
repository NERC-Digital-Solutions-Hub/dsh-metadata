# Details of data structure to ' Digestate_HF_and_NW_N2O_cum.csv '

- Overview of dataset: 7 columns and 40 rows of N2O flux data from a 2017 digestate wheat trial conducted at two sites (Henfaes Research Center, HF, and North Wyke, NW). Treatments cover different digestate and inhibitor combinations: C (control, zero N), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), and ADNI (acidified digestate with DMPP).
- Experimental context: Part of a larger CINAg experiment framework; data originate from a collaboration between HF/Bangor University and NW/Rothamsted Research. The trial includes a randomised block design with plots used for various sampling schemes, including monthly samplings for the 150 kg N ha-1 treatment on specific plots.
- Data series purpose: Provides cumulative N2O flux information derived from chamber measurements across treatment plots over the experimental period; includes data quality-filtered variants (qa2, qa3) in addition to the full dataset (qa1).

## Dataset structure and variables

- Site: HF (Henfaes) or NW (North Wyke).
- Treatment: C, D, AD, DNI, ADNI (see above for definitions).
- Block: Blocking factor in the randomised design (values 1–5).
- Plot: Plot identifier; used as the basis for all yield-related data except plots 1, 19, 25, 31, and 47 (monthly samplings for 150 kg N ha-1).
- Date: Date of the measurement.
- N2O_qa1: All N2O flux data for each chamber/plot across the full experimental period (used to derive cumulative values).
- N2O_qa2: Cumulative N2O flux data after removing fits with R² < 0.6; such data are replaced with zero flux.
- N2O_qa3: Cumulative N2O flux data after removing fits with R² < 0.6 and replacing all negative Flux_N2O values with zero.
- Note: The document lists 7 columns and 40 rows, though the named variables include Site, Treatment, Block, Plot, Date, N2O_qa1, N2O_qa2, and N2O_qa3 (eight items when counting each variable separately).

## Experimental context and design

- Sites: HF (Henfaes) and NW (North Wyke); data collected during a 2017 digestate wheat trial.
- Treatments: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Design: Randomised block design (Block 1–5); Plot-level treatments assigned within blocks.
- Plot usage: Plots 1, 19, 25, 31, and 47 used for monthly samplings for the 150 kg N ha-1 treatment.
- Plot sizes (harvest area):
  - HF: 1.2 m × 6.5 m for nitrogen addition-rate treatments; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: 2 m × 4.5 m for nitrogen addition-rate treatments; 2 m × 9 m for C, D, AD, DNI, ADNI.

## Data processing and quality control

- qa1: All N2O flux data for each chamber/plot across the entire experimental period.
- qa2: Cumulative N2O flux data with poor fits removed (R² < 0.6) and replaced with zero flux.
- qa3: Cumulative N2O flux data with poor fits removed (R² < 0.6) and all negative N2O flux values replaced with zero.
- Purpose: To provide curated data series that are more reliable for interpreting cumulative N2O emissions under the different digestate treatments.

## Provenance and usage context

- This document is a supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- The dataset Digestate_HF_and_NW_N2O_cum.csv captures the cumulative N2O flux related to the digestate treatments across two research sites, enabling cross-site comparison and evaluation of nitrogen management scenarios involving digestates and inhibitors.

## Practical notes for data operability

- The data pertain specifically to N2O flux and its cumulative values under defined digestate treatments, measured via chamber methods across multiple plots and dates.
- Users should consider the R²-based filtering (qa2/qa3) when selecting data for analyses involving flux accumulation, as these filters remove less reliable fits and adjust for negative flux values.
- Cross-reference with the related Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf for broader methodological details and integration with other data series.