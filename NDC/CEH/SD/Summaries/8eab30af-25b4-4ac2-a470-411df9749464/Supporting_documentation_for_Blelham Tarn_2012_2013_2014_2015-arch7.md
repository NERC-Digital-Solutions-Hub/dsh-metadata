# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy located in Blelham Tarn, Cumbria, England.
- Measured variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperature profiles.
- Water temperature measurements at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Time span: 2012–2015.
- Measurement cadence: every 4 minutes; hourly averages provided.

## Sampling regime and collection methods
- Instruments: meteorological sensors on the buoy and platinum resistance thermometers for lake temperature.
- Depth coverage for temperature: 0.5–12 m (various depths listed above).
- Data aggregation: hourly averages calculated from 4-minute data.
  - Pre-2012-07-19: hourly averages produced by a Campbell Scientific datalogger.
  - From 2012-07-19 onwards: hourly averages produced by an Oracle database.
- Timestamp: all data in GMT.

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual spot-checks conducted; obvious hardware-related errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and format
- Format: comma separated values (CSV).
- Columns include:
  - Date_GMT: date and time of measurement (GMT).
  - Water_temperature at depths: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m.
  - Air_Temperature (°C).
  - Pyranometer (solar radiation in W/m²).
  - Wind Speed (m/s).
- Units: Water and Air temperatures in °C; Pyranometer in W/m²; Wind Speed in m/s.
- Note: The buoy data are currently used in several ongoing scientific studies, including PhD work.

## Temporal and geographical notes
- Time reference: GMT.
- Geographic scope: Blelham Tarn, Cumbria, England.
- Data cover 2012–2015.

## GIS considerations and potential uses
- Suitable for map-based visualization and time-series analyses after cleaning and calibration.
- Can support:
  - Vertical lake temperature profiles by depth over time.
  - Spatial overlays with meteorological layers for integrated surface and subsurface conditions.
- Important caveats for GIS use:
  - Data are raw and not yet calibrated; apply appropriate quality control/offsets before analysis.
  - Data gaps may require interpolation or handling in temporal analyses.
  - Only one buoy location is represented; spatial coverage is limited.

## Data limitations and caveats
- Raw, uncalibrated data.
- Data gaps due to maintenance or sensor/logger issues.
- Temporal aggregation is hourly; finer temporal resolution is available only as 4-minute measurements (not provided as hourly data).

## Usage notes
- The dataset supports visualization and exploratory analyses of lake temperature and local meteorology but should be calibrated and validated for precision analyses.
- Widely used in ongoing research, including work by PhD students.