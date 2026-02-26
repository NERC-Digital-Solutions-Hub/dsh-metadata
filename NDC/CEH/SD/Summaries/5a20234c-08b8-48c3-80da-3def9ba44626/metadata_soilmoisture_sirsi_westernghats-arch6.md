# Soil moisture data, Sirsi, Western Ghats

## Overview
- Measurements of soil moisture profiles near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Collected from January 2020 to January 2022 at soil depths of 10, 25, 50, and 110 cm.
- Sensors: Campbell CS616 Water Content Reflectometers; installed on a gentle slope ~500 m from the valley bottom.

## Location and timing
- Geographic coordinates: 14.49 N, 74.75 E; altitude 538 m.
- Date format: DD/MM/YY; Time format: HH:MM:SS.

## Data structure and fields
- Data stored in a CSV file with columns representing date, time, and soil moisture at each depth.
- Depth-specific fields:
  - SM_m3/m3_at10cm_depth
  - SM_m3/m3_at25cm_depth
  - SM_m3/m3_at50cm_depth
  - SM_m3/m3_at110cm_depth
- NAN denotes Not A Number (missing data). Variables are ordered in columns.

## Units and measurement details
- Soil moisture is expressed as volumetric water content (m3/m3).
- Date and time formats as described above.

## Quality control and limitations
- Data were quality checked by the team.
- Sensors were not independently calibrated using soils from this site, which may affect accuracy.

## Potential uses and data products
- Time-series analyses of soil moisture by depth.
- Depth-profile moisture assessments and trend identification.
- Create self-serve data products (e.g., dashboards, charts) to explore moisture dynamics over time.

## Data notes and guidance for use
- File format: CSV (filename indicates Soilmoisture_Sirsi_WesternGhats.csv).
- Handle missing data as NaN during analysis.
- Parse date and time to construct continuous time series for each depth.