# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023. Feuchtmayr, H., Carter, H.T., Dodd, B.A., Keenan, P.O., Le Quesne, K., McShane, G., Moorhouse, H., Rankin, G., Rhodes, G., Thackeray, S.J. (2025)

## Overview
- Part of an ongoing fortnightly monitoring dataset for the Windermere South Basin (Cumbria, England) in 2023.
- Measured variables: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH; plus phytoplankton chlorophyll a (TOCA) and nutrient/water chemistry parameters: NH4N (µg N L−1), TON (µg N L−1), PO4P (µg P L−1), TOTP (µg P L−1), SIO2 (µg SiO2 L−1).
- Sampling depth and timing: integrated 0–7 m water column, using a buoy at the deepest lake location; sampling frequency is fortnightly; data cover January 2023 to December 2023.

## Data and metadata
- The dataset provided for download comprises the measured variables listed above with their units.
- Data are raw and not yet quality controlled, but TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered and visually validated by a database manager.
- Missing data result from weather, equipment limitations, or staff shortages.
- A < sign in the Sign(if<LOD) column indicates values below the detection limit.

## Data structure
- Data are delivered as CSV with columns:
  - sdate: measurement date
  - Variable, Description: variable name (TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA)
  - Value, Description: measured value
  - Sign(if<LOD), Description: indicator if value is below detection limit

## Methods and calibration
- Temperature and dissolved oxygen:
  - Measured with YSI ProODO; DO% calculated from Mortimer (1981).
  - Daily DO% calibration; biweekly single-point DO% calibration in water-saturated air; bimonthly calibration in air-saturated water.
  - Secchi depth recorded with a marked rope and disk.
- Alkalinity and pH:
  - Integrated 0–7 m water sample sealed to prevent atmospheric exchange; Gran titration with a combination electrode.
  - Electrode calibrated before each sampling.
- Nutrients and phytoplankton:
  - NH4N and TON measured colorimetrically with SEAL AQ2 after filtration through GF/C; standard colorimetric reactions with calibration, controls every ~10 samples; UKAS accredited method; range 0–2.0 mg/L.
  - TP: digestion with potassium persulfate, molybdenum blue colorimetric analysis; absorbance at 880 nm; calibration 0–0.2 mg/L; blank corrected; accuracy checked with reference materials.
  - SIO2: colorimetric with ammonium molybdate and ascorbic acid; 0–5 mg/L; quality controls at 2.0 and 4.0 mg/L every 20 samples.
  - TOCA: filtered sample, methanol extraction, spectrophotometric analysis following Talling (1974).
- General QA/QC:
  - Methods include calibration, standards, and quality control checks; several methods UKAS-accredited; reference materials used for accuracy.

## Data provenance and governance
- Funding: Data collection supported by Natural Environment Research Council (NE/R016429/1) under the UK-SCaPE programme; data validation supported by NE/Y006208/1.
- References for methods: Mackereth et al. (1978), Mortimer (1981), Talling (1974).

## Relevance for monitoring frameworks
- Demonstrates a multi-parameter environmental health monitoring approach, including:
  - Clear documentation of measurement methods, calibration routines, and QA procedures.
  - Handling of detection limits and metadata within the dataset.
  - A structure for data quality control, provenance, and governance, highlighting challenges such as data completeness, metadata sufficiency, and need for timely QC.
- Illustrates common barriers for monitoring frameworks (data quality, access, metadata adequacy, and governance) and how they are addressed in practice.