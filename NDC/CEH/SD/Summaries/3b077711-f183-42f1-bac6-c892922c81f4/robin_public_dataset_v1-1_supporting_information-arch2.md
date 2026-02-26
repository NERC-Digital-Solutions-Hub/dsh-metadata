# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## Overview
- ROBIN aims to establish and sustain a global reference hydrological network (RHN) with common standards, protocols, indicators, and data infrastructure.
- Reference Hydrometric Networks (RHNs) are gauging stations with relatively undisturbed catchments and high-quality, low-missing data; ROBIN unites these networks at a global level.
- The ROBIN Full Dataset includes 3,060 stations in 30 countries; the ROBIN Public Dataset provides metadata for all 3,060 stations and daily streamflow data for 2,386 stations (tiered due to data-sharing restrictions).
- More information available at the project website: https://www.ceh.ac.uk/our-science/projects/robin
- Citation and contributor list provided; dataset published in 2024 (DOI linked in the document).

## Collection and network criteria
- RHNs are well established in many countries; ROBIN workshops defined inclusion criteria to balance global representation.
- Criteria are qualitative to allow flexibility; thresholds differentiate two levels:
  - Level 1: near-natural regime, very high data quality, suitable for extreme flow analysis (high/low) with data from pristine catchments when possible.
  - Level 2: fairly to highly quality daily data suitable for monthly, seasonal, or annual analyses and water balances; higher tolerances for disturbances.
- Level 2 requires high-quality daily mean data with metadata; Level 1 emphasizes long, near-natural records and complete data.
- Data integrity checks consider land-use changes, disturbances, and data gaps.

## Nature, units, and coverage
- ROBIN Public Dataset: 2,386 stations provide daily streamflow data (m3/s); 3,060 stations provide metadata.
- Country-by-country counts of stations with metadata and/or streamflow data are provided (examples: United States 715 metadata; Australia 452 metadata and data; United Kingdom 146; Canada 315; others listed in the document).
- Data are provided in Local Standard Time; missing values are indicated as NULL.

## Quality control
- Central QA/QC performed after data submission by three hydrologists from the UK National River Flow Archive.
- QC methods include visual screening for change points, anomalous conditions, and infilled data gaps; stations with non near-natural regimes are removed or edited to preserve high-quality data.
- Stations are assigned to Level 1 or Level 2 based on local specialist assessment and data-length/completeness criteria, producing final listings in ROBIN_Station_Metadata_Public_V1-1.csv.

## Data structure and access
- All streamflow data are stored in a ZIP folder containing 2,386 CSV files named using a ROBIN ID convention (YYXXXXX.csv; e.g., GB00001).
- Each CSV has a header: robin_id, date [yyyy-mmdd], flow_cumecs [m3/s], with missing data as NULL; data are in Local Standard Time.
- Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv, including fields such as ROBIN_ID, LOCAL_ID, station name, coordinates (WGS84), catchment area, start/end dates, data owner, data permission, Level (1 or 2), HYDROBELT, Koppen climate classification, and many derived attributes (HydroAtlas/Caravan attributes where available).
- Catchment boundaries and additional attributes are derived from HydroAtlas via CARAVAN; boundary shapefiles are available on the ROBIN GitHub repository.
- Appendix sections (7.x) detail station metadata columns, Hydrobelt, and Koppen climate classifications used in the metadata.
- Data permissions: Open, Restricted, or Unavailable at the station level; ROBIN Public Dataset provides metadata for all stations, while daily streamflow data availability follows permissions.

## Derived attributes and related data
- Catchment attributes drawn from HydroAtlas/CARAVAN; static catchment attributes provided where available.
- Hydrobelt information (Greenland/Boreal/Northern Mid Latitude etc.) and Koppen climate classification (multiple codes and descriptions) linked to stations.
- Metadata fields also include land cover, climate, hydrology, physiography, and anthropogenic indicators (e.g., cropland extent, population, GDP, urban extent, vegetation indices) where available.

## Use for monitoring the environment (analysts’ perspective)
- Enables long-term monitoring of global hydrological health and climate-change signals via standardized daily streamflow records.
- Supports analysis of extreme flows (high/low) and long-term trends across many countries with consistent methods and data infrastructure.
- Facilitates cross-country comparisons of river regimes in near-natural settings (Level 1) and broader hydrological balances (Level 2).
- Provides a foundation for integrating hydrological data with environmental indicators (e.g., land cover, precipitation, evapotranspiration, climate indices, anthropogenic pressures) through Caravan/HydroAtlas attributes.
- Data quality assurance and standardized structure support reproducible analyses and policy performance assessments over time.

## Practical considerations for analysts
- Data access is tiered: metadata for all stations is public; daily streamflow data is Open in the ROBIN Public Dataset for the eligible 2,386 stations; other data may be Restricted or Unavailable.
- The ZIP-based structure and consistent naming convention (YYXXXXX.csv) facilitate automated data loading and integration into monitoring pipelines.
- The Appendix and metadata schema enable efficient data wrangling, including linking stations to climate and catchment descriptors (Koppen, Hydrobelt, Caravan attributes) for holistic environmental assessments.

## References and support
- Foundational methods and context cited from multiple studies on reference hydrologic networks and station networks across regions.
- Project contact and institutional support provided (UK Centre for Ecology & Hydrology).