# Agricultural census and survey information

## Overview
- Spatial agricultural data for maize, sugar cane, and wheat collected at national, subnational (states/provinces), and sub-subnational (counties/districts) levels.
- Earthstat dataset used to identify crop cultivation; data disaggregated and checked for consistency with national/global statistics.
- Yields provided in tonnes per hectare; stored in netCDF format with full metadata (grid projection, year, crop type, yield, units).
- Crop masks indicate where each crop was grown on the grid (0 = not grown, 1 = grown); crop mask projections are EPSG: 4326 (WGS84).

## Data coverage by crop

- Maize
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources: FAOSTAT, EUROSTAT, and country statistics offices.
  - Includes data for yellow maize and also maize for silage (where available) merged to form a comprehensive dataset for map generation.
  - Country-level data links and provenance vary (Europe, United States, Canada, Mexico, United Kingdom, Norway, Sweden, Finland, Denmark, Australia, India, China, Mongolia, South Africa, Argentina, Brazil, Chile, Peru, Ecuador, Colombia, Paraguay, Czech Republic, Turkey, Germany, Bolivia, Macedonia, Japan, Switzerland, Kazakhstan, etc.).
  - Some countries lack maize yield data or regional data for certain years (e.g., Norway has no maize yield data; Finland has limited or no regional data; data availability for several countries varies by year).

- Sugar cane
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources: FAOSTAT and EUROSTAT with country-level datasets (Europe, United States, Mexico, Argentina, Brazil, Colombia, Ecuador, Paraguay, Peru, Ethiopia, South Africa, China, India, Japan, Pakistan, Sri Lanka, Australia, etc.).

- Wheat
  - Global coverage at national, subnational, and sub-subnational levels.
  - Data sources: FAOSTAT and EUROSTAT with country-level and regional data (examples include Belgium, Denmark, Netherlands, France, Spain, Portugal, Italy, the United Kingdom, Ireland, Poland, etc.).
  - Data spans from around 1969/1970 to 2015/2016, with full country data available in FAOSTAT; regional data available for many countries, though some years may be limited or replaced by national figures.

## Data structure and formats
- Data stored as NetCDF files with a 2D gridded structure.
- Grid projections are in WGS84 (EPSG 4326).
- Crop mask files (e.g., cropname_cropmask_global_0.25_0.25.nc and cropname_cropmask_global_0.5_0.5.nc) indicate presence/absence of each crop per grid cell.
- Year-specific yield data per crop (maize, sugarcane, wheat) in tonnes per hectare for 2016.
- Metadata included: grid projection, year, crop type, yield, and units.

## Data sources and access
- Primary data sources: FAOSTAT, EUROSTAT, and national statistics offices (USDA, Statistics Canada, SIAP, IBGE, DNP, DGEEC, etc.).
- Data are linked to country- or region-specific datasets, with access notes (original data, processed data, and code) and dates accessed (primarily June–August 2016).
- Data quality checks performed by benchmarking against national/global statistics to ensure consistency when disaggregating spatial data.

## Data quality and limitations
- Quality control uses national/global statistics as benchmarks to validate spatial disaggregation.
- Limitations and caveats by country/region:
  - Some countries have missing regional data for certain years or crops.
  - In several cases, national yield data are used in place of regional data for specific years.
  - For certain countries (e.g., Norway for maize, Finland for maize, Denmark in some periods), maize data may be unavailable or incomplete.
  - Year ranges vary by crop and country; not all 1960s–2015 data are uniformly available at all administrative levels.
- Outputs are intended to be reliable for map generation and cross-checking against official statistics, but users should be aware of data gaps and potential substitutions with national figures for missing regional data.

## Practical notes for Data Support usage
- When exploring data products for others, validate the ask against available spatial resolutions (national, subnational, sub-subnational) and crop coverage (maize, sugar cane, wheat).
- Leverage the crop masks to filter analyses to grid cells where a crop is grown.
- Use NetCDF metadata to document data provenance, year, and units, and to ensure compatibility with downstream tools.
- Be prepared to supplement with topic-specific data from national sources when regional data are missing or incomplete for the desired years or crops.
- Consider data refresh needs, as the current documentation references data accessed in 2016; verify whether newer releases are available for ongoing analyses.