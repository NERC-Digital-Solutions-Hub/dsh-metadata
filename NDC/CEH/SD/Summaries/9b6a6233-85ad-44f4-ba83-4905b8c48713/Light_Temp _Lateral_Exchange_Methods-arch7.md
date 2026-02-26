# Temporal variation in temperature and light availability in the Hampshire Avon, United Kingdom  [Macronutrient Cycling]

## Overview
- A dataset of temperature (°C) and light (Lux) measurements collected from six streams feeding the Hampshire Avon, UK.
- Part of the NERC Macronutrient Cycles project on lateral exchange and seaward flux of C, N, P.
- Coordinated by the River Communities Group, QMUL; Dr. John Iwan Jones was a Co-Investigator responsible for data collection.
- Streams reflect contrasting geology (clay, greensand sandstone, chalk) and a gradient in base flow index.

## Data collected
- Variables: temperature (°C) and light (Lux).
- Instruments: Onset HOBO Pendant Temperature/Light UA-002-64 data loggers.
- Deployment: loggers tethered to the bed of each stream (six streams) for the duration of the dataset.
- Sampling: recordings every 15 minutes.
- Calibration and accuracy:
  - Temperature accuracy: ±0.53°C (0–50°C).
  - Time accuracy: ±1 minute per month at 25°C.
  - Light range/specs: 200–1200 nm; 60% response 500–1100 nm; 100% response 900 nm.
- Data quality: breaks due to data downloads or logger loss/malfunction.

## Spatial and Temporal coverage
- Sites and details:
  - AS1, River Sem, Priors Farm, Grid Ref ST8916428436, Start 13/02/2013, End 20/05/2014, No days 461.
  - AS2, River Sem, Share Farm, Grid Ref ST9234327392, Start 05/02/2013, End 01/12/2014, No days 664.
  - GA1, River East Avon, Marden, Grid Ref SU0973457808, Start 08/02/2013, End 19/05/2014, No days 465.
  - GN2, River Nadder, Share Farm, Grid Ref ST9235527364, Start 05/02/2013, End 01/12/2014, No days 664.
  - CE1, River Ebble, Stoke Farthing, Grid Ref SU0567225325, Start 06/02/2013, End 19/05/2014, No days 467.
  - CW2, River Wylye, Brixton Deverill, Grid Ref SU1723143894, Start 07/02/2013, End 16/10/2013, No days 222.
- Overall, records span early 2013 to mid-2014 with varying durations per site.

## Data structure and GIS considerations
- Data type: time series at each site suitable for creating spatially-resolved maps of temperature and light over time.
- GIS preparation:
  - Convert grid refs to a standard coordinate reference system (e.g., British National Grid or WGS84) for mapping.
  - Create a point feature for each site with attributes: site_id (AS1, AS2, GA1, GN2, CE1, CW2), river, location, grid_ref, start_date, end_date, days, and data_type (temperature, light).
- Data integration:
  - Potential to combine with other hydrological or environmental layers (e.g., geology, base flow index) to explore spatial-temporal patterns.
- Caveats:
  - Data gaps due to downloads or malfunctions.
  - Calibration and sensor limitations should be accounted for in analyses.

## Provenance and access
- Project: The role of lateral exchange in modulating the seaward flux of C, N, P (NE/J012106/1).
- Data collection by River Communities Group, QMUL; with involvement of QMUL personnel.
- Reference to instrument manuals for specifications (HOBO UA-002-xx).