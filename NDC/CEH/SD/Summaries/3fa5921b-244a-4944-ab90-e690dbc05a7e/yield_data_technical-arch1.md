# General information

- Scope and levels
  - Agricultural census and survey data collected at three spatial levels: national, subnational (states/provinces), and sub-subnational (counties/districts).
  - Focus crops: maize, sugar cane, and wheat.
  - Earthstat dataset used to identify where crops are grown in each country; absence of data implies no data available or crop not grown there.
  - All spatial data are checked for consistency with national/global statistics to ensure spatial disaggregation is accurate.

- Data format and metadata
  - Yields are reported as metric tonnes per hectare and refer to the year 2016.
  - Spatial data are provided in NetCDF format with metadata included (grid projection, year, crop type, yield, units).
  - Crop mask files indicate whether a crop is grown in each grid cell (values 0 = not grown, 1 = grown).
  - Crop masks use ESRI: 4326 WGS84 projection; spatial data use WGS84.

- Crop-specific datasets

  - Maize
    - Global dataset at national, subnational, and sub-subnational resolutions.
    - Data sources: FAOSTAT and EUROSTAT, with yield data from various national statistics offices.
    - Includes maize for silage; where silage data exists, it is incorporated with yellow maize data to create a combined dataset.
    - Used to generate maps of maize distribution/yield; data availability varies by country (some countries lack maize yield data or have limited regional data).

  - Sugar cane
    - Global dataset at national, subnational, and sub-subnational resolutions.
    - Data sources: FAOSTAT and EUROSTAT; national statistics offices contribute region/country data.
    - Used to generate sugar cane distribution maps; similar country-level coverage considerations as maize.

  - Wheat
    - Global dataset at national, subnational, and sub-subnational resolutions.
    - Data sources: FAOSTAT and EUROSTAT; national statistics offices (e.g., US USDA, Statistics Canada, DEFRA, etc.) provide regional or national yields.
    - Includes data at multiple scales (national and regional), with some countries providing detailed regional codes and years; where regional data are incomplete, national values are used.

- Data sources and accessibility
  - Data sources and links span multiple countries and organizations (e.g., FAOSTAT, EUROSTAT, USDA/NASS, SIAP, SIIA, IBGE, DNP, Statistics Canada, DEFRA, LUKE, etc.).
  - For many countries, data are available via original data files, processed data, and/or code. Access dates typically around 2016–2016/2018.
  - Some countries have limited or no data for certain crops or scales (e.g., some European/Northern countries with sparse regional data; certain countries lacking maize yield data).

- Data quality and validation
  - The provided data are checked for consistency against underlying national/global statistics to ensure the spatial disaggregation aligns with benchmarks.
  - National/global statistics serve as quality-control benchmarks for the final spatial dataset.

- Temporal coverage and notes
  - Although 2016 is the stated reference year for yields, some sources note data availability across broader periods (e.g., 1980–2014 for wheat in some countries; gaps or missing years in others).
  - In cases of missing regional data, national values are used for those years/areas.

- Data structure and spatial reference
  - NetCDF files store the spatially disaggregated yield data with the specified crop masks.
  - Projections: WGS84 (EPSG 4326) for the crop masks; the primary spatial dataset uses a compatible WGS84 projection.
  - Crop masks are provided at multiple resolutions, e.g., 0.25-degree and 0.5-degree grids, to indicate crop presence across the map.

- Practical implications for analysts
  - Data enable mapping and modeling of crop distribution and yields at multiple administrative scales.
  - Users should account for variable data availability across countries and the need to rely on national values where regional data are missing.
  - The datasets are designed for interoperability, with clear metadata and provenance to support reproducibility and data discovery.