# Supporting Documentation

## Part One: File summary
- Dataset name: met_data.csv; period from 02-Dec-2013 to 02-Sep-2015.
- Description: Soil temperature and volumetric water content from plots at three contrasting geologies.
- Location (OS Grid References):
  - Chalk: ST 85862 38261
  - Clay: ST 92218 27263
  - Greensand: SU 09720 57896
- Depositor: James Stockdale (York). Contact: james.stockdale@york.ac.uk

## Part Two: Dataset structure
- datetime: date and time of measurement conclusion (format: ddmmmyyyy:hh:mm:ss).
- site: two-character site code (CH = chalk, CL = clay, greensand).
- plot: number allocated to each measurement.
- treatment: two-character code (CO = control, warming).
- temp: soil temperature in °C.
- moisture: volumetric water content in m³ m⁻³.

## Part Three: Methods summary
- Measurements taken from plots co-located with lysimeters in unimproved pastures across three underlying geologies in the Hampshire Avon catchment.
- Sensors placed 5 cm below the soil surface; plots experienced either ambient conditions (control) or active surface warming.
- Near-continuous measurements of soil temperature and volumetric water content using:
  - Thermistors (ST1, Delta-T Devices)
  - Theta probes (ML2, Delta-T Devices)
- Data loggers: GP1 and DL2e (Delta-T Devices).
- Hourly mean values calculated from sensor data.
- Post-measurement quality control to remove failed sensors (typically due to animal damage).