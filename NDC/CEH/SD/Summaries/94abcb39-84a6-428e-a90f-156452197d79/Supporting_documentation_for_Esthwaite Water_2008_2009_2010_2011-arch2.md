Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Longitudinal dataset from an automatic lake monitoring buoy at Esthwaite Water, Cumbria, covering 2008–2011.
- Measurements include air temperature, solar radiation, wind speed, and lake water temperature profiles at 0.43 to 11.43 m depth.
- Data cadence: instruments record every 4 minutes; hourly averages are calculated by a Campbell Scientific datalogger.
- All timestamps are in GMT; dates span 2008–2011.
- Raw data are provided without calibration/quality control; visual checks performed and obvious hardware errors removed.
- Gaps mainly due to buoy maintenance or sensor/logger issues; notable ice-damage event and temperature chain loss in January 2010.

## Sampling regime and collection methods
- Location: automatic monitoring buoy on Esthwaite Water, Cumbria, England.
- Measured variables:
  - Air temperature (degrees C)
  - Solar radiation flux (Pyranometer; Watts per square metre)
  - Wind speed (m/s)
  - Water temperature at depths: 0.43 m, 1.43 m, 2.43 m, 3.43 m, 4.43 m, 5.43 m, 6.43 m, 7.43 m, 8.43 m, 9.43 m, 10.43 m, 11.43 m
- Data processing: hourly averages represent the period from the previous hour (excluding 1 p.m. data, including 2 p.m. data).
- All measurements recorded in GMT.

## Data structure
- File format: comma-separated values (CSV).
- Columns include:
  - Date_GMT
  - 0.43m, 1.43m, 2.43m, 3.43m, 4.43m, 5.43m, 6.43m, 7.43m, 8.43m, 9.43m, 10.43m, 11.43m (lake temperature in °C at respective depths)
  - Air_Temperature (°C)
  - Pyranometer (solar radiation flux in W/m²)
  - Wind_Speed (m/s)

## Quality Control
- Data are raw and have not been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps attributed to buoy maintenance or sensor/logger problems.
- Notable event: ice cover and buoy damage in January 2010 leading to loss of the temperature chain.

## Data usage and impact
- The buoy data have supported multiple scientific studies and PhD work.
- Documented use in publications, including:
  - Studies on onset of thermal stratification in lakes from surface measurements (Water Resources Research, 2014)
  - Diel variability in epilimnion temperatures across English lakes (Inland Waters, 2015)
  - Interannual forcing effects on hypolimnetic soluble reactive phosphorus (Freshwater Biology, 2014)
  - Sediment focusing and heterogeneity of organic carbon and phosphorus burial (Freshwater Biology, 2012; 2011)
  - Spatial heterogeneity in small temperate lakes under typical forcing (Fundamental and Applied Limnology, 2011)
- Indicates utility for environment monitors aiming to link meteorological forcing with lake thermal structure and biogeochemical processes.

## Relevance for environmental analysts
- Demonstrates end-to-end monitoring workflow: data collection from autonomous buoys, multi-parameter sensing, and hourly aggregation.
- Provides a standard data structure and metadata (column naming, depth associations, time zones) conducive to data standardization and cross-study comparisons.
- Illustrates practical QA considerations for monitoring datasets (raw vs. quality-controlled data, gap analysis, event impacts such as ice cover).
- Supports data integration with other environmental datasets to enhance monitoring value beyond single-use analyses.

## Limitations and considerations
- Data are raw and not calibrated; additional QA/QC is required for high-stakes analyses.
- Gaps due to maintenance and equipment issues; some years have more complete coverage than others.
- Specific wiring/datalogger issues (e.g., 2010 ice-related damage) may affect continuity of time series.
- Access to the data portal or repository is not specified; dataset is reported with CSV structure and published studies.