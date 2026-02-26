# General information

- The document describes agricultural census and survey data for three crops: maize, sugar cane, and wheat, collected at national, subnational (states/provinces), and sub-subnational (counties/districts) levels.
- The Earthstat dataset is used to identify whether a crop is cultivated in a country; lack of data indicates no data or no cultivation.
- Spatial data are checked for consistency with national/global statistics to prevent errors during disaggregation.
- Yields are in tonnes per hectare and refer to the year 2016.
- All spatial data are provided in NetCDF format with a WGS84 projection, and metadata includes grid projection, year, crop type, yield, and units.
- Crop masks (cropname_cropmask_global_0.25_0.25.nc and cropname_cropmask_global_0.5_0.5.nc) indicate per cell whether the crop is grown (0 = not grown, 1 = grown). Crop masks use ESPG: 4326 (WGS84).

## Data scope and resolution

- Maize, sugar cane, and wheat data are provided globally with resolution at national, subnational, and sub-subnational levels.
- Data sets combine multiple sources to generate maps and support GIS-based visualization and analysis.

## Data sources and coverage

- Maize:
  - Global data from FAOSTAT and EUROSTAT, with yield data from various national statistics offices.
  - Includes yellow maize and, where available, maize for silage (integrated into the yellow maize dataset where data exist).
  - Country-level documentation includes extensive source notes (US states, US counties, Canada, Mexico, UK, Norway, Sweden, Finland, Denmark, Australia, India, China, Mongolia, South Africa, and many others with varying year coverage).
- Sugar cane:
  - Global data from FAOSTAT and EUROSTAT, with national/subnational coverage.
  - Country-level sources include the United States (NASS), Mexico (SIAP), Argentina (SIIA), Brazil (IBGE), Colombia (DNP), Ecuador, Paraguay, Peru, etc., with regional data where available.
- Wheat:
  - Global data from FAOSTAT and EUROSTAT, with national and regional detail.
  - Examples of country-level data included: Belgium, Denmark, the United Kingdom, France, Spain, Portugal, Romania, Ireland, Italy, Greece, Hungary, Austria, Poland, Slovakia, Slovenia, United States (states/counties), Canada (provinces/regions), Mexico, and several others with varying regional detail and year ranges.
- Overall, data sources span Europe, the Americas, Africa, and Asia, with some countries lacking regional data for certain years (noted in the dataset).

## Data structure and formats

- Data are provided in NetCDF format with a 2016 reference year for yields.
- Projections are WGS84; crop masks are provided in 0.25 and 0.5 degree grids.
- Metadata included with each NetCDF file covers grid projection, year, crop type, yield, and units.
- For wheat, data availability includes multiple tiers: original data, processed data, and code, with regional breakdowns for several countries.

## Quality control and data integrity

- The dataset was checked for consistency with national/global statistics to ensure spatial disaggregation did not introduce errors.
- National/global statistics served as benchmarks for quality control of the final spatial data.

## Practical notes for GIS use

- Suitable for creating map-based visualizations of crop presence and spatial yield variation at multiple administrative levels.
- Use the crop masks to mask rasters for each crop, ensuring accurate representation of where crops are grown.
- Be aware of data gaps by country and year; some regions have limited or no regional yield data.
- Ensure alignment with the 2016 reference year when integrating with other time-series datasets.