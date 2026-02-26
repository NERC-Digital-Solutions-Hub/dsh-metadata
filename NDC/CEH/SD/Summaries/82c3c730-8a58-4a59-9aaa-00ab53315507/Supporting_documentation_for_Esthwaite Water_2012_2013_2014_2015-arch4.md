# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy on Esthwaite Water, Cumbria, England.
- Measures air temperature, solar radiation (pyranometer), wind speed, and lake water temperature profiles.
- Temporal scope: 2012–2015; times are in Greenwich Mean Time (GMT).

## Sampling regime and collection methods
- Data collection frequency: every 4 minutes.
- Hourly averages are calculated by a Campbell Scientific datalogger.
  - Example: 2 p.m. value = average of data from 1:00 to 2:00 p.m., excluding 1:00 p.m. data and including 2:00 p.m. data.

## Variables and data structure
- Water temperature: recorded at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 meters (in degrees C).
- Air temperature: (degrees C).
- Solar radiation: pyranometer, flux in Watts per square meter.
- Wind speed: (m/s).
- Data delivered as a comma-separated values (CSV) file with columns:
  - Date_GMT
  - 0.5m Water_temperature
  - 1m Water_temperature
  - 2m Water_temperature
  - 3m Water_temperature
  - 4m Water_temperature
  - 5m Water_temperature
  - 6m Water_temperature
  - 7m Water_temperature
  - 8m Water_temperature
  - 9m Water_temperature
  - 10m Water_temperature
  - 12m Water_temperature
  - Air_Temperature
  - Pyranometer
  - Wind_Speed

## Quality control and data health
- The dataset comprises raw data that have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.
- A new temperature chain was installed in August 2015.

## Temporal and site context
- Site location: Esthwaite Water, Cumbria, England.
- Depths covered for lake temperature profiling up to 12 m.

## Data accessibility and usage notes
- Data from this buoy are being used in several current scientific studies, including work by PhD students.
- Suitable for analyses requiring high-frequency, depth-resolved lake temperature and atmospheric coupling, with caveats about calibration status.

## Considerations for data governance and reuse (Data Leaders)
- Metadata completeness: units and column descriptions are specified, with explicit depth levels and measurement types.
- Data provenance: raw data with documented collection regime and processing (hourly averaging rules).
- Quality and reliability: raw status means future calibration/QA may be required for some applications.
- Discoverability and integration: structured CSV format facilitates integration with other data systems, enabling cross-dataset comparisons and co-ownership of data products.
- Potential use cases: baseline environmental monitoring, validation of models, cross-site comparisons, and collaborative research with ongoing studies.