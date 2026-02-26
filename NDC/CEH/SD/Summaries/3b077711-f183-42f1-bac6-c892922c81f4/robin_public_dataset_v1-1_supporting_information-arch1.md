# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

- The ROBIN project establishes and sustains a global reference hydrological network (RHN) with common standards, indicators, and data infrastructure to detect climate-related changes in streamflow.
- The ROBIN Public Dataset includes metadata for all 3,060 stations and daily streamflow data for 2,386 stations, spanning 1863–2022, across 30 countries.
- More information available at the ROBIN project website: https://www.ceh.ac.uk/our-science/projects/robin
- Citation: Turner et al. (2024) for the Global hydrological dataset; dataset held at NERC EDS Environmental Information Data Centre.

## 1) Collection and criteria for inclusion

- RHNs are established in various countries; ROBIN aims to unify them globally with standardized criteria.
- Station inclusion is guided by qualitative criteria to balance global coverage with regional representativeness.
- Two-level network design:
  - Level 1: stations with near-natural regimes, minimal human disturbance, high data quality, suitable for extreme-flow analysis.
  - Level 2: stations suitable for less sensitive hydrological variables (monthly/seasonal/annual means) with metadata and high-quality daily data; data length criteria are more modest.
- Disturbance thresholds (e.g., urbanization, land-use changes) and data completeness influence Level assignment.
- Level 1 data prioritized for extremes; Level 2 data used for hydrological balances and mean flows.
- Data sharing restrictions mean the ROBIN Full Dataset (3,060 stations + metadata) is partially split; Public Dataset contains metadata for all stations and daily data for 2,386 stations.
- Country-level counts of metadata and streamflow data are provided (e.g., United States, Australia, Canada, UK, etc.).

## 2) Nature and units of recorded values

- Daily streamflow data: 2,386 stations; measured in cubic meters per second (m3/s).
- Metadata: 3,060 stations with records of station characteristics and catchment context.
- Data format and accessibility:
  - Data in a ZIP folder containing 2,386 CSV files named YYXXXXX.csv (YY = country UN code; XXXXX = ROBIN ID e.g., GB00001).
  - Each CSV has:
    - Headers: robin_id, date [yyyy-mmdd], flow_cumecs [m3/s].
    - Data rows follow; missing values are NULL.
    - Times are Local Standard Time.
  - Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv (ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA, START_DATE, END_DATE, DATA_OWNER_NAME, COUNTRY, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, etc.).
  - Catchment attributes are derived from HydroAtlas using CARAVAN; related shapefiles available on ROBIN GitHub (ROBIN_pipeline).
- Additional derived attributes available in metadata (e.g., catchment area, Koppen climate classification, hydrobelt).

## 3) Quality control

- Central quality control performed by a small team (three hydrologists) using QC software standard in national hydrometric centers.
- Procedures include:
  - Visual screening for change points and anomalous data, evidence of methodology changes, and infilled gaps.
  - Edits to remove obviously erroneous data; retention of as much valid data as possible.
  - Stations are assigned to Level 1 or Level 2 by local specialists; Level 1 stations from Low Flow Project also identified accordingly.
  - Quantitative checks for record length and completeness applied to finalize Level 1 and Level 2 listings (ROBIN_Station_Metadata_Public_V1-1.csv).

## 4) Data structure and metadata details

- 5.1 Data structure
  - All streamflow data are in a ZIP folder.
  - 2,386 station CSV files with naming convention YYXXXXX.csv (ROBIN ID).
  - Each CSV includes robin_id, date, flow_cumecs; missing data as NULL.
  - Data provided in Local Standard Time.
  - Metadata file ROBIN_Station_Metadata_Public_V1-1.csv includes fields such as ROBIN_ID, LOCAL_ID, NAME, LATITUDE, LONGITUDE, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, and many CARAVAN-derived attributes.
  - Catchment boundaries and static attributes derived from HydroAtlas (CARAVAN) are provided where available; catchment boundary shapefiles are on GitHub.
- 7.1 Station Metadata Column Information
  - Extensive list of fields including ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA, START_DATE, END_DATE, DATA_OWNER_NAME, COUNTRY, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, CARAVAN_AREA, and numerous climate, hydrology, land cover, and sociogeographic attributes (e.g., AET, PET, PRE, PRE-SYR, urban extent, GDP, population, soil properties, vegetation, etc.).
  - Metadata also documents data usage details (FREE_TEXT) and data aggregation scales.
- 7.2 Hydrobelt Information
  - Hydrobelt codes and descriptions (e.g., Greenland/Ice, Boreal, Northern Mid Latitude, Northern Dry, Northern Sub Tropical, Equatorial, Southern Sub Tropical, Southern Dry, Southern Mid Latitude).
- 7.3 Koppen Information
  - Koppen climate classifications (e.g., Af, Am, Aw, BWh, BWk, BSh, BSk, Csa, Csb, Csc, Cwa, etc.) with multiple subcodes and descriptive mappings.

## 5) Access, usage, and references

- Data availability and permissions:
  - DATA_PERMISSION field indicates Open, Restricted, or Unavailable data for RO BIN Public Dataset; some data may be accessible to ROBIN collaborators only.
- Use cases for analysts with data-focused aims:
  - Identify long-term hydrological trends and climate-change signals using daily streamflow records.
  - Analyze extremes (high/low flows) and changes in flow regimes across global regions.
  - Develop or calibrate predictive models using standardized, globally sourced streamflow data and rich metadata.
  - Compare basins using harmonized catchment attributes (CARAVAN) and climate/geography classifications (HYDROBELT, Koppen).
- References and related works:
  - Do et al. (2022), Harrigan et al. (2018), Jain (2015), Murphy et al. (2013), Whitfield et al. (2012), Yeste et al. (2018), Kratzert et al. (2023), and others cited in the document.
- Contact and repository information:
  - Enquiries: enquiries@ceh.ac.uk
  - Project and data repository: ROBIN pipeline and related materials on ROBIN GitHub; CEH contact points provided.

- Note for analysts: While the ROBIN Public Dataset provides broad, standardized daily streamflow data and rich station metadata, data accessibility varies by country and data permissions. The dataset is designed to enable cross-regional analyses with careful attention to Level 1 vs Level 2 suitability, data quality controls, and metadata completeness.