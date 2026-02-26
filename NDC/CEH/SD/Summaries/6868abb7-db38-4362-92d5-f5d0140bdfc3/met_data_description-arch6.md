# Supporting Documentation

## Dataset provenance
- Dataset: Hampshire Avon: soil temperature and water content data from three sub-catchments
- File: met_data.csv
- Depositor: James Stockdale; Contact: james.stockdale@york.ac.uk

## Part One: File summary
- File name: met_data.csv
- Timeframe: From 02 Dec 2013 to 02 Sep 2015
- Description: Soil temperature and volumetric water content from plots at three contrasting geologies
- Location references:
  - Chalk: ST 85862 38261
  - Clay: ST 92218 27263
  - Greensand: SU 09720 57896

## Part Two: Dataset structure
- Columns and descriptions:
  - datetime: date and time at conclusion of measurement (format ddmmmyyyy:hh:mm:ss)
  - site: two-character code for site; CH = chalk, CL = clay, greensand
  - plot: plot number
  - treatment: two-character code; CO = control, warming
  - temp: soil temperature in °C
  - moisture: volumetric water content in m3 m-3

## Part Three: Methods summary
- Study design: Measurements from plots co-located with lysimeters in unimproved pastures across three geologies in the Hampshire Avon catchment
- Sensor placement: 5 cm below soil surface
- Treatments: ambient (control) and active surface warming (warming)
- Sensors and instruments: single thermistors (ST1) for temperature and theta probes (ML2) for moisture
- Data collection: near-continuous measurements recorded on data loggers (GP1 and DL2e); hourly mean values calculated
- Data quality: post-measurement quality control to remove failed sensors (often due to animal damage)