# Soil moisture data, Sirsi, Western Ghats

## Overview
- Measurements of soil moisture profiles near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Spatial context: latitude 14.49 N, longitude 74.75 E; altitude 538 m; on a gentle slope ~500 m from a valley bottom.
- Timeframe: January 2020 to January 2022.
- Depths measured: 10 cm, 25 cm, 50 cm, and 110 cm.
- Sensor type: Campbell CS616 Water Content Reflectometers.

## Data structure and format
- Data stored in a CSV file: Soilmoisture_Sirsi_WesternGhats.csv.
- Columns are organized in a fixed order with NaN indicating missing data.
- Date format: DD/MM/YY; Time format: HH:MM:SS.
- Recorded variables:
  - SM_m3/m3_at10cm_depth (soil moisture at 10 cm)
  - SM_m3/m3_at25cm_depth (soil moisture at 25 cm)
  - SM_m3/m3_at50cm_depth (soil moisture at 50 cm)
  - SM_m3/m3_at110cm_depth (soil moisture at 110 cm)

## Spatial and data quality context
- Data collected from a single farm site near Sirsi, Western Ghats.
- Quality control performed by the project team; sensors were not independently calibrated using soils from this site.
- Data may have gaps (NaN values) where measurements are unavailable.

## Practical GIS considerations
- Suitable for map-based visualization of depth-dependent soil moisture and for integrating with other spatial datasets (e.g., topography, land cover, rainfall).
- Users should account for missing values and consider the single-site nature when generalizing findings.
- Coordinate reference system is not specified; given explicit lat/lon, users can assign an appropriate CRS (e.g., WGS84) for GIS work.