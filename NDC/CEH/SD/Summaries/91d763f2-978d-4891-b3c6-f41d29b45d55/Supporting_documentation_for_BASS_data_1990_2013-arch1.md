# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

## Overview
- Long-term fortnightly monitoring dataset from Bassenthwaite Lake, Cumbria, England (1990–2013).
- Captures surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.
- Data intended for analysis of temporal trends, correlations, and potential predictive relationships among physical, chemical, and biological variables.

## Sampling regime and collection methods
- Sampling frequency: fortnightly.
- Depth and integration: samples integrated from 0 to 5 m depth.
- Location: collected from a boat at the buoy at the deepest part of the lake; if the buoy was inaccessible, samples taken from the shore (Flag 2).
- Variables measured (and units):
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per litre
  - PH: pH
  - NH4N: ammonium, µg N per litre
  - NO3N: nitrate, µg N per litre
  - PO4P: soluble reactive phosphate, µg P per litre
  - TOTP: total phosphorus, µg P per litre
  - SIO2: dissolved reactive silicon, µg per litre
  - TOCA: phytoplankton chlorophyll a, µg per litre
- Data are labeled with sdate (measurement date) and value for each variable; sign_if_LT_LOD indicates below detection limit when present.
- Data completeness note: 2005 onward includes some double entries; overall dataset contains August 1990 through end of 2013.

## Quality control and limitations
- Raw data: not quality controlled or calibrated (except for some double entries from 2005 onward); visually checked.
- Notable gaps: March–June 2001 missing due to foot-and-mouth disease restricting access.
- Below-detection values: indicated by a "<" sign in sign_if_LT_LOD column.
- Sampling variations: occasional shore-based samples (Flag 2) when buoy access was unavailable.

## Data structure and file format
- File format: comma separated values (CSV).
- Columns:
  - sdate: date of measurement
  - variable, Description: name of the measured variable (e.g., TEMP, OXYG, SECC, etc.)
  - value, Description: measured value for each variable
  - sign_if_LT_LOD, Description: indicates detection-limit status (e.g., "<" when below detection)
  - flag, Description: sampling location indicator (1 = buoy, 2 = shore)
- The dataset provides a structured, raw data table suitable for cleaning, calibration, and downstream analyses.

## Usage notes and caveats
- Data require quality control and calibration before formal analyses or publishing; users should account for raw status.
- Scale considerations: long-term, lake-wide averages may mask spatial heterogeneity; be mindful of buoy vs shore sampling differences.
- Data gaps exist (temporal gaps and potential missing metadata) that may affect time-series analyses at finer scales.
- When using values below detection limit, choose appropriate imputation or statistical methods.

## Example publications and usage
- Dataset has been used in multiple studies, including:
  - Modelling effects on phytoplankton with changing mixed depth and background extinction coefficients.
  - Assessing nutrient sources, retention time effects, and climate-change influences on vendace habitat and phytoplankton dynamics.
  - Analyses of lake CO2 emissions, phytoplankton phenology shifts, and climate-change impacts on lake ecosystems.
- A range of references demonstrates the dataset’s utility for understanding lake limnology, nutrient dynamics, and climate-related responses.