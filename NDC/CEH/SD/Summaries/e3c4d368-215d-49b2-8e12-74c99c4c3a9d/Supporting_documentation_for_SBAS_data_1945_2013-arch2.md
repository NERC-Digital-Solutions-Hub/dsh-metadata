# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013. Maberly, S.C., Brierley, B., Carter, H.T., Clarke, M.A., De Ville, M.M., Fletcher, J.M., James, J.B., Keenan, P., Kelly, J.L., Mackay, E.B., Parker, J.E., Patel, M., Pereira, M.G., Rhodes, G., Tanna, B., Thackeray, S.J., Vincent, C., Feuchtmayr, H. (2017)

## Overview
- Long-term monitoring dataset from the South Basin of Windermere, Cumbria, England, spanning 1945–2013 for selected variables.
- Variables include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved silica, and phytoplankton chlorophyll a.
- Initial data collection by the Freshwater Biological Association; since 1989 by CEH and its predecessor.
- Data are provided in a CSV format with standardized variable codes and units.

## Sampling regime and methods
- Sampling frequency: weekly or fortnightly (varies by variable; began in 1945 for some variables).
- Depth-integrated water samples:
  - 0–5 m (1945–1962)
  - 0–10 m (1962–1964)
  - 0–7 m (1964 onwards)
- Collection location: boat at a buoy in the deepest part of Windermere.
- Measured variables and units (examples):
  - TEMP: surface temperature, degrees Celsius
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, metres
  - ALKA: alkalinity, µg CaCO3 per litre
  - PH: pH
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: concentrations in µg per litre (as noted)
- Data available to download as CSV with specific column definitions.

## Data quality and structure
- Data are raw (not quality controlled/calibrated) except for double entries from 2005 onwards; visually checked.
- Data structure:
  - sdate: measurement date
  - variable, Description: variable code and description (e.g., TEMP, OXYG, SECC, etc.)
  - value, Description: measured values
  - sign_if_LT_LOD, Description: indicator if below detection limit (a < sign)
- Data quality caveat: users should perform QA/QC and calibration prior to formal analysis.

## Dataset contents and scope
- Variables included: TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA.
- Units and depth-collection method clearly defined to support standardized analyses.

## Temporal coverage and accessibility
- Time span: March 1945 to end of 2013.
- Data originate from the Windermere South Basin monitoring program and are associated with CEH and predecessors.
- Dataset used in recent publications demonstrates its utility for long-term ecological and climate-related analyses.
- Available for download; intended for long-term monitoring and comparative analyses with standardized formats.

## Usage and applications
- Suitable for:
  - Long-term environmental health assessment and trend analysis.
  - Monitoring responses to nutrient loading, temperature changes, and chemical conditions.
  - Cross-study comparisons with other lake datasets given standardized variable definitions.
- Recent publications citing the dataset indicate its value for early warning indicators, phytoplankton phenology, nutrient dynamics, and climate-related lake responses.

## Considerations and challenges for analysts
- Value enhancement: integrate this dataset with other relevant data (e.g., external nutrient loads, climatic variables) to maximize usefulness beyond single-use applications.
- Data accessibility: ensure access to underlying raw data and supporting metadata to enable reproducible analyses and data reuse.
- QA requirement: plan for quality control and calibration steps before applying standard monitoring analytics.
- Data completeness: 2013 is the most recent year; assess gaps and compatibility with newer datasets when integrating into ongoing monitoring programs.