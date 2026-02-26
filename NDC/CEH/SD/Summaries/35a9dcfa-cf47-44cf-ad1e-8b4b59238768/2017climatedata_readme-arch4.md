# Data collected 2017-18 during field transplant on Mt Etna

## Overview
- Field transplant study conducted on Mt Etna during 2017-2018.
- At each transplant elevation (500 m, 1000 m, 1500 m, 2000 m ASL) deployed three replicate plots (A, B, C).
- Three Tinytag dataloggers placed at plant height adjacent to transplanted plants; left in the field for 1 year and then collected.
- From dataloggers, daily minimum (Temp.Min) and maximum (Temp.Max) temperatures were extracted in degrees Celsius.

## Data collection design and variables
- Elevation: Transplant elevations 500 m, 1000 m, 1500 m, 2000 m ASL.
- Block: Three replicate plots (A, B, C) within each elevation.
- Date: Date of the recorded temperature.
- Temp.Min: Daily minimum temperature (°C).
- Temp.Max: Daily maximum temperature (°C).

## Quality control and data processing
- Dataloggers were kept together before deployment to ensure accuracy.
- Daily Temp.Min and Temp.Max were extracted from the logger readings after the deployment period.

## Data governance and structure
- Dataset likely organized by Date, Elevation, and Block with Temp.Min and Temp.Max values.
- Represents one year of temperature data per site/elevation, gathered via in-field sensors.

## Usage considerations for data leadership
- Replication (A, B, C) enables assessment of within-elevation variability.
- Clear variable naming (Date, Elevation, Block, Temp.Min, Temp.Max) supports discoverability and reuse.
- Documentation notes calibration/quality check step (keeping dataloggers together) as a QA measure; provenance is explicit through deployment and collection timeline.
- Limitations not detailed: no instrument metadata (IDs, calibration dates beyond initial check), file formats, or missing data handling described; scope is limited to Mt Etna field sites and specified elevations.