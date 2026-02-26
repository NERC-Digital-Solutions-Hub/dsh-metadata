# Data collected 2017-18 during field transplant on Mt Etna

## Overview
- Field study on Mt Etna (2017–2018) deploying Tinytag dataloggers to record temperature near transplanted plants.
- Three dataloggers per transplant site, left in the field for 1 year; daily min and max temperatures were extracted.

## Methods
- Deployment: Tinytag dataloggers placed at plant height adjacent to transplanted plants at each site.
- Quality control: Dataloggers were kept together before deployment to ensure accuracy.
- Recording: Daily minimum and maximum temperatures (°C) were captured for each day over the deployment period.

## Variables / Dataset structure
- Elevation: Transplant elevations at 500 m, 1000 m, 1500 m, and 2000 m above sea level (ASL).
- Block: Three replicate experimental plots per elevation, labeled A, B, and C.
- Date: Date of temperature recording.
- Temp.Min: Daily minimum temperature (°C).
- Temp.Max: Daily maximum temperature (°C).

## Data considerations for GIS use
- Spatial references: No explicit coordinates provided; data are organized by elevation and replicate blocks, suitable for spatial strata analysis if geolocated elsewhere.
- Temporal scope: Daily temperature data spanning approximately 2017–2018.
- Units: Celsius for temperature; elevations in meters ASL.
- Potential GIS applications: create time-series or thematic maps of daily min/max temperatures by elevation and block; aggregate to seasonal or annual summaries; integrate with other environmental layers if location metadata is added.