# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015

## Sampling regime and collection methods
- Location: automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Sensors: meteorological instruments and in-lake temperature sensors.
- Variables measured: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), lake water temperature at depths of 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30 and 35 m.
- Sampling frequency: data every 4 minutes; hourly averages computed.
- Time basis: all data in GMT; dates span 2012, 2013, 2014 and 2015.
- Data processing: hourly averages calculated from the 4-minute data (example given for 2 p.m.).
- Data storage lineage: Campbell Scientific datalogger used until 1 June 2012; Oracle database used from 1 June 2012 onwards.

## Quality control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure
- Format: comma separated values (CSV) file.
- Columns:
  - Date_GMT: date and time of measurement (GMT).
  - Water_temperature at depths: 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (°C).
  - Air_Temperature (°C).
  - Pyranometer: Solar radiation flux (W/m^2).
  - Wind Speed (m/s).

## Data usage and references
- Widely used in current scientific studies, including PhD work.
- Notable related publication: Woolway, Maberly, Jones, Feuchtmayr (2014) on a method for estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research, 50(6), 5131-5140).

## Data considerations and notes
- Raw data require calibration/quality control before formal analysis.
- Gaps exist due to maintenance and instrument issues; data coverage is limited to 2012–2015.

## Data access and discoverability
- Provided as a CSV file with clearly defined columns and units; time stamps in GMT.
- Specific repository/location not stated, but data structure and lineage are documented.