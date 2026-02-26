# Crop yield data for maize, sugar cane, and wheat

## Overview
- Spatially explicit agricultural data were collected from the smallest feasible administrative units at three levels: national, subnational, and sub-subnational (e.g., counties or districts).
- Maize, sugar cane, and wheat cultivation is identified using the earthstat dataset; where data are missing, it is interpreted as either non-cultivation or no data.
- Generated spatial data are checked for consistency with national/global statistics to prevent errors from disaggregation.
- Yields are provided in tonnes per hectare (t/ha) and stored in netCDF format, with full metadata (grid projection, year, crop type, yield, units).

## Data collection and spatial framework
- Data are organized by three geographic resolutions: global, national, and subnational (including regional subdivisions) to enable maps and analyses at multiple scales.
- The 2016 year is used for yield values across the datasets.
- Spatial data are projected in WGS84 (EPSG 4326 for crop masks), and crop presence is indicated in cropmask files (0 = not grown, 1 = grown).

## Crops and datasets (high-level)
- Maize
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources combine FAOSTAT and EUROSTAT with national statistics offices; includes data for yellow maize and, where available, maize for silage (added to create a combined dataset).
- Sugar cane
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources primarily FAOSTAT and EUROSTAT; used to generate maps of sugar cane cultivation and yield.
- Wheat
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources include FAOSTAT and EUROSTAT; supports national and regional yield data, with detailed country-level notes (e.g., US, Canada, European countries, etc.).

## Data sources and links (overview)
- Europe
  - EUROSTAT (regional data and national data where available)
- Global
  - FAOSTAT (global and national scales)
- Country-specific statistics
  - United States: NASS (USDA)
  - Canada: Statistics Canada
  - Mexico: SIAP (Servicio de Información Agroalimentaria y Pesquera)
  - Argentina: SIIA
  - Brazil: IBGE
  - Chile, Peru, Ecuador, Colombia, Paraguay, Dominican Republic, and others with national statistical offices or agricultural agencies
- Additional country notes
  - For several countries, regional data exist only for certain years; national data are used to fill or harmonize across years.
  - In some cases, no data are available for specific crops or regions (e.g., some European countries for certain maize data; Norway often lacks maize yield data due to limited cultivation).

## Data structure and formats
- Data are provided in netCDF format with a consistent global projection (WGS84).
- Crop masks (cropname_cropmask_global_0.25_0.25.nc and cropname_cropmask_global_0.5_0.5.nc) indicate, per map cell, whether the crop is grown (1) or not (0); crop masks use EPSG 4326.
- Metadata accompany the netCDF files, including year, crop type, yield values, units, and grid projection.

## Metadata, units, and quality control
- Yields: tonnes per hectare (t/ha).
- Year: 2016 (for yield values across crops).
- Data quality: the spatial data were validated against underlying national/global statistics to ensure disaggregation did not introduce errors; national/global statistics served as benchmarks for quality control of the final spatial data.

## Accessibility and data reuse (alignment with Analysts Monitoring the Environment)
- The datasets are designed for consistent, standardized environmental monitoring over time, enabling scrutiny of agricultural land use and policy performance.
- Data management practices include verification, quality assurance, cleaning, transformation, and storage in appropriate data portals, aligning with standard monitoring workflows.
- The datasets aim to be more valuable than single-use by enabling combination with other relevant data and by facilitating access to underlying data used to generate final outputs.

## Key takeaways for environmental monitoring
- A comprehensive, multi-resolution dataset exists for maize, sugar cane, and wheat yields in 2016, grounded in established global and national statistical sources and harmonized in netCDF format.
- Spatial aggregation and validation steps are explicitly documented to ensure reliability for trend analyses and policy evaluation.
- The inclusion of crop masks provides clear indicators of where each crop is grown, supporting land-use and agricultural footprint analyses.
- While widely sourced, some data gaps remain at regional levels or for certain crops/countries, requiring reliance on national-level values or noting data limitations.