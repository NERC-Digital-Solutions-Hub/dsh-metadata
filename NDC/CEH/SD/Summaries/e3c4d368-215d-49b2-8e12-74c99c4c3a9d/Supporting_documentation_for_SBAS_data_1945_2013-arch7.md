# Supporting Document
Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013. Maberly, S.C., Brierley, B., Carter, H.T., Clarke, M.A., De Ville, M.M., Fletcher, J.M., James, J.B., Keenan, P., Kelly, J.L., Mackay, E.B., Parker, J.E., Patel, M., Pereira, M.G., Rhodes, G., Tanna, B., Thackeray, S.J., Vincent, C., Feuchtmayr, H. (2017)

## Overview
- Long-term monitoring dataset (1945–2013) for Windermere's South Basin.
- Variables: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), phytoplankton chlorophyll a (TOCA).
- Historical custody: Freshwater Biological Association; since 1989, Centre for Ecology & Hydrology (CEH) and predecessors.
- Data provided for download as CSV; raw/uncalibrated (except some 2005+ double entries) but visually checked.

## Sampling regime and collection methods
- Frequency: weekly or fortnightly sampling.
- Depths covered: integrated samples from 0–5 m (1945–1962), 0–10 m (1962–1964), and 0–7 m (1964 onward).
- Location and collection: measurements taken from a boat at a marked buoy at the deepest part of the lake.
- Time frame: measurements from March 1945 to end of 2013.

## Data content and units
- TEMP: surface temperature, degrees Celsius.
- OXYG: surface oxygen saturation, % air-saturation.
- SECC: Secchi depth, metres.
- ALKA: alkalinity, µg CaCO3 per litre.
- pH: unitless.
- NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: concentrations in µg per litre (with TOCA as chlorophyll a).
- Data structure: each row includes sdate (measurement date), variable, value, and sign_if_LT_LOD (indicates below detection limit with a "<" sign).

## Data quality and limitations
- RAW data are not quality controlled or fully calibrated.
- Data have been visually checked; formal QC/calibration not applied within this dataset.
- Depth-integrated sampling means some variables come from different depth ranges over time; users should account for this when comparing periods.

## Data structure (for GIS use)
- File format: CSV.
- Columns: sdate, variable, value, sign_if_LT_LOD.
- Each row represents a single measurement for a given variable at the South Basin buoy location and date.

## Spatial and temporal context for GIS applications
- Spatial: single fixed sampling location (South Basin buoy, deepest part of Windermere); suitable for time-series mapping and trend analysis at a single site or as part of a larger lake/watershed GIS dataset.
- Temporal: 1945–2013; long-running record enables historical change detection, with variable sampling intervals and depth integration that should be considered in time-based analyses.

## Recent publications and usage
- Examples of dataset usage include studies on early warning indicators, perch ecology, climate-related ecological dynamics, phytoplankton phenology, environmental DNA in lakes, and broader climate/change research related to lakes and windermere.

## Practical considerations for GIS specialists
- Prepare for potential depth-scale inconsistencies when modeling across years.
- Treat data as raw inputs needing QC/calibration if precise quantitative comparisons are required.
- Integrate with other Windermere or CEH datasets to enhance spatial analysis beyond a single buoy location.