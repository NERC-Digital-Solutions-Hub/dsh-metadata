# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023.

## Purpose and context
- Ongoing fortnightly monitoring dataset for Windermere South Basin (Cumbria, England) covering surface temperature, surface oxygen, Secchi depth, water chemistry, and phytoplankton chlorophyll a.
- Focused on data collected in 2023 from a single site: integrated 0–7 m sample, measured from a boat at the deepest part of the lake (buoy location).
- Data are provided to support assessment of environmental health and policy performance over time in a consistent format.

## What was measured (variables and units)
- Temperature (TEMP): degrees Celsius
- Surface oxygen saturation (OXYG): % air-saturation
- Secchi depth (SECC): metres
- Alkalinity (ALKA): µg CaCO3 per litre
- pH: dimensionless
- Total ammoniacal nitrogen (NH4N): µg N per litre
- Total oxidised nitrogen (TON): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre
- Data are presented with a flag for detections below the limit of detection (Sign if<LOD).

## Data structure and access
- Data are delivered as a comma separated values (CSV) file.
- Columns:
  - sdate: date of measurement
  - Variable, Description: variable name (e.g., TEMP, OXYG, SECC, etc.)
  - Value, Description: measured value
  - Sign(if<LOD), Description: indicates if value is below detection limit
- Sampling regime: fortnightly in 2023; sample integrated from 0 to 7 m; site at the deepest part of Windermere South Basin.

## Methods and quality control
- Instrumentation:
  - TEMP and OXYG: YSI ProODO; DO in mg/L; oxygen saturation calculated using Mortimer method; DO % calibrated daily (pass when 98–102%); biweekly and bimonthly calibrations.
  - Secchi depth: measured with Secchi disk on labelled rope.
  - Alkalinity (ALKA) and pH: integrated water sample sealed to prevent air exchange; Gran titration with a radiometer electrode; electrode calibrated before sampling.
  - NH4N and TON: SEAL AQ2 colorimetric analyser after filtration; nitrogen species measured via established colorimetric reactions; UKAS accredited methods; calibration and control standards employed.
  - TP: digestion with potassium persulphate, followed by molybdenum blue colorimetric analysis; absorbance at 880 nm; calibration and accuracy checks performed; blank corrected.
  - SIO2: colorimetric molybdate method; absorbance at 880 nm; QC samples run at set intervals.
  - TOCA: filtration, methanol extraction, spectrophotometric analysis.
  - PO4P: filtration, molybdenum blue colorimetric analysis; blanks and accuracy checks used.
- Data verification:
  - Raw data not yet quality controlled/calibrated.
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered from field notebooks/lab records and validated by a database manager; data checked visually (line graphs).
- Missing data: due to weather, equipment limitations, or staff shortages.
- Context: referenced standard analytical methods and UKAS-accredited procedures for nutrient analyses.

## Data quality, limitations, and provenance
- Data are raw and pending full quality control and calibration.
- Provenance includes field notebooks/lab records, with a dedicated database manager performing validation.
- Some variables have detection-limit flags; missing values indicate non-detections or data gaps.

## Coverage, availability, and funding
- Timeframe: January 2023 – December 2023.
- Location: Windermere South Basin, Cumbria, England; sampling at the deepest part of the lake from a buoy.
- Data availability: provided as CSV with explicit field descriptions and <LOD flags; designed for integration with other datasets and downstream analyses.
- Funding:
  - Data collection: Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme).
  - Data validation: NERC through UKCEH National Capability (NE/Y006208/1).

## Relevance for environmental monitoring and data sharing
- Aligns with standardised, verifiable environmental datasets suitable for monitoring ecosystem health over time.
- Highlights common challenges for analysts: enhancing dataset value through integration with additional data and enabling access to underlying data and metadata for transparency and reuse.
- The dataset structure and documented methods support reproducibility, cross-dataset comparisons, and eventual quality-controlled releases.