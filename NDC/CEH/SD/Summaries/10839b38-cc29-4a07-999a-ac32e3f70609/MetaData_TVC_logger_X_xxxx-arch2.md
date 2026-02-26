# Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- Multi-variable climate and soil dataset collected at SikSik Creek catchment, Trail Valley Creek, NWT, Canada.
- 5 vegetation-type locations with 10-minute interval measurements from 2013 to mid-2015.
- Variables include soil temperature, soil volumetric moisture content, air temperature, relative humidity, and surface wetness (where measured).

## Data structure and content
- Data files: 5 CSVs, each corresponding to one logger and vegetation type:
  - TVC_logger 1_sedge.csv
  - TVC_logger 2_riparian.csv
  - TVC_logger 3_betula.csv
  - TVC_logger 4_alder.csv
  - TVC_logger 5_lichen heath.csv
- Vegetation types represented:
  - Logger 1: sedge
  - Logger 2: riparian
  - Logger 3: Betula
  - Logger 4: Alder
  - Logger 5: Lichen heath
- Period of record (per logger):
  - Logger 1: 02-Aug-2013 to 29-Jul-2015
  - Logger 2: 02-Aug-2013 to 21-Aug-2015
  - Logger 3: 02-Aug-2013 to 21-Aug-2015
  - Logger 4: 02-Aug-2013 to 21-Aug-2015
  - Logger 5: 02-Aug-2013 to 29-Jul-2015
- Number of records:
  - Logger 1: 418,072
  - Logger 2: 539,115
  - Logger 3: 539,115
  - Logger 4: 539,110
  - Logger 5: 418,060
- GPS coordinates (approximate):
  - Logger 1: 68.74459771 N, 133.5021632 W
  - Logger 2: 68.74533925 N, 133.4939524 W
  - Logger 3: 68.74526449 N, 133.4925088 W
  - Logger 4: 68.74516902 N, 133.4952195 W
  - Logger 5: 68.74549767 N, 133.4969109 W

## Methods and instrumentation
- Soil temperature: measured at 5 cm depth using Onset 12-bit Temperature Smart sensors.
- Air temperature and/or relative humidity: measured at ~0.5 m above ground, shielded from radiation with an Onset solar radiation screen; in some cases RH measured with Onset Temperature/Relative Humidity sensors.
- Surface wetness: measured at the lichen heath site with an Onset Leaf Wetness sensor.
- Volumetric water content (VWC): measured at 5 cm depth with ECH2O EC-5 sensors (factory calibration where possible; sampled in hummock and inter-hummock positions).
- Sampling interval: 10 minutes; data are continuous with no gap-filling.
- Not all variables measured at every location; per-logger variable coverage:
  - Logger 1: soil temperature, air temperature, RH, soil VWC
  - Logger 2: soil temperature, air temperature, RH, soil VWC (Sphagnum moss), soil VWC (under willow shrub)
  - Logger 3: soil temperature (hummock), air temp, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 4: soil temperature (hummock), air temp, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 5: soil temperature (hummock), surface wetness, soil VWC (hummock), soil VWC (interhummock)

## Variables and units
- DateTime: Date and Time (dd/mm/yyyy HH:MM:SS)
- Tsoil.C: Soil temperature at 5 cm depth, °C
- Tair.C: Air temperature, °C
- RH.percent: Relative humidity, %
- VWC.m3.per.m3: Volumetric water content, m3/m3
- Wetness.percent: Surface wetness, %
- Missing value code: .
- Note: Not all variables are present at every location; some entries may be missing (represented by a dot).

## Data quality and accessibility
- Data quality emphasis: continuous measurements with no gap-filling; explicit per-logger variable coverage highlights site-specific measurement limitations.
- Data format: CSV files, suitable for ingestion into standard environmental analysis workflows.
- Access and contact: Authored by Lorna Street and Philip Wookey; Maintainer Lorna Street; contact l.e.street@ed-alumni.net.

## Temporal and spatial coverage
- Temporal span limited to 2013–2015, varying slightly by logger.
- Spatial coverage limited to five discrete locations within SikSik Creek’s main vegetation types, with precise GPS coordinates provided for each logger.

## Usage considerations for Analysts
- Suitable for monitoring and comparing microclimate and soil moisture dynamics across vegetation types over time.
- Can be combined with other environmental datasets for broader environmental health assessments and policy performance analyses.
- When comparing sites, account for variable-specific availability and slight differences in sensor configurations between loggers.
- Consider time-series alignment due to minor differences in period of record and any site-specific data gaps.