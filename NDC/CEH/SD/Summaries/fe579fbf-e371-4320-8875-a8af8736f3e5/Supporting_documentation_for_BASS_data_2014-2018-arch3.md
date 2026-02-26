# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018

## Purpose and scope
- Part of an ongoing long-term monitoring dataset at Bassenthwaite Lake, Cumbria, England.
- Measures: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sampling frequency: fortnightly.
- Sample location: integrated from 0–5 m; collected from boat at the deepest part near a buoy; if buoy inaccessible, samples collected from shore.
- Timeframe: data from January 2014 to end of 2018; long-term monitoring ended early 2019 due to funding shortages.

## Sampling regime and collection methods
- Data are provided as a CSV with fields: Date, Variable/Description (each measured parameter and units), Value/Description, Sign (indicating below detection limit with a < sign), Flag (1 = buoy site, 2 = shore site when buoy visit not possible).
- Water samples are from 0–5 m integrated depth; measurements made at a specified buoy location when possible.

## Quality control and data quality
- Data are raw and have not yet been quality controlled or calibrated.
- Data quality processes performed: double data entry and visual checks.
- Missing data attributed to weather conditions or staff shortages.

## Data structure and format
- CSV columns include:
  - Date: measurement date
  - Description: variable name (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value
  - Sign (if<LOD): indicates values below detection limit
  - Flag: sampling site indicator (1 = buoy, 2 = shore)
- Units:
  - TEMP: °C
  - OXYG: % air-saturation
  - SECC: m
  - ALKA: µg CaCO3 per L
  - pH: unitless
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: µg per L

## Data usage and provenance
- Example publications using the dataset:
  - Wang et al. (2016) Scientific Reports
  - Winfield, Fletcher & James (2017) Fundamental and Applied Limnology
  - Woolway et al. (2016) Bulletin of the American Meteorological Society (surface temperatures mention)
- Overview reference: Maberly et al. (2017) Ecological Informatics; long-term ecological knowledge from English Lake District.

## Practical implications for monitoring frameworks
- Demonstrates integration of multi-parameter lake health indicators into a single long-term dataset.
- Highlights practical data management needs:
  - Metadata completeness and clarity (unit definitions, detection limits, sampling location flags).
  - Consistency in sampling protocols and documentation, especially when sampling site access changes.
  - Open data considerations balanced with governance; dataset provided in CSV with explicit metadata on sampling and detection limits.
- Sustainability considerations:
  - Long-term datasets at risk when funding ends, underscoring the importance of ongoing support and clear data-sharing governance.