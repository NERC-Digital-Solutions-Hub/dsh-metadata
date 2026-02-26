# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022. Feuchtmayr, H., Clarke, M.A., Dodd, B.A., Guyatt, H., Hunt, A.G., James, J.B., Kelsall, M., Mackay, E.B., McShane, G., Rankin, G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2025)

## Overview
- Long-term fortnightly monitoring dataset from Esthwaite Tarn, Cumbria, England (2021–2022)
- Variables and units included:
  - Surface temperature (TEMP) in °C
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in metres
  - Alkalinity (ALKA) in µg CaCO3 per litre
  - pH
  - Ammonium (NH4N) in µg N per litre
  - Nitrate (NO3N) in µg N per litre
  - Soluble reactive phosphate (PO4P) in µg P per litre
  - Total phosphorus (TOTP) in µg P per litre
  - Dissolved reactive silicon (SIO2) in µg per litre
  - Phytoplankton chlorophyll a (TOCA) in µg per litre
- Water samples integrated from 0 to 5 m; collected from a boat at the deepest buoy location; shore sampling when buoy access was not possible
- Data are raw (not yet quality controlled/calibrated) but double entered and visually checked
- Timeframe: January 2021 to end of 2022
- Data available to download as a CSV with structured fields

## Sampling regime and collection methods
- Fortnightly sampling as part of an ongoing long-term monitoring program
- Measurements taken at a marked buoy location (deepest part of the lake); if not possible, sampling conducted from the shore
- Water samples are integrated from 0–5 m depth
- Measurements include TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA
- When visits to buoy were not possible, samples taken from shore and recorded with Flag 2

## Quality control and data handling
- Data provided are raw and have not undergone final quality control or calibration
- Data have been double entered and visually checked
- Missing data attributed to weather, lake access restrictions, COVID-19 restrictions, or staff shortages

## Data structure
- Data provided as a comma-separated values (CSV) file
- Columns:
  - Date: Date of measurement
  - Variable: Name of the measurement (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: Measured value
  - Sign(if<LOD): Indicates values below detection limit with a < sign
  - Flag: 1 = sample from buoy location; 2 = sample from shore (buoy visit not possible)

## Scope and funding
- Groundwork supported by Natural Environment Research Council (NERC) grant NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability
- Data validation supported by NERC grant NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability

## Relevance for environmental monitoring analysts
- Provides a standardized, long-term data record across multiple key water quality and ecosystem indicators
- Raw data context enables independent quality control and calibration prior to integration into standardized datasets
- Documentation supports reproducibility of analyses and facilitates potential data integration with other datasets
- Aligns with goals to increase dataset value through cross-dataset comparisons and broader accessibility of underlying data
- Clear method notes aid interpretation of measurements and enable appropriate data cleaning and quality assurance before downstream use