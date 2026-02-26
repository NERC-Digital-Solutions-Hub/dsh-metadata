# Crop yield data for Maize, Sugar Cane and Wheat (netCDF) 2016

## Overview
- Global spatial dataset of agricultural census and survey information, disaggregated to national, subnational (states/provinces), and sub-subnational (counties/districts) levels.
- Crops covered: maize (including yellow maize and silage), sugar cane, and wheat.
- Data has been checked for consistency with underlying national/global statistics to ensure accurate spatial disaggregation.
- All yield values are in metric tonnes per hectare and refer to the year 2016.
- Data are provided in netCDF format with comprehensive metadata and a crop mask to indicate where each crop is grown. The crop mask uses WGS84 (EPSG 4326).

## Data content by crop
- Maize
  - Resolution: Global, national to sub-subnational.
  - Data sources: FAOSTAT, EUROSTAT, and country statistical offices.
  - Special notes: Includes data for maize silage where available; used to generate maps; some countries have limited or no yield data (explicit notes per country).
  - Data links: Country/regional data sources and access notes (e.g., Europe, United States, Canada, Mexico, etc.).
- Sugar cane
  - Resolution: Global, national to sub-subnational.
  - Data sources: FAOSTAT, EUROSTAT, and national statistical offices.
  - Data links: Regional and national datasets across Europe, the Americas, Africa, Asia, etc.
- Wheat
  - Resolution: Global, national to sub-subnational.
  - Data sources: FAOSTAT, EUROSTAT, and national statistical offices.
  - Data links: Individual country datasets with access details; includes regional data where available and notes on data coverage by year.

## Data sources and provenance
- Primary sources: FAOSTAT, EUROSTAT, and a range of national statistical agencies (e.g., USDA, Statistics Canada, DEFRA, LUKE, etc.).
- For Europe and other regions, data links specify originals, processed data, and code where applicable; for some countries, only national or regional data are available.
- Data were accompanied by documentation on access dates (e.g., June 2016, August 2016) and the specific data exports or zip files.

## Data structure and format
- Format: Network Common Data Form (netCDF).
- Projection: WGS84 for the spatial data; crop masks also provided in a separate ESPG: 4326 format.
- Crop masks: Provide a 0/1 indicator per cell whether the crop is grown in that location.
- Metadata: Each netCDF file includes grid projection, year, crop type, yield, and units.

## Quality assurance and validation
- The provided data were checked for consistency against underlying national/global statistics to ensure that spatial disaggregation did not introduce errors.
- National/global statistics used as benchmarks to validate final spatial data.

## Metadata and documentation
- All necessary metadata are included within the netCDF files (grid projection, year, crop type, yield, units).
- Crop mask files accompany the dataset to facilitate interpretation of cultivated areas.

## Access, governance, and updates
- The dataset notes data availability and limitations, including disclosure risks, proprietary issues, and embargoes where applicable.
- scope for updates is acknowledged; systems should be in place to manage updates and maintain currency.
- Datasets are intended to be uploaded to relevant portals and catalogued within data holdings; work performed on datasets may be documented for provenance and reuse.

## Practical considerations for Data Stewards
- Alignment with data management practices: standard formats (netCDF), consistent units (tonnes/ha), and standardized spatial reference (WGS84).
- Clear provenance: comprehensive listing of data sources and links to individual datasets by country/region.
- Metadata completeness: ensure all relevant metadata fields are present and updated as data are refreshed.
- Handling limitations: track and communicate data gaps (countries with no yield data or incomplete regional data) and embargoed data.
- Interoperability and updateability: maintain compatibility with other datasets and plan for iterative updates as new statistical data become available.

## Key notes and caveats
- Some countries lack yield data or have only partial regional data; notes are attached per country to reflect data availability.
- 2016 is the reference year for all yield values; some historical or regional data (where present) may exist but are not included in the primary 2016 dataset.
- The dataset includes a combined approach for maize (including silage) to enhance map generation where data are available.