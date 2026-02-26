# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Data collected from an automatic lake monitoring buoy in Esthwaite Water, Cumbria, England.
- Measurements include air temperature, solar radiation, wind speed, and a vertical temperature profile of the lake.
- Temperatures are recorded at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 meters.
- Sampling frequency is every 4 minutes; hourly averages are calculated by a Campbell Scientific datalogger.
- All timestamps are in GMT and cover the years 2012–2015.

## Sampling regime and collection methods
- Instruments on the buoy measure:
  - Air temperature (°C)
  - Solar radiation flux (Pyranometer) (W/m²)
  - Wind speed (m/s)
  - Water temperature at multiple depths (°C)
- Data are stored in a CSV format with a defined column structure and descriptions.

## Data quality and limitations
- The dataset consists of raw data not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps occur due to buoy maintenance or sensor/logger problems.
- A new temperature chain was installed in August 2015.

## Data structure and schema
- Data format: comma separated values (CSV).
- Key columns:
  - Date_GMT (timestamp in GMT)
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (water temperature at each depth, °C)
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation flux, W/m²)
  - Wind_Speed (m/s)

## Measurements and units
- Water temperatures: degrees Celsius (°C) at listed depths.
- Air temperature: degrees Celsius (°C).
- Solar radiation: Watts per square metre (W/m²).
- Wind speed: metres per second (m/s).

## Usage and context
- The buoy data are being used in several current scientific studies, including those involving PhD students.

## GIS relevance and potential uses
- Enables time-series analysis of vertical temperature structure in the lake.
- Can be integrated with meteorological datasets for correlative studies (air temperature, solar radiation, wind).
- Suitable for creating temporal layers or indicators of thermal stratification; note that data come from a single buoy, so spatial interpretation should be limited and ideally supplemented with additional monitoring locations.

## Data provenance and referencing
- Source: Esthwaite Water buoy observations, 2012–2015.
- Citation: Jones, I.D.; Feuchtmayr, H.; Maberly S.C. (2017). Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015.