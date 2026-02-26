# Supporting Documentation

## Overview
- Provides soil temperature and volumetric water content data from plots in unimproved pastures across three geologies in the Hampshire Avon catchment.
- Depositor: James Stockdale (james.stockdale@york.ac.uk)

## Part One: File summary
- met_data.csv
- From: 02 December 2013
- To: 02 September 2015
- Description: Soil temperature and volumetric water content from plots at three contrasting geologies
- Location (OS Grid References):
  - Chalk: ST 85862 38261
  - Clay: ST 92218 27263
  - Greensand: SU 09720 57896

## Part Two: Dataset structure
- datetime: date and time at conclusion of measurement (format ddmmmyyyy:hh:mm:ss)
- site: two-character code assigned to each site
  - CH = Chalk
  - CL = Clay
  - greensand
- plot: measurement plot number
- treatment: two-character code for treatment
  - CO = control
  - warming
- temp: soil temperature (°C)
- moisture: volumetric water content (m3 m-3)

## Part Three: Methods summary
- Plot setup: co-located with lysimeters in unimproved pastures across three underlying geologies in the Hampshire Avon catchment
- sensors: placed 5 cm below soil surface
- treatments: ambient control or active surface warming
- measurements: near-continuous soil temperature (thermistors, ST1) and volumetric water content (theta probes, ML2)
- data collection: recorded by data loggers (GP1, DL2e) with hourly mean values
- quality control: post-measurement QC to remove failed sensors (often due to animal damage)