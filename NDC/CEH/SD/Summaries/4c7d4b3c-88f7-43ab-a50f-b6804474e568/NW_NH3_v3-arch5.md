# Details of data structure to ' NW_NH3.csv '

## Overview
- Dataset: NH3 emissions data from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).
- Content: 7 columns, 683 rows; measurements taken daily for 3 weeks after fertiliser application.
- Fertilisers: ammonium nitrate (AN), urea (U), inhibited urea (IU/agrotain).
- Emission measurements: NH3 flux from plots amended with fertilisers; wind tunnel measurements used (some sensor failures noted and corrected).

## Dataset structure and variables
- Time_Start: Date and time at the start of the sampling period.
- Time_End: Date and time at the end of the sampling period.
- N_app: Fertiliser application index (1, 2, or 3); corresponding rates: 1st & 2nd applications at 90 kg ha^-1, 3rd at 60 kg ha^-1.
- Block: Blocking factor of the randomised block design (1–4).
- Plot: Plot identifier (1–16); plot size 2 × 4 m.
- Treatment: Fertiliser type; values are AN (ammonium nitrate), U (urea), IU (inhibited urea).
- Emission_rate_kghad: Daily NH3 emission rate from the plot (kg NH3-N ha^-1 d^-1).

## Data quality handling and cleaning
- Sensor issues: Wind tunnel anemometers on plot 3 (first and second applications) and plot 14 (third application) failed; affected values removed and replaced with the mean of surrounding tunnels.
- Detection limit: 0.1 mg NH4-N L^-1.
- Negative fluxes: Replaced with 0.
- Missing day-1 data (imputation): Mean imputation used to estimate day 1 NH3 emissions where data were missing in the following cases:
  - N_app 1, day 1, plot 3 (no wind tunnel on plot 3)
  - N_app 2, day 1, plot 2 (samples lost)
  - N_app 2, day 1, plot 3 (pump did not run)
- Additional missing data due to equipment/pump issues:
  - N_app 2, day 19, plot 9
  - N_app 3, day 11, plot 9
  - N_app 3, day 3, plot 14 (pump did not run)

## Provenance and collection context
- Supersedes and complements supporting documentation for CINAg experiments; original data series documented in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Data originate from a 2016 grassland fertiliser trial at North Wyke, measuring NH3 emissions over 3 weeks post-application using wind tunnel methods.

## Implications for reuse and data governance
- Clear documentation of data cleaning and imputation is essential for accurate interpretation and reproducibility.
- Users should be aware of sensor failures, detection limits, and imputation flags when analyzing emission trends.
- Metadata should explicitly capture the data quality decisions (which rows were imputed or adjusted) and the rationale behind them.

## Recommendations for storage, sharing, and updates
- Store with a detailed data dictionary (this document serves as a starting point) and include a data quality log outlining sensor issues and imputation cases.
- Version the dataset to reflect corrections (e.g., sensor replacements, imputation events) and document changes in release notes.
- Ensure accessibility through appropriate data portals and link to the Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf for full methodological context.