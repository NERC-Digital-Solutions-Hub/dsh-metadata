# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018

## Overview
- Long-term monitoring dataset (2014–2018) of surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a from Derwent Water, Cumbria, England.
- Fortnightly sampling; measurements taken from a boat at a marked buoy location (deepest part of the lake) or from the shore when the buoy could not be visited.
- Variables and units include: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 L−1), pH, NH4N (µg N L−1), NO3N (µg N L−1), PO4P (µg P L−1), TOTP (µg P L−1), SIO2 (µg SiO2 L−1), TOCA (µg L−1).
- Data cover January 2014 to the end of 2018; long-term monitoring ended early 2019 due to funding shortages.

## Sampling regime and collection methods
- Fortnightly sampling regime as part of ongoing monitoring.
- Measurements collected from the deepest part of the lake at the buoy location; when inaccessible, samples taken from the shore.
- Water samples are integrated from 0 to 5 m depth.
- Some samples were not integrated due to visit constraints (Flag 2).
- Data provided as raw observations (not yet quality controlled/calibrated) but double entered and visually checked.
- Missing data typically due to weather conditions or staff shortages.

## Quality control and data integrity
- Data are raw and have not undergone formal quality control or calibration.
- Double entry and visual checks performed to ensure accuracy.
- Be cautious when using data for high-precision analyses; consider applying quality control/calibration steps when appropriate.

## Data structure and contents
- File format: comma-separated values (CSV).
- Columns:
  - Date: measurement date.
  - Variable, Description: name and description of each measured variable (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value, Description: measured values for each variable.
  - Sign (if<LOD), Description: indicates if a value is below the detection limit (a "<" sign).
  - Flag, Description: indicates sampling location; Flag=1 = buoy; Flag=2 = shore.
- Example structure supports joining with other datasets and creating data products (dashboards, reports) for self-serve exploration.

## Use, limitations, and access
- Examples of published work using this dataset include: 
  - Winfield et al. (2017) on vendace reappearance in Bassenthwaite Lake.
  - Woolway et al. (2016) on lake surface temperatures.
  - Related overview: Maberly et al. (2017) on long-term ecological informatics in the English Lake District.
- Suitable for analyses of long-term water quality and phytoplankton dynamics, trend analysis, and cross-variable relationships.
- Accessibility note: dataset is downloadable as CSV; users should account for raw status and potential gaps/non-integrated samples.

## End of monitoring and context
- Data capture period: 2014–2018.
- Long-term monitoring ended early 2019 due to funding shortages; consider this when planning longitudinal analyses or seeking extension data.

## Practical considerations for Data Support
- When building data products, clearly document the raw status and any planned QC steps.
- Provide guidance on handling Flag 2 (shore) samples and non-integrated depth data.
- Include metadata on units, detection limits, and any data gaps or anomalies to support robust analysis and reproducibility.