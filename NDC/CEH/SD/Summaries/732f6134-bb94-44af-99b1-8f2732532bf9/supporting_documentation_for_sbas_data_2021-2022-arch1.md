# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2021 - 2022

- Overview
  - Fortnightly monitoring dataset from the South Basin of Windermere, Cumbria, England.
  - Time period: January 2021 to end of 2022.
  - Parameters measured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), phytoplankton chlorophyll a (TOCA, µg per L).

- Sampling regime and collection methods
  - Part of an ongoing monitoring dataset; sampling frequency is fortnightly.
  - Location and depth: water samples collected from a boat at a buoy in the deepest part of the South Basin; integrated from 0 to 7 m.
  - Data collected in multiple variables related to temperature, oxygen, clarity, water chemistry, and phytoplankton chlorophyll a.

- Data quality and limitations
  - Data are raw and have not yet undergone quality control or calibration.
  - Data have been double entered and visually checked.
  - Missing data attributed to weather conditions, COVID-19 restrictions, or staff shortages.
  - Some measurements below detection limits are indicated with a “<” sign in the sign(if<LOD) column.

- Data structure and formats
  - Provided as a comma-separated values (CSV) file.
  - Columns include:
    - Date: date of measurement.
    - Variable, Description: name of each measured parameter (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
    - Value, Description: measured values for each variable.
    - Sign(if<LOD), Description: indicator if values are below detection limit.
  - Water chemistry values are reported for samples from 0 to 7 m depth.

- Provenance and data stewardship
  - Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme (delivering National Capability).
  - Data validation supported by NERC award NE/Y006208/1 as part of the ACCESS-UK programme (delivering National Capability).

- Relevance for analysis
  - Enables analysis of relationships between surface temperature, oxygen, water clarity, chemical nutrients, and phytoplankton chlorophyll a.
  - Suitable for identifying seasonal patterns, correlations, and potential drivers of phytoplankton dynamics.
  - Note: because the dataset is raw and not yet QC’d, analysts should plan for data cleaning, calibration, and assessment of detection-limit issues before formal modeling.