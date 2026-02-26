# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023

- Overview
  - Part of an ongoing fortnightly monitoring dataset for the Windermere North Basin (Cumbria, England) covering surface temperature, surface oxygen, Secchi depth (water clarity), water chemistry, and phytoplankton chlorophyll a for 2023.
  - Variables included: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), pH, NH4N (µg N per L), TON (µg N per L), PO4P (µg P per L), TOTP (µg P per L), SIO2 (µg SiO2 per L), TOCA (µg per L).

- Sampling regime and collection methods
  - Frequency: Fortnightly sampling in 2023.
  - Location and depth: Integrated water samples from 0 to 7 m, collected from a boat at a marked buoy location in the deepest part of Windermere North Basin; when the buoy was inaccessible, shore sampling was conducted for TEMP, OXYG, and occasionally other measurements.
  - Data available for download: TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA (units specified in dataset).

- Data structure and content
  - File format: Comma separated values (CSV).
  - Columns:
    - sdate: measurement date
    - Description: variable name (e.g., TEMP, OXYG, SECC, etc.)
    - Value: measured value
    - Sign(if<LOD): indicator if below detection limit (1 indicates presence of <)
    - Flag: 1 = sample from buoy; 2 = sample from shore (visit to buoy not possible)
  - Coverage: January 2023 to December 2023.

- Quality control and validation
  - Data are raw and have not yet undergone full quality control and calibration.
  - Partial validation: TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA have been double-entered from field notebooks/lab sheets and visually checked by a database manager.
  - Missing data: Attributable to weather, equipment limitations, or staffing.
  - Calibration and QA details:
    - Instruments: YSI ProODO for TEMP and DO.
    - DO calibration: daily water-saturated air zero/span, biweekly single-point DO% calibration, and bimonthly calibration in air-saturated water; DO % target 98–102%.
    - Alkalinity and pH: integrated samples sealed to prevent atmospheric exchange; Gran titration with radiometer electrode; electrode calibration before each sampling.
    - NH4N and TON: colorimetric analysis using SEAL AQ2 with filtration; UKAS-accredited methods; calibration and control standards described.
    - TP: digestion with potassium persulfate followed by molybdenum blue colorimetric analysis; UV-Vis measurement at 880 nm; accuracy checked with reference materials.
    - SIO2: colorimetric silica determination (silicomolybdenum blue) at 880 nm; QA samples run with each batch.
    - TOCA: chlorophyll a extraction and spectrophotometric analysis after filtration.
  - Data integrity: validated through duplication and manual checks; occasional missing data due to practical sampling constraints.

- Data governance, openness, and metadata
  - The dataset includes substantial methodological metadata (sampling depth, integration, instruments, calibration, and analytical methods) to support traceability and reproducibility.
  - Raw data availability highlights the importance of subsequent quality assurance steps before public dissemination; some metadata fields (e.g., below-detection indicators, sampling flags) are captured to aid interpretation.
  - Data collection and validation funded by UK Natural Environment Research Council (NERC) under specific awards; data validation support also provided through UKCEH National Capability.

- Practical implications for monitoring frameworks
  - Enables monitoring of key environmental health indicators (temperature, oxygen, clarity, nutrient chemistry, and phytoplankton pigment) over a defined annual cycle.
  - The explicit data structure and flagging facilitate integration with dashboards and reporting tools, while the documented QA/QC status informs confidence levels in analyses.
  - Highlights common governance considerations: reliance on raw data pre-QC, need for ongoing metadata completeness, and ensuring timely data sharing and data quality improvements.

- Funding and references
  - Funding: NERC award NE/R016429/1 (Windermere North Basin data collection) and UKCEH National Capability support NE/Y006208/1 for validation.
  - Method references: Mackereth et al. (1978) for phosphate analysis, Mortimer (1981) for oxygen calculations, Talling (1974) for standing waters methods.