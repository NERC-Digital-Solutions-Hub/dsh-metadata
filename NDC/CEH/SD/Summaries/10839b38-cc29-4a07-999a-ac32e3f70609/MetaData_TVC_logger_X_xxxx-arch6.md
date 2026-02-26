# Dataset Title: Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- Dataset from Onset Microstation Data Loggers at 5 locations within main vegetation types at SikSik Creek catchment, Trail Valley Creek, NWT, Canada.
- Variables include soil temperature (5 cm depth), surface and air temperature, relative humidity, soil volumetric moisture content (VWC), and surface wetness (at the lichen heath site).
- Measurements taken at 10-minute intervals; data are continuous with no gap-filling.

## Data Structure and Access
- Data comprises 5 CSV files, each corresponding to one logger in a vegetation type:
  - TVC_logger 1_sedge.csv
  - TVC_logger 2_riparian.csv
  - TVC_logger 3_betula.csv
  - TVC_logger 4_alder.csv
  - TVC_logger 5_lichen heath.csv
- Filenames reflect logger number and vegetation type.
- Authors/Owner: Lorna Street and Philip Wookey. Maintainer: Lorna Street. Contact: l.e.street@ed-alumni.net

## Period of Record and Size
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

## Location (GPS)
- Logger 1: 68.74459771 N, 133.5021632 W
- Logger 2: 68.74533925 N, 133.4939524 W
- Logger 3: 68.74526449 N, 133.4925088 W
- Logger 4: 68.74516902 N, 133.4952195 W
- Logger 5: 68.74549767 N, 133.4969109 W

## Methods and Sensors
- Soil temperature: measured at 5 cm depth with Onset 12-bit Temperature Smart sensors.
- Air temperature: measured approximately 0.5 m above ground; shielded from radiation using Onset solar radiation screen. If RH data not available, temperature sensor used (Onset 12-bit Temperature Smart sensors).
- Relative humidity: measured with Onset sensors (when available).
- Surface wetness: measured at the lichen heath location with Onset Leaf wetness sensor.
- Volumetric water content (VWC): measured at 5 cm depth with ECH2O EC-5 sensors; factory calibration used where possible (hummock and interhummock positions).
- Data cadence: 10-minute intervals; data are continuous with no gap-filling.

## Variables and Units
- DateTime: dd/mm/yyyy HH:MM:SS (no units; missing value code = .)
- Tsoil.C: Soil temperature at 5 cm depth. Units: °C. Missing value code = .
- Tair.C: Air temperature. Units: °C. Missing value code = .
- RH.percent: Relative humidity. Units: %. Missing value code = .
- VWC.m3.per.m3: Volumetric water content. Units: m3 m-3. Missing value code = .
- Wetness.percent: Surface wetness. Units: %. Missing value code = .

## Notes and Considerations
- Not all variables were measured at every location, per logger:
  - Logger 1: Tsoil.C, Tair.C, RH, VWC
  - Logger 2: Tsoil.C, Tair.C, RH, VWC (Sphagnum moss), VWC (under willow shrub)
  - Logger 3: Tsoil.C (hummock), Tair.C, RH, VWC (hummock), VWC (interhummock)
  - Logger 4: Tsoil.C (hummock), Tair.C, RH, VWC (hummock), VWC (interhummock)
  - Logger 5: Tsoil.C (hummock), Wetness.percent, VWC (hummock), VWC (interhummock)
- Data are presented as 5 separate files, enabling comparison across vegetation types but requiring careful alignment of variables by location.
- Data quality notes highlight the presence of patchy data across locations and the lack of gap-filling, which may affect time-series analyses.
- For data access or further details, contact the listed maintainer.