# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## Overview and aim
- ROBIN establishes a global reference hydrological network (RHN) with common standards, protocols, indicators, and data infrastructure.
- RHNs consist of high-quality, near-natural gauging stations intended for long-term monitoring of streamflow.
- ROBIN Public Dataset includes metadata for all 3,060 stations and daily streamflow data for 2,386 stations across 30 countries; a Full Dataset with complete data exists but data sharing restrictions apply in some countries.

## Dataset composition
- ROBIN Public Dataset: metadata for all 3,060 stations; daily streamflow data for 2,386 stations.
- Full ROBIN Dataset: 3,060 stations with metadata and daily data (limited access in some regions).
- Daily data are provided in cubic meters per second (m³/s); metadata and catchment attributes are derived from HydroAtlas using CARAVAN.

## Collection/generation and network design
- ROBIN Network comprises countries with established RHNs and those where RHNs are in earlier stages.
- Workshops established criteria for including gauging stations, balancing quality, geographic representation, and data availability.
- Two levels of network inclusion:
  - Level 1: focuses on extreme flows (high/low) from pristine or near-pristine catchments.
  - Level 2: suitable for monthly, seasonal, or annual means and water balance analyses; requires high-quality data with appropriate metadata and longer records.
- Level 2 requirements include: high-quality daily mean data, minimal human disturbance, long enough record length (≥ 20 years for Level 2; Level 1 prioritizes longer, more extreme-flow-focused records).

## Nature and units of recorded values
- ROBIN Public Dataset includes daily streamflow records (flow_cumecs [m³/s]) for 2,386 stations; 3,060 stations hold metadata.
- Country-level counts show varying availability of metadata and daily data (e.g., USA and Australia have comprehensive metadata and data; several countries have metadata only or data availability limited by sharing restrictions).
- Data are provided in Local Standard Time.

## Quality control
- Data and metadata submissions undergo centralized quality control.
- QC process involves three hydrologists using standard QC software to visually screen for change points, anomalies, and infilling; ensure near-natural regimes; remove obviously erroneous periods.
- Stations are categorized into Level 1 or Level 2 after QC and thorough screening; final listings reflect data completeness and record length criteria.

## Details of data structure
- All data packaged in a ZIP file.
- Inside: 2,386 CSV files named with the convention YYXXXXX.csv (YY = country code; XXXXX = ROBIN ID).
- Each CSV contains: header row with robin_id, date [yyyy-mmdd], flow_cumecs [m³/s], followed by data rows; missing values shown as NULL.
- Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv with fields such as ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, CARAVAN_AREA, and numerous derived climate/land-cover attributes.
- Catchment attributes derived from HydroAtlas/CARAVAN and catchment boundary shapefiles available on ROBIN GitHub.
- Additional sections in appendices provide detailed metadata field explanations (Section 7.1) and further hydrobelt/Köppen classification mappings (Sections 7.2, 7.3).

## Metadata and derived attributes
- Core station metadata: ROBIN_ID, LOCAL_ID, station name, geographic coordinates, catchment area, start/end dates, data provider, country, and data permissions.
- Derived attributes include: HYDROBELT (Hydrobelt codes), KOPPEN (Köppen climate classification), CARAVAN area, a wide set of climate, hydrology, land cover, soils, and anthropogenic attributes (e.g., AET, PET, PRE, PRM, GDP proxies, urban fraction, cropland extent, forest cover, etc.).
- Some attributes are provided per month or year (e.g., precipitation, evapotranspiration, soil moisture, land cover extents) and are wired to monthly/annual aggregations.

## Data access and permissions
- Data permissions are captured in the metadata with Open, Restricted, or Unavailable statuses.
- ROBIN Public Dataset provides open data where possible; some data or metadata may be restricted or unavailable to the public and available only to ROBIN collaborators.

## Temporal scope and units
- Temporal coverage: 1863 to 2022 (daily streamflow records).
- Data units: flow_cumecs [m³/s].
- Time convention: Local Standard Time.

## Practical implications for monitoring frameworks
- Provides a global, standardized baseline of daily streamflow records suitable for:
  - Assessing extreme flows and hydrological change indicators (Level 1) and
  - Analyzing seasonal/annual means and water balances (Level 2).
- Enables cross-country comparability through a harmonized data structure, metadata schema, and quality control practices.
- Supports transparent data governance and open data principles where possible, while acknowledging data-sharing constraints in some jurisdictions.
- Useful for evaluating policy impacts on hydrology, climate-change detection studies, and long-term water-resource planning.

## Limitations and considerations
- Data gaps: some stations have incomplete records; Level 2 requires minimum continuous records (e.g., 20 years) and limited long gaps.
- Access restrictions: not all stations/data are openly available in ROBIN Public Dataset; some are restricted or unavailable.
- Metadata completeness: while extensive, some countries may have less complete metadata or attribution.
- Data transformation needs: data are provided in local time and require transformation for some global analyses; varying data collection methods over time may introduce inhomogeneities.
- Transportability: while designed for global application, network density varies by country, which can affect regional representativeness.

## References and contact
- Turner, S. et al. (2024). Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022. NERC EDS Environmental Information Data Centre. DOI: https://doi.org/10.5285/3b077711-f18342f1-bac6-c892922c81f4
- ROBIN project website: https://www.ceh.ac.uk/our-science/projects/robin
- Contact for inquiries: enquries@ceh.ac.uk; @UK_CEH; ceh.ac.uk
- ROBIN data repository and related materials: ROBIN GitHub Repository (ROBIN_pipeline)