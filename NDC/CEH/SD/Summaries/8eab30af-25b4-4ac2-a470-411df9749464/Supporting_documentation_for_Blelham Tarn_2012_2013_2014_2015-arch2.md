# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Purpose and scope
- Describes a dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measures meteorological variables and in-lake temperature across multiple depths to support environmental monitoring and analyses.

## Sampling regime and collection methods
- Instruments: meteorological sensors and platinum resistance thermometers for lake temperatures.
- Variables included: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperatures.
- Depths for water temperature: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 meters.
- Sampling interval: every 4 minutes.
- Hourly averages: calculated by a Campbell Scientific datalogger (until 19 July 2012) and an Oracle database (from 19 July 2012 onwards). Hour value represents the average of the interval ending at that hour (e.g., 2 p.m. is the average of 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- Time standard: all data in GMT.

## Data quality and limitations
- Data are raw and not yet calibrated or quality controlled.
- Visually checked; obvious hardware errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and variables
- Data provided as a CSV with columns including:
  - Date_GMT (date/time in GMT)
  - Water_temperature at depths: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m
  - Air_Temperature (°C)
  - Pyranometer (solar radiation flux in W/m^2)
  - Wind Speed (m/s)

## Temporal coverage
- Years: 2012, 2013, 2014, and 2015.

## Reuse and potential analyses
- Dataset has been used in several current scientific studies, including PhD research.
- Suitable for environmental monitoring analyses, lake temperature profiling, and examining relationships with meteorological variables.
- Aligns with standardised data presentation for integration into reports, maps, and charts; supports data sharing and portal uploads.

## Processing and notes for analysts
- Data are raw and should be calibrated/quality controlled for precise analyses.
- Hourly averaging method is explicitly defined and should be applied consistently during processing.
- When integrating with other datasets, consider time alignment (GMT) and depth-resolved temperature fields for robust environmental health assessments.