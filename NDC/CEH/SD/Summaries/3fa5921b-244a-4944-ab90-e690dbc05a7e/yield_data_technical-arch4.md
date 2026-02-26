# Data sources plus links to individual datasets

- General purpose: Agricultural census and survey information collected at the smallest practical political units, with three spatial levels (national, subnational, sub-subnational) to identify cultivation of maize, sugarcane, and wheat.
- Crop identification: Earthstat used to determine whether maize, sugarcane, and wheat are cultivated in a country; data are checked for consistency with national/global statistics to prevent spatial disaggregation errors.
- Data units and scope: Yields are expressed in tonnes per hectare and pertain to the year 2016. All spatial data are provided in netCDF format with a WGS84 projection. Crop masks indicate where each crop is grown (0 = not grown, 1 = grown).

- Maize dataset
  - Global resolution: national, subnational, and sub-subnational
  - Data sources: FAOSTAT and EUROSTAT datasets plus country-level yield data from various national statistics offices
  - Content: Data for yellow maize (grain maize, corn cob, popcorn, etc.)
  - Additional data: Maize for silage data included where available and combined with the yellow maize dataset
  - Data links: Multiple country-specific and regional data files; detailed provenance provided (e.g., EU regional data, US states, Canadian provinces, etc.)
  - Notes: Some countries lack data (e.g., Norway, Finland, Denmark in certain years)

- Sugar cane dataset
  - Global resolution: national, subnational, and sub-subnational
  - Data sources: FAOSTAT and EUROSTAT datasets plus country-level yield data from national offices
  - Content: Global sugar cane yield data with regional breakdowns where available
  - Data links: Country-specific data sources listed (e.g., US, Mexico, Brazil, India, China, etc.)
  - Notes: Detailed regional data available for several countries; some regions may have limited or no regional data

- Wheat dataset
  - Global resolution: national, subnational, and sub-subnational
  - Data sources: FAOSTAT and EUROSTAT datasets plus country-level yield data from national offices
  - Data links: Regional data and national datasets per country (e.g., Europe, US, Canada, Mexico, UK, Norway, Sweden, etc.)
  - Temporal and regional detail: Data coverage varies by country; some years/regions have national data while others rely on regional data or FAOSTAT
  - Notes: Some countries only have regional data for certain years; national data used for other years as needed

- Data sources and links (overview)
  - Europe: EUROSTAT (regional data) and other country-specific sources
  - Global: FAOSTAT
  - United States: National Agricultural Statistics Service (USDA)
  - Canada: Statistics Canada
  - Mexico: SIAP (Servicio de Información Agroalimentaria y Pesquera)
  - Argentina, Brazil, Colombia, Peru, Chile, etc.: national statistical offices or agricultural ministries
  - Ethiopia, South Africa, India, China, Japan, Australia, Denmark, Norway, Sweden, Finland, Mongolia, Kazakhstan, etc.: national or regional statistical bodies
  - Date context: Data accessed/updated around June–August 2016 for many sources

- Data quality and consistency
  - Final spatial data were checked against underlying national/global statistics to ensure that disaggregation did not introduce errors
  - National/global statistics used as quality benchmarks for the final spatial data

- Data structure and accessibility
  - File format: netCDF
  - Projection: WGS84 (EPSG 4326 for crop masks)
  - Crop masks: separate files indicating whether each crop is grown in each map cell (0 or 1)
  - Metadata: Included within the netCDF files (grid projection, year, crop type, yield, units)

- caveats and considerations for data leaders
  - Data availability is uneven across countries and years; gaps may require reliance on national or FAOSTAT data
  - Granularity varies (national vs. subnational); some regions have detailed provincial/state data, others only national data
  - Access barriers may exist for certain datasets or historical regional data; some data are only partially available for 2016
  - Documentation provides extensive provenance, access details, and year-by-year notes to support data discovery, sourcing, and governance