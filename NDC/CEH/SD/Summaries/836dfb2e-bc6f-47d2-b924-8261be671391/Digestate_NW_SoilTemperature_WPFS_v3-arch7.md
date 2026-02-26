# Details of data structure to ' Digestate_NF_SoilTemperature_WFPS.csv '

## Overview
- Supplements supporting documentation for data series in CINAg experiments.
- Metadata for dataset Digestate_NF_SoilTemperature_WFPS.csv.
- 4 columns and 31,778 rows.
- Origin: digestate from the wheat trial 2017, North Wyke Research station, Rothamsted Research.
- Measures soil temperature and water-filled pore space (WFPS) at 2.5 cm depth across ten plots.

## Dataset structure
- Columns (4 total) with headers, explanations, and units:
  - Time: Date and time of day.
  - Block: Blocks 1 to 5 (experimental design).
  - Soil_Temperature_degrees_celcius: soil temperature at 2.5 cm depth. Unit: Degrees Celsius.
  - WFPS_percent: water-filled pore space at 2.5 cm soil depth. Unit: Percent.
- Rows: 31,778.

## Spatial and temporal context
- Ten plots observed at a fixed depth of 2.5 cm.
- Study period: 2017 wheat trial.
- Locations: North Wyke Research station and Rothamsted Research.
- Temporal granularity implied by Time column (date and time of day).

## GIS relevance and potential uses
- Suitable for map-based visualisations of spatial variation and temporal change in soil temperature and WFPS.
- Can be mapped per plot (or block) and time point; supports time-series analyses.
- Potential to combine with other geospatial or agronomic datasets using Time and Block as linking keys.

## Data quality and integration notes
- This file is a structured extract supplement; ensure alignment with the main CINAg documentation.
- Verify timestamp consistency and handle any missing values when integrating with other layers.
- Units are explicit; maintain Celsius for soil temperature and percent for WFPS during integration.

## Provenance and references
- Related to supporting documentation: 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'.
- Dataset name: Digestate_NF_SoilTemperature_WFPS.csv.
- Part of the Digestate study components at North Wyke and Rothamsted Research.