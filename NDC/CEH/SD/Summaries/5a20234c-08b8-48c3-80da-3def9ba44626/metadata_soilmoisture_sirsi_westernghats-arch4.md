# Soil moisture data, Sirsi, Western Ghats

## Overview
- Dataset of soil moisture profiles from soil near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Measurements conducted from January 2020 to January 2022.
- Depths measured: 10 cm, 25 cm, 50 cm, and 110 cm.
- Location coordinates: latitude 14.49 N, longitude 74.75 E; altitude 538 m.
- Sensors: Campbell CS616 Water Content Reflectometers.
- Sensors installed on a gentle slope approximately 500 m from the local valley bottom.

## Collection method
- Measurements taken in situ on the farm site.
- Quality control performed by the team.
- Sensors were not independently calibrated using soils from this site.

## Data structure and format
- Data organized in columns within a CSV file.
- Missing data represented as NaN (Not A Number).

## Nature and units of recorded data
- Date format: DD/MM/YY; Time format: HH:MM:SS.
- Variables:
  - SM_m3/m3_at10cm_depth (soil moisture at 10 cm)
  - SM_m3/m3_at25cm_depth (soil moisture at 25 cm)
  - SM_m3/m3_at50cm_depth (soil moisture at 50 cm)
  - SM_m3/m3_at110cm_depth (soil moisture at 110 cm)
- Units: m3 m-3 (dimensionless soil moisture content)

## Quality control and limitations
- Data quality checked by the team.
- No independent calibration of sensors with site soils performed.
- Presence of NaN indicates missing data; no detail on data completeness or gap distribution provided.