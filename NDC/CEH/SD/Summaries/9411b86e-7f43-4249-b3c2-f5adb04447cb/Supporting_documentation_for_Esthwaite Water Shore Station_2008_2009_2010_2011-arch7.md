# Data from a meteorological station next to Esthwaite Water 2008, 2009, 2010 and 2011.

## Overview
- Meteorological dataset from a station on top of a boathouse in Cumbria, England, next to Esthwaite Water.
- Records air temperature and wind speed from 2008 to 2011.
- Measurements are taken every 4 minutes; hourly averages are produced by a Campbell Scientific datalogger.
- All times are in GMT (UTC).

## Sampling regime and collection methods
- Instruments located at the boathouse site; suitable for integration with spatial context in GIS.
- Parameters include:
  - Air_Temperature: degrees Celsius
  - Wind_Speed: metres per second
- Hourly average values represent the preceding hour (e.g., 2 PM value = average of 1–2 PM, including the 2 PM measurement and excluding the 1 PM measurement).

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to maintenance or sensor/logger problems.

## Data structure
- Stored as CSV with columns:
  - Date_GMT: date and time in GMT
  - Air_Temperature: air temperature in degrees C
  - Wind_Speed: wind speed in m/s

## Temporal coverage and context
- Time period: 2008–2011
- All timestamps are in Greenwich Mean Time; data are used in ongoing scientific studies (including PhD work).

## GIS considerations and recommended usage
- Location awareness: fixed site near Esthwaite Water; include latitude/longitude metadata for mapping.
- Use in map-based visualizations:
  - Time-enabled maps or dashboards showing temperature and wind trends from this site.
  - Potential integration with other spatial datasets (topography, land cover, water body features).
- Data quality and preparation:
  - Treat as raw data; apply calibration/QA if combining with calibrated datasets.
  - Address gaps through documentation or gap-filling strategies as appropriate.
  - Ensure consistent time handling (UTC/GMT) when linking with other time-series data.
- Metadata and provenance:
  - Document measurement cadence (4-minute interval) and hourly aggregation method.
  - Note the single-station limitation and consider incorporating additional stations for broader spatial analysis.