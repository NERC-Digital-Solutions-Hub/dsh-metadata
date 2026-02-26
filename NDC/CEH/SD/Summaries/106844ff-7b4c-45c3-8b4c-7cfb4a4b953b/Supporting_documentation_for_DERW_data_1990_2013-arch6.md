# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013.

## Overview
- Long-term, fortnightly monitoring dataset from Derwent Water, Cumbria, England (1990–2013).
- Variables cover physical, chemical, and biological water properties: surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Data are raw (unquality controlled) with some data checks performed visually; some entries are flagged for detection limits or sampling location.

## Sampling regime and collection methods
- Sampling cadence: fortnightly throughout the study period.
- Sampling location: from a boat at a buoy located at the deepest part of the lake; when unavailable, samples were taken from the shore.
- Water integration: samples are integrated from 0 to 5 meters when collected at the buoy; shore samples are not integrated.
- Timeframe: August 1990 to end of 2013.
- Data are provided as CSV with clearly documented fields.

## Variables and units
- Temperature (TEMP): degrees Celsius.
- Surface oxygen saturation (OXYG): percent air-saturation.
- Secchi depth (SECC): meters.
- Alkalinity (ALKA): micrograms per liter as CaCO3.
- pH (PH): dimensionless.
- Ammonium (NH4N): micrograms N per liter.
- Nitrate (NO3N): micrograms N per liter.
- Soluble reactive phosphate (PO4P): micrograms P per liter.
- Total phosphorus (TOTP): micrograms P per liter.
- Dissolved reactive silicon (SIO2): micrograms per liter.
- Phytoplankton chlorophyll a (TOCA): micrograms per liter.
- Data values are accompanied by Sign_if_LT_LOD to indicate detections below the limit of detection and Flag to indicate sampling location (1 = buoy, 2 = shore).

## Data structure and format
- File format: comma separated values (CSV).
- Columns include:
  - Date: measurement date.
  - Variable, Description: one of the listed variables and its description.
  - Value, Description: measurement value and units.
  - Sign_if_LT_LOD, Description: indicates below-detection-limit status (e.g., "<" symbol).
  - Flag, Description: sampling location flag (1 = buoy, 2 = shore).

## Quality control, limitations, and gaps
- Data are raw and not calibrated/fully quality controlled (except for duplicate entries from 2005 onward); visual checks performed.
- Missing data periods:
  - March–June 2001: due to foot-and-mouth disease preventing lake access.
  - 2009: additional missing data due to weather conditions.
- Some samples taken from shore (Flag 2) when buoy access was not possible, which may affect integration depth comparability.

## Usage considerations and data preparation
- Suitable for long-term trend analysis, climate-related studies, lake chemistry modelling, and correlating physical/chemical parameters with phytoplankton dynamics.
- Prior to analysis, users should:
  - Apply quality control to identify and handle outliers and potential calibration offsets.
  - Address non-integrated shore samples vs buoy-integrated samples (consider stratification implications).
  - Properly handle detection-limit indicators (<) in analyses.
  - Manage gaps due to missing periods (e.g., 2001, 2009) and assess impact on time-series analyses.
  - Consider combining with external datasets (climate data, other lake records) for broader insights.

## Example publications using the dataset
- George, G., Hurley, M., Hewitt, D. (2007). The impact of climate change on the physical characteristics of the larger lakes in the English Lake District. Freshwater Biology.
- Maberly, S.C., Barker, P.A., Stott, A.W., De Ville, M.M. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change.
- Winfield et al. (2006–2017) various works on fisheries, vendace conservation, and lake ecosystem responses in the English Lake District.
- These publications exemplify applications in climate impacts, lake productivity, and fish community dynamics using this dataset.