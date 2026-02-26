# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Dataset from common guillemots Uria aalge at the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W) for the 2016-2017 annual cycle.
- Data collected via biologging: light, temperature and conductivity from bird-borne GLS devices attached to Darvic leg-rings.
- Derived daily metrics include activity (hours spent foraging), sea surface temperature (SST), energy expenditure, location fixes, and daily daylight hours.
- Purpose aligned with environmental monitoring and providing standardized outputs for ecosystem assessment.

## Data collection and measurements
- Method: capture chick-rearing adults, attach GLS devices (MK3006, Biotrack, UK) to Darvic rings; weigh birds before deployment and after retrieval using a Pesola spring balance.
- Handling: retrieval and device removal occur during the breeding season; typical handling time under 5 minutes.
- Measurements from devices: light intensity, temperature, and conductivity.
- Derived data: daily estimates of foraging time, SST, energy expenditure, location coordinates, and daylight duration.
- Data processing: Ruth Dunn contributed to data processing; field planning and management involved Scottish Natural Heritage and researchers (Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, Maria Bogdanova).

## File structure and columns
- Single CSV file: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv.
- Ten columns:
  1. logger.id: unique ID for each individual
  2. Adult.E: daily adult energy expenditure (kJ)
  3. sst: sea surface temperature (°C)
  4. Foraging: daily time spent foraging (hours)
  5. day.length: daily daylight hours (hours)
  6. lon: longitude
  7. lat: latitude
  8. distance.coast.km: distance to nearest coastline (km)
  9. start.mass: mass at GLS deployment (g)
  10. end.mass: mass at GLS retrieval (g)

## Provenance and contributors
- Location: Isle of May National Nature Reserve, Scotland.
- Permissions: Scottish Natural Heritage granted access for the study.
- Contributors: planning and data management by Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, Maria Bogdanova; data processing by Ruth Dunn.

## Relevance for environmental monitoring
- Provides standardized, trackable metrics linking animal behavior and energetics to environmental variables (SST, daylight, proximity to coast).
- Facilitates cross-dataset integration to enhance understanding of marine ecosystem health and guillemot ecology.
- Data are suitable for inclusion in monitoring portals and for broader analyses of environmental health and policy performance over time.