# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Dataset from common guillemots (Uria aalge) at the Isle of May National Nature Reserve, Scotland, for the 2016-2017 annual cycle.
- Combines biologging and morphometric data to derive daily metrics on foraging, temperature exposure, energy expenditure, and movement.

## Data collection and processing
- Chick-rearing adult guillemots were captured to attach GLS devices (MK3006 by Biotrack) to Darvic leg-rings.
- Birds weighed before GLS deployment and after retrieval using a Pesola spring balance.
- Handling time was under 5 minutes per individual.
- Devices recorded light intensity, temperature, and conductivity.
- Derived daily data include: hours spent foraging, sea surface temperature (SST) from bird-borne loggers, energy expenditure, location fixes, and daily daylight hours.
- Access and project governance:
  - Scottish Natural Heritage granted access to the Isle of May site.
  - Contributions to planning, collection, and management by Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, and Maria Bogdanova.
  - Data processing conducted by Ruth Dunn.

## Dataset structure
- Contains a single CSV file: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv.
- File includes ten columns as described below.

## Column definitions
- logger.id: unique identifier for each individual
- Adult.E: daily adult guillemot energy expenditure (kJ)
- sst: sea surface temperature recorded by the logger (°C)
- Foraging: daily time spent foraging (hours)
- day.length: daily daylight hours (hours)
- lon: longitude
- lat: latitude
- distance.coast.km: distance to the closest coastline point (km)
- start.mass: body mass at deployment (grams)
- end.mass: body mass at retrieval (grams)

## Relevance for monitoring frameworks
- Exemplifies end-to-end data lifecycle for environmental health monitoring: from field collection and device deployment to data processing, derivation of key indicators (foraging effort, SST exposure, energy expenditure), and structured metadata.
- Highlights data governance considerations relevant to monitoring work: provenance, unit definitions, and openness of underlying data.
- Illustrates typical challenges for monitoring frameworks, such as ensuring metadata completeness, data accessibility, and the need for consistent data formats and documentation to enable reuse and reporting.