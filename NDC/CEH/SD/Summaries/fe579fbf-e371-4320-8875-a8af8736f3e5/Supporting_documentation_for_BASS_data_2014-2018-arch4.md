# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018

## Overview
- Long-term monitoring dataset collected fortnightly at Bassenthwaite Lake, Cumbria, England (2014–2018).
- Variables included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Units: TEMP (°C); OXYG (% air-saturation); SECC (m); ALKA (µg CaCO3 per L); pH (unitless); NH4N, NO3N, PO4P, TOTP, SIO2, TOCA (µg per L).
- Water samples were integrated from 0 to 5 m; measurements were taken from a boat at the deepest part buoy; some shore samples when buoy access was not possible.
- Data cover January 2014 through end of 2018; long-term monitoring ended early 2019 due to funding shortages.

## Sampling regime and collection methods
- Fortnightly sampling as part of ongoing long-term monitoring.
- Primary sampling from a marked buoy location at the lake’s deepest point; when infeasible, shore sampling occurred alongside temperature and oxygen measurements.
- Water samples were not integrated on shore-sampling occasions (Flag 2).

## Quality control
- Data delivered are raw and have not been quality controlled or calibrated.
- Double entered and visually checked for errors.
- Missing data attributed to weather conditions or staff shortages.

## Data structure
- Data provided as a comma separated values (CSV) file with the following columns:
  - Date: Date of measurement.
  - Variable, Description: Temperature (TEMP, °C); OXYG (% air-saturation); SECC (m); ALKA (µg CaCO3 per L); pH; NH4N (µg N per L); NO3N (µg N per L); PO4P (µg P per L); TOTP (µg P per L); SIO2 (µg SiO2 per L); TOCA (µg per L).
  - Value, Description: Measured values for each variable.
  - Sign (if<LOD), Description: Indicates if value is below detection limit with a < sign.
  - Flag, Description: 1 = sampled at buoy; 2 = shore sample (buoy visit not possible).

## Data availability and usage
- Data are available to download as part of the published dataset.
- Example publications utilizing this dataset include:
  - Wang et al. (2016) Scientific Reports – coupling of carbon and silicon geochemical cycles in rivers and lakes.
  - Winfield et al. (2017) Fundamental and Applied Limnology – vendace reappearance in Bassenthwaite Lake under multiple stressors.
  - Woolway et al. (2016) Bulletin of the American Meteorological Society – lake surface temperatures (in State of the Climate 2015).
- An overview reference: Maberly et al. (2017) on long-term ecological informatics and knowledge generation from research in the English Lake District.

## Limitations and considerations for data management
- Raw data status means downstream users should apply quality control and calibration as needed for analyses.
- Gaps may exist due to weather, access, or funding constraints; end of long-term monitoring occurred in 2019.
- Careful attention to detection limits (Sign <LOD) and sampling flags when integrating with other datasets.
- Metadata scope includes sampling methods, units, and data collection context to support proper data use and integration into broader data systems.