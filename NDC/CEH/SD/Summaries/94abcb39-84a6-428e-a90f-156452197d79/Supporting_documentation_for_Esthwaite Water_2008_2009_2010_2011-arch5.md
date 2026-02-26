# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Scope and contents
- Dataset from an automatic lake monitoring buoy on Esthwaite Water, Cumbria, England.
- Measurements include air temperature (C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperatures at multiple depths (0.43–11.43 m).
- Data collection frequency: 4-minute measurements with hourly averages calculated by a Campbell Scientific datalogger.
- Time reference: GMT; dates cover 2008–2011.

## Sampling regime and collection methods
- Instruments on the buoy provide meteorological and in-lake temperature data.
- Water temperatures are recorded at 0.43 m, 1.43 m, 2.43 m, 3.43 m, 4.43 m, 5.43 m, 6.43 m, 7.43 m, 8.43 m, 9.43 m, 10.43 m, and 11.43 m depths.
- Data are provided in a CSV format with clearly defined column names and unit descriptions.

## Quality control and data limitations
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps attributable to buoy maintenance or sensor/logger issues.
- Notable incidents: unusually cold January 2010 with ice cover, buoy damage, and loss of the temperature chain.

## Data structure and metadata
- CSV file structure:
  - Date_GMT (Date and time of measurement)
  - 0.43m, 1.43m, ..., 11.43m (water temperatures in C)
  - Air_Temperature (C)
  - Pyranometer (Solar radiation flux in W/m^2)
  - Wind_Speed (m/s)
- Data descriptions accompany each column (depths, temperatures, and sensor types).

## Data usage and impact
- The buoy data are used in ongoing scientific studies and have been cited in multiple publications:
  - Woolway et al. (2014) on estimating onset of thermal stratification
  - Woolway et al. (2015) on diel variability in epilimnetic temperature
  - Mackay et al. (2012, 2011, 2014) on sediment focusing, organic carbon, phosphorus dynamics, and spatial heterogeneity
  - DeGasperi et al. (2016) and related works cited in the dataset description
- The dataset supports broader research in lake carbon, phosphorus cycling, and thermal dynamics.

## Governance considerations for Data Stewards
- Metadata should document:
  - Instrumentation (Campbell Scientific datalogger), measurement types, units, depths, and time standard (GMT).
  - Calibration status and any quality control steps (and noted limitations of raw data).
  - Sensor maintenance events and known gaps (including 2010 ice damage and data loss).
- Data provenance and citation: maintain clear references to publications that used the data for discoverability and credit.
- Data sharing and reuse: provide access via a discoverable repository with full metadata, data dictionary, and any future calibration or processing steps.
- Data maintenance: track updates, versioning, and any reprocessing (e.g., calibration) to ensure users understand the lineage of the hourly-averaged values derived from 4-minute measurements.