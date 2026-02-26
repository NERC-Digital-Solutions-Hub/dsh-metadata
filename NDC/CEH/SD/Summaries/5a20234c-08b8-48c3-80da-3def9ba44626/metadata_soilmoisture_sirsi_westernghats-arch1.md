# Soil moisture data, Sirsi, Western Ghats

## Overview
- Measurements of soil moisture near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Location: 14.49 N, 74.75 E; altitude 538 m.
- Timeframe: January 2020 – January 2022.
- Depths: 10 cm, 25 cm, 50 cm, 110 cm.
- Sensor: Campbell CS616 Water Content Reflectometers.
- Site context: sensors on a gentle slope ~500 m from the local valley bottom.

## Data structure and content
- Data stored in a CSV with variables/columns.
- NaN indicates missing data.
- Key columns:
  - Date (DD/MM/YY)
  - Time (HH:MM:SS)
  - SM_m3/m3_at10cm_depth
  - SM_m3/m3_at25cm_depth
  - SM_m3/m3_at50cm_depth
  - SM_m3/m3_at110cm_depth
- Units: soil moisture (m3/m3). 

## Measurement details
- Multi-depth soil moisture measurements (10, 25, 50, 110 cm) over two years.
- Collected at a farm on a gentle slope, approximately 500 m from the valley bottom.

## Quality control and limitations
- Data were quality checked by the team.
- Sensors were not independently calibrated using soils from this site.
- Implication: potential limitations in absolute accuracy due to lack of site-specific calibration.

## Considerations for analysis
- Provides local, multi-depth time series suitable for examining vertical moisture profiles and temporal trends.
- Be mindful of calibration caveat when interpreting absolute moisture values.