# The EMEP-WRF global model, version 4.45

## Overview
- Global atmospheric chemistry model dataset based on EMEP MSC-W, using the Weather Research and Forecasting (WRF) model.
- Global horizontal resolution of 1° x 1°, with 21 vertical layers (surface ~40 m to ~16 km).
- Outputs provide daily mean surface ozone concentrations for 2018, focused on a grassland growing-season average for UK and USA.

## Data generation and inputs
- WRF version 4.2.2 used to compute hourly 3D meteorological data driving EMEP-WRF for 2018.
- Model initialisation and six-hour nudging with GFS-FNL reanalysis data.
- Emissions based on IIASA ECLIPSE v6a GAINS for the year 2015.

## Outputs and scope
- Daily mean surface ozone (6:00–18:00) on a 1° x 1° grid.
- Seasonal (grassland growing season) mean per grid cell for mid-April to mid-July, 2018.
- Dataset includes the entire globe, but the provided shapefile attributes indicate data for the USA and UK.

## Data format and structure
- Shapefile with gridded data (1° x 1° resolution) and 5 attributes:
  - FID: Unique grid cell identifier
  - Lon: Longitude of the grid cell center (decimal degrees)
  - Lat: Latitude of the grid cell center (decimal degrees)
  - NAME: Country (USA or UK)
  - O3_ppb: Daily surface ozone concentration in ppb, seasonal mean for mid-April to mid-July, 2018
- O3_ppb values range from 19.3 to 50.9 ppb.
- Coordinate Reference System: WGS 1984; units in decimal degrees.

## Quality control and validation
- Data undergo QA/QC before use.
- Model performance is documented in Mills et al. (2018) with supplementary figures; comparison of modelled vs. observed ozone from the Global Atmosphere Watch (GAW) network shows the model captures spatial and temporal variations, including peak ozone episodes.

## Spatial details
- Grid: 1° x 1° global resolution.
- Shapefile attributes provide per-grid cell location and ozone values for UK and USA during the specified period.

## References
- Mills et al. (2018) Global Change Biology: ozone and crop impacts; model validation details.
- Simpson et al. (2012) The EMEP MSC-W chemical transport model: technical description.
- Vieno et al. (2016) Sensitivities of emissions reductions for UK PM2.5.

## Usage notes
- Suitable for regional exposure analyses and comparisons of ozone levels between the UK and USA during the 2018 grassland-growing season.
- When using, consider the global model’s inputs (WRF meteorology, GFS-FNL nudging, GAINS emissions) and the QA/QC context.