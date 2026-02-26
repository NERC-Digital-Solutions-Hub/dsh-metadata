# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

## Overview
- Long-term, fortnightly monitoring dataset from Bassenthwaite Lake, Cumbria, England, spanning August 1990 to the end of 2013.
- Aims to document multiple environmental parameters to support assessment of lake health and policy performance.

## Data collected and variables
- Variables and units available for download:
  - Surface temperature (TEMP) in °C
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in metres
  - Alkalinity (ALKA) in µg CaCO3 per litre
  - pH (PH)
  - Ammonium (NH4N) in µg N per litre
  - Nitrate (NO3N) in µg N per litre
  - Soluble reactive phosphate (PO4P) in µg P per litre
  - Total phosphorus (TOTP) in µg P per litre
  - Dissolved reactive silicon (SIO2) in µg SiO2 per litre
  - Phytoplankton chlorophyll a (TOCA) in µg per litre
- Water samples are integrated from 0 to 5 m.

## Sampling regime and collection methods
- Sampling frequency: Fortnightly.
- Collection site: Boat at a marked buoy located at the deepest part of the lake.
- In cases where the buoy could not be reached, samples were taken from the shore (Flag 2 indicates shore sampling).
- All data represent August 1990 to end 2013.

## Quality control and data limitations
- Data are raw (not yet quality controlled or calibrated); only duplicate entries from 2005 onward have QC.
- Visual checks performed; no formal QC beyond that.
- Missing data period: March–June 2001 due to foot-and-mouth disease restricting lake access.
- Some values below detection limit are indicated with a "<" sign in sign_if_LT_LOD.

## Data structure and metadata
- Data provided as a CSV with columns:
  - sdate: measurement date
  - variable: parameter description (e.g., TEMP, OXYG, SECC, etc.)
  - value: measured value for each variable
  - sign_if_LT_LOD: indicator for values below detection limit
  - flag: 1 if sample taken at buoy location; 2 if sample taken from shore

## Data availability and usage
- The dataset is used in recent publications for modeling phytoplankton dynamics, nutrient sources, climate-change impacts, and lake ecology.
- Example topics include effects of mixing depth and extinction coefficients on phytoplankton, influence of nutrient sources and retention time, climate-change-related habitat shifts, and lake carbon-silicon cycling.

## Notable publications using the dataset
- Series of studies cited, including works on phytoplankton responses to changing lake conditions, nutrient sources, climate-driven habitat changes, and long-term lake ecology.

## Practical considerations for analysts
- Suitable for assessing temporal trends in temperature, oxygen, clarity, chemistry, and chlorophyll a.
- Use with caution due to raw data status; apply quality checks and calibration if integrating with other datasets.
- Account for the 2001 gap when conducting time-series analyses.
- Leverage missing data flags and detection-limit indicators in analyses to avoid bias.