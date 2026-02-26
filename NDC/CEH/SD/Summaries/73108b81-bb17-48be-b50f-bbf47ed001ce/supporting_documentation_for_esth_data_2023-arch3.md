# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023.

## Overview
- Part of an ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling during 2023; data downloaded include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, and nutrients/phytoplankton parameters: NH4N, TON, PO4P, TOTP, SIO2, and TOCA.
- Sampling location: integrated 0–5 m water column; measurements from a boat at the deepest part of the lake (buoy); when buoy access was not possible, shore samples were collected.

## Data collected and variables (units)
- TEMP: degrees Celsius
- OXYG: % air-saturation
- SECC: metres
- ALKA: µg CaCO3 per litre
- pH: unitless
- NH4N: µg N per litre
- TON: µg N per litre
- PO4P: µg P per litre
- TOTP: µg P per litre
- SIO2: µg SiO2 per litre
- TOCA: µg per litre

## Sampling regime and methods
- Part of an ongoing long-term dataset with fortnightly sampling in 2023.
- Water samples are integrated from 0 to 5 m; taken from buoy at the deepest lake location; some shore samples when buoy sampling wasn’t possible.
- Analysis methods (selected highlights):
  - TEMP and OXYG measured with YSI ProODO; DO% calibrated daily; DO pass criteria 98–102%.
  - SECC measured with Secchi disk.
  - Alkalinity (ALKA) and pH measured by Gran titration with a Radiometer electrode; integrated sample sealed to prevent atmospheric exchange.
  - NH4N and TON measured colorimetrically with SEAL AQ2 after filtration; UKAS-accredited methods; detailed calibration and quality checks described.
  - TP determined via K2S2O8 digestion and molybdenum blue colorimetry (880 nm) using a UV spectrophotometer.
  - SIO2 determined colorimetrically (silicomolybenum blue) at 880 nm; QC checks with known standards.
  - TOCA measured by filtration, methanol extraction, and spectrophotometric analysis.
  - PO4P measured colorimetrically after filtration (molybdenum blue) with calibration and blanks for accuracy.
- Calibration and quality assurances summarized for each method; UKAS accreditation cited for NH4N and TON analyses.

## Quality control, metadata, and data governance
- Data presented are raw and have not yet undergone full quality control or calibration.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and visually validated by a database manager.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- Public sharing of underlying data is a potential barrier discussed in the cycle of governance, though not explicitly blocking this dataset’s availability.

## Data structure and access
- Data provided in a CSV format with:
  - sdate: measurement date
  - variable, Description: name and description of each measurement (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA)
  - value: measured value for each variable
  - sign(if<LOD): indicator of below-detection-limit (< sign)
  - flag: sampling flag (1 = at buoy; 2 = sampled from shore when buoy unavailable)

## Funding and provenance
- Data collection supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Data validation supported by NERC through the UKCEH National Capability for UK Challenges Programme NE/Y006208/1.

## Relevance for monitoring frameworks and policy
- Demonstrates a multi-parameter, long-term environmental health monitoring approach suitable for evaluating policy decisions and informing future actions.
- Highlights practical data governance considerations (metadata completeness, data sharing, and QA/QC workflows) relevant to designing robust monitoring frameworks.
- Provides a transparent account of measurement methods, calibration, and QA steps, critical for evaluating data reliability and comparability over time.

## Limitations and caveats for use
- Raw data not yet fully quality controlled or calibrated; users should account for potential data quality issues.
- Some data gaps due to sampling logistics or weather/staffing; interpretation should consider missing periods.
- Metadata completeness and standardization may need enhancement to ensure easy re-use and integration with other datasets.