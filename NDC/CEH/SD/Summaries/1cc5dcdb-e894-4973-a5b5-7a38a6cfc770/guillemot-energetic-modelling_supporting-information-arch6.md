# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- A single CSV dataset containing biologging-derived data for common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland.
- Covers the 2016-2017 annual cycle.
- Data include activity, energy expenditure, sea surface temperature, location, and mass changes derived from bird-borne GLS devices.

## Data collection and provenance
- Birds were chick-rearing adults captured to attach GLS devices (MK3006 from Biotrack, UK) and weighed before deployment.
- Loggers were retrieved after a breeding season recapture; birds were weighed again.
- Handling time was brief (<5 minutes per capture/retrieval).
- Light, temperature, and conductivity were recorded by the devices; derived daily measures include activity, SST, and daylight.
- Access granted by Scottish Natural Heritage; contributors include Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, Maria Bogdanova, with Ruth Dunn processing the data.

## Dataset and file details
- File name: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv
- Contents: one CSV file with ten columns (variables described below)

## Variables and columns
- logger.id: unique identifier for each individual guillemot
- Adult.E: daily adult energy expenditure (kJ)
- sst: sea surface temperature recorded by the logger (°C)
- Foraging: daily time spent foraging (hours)
- day.length: daily daylight hours (hours)
- lon: longitude
- lat: latitude
- distance.coast.km: distance to the nearest coastline (km)
- start.mass: mass at deployment (grams)
- end.mass: mass at retrieval (grams)

## Data processing and quality
- Derived from raw biologging data; daily summaries were produced from device recordings.
- Minimal handling time and careful recapture ensured data integrity.
- Data reflect a specific seasonal window (2016-2017) and may not be representative of other years or locations without further expansion.

## Potential analyses and data products
- Time-series analyses of foraging effort, energy expenditure, SST, and mass changes per individual.
- Spatial analyses of movement patterns using lon/lat and distance to coast.
- Correlations or models linking foraging duration and energy expenditure with SST and daylight.
- Creation of dashboards or self-serve reports to explore per-individual trajectories and environmental associations.

## Access and credits
- Data are associated with Isle of May research efforts; contributors include Ruth Dunn (data processing) and researchers listed for planning, collection, and management (Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, Maria Bogdanova).