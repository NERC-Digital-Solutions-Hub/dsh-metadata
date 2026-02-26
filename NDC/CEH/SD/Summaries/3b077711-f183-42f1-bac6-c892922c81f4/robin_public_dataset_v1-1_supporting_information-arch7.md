# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## Overview
- ROBIN establishes a global reference hydrological network (RHN) with common standards, protocols, indicators, and data infrastructure.
- RHNs are gauging stations with near-natural regimes and high-quality data; the ROBIN Network integrates networks across countries at a global level.
- ROBIN Public Dataset includes metadata for all 3,060 stations and daily streamflow data for 2,386 stations (3,060 total stations metadata; 2,386 with daily data).
- More information available at the ROBIN project website.
- Citation provided for the dataset (Turner et al., 2024) with DOI.

## Data content
- Daily streamflow data (cubic meters per second, m³/s) for 2,386 stations; station metadata for 3,060 stations.
- Data span: 1863–2022; provided in Local Standard Time.
- File structure:
  - ZIP file containing 2,386 CSV files named YYXXXXX.csv (YY = country code, XXXXX = ROBIN ID, e.g., GB00001).
  - Each CSV has header: robin_id, date [yyyy-mmdd], flow_cumecs [m³/s]; missing values = NULL.
- Metadata:
  - ROBIN_Station_Metadata_Public_V1-1.csv with fields including ROBIN_ID, LOCAL_ID, station NAME, LATITUDE, LONGITUDE, CATCHMENT AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, and CARAVAN-derived attributes.
- Catchment attributes:
  - Derived from HydroAtlas via CARAVAN; available in metadata.
  - Catchment boundary shapefiles hosted on ROBIN GitHub.
- Appendix details and field definitions for metadata.

## Collection and generation methods
- RHN concepts established in multiple countries; ROBIN Workshops define station inclusion criteria with flexibility for global geographic representativeness.
- Two levels of network data:
  - Level 1: High-priority, near-pristine stations (for extreme flow analysis, high data quality).
  - Level 2: Broadly suitable stations for monthly/seasonal/annual analyses with high-quality daily data and metadata.
- Station levels determined by local specialists; Level classification also aligned with data availability and completeness criteria.
- Data contributed by national or data-provider networks; collaboration ensures consistent approach to station selection.

## Quality control
- Central quality control conducted by three hydrologists from the UK National River Flow Archive.
- Visual screening for change points, anomalies from infilling, and obvious errors; removal of stations with non-near-natural regimes.
- Edits applied to retain as much valid data as possible; stations categorized into Level 1 or Level 2 after QC using established criteria.

## Data structure and access
- Data packaged as a ZIP containing 2,386 daily data CSVs and a metadata CSV.
- File naming and structure:
  - CSVs: YYXXXXX.csv (Robin ID) with columns robin_id, date, flow_cumecs.
- Metadata:
  - ROBIN_Station_Metadata_Public_V1-1.csv includes ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, and CARAVAN attributes.
- Spatial data:
  - Catchment attributes derived from HydroAtlas using CARAVAN; boundary shapefiles available on ROBIN GitHub.
- Appendix (Document) provides detailed field definitions for station metadata and related attributes.

## Station metadata and attributes (key fields)
- ROBIN_ID, LOCAL_ID, NAME, LATITUDE, LONGITUDE, AREA (catchment, km²), START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL.
- Hydrobelt (e.g., BOR, NML, NDR, NST, EQT, SST, SDR, SML) and Koppen climate classification codes.
- CARAVAN-derived attributes (extensive climate, land cover, hydrology, soils, and geography descriptors) such as AET, PRE, PET, PET-Monthly, PRE-Monthly, land cover extents, drought/moisture indices, anthropogenic indicators, and more.
- Data permission levels: Open, Restricted, Unavailable (Open allows public streamflow data; Restricted may give access to metadata or data to collaborators).

## Spatial and temporal coverage
- Global scope: 30 countries represented in the dataset; daily streamflow records for 2,386 stations, with metadata for 3,060 stations.
- Time range: 1863–2022.
- Data are in Local Standard Time for each station.

## GIS relevance and usage
- Ideal for map-based visualization and spatial analysis of river flow regimes, extreme flows, and hydrological change detection.
- Join daily values (via ROBIN_ID) to station metadata (location, catchment area, climate, land cover, and anthropogenic attributes) for enriched maps and analyses.
- Catchment boundaries and CARAVAN-derived attributes enable basin-level mapping and integration with other GIS layers (HydroAtlas, Koppen, Hydrobelt, land cover, climate indices).
- Metadata supports data provenance, data permissions, station level (1 or 2), and data source details for reproducibility.

## Data quality considerations and limitations
- Level 1 data prioritized for near-natural catchments; Level 2 data include high-quality daily records but with broader applicability.
- Quality control focused on ensuring consistency with established QC practices from prior projects; some data gaps and infilling are possible but flagged through QC process.
- Data availability varies by country and data provider; metadata includes data permission status (Open/Restricted/Unavailable).

## References and further information
- Turner, S. et al. (2024). Global hydrological dataset of daily streamflow data from the ROBIN, 1863–2022. NERC EDS Environmental Information Data Centre. DOI provided in document.
- Project website: https://www.ceh.ac.uk/our-science/projects/robin
- ROBIN GitHub repository for catchment shapefiles and pipeline resources.