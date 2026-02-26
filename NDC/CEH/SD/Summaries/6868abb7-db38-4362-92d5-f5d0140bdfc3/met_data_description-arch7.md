# Supporting Documentation

## Overview
- Dataset focusing on soil temperature and volumetric water content (VWC) from plots at three contrasting geologies in Hampshire Avon (chalk, clay, greensand) within unimproved pastures.
- Timeframe: measurements from 02 December 2013 to 02 September 2015.
- Spatial scope: three sites with OS Grid References:
  - Chalk: ST 85862 38261
  - Clay: ST 92218 27263
  - Greensand: SU 09720 57896
- Experimental design: plots subject to ambient (control) conditions or active surface warming.

## Part One: File summary
- File: met_data.csv
- Description: Soil temperature and volumetric water content data from plots at three contrasting geologies.
- Location identifiers: Chalk (CH), Clay (CL), and Greensand (site code for Greensand not explicitly specified in the text).

## Part Two: Dataset structure
- datetime: date and time at the conclusion of measurement, format ddmmmyyyy:hh:mm:ss
- site: two-character code per site (CH = chalk, CL = clay; Greensand code not specified)
- plot: numeric identifier for each measurement
- treatment: two-character code (CO = control, warming)
- temp: soil temperature in °C
- moisture: volumetric water content in m3 m-3

## Part Three: Methods summary
- Sampling frame: plots co-located with lysimeters in unimproved pastures across three underlying geologies in the Hampshire Avon catchment.
- Depth and sensors: sensors placed 5 cm below the soil surface; thermistor (ST1) for temperature and theta probe (ML2) for VWC.
- Data collection: near-continuous measurements; data loggers GP1 and DL2e; hourly mean values calculated for all sensors.
- Quality control: post-measurement QC to remove failed sensors (often due to animal damage); data cleaned and transformed, with datasets potentially combined across plots.

## Depositors and contact
- Depositor: James Stockdale
- Contact: james.stockdale@york.ac.uk

## Relevance for GIS Specialists
- Produces a spatially-referenced time-series dataset across three geologies, suitable for map-based analyses of soil temperature and moisture dynamics under different warming treatments.
- Clear attribute schema (site, plot, treatment, temp, moisture) and precise spatial references enable integration with GIS layers and temporal analysis.