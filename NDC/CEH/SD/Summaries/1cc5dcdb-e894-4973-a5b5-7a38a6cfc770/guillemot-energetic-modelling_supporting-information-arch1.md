# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Data from common guillemots (Uria aalge) at the Isle of May National Nature Reserve, Scotland (coordinates provided).
- Collected during the 2016-2017 annual cycle using bird-borne GLS devices attached to Darvic leg-rings on chick-rearing adults.
- Birds weighed to the nearest gram before deployment and after retrieval; handling time < 5 minutes per bird.
- Derived daily metrics include foraging hours, sea surface temperature (SST) from bird-borne loggers, energy expenditure, location fixes, and daily daylight hours.

## Data collection and processing
- Access granted by Scottish Natural Heritage; contributors include Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, and Maria Bogdanova; Ruth Dunn processed the data.
- GLS devices recorded light intensity, temperature, and conductivity.
- Data were transformed into daily records of activity, SST, energy expenditure, locations, and daylight.
- Dataset provided as a single CSV file: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv.

## File and variables
- File: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv
- Ten columns:
  - logger.id: unique identifier for each individual
  - Adult.E: daily adult guillemot energy expenditure (kJ)
  - sst: sea surface temperature (°C)
  - Foraging: daily time spent foraging (hours)
  - day.length: daily daylight hours (hours)
  - lon: longitude
  - lat: latitude
  - distance.coast.km: distance to nearest coastline (km)
  - start.mass: mass at GLS deployment (g)
  - end.mass: mass at GLS retrieval (g)

## Purpose and potential analyses
- Enables investigation of relationships among energy expenditure, foraging effort, SST, spatial position relative to coast, and body-mass changes.
- Suitable for correlational analyses, predictive modelling, and assessments of environmental impacts on guillemot behavior during the annual cycle.

## Context and metadata
- Study site: Isle of May National Nature Reserve, Scotland.
- Data span: 2016-2017 annual cycle.