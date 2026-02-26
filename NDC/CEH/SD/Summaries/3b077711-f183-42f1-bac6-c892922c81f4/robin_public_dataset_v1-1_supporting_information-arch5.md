# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## Overview
- ROBIN aims to establish and sustain a global reference hydrological network (RHN) with common standards, protocols, indicators, and data infrastructure.
- RHNs consist of gauging stations with near-natural catchments, high-quality data, and minimal missing data.
- ROBIN Public Dataset includes metadata for all 3,060 stations and daily streamflow data for 2,386 stations (full dataset has 3,060 stations with metadata; 2,386 with data) due to data-sharing restrictions in some countries.

## Data collection and network criteria
- Founding ROBIN members have led efforts to establish RHN catchments; multiple international workshops agreed on station inclusion criteria.
- Criteria are qualitative to allow geographic representativeness and flexibility.
- Two levels:
  - Level 1: stations suitable for extreme-flow analyses; near-pristine catchments; minimal human disturbance.
  - Level 2: higher-coverage suitability for monthly/annual analyses; very high-quality daily data with metadata; longer records and fewer data gaps.
- Level 2 requires longer records (e.g., at least 20–40 years depending on criteria) and high data completeness.

## Nature and units of recorded values
- Daily streamflow data (cubic meters per second, m3/s) for 2,386 stations; 3,060 stations with metadata records.
- Metadata and data are country-coded; country-wise counts shown (e.g., Australia, United States, United Kingdom, Canada, etc.).
- Data are provided in Local Standard Time.

## Data structure and accessibility
- All data are delivered as a ZIP file containing 2,386 CSV files named YYXXXXX.csv (YY = UN country code, XXXXX = ROBIN ID).
- Each CSV includes: header with columns robin_id, date [yyyy-mmdd], flow_cumecs [m3/s]; missing values are NULL.
- Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv includes ROBIN_ID, LOCAL_ID, station name, coordinates (WGS84), catchment area, data provider, and other fields; static catchment attributes derived from HydroAtlas via CARAVAN and available in the metadata.
- Catchment boundary shapefiles and supplementary metadata attributes available on ROBIN GitHub (ROBIN_pipeline).
- Appendix sections detail the fields of the metadata and provide additional station information.

## Quality control and provenance
- Central QC conducted by three hydrologists from the UK National River Flow Archive using established QC software.
- Data visually screened for change points, anomalous conditions, infilled gaps, and obvious errors; stations with non near-natural regimes removed or edited accordingly.
- Stations assigned to Level 1 or Level 2 by local specialists after QC; final Level designations recorded in ROBIN_Station_Metadata_Public_V1-1.csv.
- QC process built on prior projects (e.g., Low Flow Studies) to ensure consistency across ROBIN stations.

## Metadata, documentation, and technical details
- Station metadata field information provided in the document (e.g., ROBIN_ID, LOCAL_ID, NAME, LAT/LON, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, Koppen classification, and a rich set of derived climate, hydrology, land cover, and anthropogenic attributes).
- Hydrobelt and Koppen climate classifications included for stations (mapping tables provided).
- Derived attributes drawn from CARAVAN/HydroAtlas, enabling broad contextual analyses (e.g., AET, PET, precipitation, soil & geology, land cover, population, GDP, etc.).
- Appendix sections (7.1 Station Metadata Column Information, 7.2 Hydrobelt Information, 7.3 Koppen Information) document the metadata schema and classification mappings.

## Access permissions and usage
- Data permissions in metadata include:
  - Open: streamflow data available in the ROBIN Public Dataset.
  - Restricted: metadata available in ROBIN Public Dataset; streamflow data available to ROBIN Collaborators only.
  - Unavailable: metadata only.
- ROBIN Public Dataset provides access to station metadata and daily streamflow data for a subset of stations; restrictions reflect data-sharing agreements by country.
- Citation guidance provided (Turner et al., 2024; dataset DOI available in references).

## Practical use and considerations for data stewards
- Supports global discovery and comparison of hydrological regimes through standardized formats and metadata.
- Enables extreme-flow (Level 1) vs mean/monthly-flow analyses (Level 2) based on data quality and completeness.
- Requires ongoing governance for updates, new data uploads, and maintenance of access permissions (Open/Restricted/Unavailable) in line with partner agreements.
- Documentation and provenance are rich, including metadata completeness, catchment attributes, and climate/land-cover contextual layers to facilitate interoperable analyses across systems and formats.
- Ensures traceability through explicit data owners, start/end dates, and standardized time zones.

## Contact and resources
- Documentation, project website, and data contact details are provided (Enquiries, CEH contact points, and institutional locations in the UK).