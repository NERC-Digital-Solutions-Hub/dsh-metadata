# The EMEP-WRF global model, version 4.45

## Overview
- A global chemical transport modeling framework (EMEP-WRF) built on the EMEP MSC-W model, integrating WRF for meteorology.
- Uses a 1° x 1° latitude-longitude grid with 21 vertical layers (surface ~40 m to ~2 km near the top ~16 km).
- WRF version 4.2.2 drives the model with hourly 3D meteorological data; initialization and six-hour nudging with GFS-FNL data.
- Emissions are based on IIASA ECLIPSE v6a GAINS data for 2015.
- Outputs daily mean surface ozone concentrations (6 am–6 pm) on the 1° x 1° grid.
- Seasonal averaging applied to the grassland growing season (mid-April to mid-July) for the UK and USA in 2018.

## Data specifics

- Output dataset: daily surface ozone (O3) concentrations by grid cell; seasonal mean for mid-April to mid-July, 2018, for UK and USA.
- Spatial domain and resolution: global domain at 1° x 1° grid resolution.
- Coordinate system and units: Geographic Coordinate System WGS 1984; ozone values in parts per billion (ppb).

## Quality assurance and validation

- Data undergo QA/QC before use; model validation discussed in Mills et al. (2018).
- Validation compares modelled vs. observed ozone from the Global Atmosphere Watch (GAW) network, particularly during daily peak ozone periods.
- Overall, the model captures spatial and seasonal variations, demonstrating reliability for policy-relevant assessments.

## Data structure and attributes

- Shapefile granularity: gridded 1° x 1° cells.
- Attributes (5 columns):
  - FID: Unique grid cell identifier
  - Lon: Longitude of grid cell center
  - Lat: Latitude of grid cell center
  - NAME: Country designation (USA or UK)
  - O3_ppb: Daily surface ozone concentration in ppb; seasonal mean for mid-April to mid-July, 2018
- Observed data range in the dataset: 19.3 ppb to 50.9 ppb

## References
- Mills et al. (2018): Model validation and performance details
- Simpson et al. (2012): The EMEP MSC-W chemical transport model technical description
- Vieno et al. (2016): EMEP-WRF model sensitivities and related work

## Relevance for monitoring frameworks

- Provides a harmonized, model-based estimate of surface ozone with clear spatial (1°) and temporal (daily, seasonal) resolution suitable for evaluating environmental health policies.
- Includes explicit metadata (grid, coordinates, units, seasonal window) and documented QA/QC and validation steps to support data governance and traceability.
- Data accessibility implied by structured shapefile output and clear documentation, though explicit open-access statements are not provided in the excerpt.