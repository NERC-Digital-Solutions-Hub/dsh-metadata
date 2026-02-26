# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 2014 to 2018.

## Overview
- Long-term monitoring dataset from the North Basin of Windermere, Cumbria, England.
- Fortnightly sampling conducted from 2014 through 2018.
- Measurements cover physical, chemical, and biological indicators: surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.

## Data collected and sampling regime
- Water samples collected from a boat at a marked buoy location in the deepest part of the lake.
- Integrated sampling from the 0 to 7 m depth interval.
- Variables recorded: temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L^-1), pH, ammonium (NH4N, µg N L^-1), nitrate (NO3N, µg N L^-1), soluble reactive phosphate (PO4P, µg P L^-1), total phosphorus (TOTP, µg P L^-1), dissolved reactive silicon as SiO2 (SIO2, µg L^-1), phytoplankton chlorophyll a (TOCA, µg L^-1).

## Variables and units
- TEMP: surface temperature in degrees Celsius (°C)
- OXYG: surface oxygen saturation in % air-saturation
- SECC: Secchi depth in metres
- ALKA: alkalinity in µg CaCO3 per litre
- pH: acidity/alkalinity measure
- NH4N: ammonium in µg N per litre
- NO3N: nitrate in µg N per litre
- PO4P: soluble reactive phosphate in µg P per litre
- TOTP: total phosphorus in µg P per litre
- SIO2: dissolved reactive silicon as SiO2 in µg per litre
- TOCA: phytoplankton chlorophyll a in µg per litre

## Data structure and availability
- Data provided as a comma-separated values (CSV) file.
- Columns: Date (measurement date), Description (variable), Value (measurement value), Sign (indicates below detection limit with a < sign when applicable).
- Signalling for values below the limit of detection (LOD) is indicated in the Sign column (e.g., "<LOD").
- Data are raw (not yet quality controlled or calibrated) but have undergone double-entry and visual checks.

## Quality control and limitations
- Raw data not quality controlled or calibrated yet.
- Missing data occur due to weather conditions or staff shortages.
- Data may require QC/ calibration and handling of detection-limit issues before formal analysis.

## Funding and context
- Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Dataset has been used in published works related to climate state assessments, ecological dynamics, and long-term lake monitoring, illustrating its applicability for trend analysis and cross-domain studies.

## Examples of use and relevance for analysis
- Enables analysis of temporal trends and correlations among physical, chemical, and biological indicators in a freshwater lake.
- Suitable for developing and testing predictive relationships between water temperature, oxygen, nutrient chemistry, and chlorophyll a.
- Can be integrated with other ecological or meteorological datasets, with attention to its raw status and detection-limit considerations.
- Supports long-term ecological and climate-related research, as demonstrated by its use in related publications and ecological informatics studies.