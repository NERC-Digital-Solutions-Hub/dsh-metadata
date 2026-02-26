# Dataset Title: Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- A multi-logger environmental monitoring dataset capturing soil temperature, soil moisture, air temperature, relative humidity, and surface wetness across five vegetation-types at SikSik Creek, Trail Valley Creek, NWT, Canada.
- Data structure: five CSV files, each corresponding to one logger and vegetation type.
  - Filenames: TVC_logger 1_sedge.csv; TVC_logger 2_riparian.csv; TVC_logger 3_betula.csv; TVC_logger 4_alder.csv; TVC_logger 5_lichen heath.csv
- Period of record (by logger): 
  - Logger 1: 02-Aug-2013 to 29-Jul-2015
  - Logger 2: 02-Aug-2013 to 21-Aug-2015
  - Logger 3: 02-Aug-2013 to 21-Aug-2015
  - Logger 4: 02-Aug-2013 to 21-Aug-2015
  - Logger 5: 02-Aug-2013 to 29-Jul-2015
- Number of records (per logger):
  - Logger 1: 418,072
  - Logger 2: 539,115
  - Logger 3: 539,115
  - Logger 4: 539,110
  - Logger 5: 418,060
- GPS locations provided for each logger (latitude, longitude).

## Location and sampling design
- Five locations within main vegetation types at SikSik Creek catchment, Trail Valley Creek, NWT, Canada.
- GPS coordinates listed for precise positioning of each logger.

## Measurements and methods
- Sensor setup and depths:
  - Soil temperature: measured at 5 cm depth using Onset 12-bit Temperature Smart sensors.
  - Air temperature: measured approximately 0.5 m above ground; shielded from radiation with Onset radiation screen; sometimes using Onset Temperature Smart sensors.
  - Relative humidity: measured with Onset 12-bit Temperature/Relative Humidity Smart sensors (where applicable).
  - Surface wetness: measured at the lichen heath location with Onset Leaf wetness sensor.
  - Volumetric water content (VWC): measured at 5 cm depth using ECH2O EC-5 sensors (calibrated where possible; measurements collected for hummock and inter-hummock positions).
- Sampling interval: every 10 minutes; data are continuous with no gap-filling.
- Variable coverage by logger (not all variables present at every location):
  - Logger 1: soil temperature, air temperature, RH, soil VWC
  - Logger 2: soil temperature, air temperature, RH, soil VWC (in Sphagnum moss), soil VWC (under willow shrub)
  - Logger 3: soil temperature (hummock), air temperature, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 4: soil temperature (hummock), air temperature, RH, soil VWC (hummock), soil VWC (interhummock)
  - Logger 5: soil temperature (hummock), surface wetness, soil VWC (hummock), soil VWC (interhummock)

## Data definitions and units
- Record: Record number.
- DateTime: Date and Time in format dd/mm/yyyy HH:MM:SS.
- Tsoil.C: Soil temperature at 5 cm depth; units: °C.
- Tair.C: Air temperature; units: °C.
- RH.percent: Relative humidity; units: %.
- VWC.m3.per.m3: Volumetric water content; units: m3/m3.
- Wetness.percent: Surface wetness; units: %.
- Missing value code: . (period)

## Data governance and accessibility considerations
- Data are organized per logger with direct, clearly defined metadata (sensor types, depths, locations, and units).
- Continuous time-series data with explicit 10-minute resolution and no imputation.
- Variable availability varies by location, which should be considered in summaries or comparative analyses across vegetation types.
- Explicit contact for authors/owner (Lorna Street and Philip Wookey) and maintainer (Lorna Street) provided for data queries.