# Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- Dataset comprises 5 CSV files, each corresponding to a single logger in a different vegetation type:
  - TVC_logger 1_sedge.csv
  - TVC_logger 2_riparian.csv
  - TVC_logger 3_betula.csv
  - TVC_logger 4_alder.csv
  - TVC_logger 5_lichen heath.csv
- Authors/Owner: Lorna Street / Philip Wookey
- Maintainer: Lorna Street (l.e.street@ed-alumni.net)
- Focus: soil temperature, soil moisture content, air temperature, relative humidity, and surface wetness across main vegetation types at SikSik Creek, Trail Valley Creek, NWT, Canada.

## Data structure and access
- Files: 5 CSV data files, each named by logger number and vegetation type as above.
- Variables covered: soil temperature at 5 cm depth (Tsoil.C), air temperature (Tair.C), relative humidity (RH.percent), volumetric water content (VWC.m3.per.m3), surface wetness (Wetness.percent).
- Units: Tsoil.C and Tair.C in degrees Celsius; RH in percent; VWC in m3/m3; Wetness in percent.
- Date/time format: dd/mm/yyyy HH:MM:SS
- Missing value code: .
- Data are continuous, with no gap-filling.

## Temporal and spatial coverage
- Period of record by logger:
  - Logger 1 (sedge): 02-Aug-2013 to 29-Jul-2015
  - Logger 2 (riparian): 02-Aug-2013 to 21-Aug-2015
  - Logger 3 (betula): 02-Aug-2013 to 21-Aug-2015
  - Logger 4 (alder): 02-Aug-2013 to 21-Aug-2015
  - Logger 5 (lichen heath): 02-Aug-2013 to 29-Jul-2015
- GPS coordinates for each logger:
  - Logger 1: 68.74459771 N, 133.5021632 W
  - Logger 2: 68.74533925 N, 133.4939524 W
  - Logger 3: 68.74526449 N, 133.4925088 W
  - Logger 4: 68.74516902 N, 133.4952195 W
  - Logger 5: 68.74549767 N, 133.4969109 W

## Instrumentation and methodology
- Soil temperature: measured at 5 cm depth using Onset 12-bit Temperature Smart sensors.
- Air temperature and RH: measured approximately 0.5 m above ground; shielded from radiation with Onset solar radiation screen; when RH measured, sensors are Onset 12-bit Temperature/Relative Humidity Smart sensors.
- Surface wetness: measured at the lichen heath location with Onset Leaf Wetness sensor.
- Volumetric water content (VWC): measured at 5 cm depth using ECH2O EC-5 sensors, factory calibration where possible for hummock and inter-hummock positions.
- Sampling interval: 10 minutes for all measurements.
- Data quality: continuous time series with no gap-filling.
- Not all variables are collected at every location; variable availability per logger is as follows:
  - Logger 1: soil temperature, air temperature, RH, soil VWC
  - Logger 2: soil temperature, air temperature, RH, soil VWC (in Sphagnum moss), soil VWC (under willow shrub)
  - Logger 3: soil temperature (hummock), air temperature, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 4: soil temperature (hummock), air temperature, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 5: soil temperature (hummock), surface wetness, soil VWC (hummock), soil VWC (interhummock)

## Data quality considerations and governance
- Data are attributed to specific vegetation types and locations within SikSik Creek catchment.
- Variable definitions and units are provided, with clear records of missing value indicators.
- Notable caveats for data leaders: some variables are unavailable at certain loggers; cross-location or cross-vegetation comparisons should account for these gaps.

## Stewardship and contact
- Owner/Authors: Lorna Street; Primary contact: l.e.street@ed-alumni.net
- Maintainer: Lorna Street

## Practical implications for data leadership
- Useful for assessing microclimate and soil moisture dynamics across vegetation types over a two-year window (2013–2015).
- Enables cross-vegetation comparisons of soil temperature, soil moisture, and humidity at 10-minute resolution, with explicit GPS context for location-based analyses.
- Facilitates evaluation of data completeness and gaps when planning broader data integration or network coordination in Arctic/subarctic field contexts.