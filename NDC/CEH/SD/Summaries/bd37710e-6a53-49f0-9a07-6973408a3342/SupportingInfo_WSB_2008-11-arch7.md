# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011

## Data availability and citation
- Data come from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Measured variables include air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths.
- Data are provided as a comma separated values (CSV) file.
- Available from the NERC Environmental Information Data Centre (EIDC) with DOI: https://doi.org/10.5285/bd37710e-6a53-49f0-9a07-6973408a3342

## Sampling regime and collection methods
- Location: Windermere South Basin, Cumbria, England.
- Buoy instruments include meteorological sensors and in-lake temperature sensors.
- Variables and units:
  - Air Temperature (degrees C)
  - Pyranometer / Solar radiation flux (Watts per square metre)
  - Wind Speed (metres per second)
  - Water temperature at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 metres (degrees C)
- Sampling frequency: data every 4 minutes; hourly averages provided by the Campbell Scientific datalogger.
- Time reference: all data in GMT (Greenwich Mean Time); dates from 2008–2011.

## Quality control
- Data are raw (not calibrated or fully quality controlled).
- Visual checks performed; obvious hardware-related errors removed.
- ~10 days in 2010 with no data due to logger/telemetry changes.
- Other gaps result from buoy maintenance or sensor/logger problems.

## Data structure
- Format: CSV with columns for:
  - Date GMT
  - Water temperature at 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m
  - Air Temperature
  - Pyranometer (solar radiation flux)
  - Wind Speed
- Temporal aggregation: hourly averages derived from 4-minute measurements (e.g., the value for 2 p.m. is the average of data between 1 and 2 p.m., including 2 p.m. measurement and excluding 1 p.m.).
- All timestamps are in GMT.

## Additional information
- The buoy dataset is used in multiple scientific studies, including PhD research.
- Notable publications that have used this dataset include:
  - 2014: A novel method for estimating onset of thermal stratification in lakes from surface measurements (Water Resources Research)
  - 2015: Diel variability in epilimnetic temperature for five lakes in the English Lake District (Inland Waters)
  - 2016: Diel surface temperature range scales with lake size (PLOS ONE)
- This context indicates the dataset supports broader ecological and limnological analyses and GIS-based mapping of lake conditions.