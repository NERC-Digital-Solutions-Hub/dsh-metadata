# Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Dataset overview
- Time-series environmental dataset from Onset data loggers measuring soil temperature, soil moisture, air temperature, relative humidity, and surface wetness.
- Collected across 5 locations representing main vegetation types at SikSik Creek catchment, Trail Valley Creek, NWT, Canada.
- Data are suitable for GIS-based visualization and spatial-temporal analysis of microclimate and moisture conditions.

## Data structure and files
- Data stored in 5 CSV files, each corresponding to one logger and vegetation type:
  - TVC_logger 1_sedge.csv
  - TVC_logger 2_riparian.csv
  - TVC_logger 3_betula.csv
  - TVC_logger 4_alder.csv
  - TVC_logger 5_lichen heath.csv

## Authors, maintainer, and contact
- Author/Owner: Lorna Street / Philip Wookey
- Maintainer: Lorna Street
- Contact email: l.e.street@ed-alumni.net

## Period of record
- Logger 1 (sedge): 02-Aug-2013 to 29-Jul-2015
- Logger 2 (riparian): 02-Aug-2013 to 21-Aug-2015
- Logger 3 (betula): 02-Aug-2013 to 21-Aug-2015
- Logger 4 ( alder): 02-Aug-2013 to 21-Aug-2015
- Logger 5 (lichen heath): 02-Aug-2013 to 29-Jul-2015

## Data records
- Logger 1: 418,072 records
- Logger 2: 539,115 records
- Logger 3: 539,115 records
- Logger 4: 539,110 records
- Logger 5: 418,060 records

## Locations (GPS)
- Logger 1: 68.74459771 N, 133.5021632 W
- Logger 2: 68.74533925 N, 133.4939524 W
- Logger 3: 68.74526449 N, 133.4925088 W
- Logger 4: 68.74516902 N, 133.4952195 W
- Logger 5: 68.74549767 N, 133.4969109 W
- Note: Coordinates are provided in decimal degrees; coordinate reference system is not specified.

## Methods and instrumentation
- Soil temperature: measured at 5 cm depth with Onset 12-bit Temperature Smart sensors.
- Air temperature and RH: measured at approximately 0.5 m above ground, shielded from radiation using Onset solar radiation screen; where applicable, measurements made with Onset 12-bit Temperature Smart sensors or Onset 12-bit Temperature/Relative Humidity Smart sensors.
- Surface wetness: measured at the lichen heath location using Onset Leaf Wetness sensor.
- Volumetric water content (VWC): measured at 5 cm depth using ECH2O EC-5 sensors with factory calibration (in hummock and inter-hummock positions where applicable).
- Sampling interval: 10 minutes; data are continuous with no gap-filling.
- Not all variables were measured at every location:
  - Logger 1: soil temp, air temp, RH, soil VWC
  - Logger 2: soil temp, air temp, RH, soil VWC (Sphagnum moss), soil VWC (under willow shrub)
  - Logger 3: soil temp (hummock), air temp, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 4: soil temp (hummock), air temp, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 5: soil temp (hummock), surface wetness, soil VWC (hummock), soil VWC (interhummock)

## Variables and units
- DateTime: Date and Time (dd/mm/yyyy HH:MM:SS)
- Tsoil.C: Soil temperature at 5 cm depth (°C)
- Tair.C: Air temperature (°C)
- RH.percent: Relative humidity (%)
- VWC.m3.per.m3: Volumetric water content (m3 m-3)
- Wetness.percent: Surface wetness (%)
- Missing value code: . (period)

## Data quality and usage notes for GIS
- Data are continuous with no gap-filling, enabling seamless time-series analysis within GIS.
- Five spatially distinct sites enable comparative vegetation-type analyses and microclimate mapping.
- Variants and partial measurements per site should be accounted for when integrating variables across loggers.
- CRS not specified; ensure consistent geographic reference when integrating with other spatial layers.