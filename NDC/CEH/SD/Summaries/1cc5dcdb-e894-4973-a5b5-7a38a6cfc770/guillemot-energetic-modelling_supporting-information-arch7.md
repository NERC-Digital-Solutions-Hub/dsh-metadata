# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Dataset for common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W) collected during the 2016-2017 annual cycle.
- Biologging approach: captured chick-rearing adults, attached GLS devices (MK3006 by Biotrack), weighed before deployment and after retrieval with a Pesola spring balance.
- Retrieval and handling were completed in under 5 minutes per bird.
- Data streams from the devices include light, temperature, and conductivity; derived daily metrics cover foraging activity, sea surface temperature (SST), energy expenditure, location fixes, and daylight hours.

## Data collection and provenance
- Scottish Natural Heritage granted access to the Isle of May; contributions from Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, and Maria Bogdanova to planning, collection, and management.
- Ruth Dunn processed the data.
- The dataset consists of one CSV file: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv.

## Dataset structure
- The CSV file contains ten columns with the following data:
  1. logger.id: unique identifier for each individual
  2. Adult.E: daily adult guillemot energy expenditure (kJ)
  3. sst: sea surface temperature recorded by the logger (°C)
  4. Foraging: daily time spent foraging (hours)
  5. day.length: daily daylight hours (hours)
  6. lon: longitude
  7. lat: latitude
  8. distance.coast.km: distance to the closest coastline point (km)
  9. start.mass: mass at GLS deployment (g)
  10. end.mass: mass at GLS retrieval (g)

## Geospatial context
- Location data are provided as precise lon/lat coordinates, enabling spatial analyses of movement, habitat use, and proximity to coastlines.
- The distance to the coast (distance.coast.km) facilitates coastal proximity analyses and shoreline interactions.

## Potential GIS applications
- Create map-based visualizations of daily foraging effort and movement patterns.
- Link foraging activity and energy expenditure to SST and daylight, enabling spatial-temporal analyses of habitat use.
- Assess relationships between proximity to coastlines and energy costs or foraging behavior.
- Integrate with other geospatial layers (e.g., bathymetry, sea ice) for broader ecological context.

## Credits and acknowledgments
- Data collected under the Isle of May National Nature Reserve program.
- Contributions from SNH and named researchers to planning, collection, and data management.
- Data processing performed by Ruth Dunn.