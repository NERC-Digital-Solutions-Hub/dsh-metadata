# Digestate_HF_and_NW_N2O_v2.csv

## Overview
- Supplement detailing the data structure for the Digestate_HF_and_NW_N2O_v2.csv dataset.
- 8 columns and 2800 rows from a 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations.
- Treatments: C (control, no N), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Sites: HF and NW; randomized block design with blocks 1–5.

## Data structure and variables
- Site: HF or NW.
- Treatment: C, D, AD, DNI, ADNI.
- Block: 1–5 (blocking factor of the randomised design).
- Plot: plot number (origin of yield measurements; note some plots used for monthly samplings under specific treatment).
- Date: date of measurement.
- N2O_qa1: all N2O flux data for each chamber/plot across the entire experimental period (used to derive cumulative values).
- N2O_qa2: cumulative N2O flux data with poor fits (R^2 < 0.6) removed and replaced with zero flux; the R^2 threshold is adjustable.
- N2O_qa3: cumulative N2O flux data with poor fits (R^2 < 0.6) removed and all negative Flux_N2O values replaced with zero.
- Flux_N2O: flux values (sensibly the instantaneous or chamber flux data used in processing; detail is tied to QA steps above).
- Plot size notes:
  - HF: harvest area 1.2 m × 6.5 m for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI.
  - NW: harvest area 2 m × 4.5 m for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI.
- NA: Not Assessed (as a placeholder when a field is not applicable).

## Experimental design and context
- Digestate wheat trial conducted in 2017 at two sites (HF and NW).
- Data are structured to support analysis of N2O flux under different digestate treatments.
- Blocking design with five blocks; plot-level measurements underpin yield and gas flux analyses.
- Some plots (e.g., plots 1, 19, 25, 31, 47) were used for monthly samplings at the 150 kg N ha^-1 treatment, indicating targeted sampling within the design.

## Data quality and processing notes
- QA fields (N2O_qa1, N2O_qa2, N2O_qa3) reflect progressive cleaning and curation of flux data.
- N2O_qa2 and N2O_qa3 remove low-quality fits (R^2 < 0.6) and, in qa3, replace negative Flux_N2O values with zero.
- R^2 threshold is stated as arbitrary and configurable, indicating that criteria can be adjusted for sensitivity.
- The documentation emphasizes that the dataset is a structured extract intended to support further analysis and product development (e.g., dashboards, reports).

## Potential uses and considerations for data support
- Analyzing treatment effects on N2O emissions across two sites and over time.
- Comparing effects of acidification and nitrification inhibition on N2O flux (AD, DNI, ADNI).
- Combining with other agronomic or environmental data to build dashboards or self-serve data products for end users.
- Evaluating how QA processing (qa1–qa3) influences interpretation of cumulative N2O flux.
- When using the data, consider the adjustable QA threshold (R^2) and site-specific plot size differences for normalization or cross-site comparisons.

## Limitations and cautions
- R^2-based filtering is arbitrary and may affect the inclusion of certain flux estimates; results may vary with threshold changes.
- Specific units for N2O flux are not explicitly stated in the excerpt; users should consult the full documentation for exact units.
- Some plots were designated for monthly sampling under a specific N treatment, which could influence representativeness for those treatments at that N level.