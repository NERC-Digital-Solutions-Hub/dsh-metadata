# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## 1. Summary
- ROBIN establishes a global reference hydrological network (RHN) with common standards, protocols, indicators, and data infrastructure to detect climate-related changes in river flows.
- RHNs comprise gauging stations with near-natural catchments, high-quality data, and minimal missing data; ROBIN is the first global integration of RHNs.
- The ROBIN Public Dataset contains metadata for 3,060 stations and daily streamflow data for 2,386 stations (dataset is tiered due to varying data-sharing restrictions across countries).
- Full ROBIN Network and dataset information are available at the project site: https://www.ceh.ac.uk/our-science/projects/robin.
- Citation: Turner et al. (2024). Global hydrological dataset of daily streamflow data from the ROBIN, NERC EDS Environmental Information Data Centre.

## 2. Collection/generation methods
- RHNs are already established in many countries; ROBIN held workshops to agree criteria for station inclusion and network structure.
- Criteria define two levels (Level 1 and Level 2) to balance data quality and global coverage:
  - Level 1: prioritized for near-natural stations suitable for extreme-flow analysis (high data quality, minimal human disturbance).
  - Level 2: includes stations suitable for monthly/seasonal/annual analyses with metadata and longer records.
- The criteria aim for geographic representativeness while allowing compromises where needed.
- Stations originate from national reference networks and are vetted through centralized coordination.

## 3. Nature and Units of recorded values
- Data coverage:
  - ROBIN Public Dataset: 2,386 stations with daily streamflow data (m³/s).
  - ROBIN Metadata: 3,060 stations.
- Data format:
  - Data delivered as a ZIP containing 2,386 CSV files named YYXXXXX.csv (YY = country code; XXXXX = ROBIN ID).
  - Each CSV has columns: robin_id, date [yyyy-mmdd], flow_cumecs [m³/s]. Missing data are NULL. Times are in Local Standard Time.
- Metadata and derived attributes:
  - ROBIN_Station_Metadata_Public_V1-1.csv contains ROBIN_ID, LOCAL_ID, station name, coordinates, catchment area, start/end dates, data owner, country, and data permission (Open / Restricted / Unavailable).
  - Catchment attributes are derived from HydroAtlas using CARAVAN (static attributes) and available as part of the metadata; catchment boundary shapefiles are on the ROBIN GitHub repository.
- Country distribution (per country counts are provided in the metadata file):
  - Examples include large numbers of stations in the United States, Australia, Canada, United Kingdom, France, Germany, and others.

## 4. Quality control
- QC is conducted centrally by three hydrologists using the standard QC software used by the UK National River Flow Archive.
- Procedures include visual screening for change points, infilled data periods, and obviously erroneous data; stations with non near-natural regimes are removed or edited to preserve high-quality data.
- Stations are assigned to Level 1 or Level 2 by local specialists, with Level 2 applying quantitative criteria for length and completeness (final listings are in ROBIN_Station_Metadata_Public_V1-1.csv).
- Many stations contributed via earlier Low Flow Studies projects, reinforcing QC continuity and comparability.

## 5. Details of data structure
- Data packaging:
  - All streamflow data are contained in a ZIP file.
  - 2,386 CSV files within the ZIP, named YYXXXXX.csv (ROBIN ID).
- CSV structure:
  - Header includes robin_id, date [yyyy-mmdd], flow_cumecs [m³/s].
  - Data compared in Local Standard Time; missing values are NULL.
- Metadata and attributes:
  - ROBIN_Station_Metadata_Public_V1-1.csv contains station-level metadata (ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, etc.).
  - The metadata file also includes a wide range of derived catchment attributes, many of which come from HydroAtlas/CARAVAN and other environmental descriptors.
- Access to boundaries:
  - Catchment boundary shapefiles and additional metadata are available via the ROBIN GitHub repository.

## 6. References
- Do, H. X., Le, M. H., Pham, H. T., et al. (2022). Identifying hydrologic reference stations to understand changes in water resources across Vietnam - a data-driven approach.
- Harrigan, S., Hannaford, J., Muchan, K., & Marsh, T. J. (2018). Designation and trend analysis of the updated UK Benchmark Network of river flow stations: the UKBN2 dataset.
- Hodgkins, G. A., Renard, B., Whitfield, P. H., et al. (2024). Climate Driven Trends in Historical Extreme Low Streamflows on Four Continents.
- Jain, S. K. (2015). Reference Climate and Water Data Networks for India.
- Kratzert, F., Nearing, G., Addor, N., et al. (2023). Caravan - A global community dataset for large-sample hydrology.
- Murphy, C., Harrigan, S., Hall, J., & Wilby, L. R. (2013). Climate-driven trends in mean and high flows from a network of reference stations in Ireland.
- Whitfield, P. H., Burn, D. H., Hannaford, J., et al. (2012). Reference hydrologic networks I. The status and potential future directions of national reference hydrologic networks for detecting trends.
- Yeste, P., Dorador, J., Martin-Rosales, W., et al. (2018). Climate-driven trends in the streamflow records of a reference hydrologic network in Southern Spain.
- Zhang, X. S., Amirthanathan, G. E., Bari, M. A., et al. (2016). How streamflow has changed across Australia since the 1950s: Evidence from the network of hydrologic reference stations.
- Turner, S.; Hannaford, J.; Barker, L.J.; et al. (2024). Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/3b077711-f18342f1-bac6-c892922c81f4

## 7.1 Station Metadata Column Information
- The ROBIN_Station_Metadata_Public_V1-1.csv includes columns such as:
  - ROBIN_ID, LOCAL_ID, NAME, LATITUDE, LONGITUDE, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL
  - HYDROBELT (Hydrobelt code), KOPPEN (Köppen climate code)
  - Extensive climate, hydrology, land cover, and anthropogenic attributes (e.g., AET, PRE, PET, PNV, GLC, POP counts, GDP indicators, land cover extents, etc.)
  - Catchment- and reach-scale attributes derived from HydroAtlas/CARAVAN and related datasets
- The dataset provides a wide set of monthly and annual metrics alongside static catchment descriptors to facilitate diverse analyses.

## 7.2 Hydrobelt Information
- Hydrobelt codes and descriptions:
  - 0: Greenland (Ice)
  - 1: BOR – Boreal
  - 2: NML – Northern Mid Latitude
  - 3: NDR – Northern Dry
  - 4: NST – Northern Sub Tropical
  - 5: EQT – Equatorial
  - 6: SST – Southern Sub Tropical
  - 7: SDR – Southern Dry
  - 8: SML – Southern Mid Latitude

## 7.3 Koppen Information
- Köppen climate classification codes used in metadata (selected examples):
  - Af – Tropical rainforest
  - Am – Tropical monsoon
  - Aw – Tropical savannah
  - BWh – Arid, desert, hot
  - BWk – Arid, desert, cold
  - BSh – Arid, steppe, hot
  - BSk – Arid, steppe, cold
  - Csa – Temperate, dry summer, hot summer
  - Csb – Temperate, dry summer, warm summer
  - Csc – Temperate, dry summer, cold summer
  - Cwa – Temperate, dry winter, hot summer
  - Cwb – Temperate, dry winter, warm summer
  - Cwc – Temperate, dry winter, cold summer
  - Cfa – Temperate, no dry season, hot summer
  - Cfb – Temperate, no dry season, warm summer
  - Cfc – Temperate, no dry season, cold summer
  - Dsa – Cold, dry winter, hot summer
  - Dsb – Cold, dry winter, warm summer
  - Dsc – Cold, dry winter, cold summer
  - Dsd – Cold, dry winter, very cold winter
  - Dwa – Cold, dry winter, hot summer
  - Dwb – Cold, dry winter, warm summer
  - Dwc – Cold, dry winter, cold summer
  - Dwd – Cold, dry winter, very cold winter
  - Dfa – Cold, no dry season, hot summer
  - Dfb – Cold, no dry season, warm summer
  - Dfc – Cold, no dry season, cold summer
  - Dfd – Cold, no dry season, very cold winter
  - ET – Polar, tundra
  - EF – Polar, ice cap

Note: Full mappings and additional monthly/annual attributes are available in the ROBIN metadata and accompanying appendix.