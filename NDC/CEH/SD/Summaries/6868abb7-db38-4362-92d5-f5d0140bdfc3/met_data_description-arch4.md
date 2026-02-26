# Supporting Documentation

## Overview
- Datasets: Hampshire Avon: soil temperature and water content data from three sub-catchments (two dataset entries)
- Depositor: James Stockdale
- Contact: james.stockdale@york.ac.uk

## File summary
- met_data.csv
- Timeframe: 02-Dec-2013 to 02-Sep-2015
- Description: Soil temperature and volumetric water content from plots at three contrasting geologies
- Location references (OS Grid):
  - Chalk: ST 85862 38261
  - Clay: ST 92218 27263
  - Greensand: SU 09720 57896

## Dataset structure
- datetime: date and time of measurement (format: ddmmmyyyy:hh:mm:ss)
- site: two-character site code per location; CH = chalk, CL = clay, greensand (code not specified for greensand)
- plot: measurement number
- treatment: two-character code; CO = control, warming
- temp: soil temperature in °C
- moisture: volumetric water content in m3 m-3

## Methods summary
- Setting: measurements from lysimeter-equipped plots in unimproved pastures across three underlying geologies in the Hampshire Avon catchment
- Sensor placement: 5 cm below the soil surface
- Treatments: ambient (control) or active surface warming (warming)
- Instruments: thermistors (ST1, Delta-T Devices) and theta probes (ML2, Delta-T Devices)
- Data recording: data loggers (GP1, DL2e); hourly means calculated
- Quality control: post-measurement QC to remove failed sensors (often due to animal damage)