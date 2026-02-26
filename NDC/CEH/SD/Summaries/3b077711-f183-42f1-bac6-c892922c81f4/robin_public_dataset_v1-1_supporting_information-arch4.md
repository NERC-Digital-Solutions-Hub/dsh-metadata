# Global hydrological dataset of daily streamflow data from the Reference Observatory of Basins for INternational hydrological climate change detection (ROBIN), 1863 - 2022

## Summary
- ROBIN established a global Reference Hydrometric Network (RHN) with common standards, protocols, indicators, and data infrastructure to detect climate-driven changes in hydrology.
- RHNs require stations with near-natural catchments, high data quality, and minimal missing data. ROBIN integrates these networks across borders for global analysis.
- The ROBIN Full Dataset includes 3,060 stations with metadata and daily flow data; the ROBIN Public Dataset provides metadata for all 3,060 stations and daily streamflow data for 2,386 stations (data-sharing restrictions apply in some countries).
- Data and metadata are accessible via the ROBIN project (website: ceh.ac.uk/our-science/projects/robin). Citation: Turner et al. (2024), NERC EDS Environmental Information Data Centre.
- For data governance, there are two access levels (Open, Restricted, Unavailable) and a two-tier station classification (Level 1 for high-quality, near-pristine data; Level 2 for high-quality data suitable for broader hydrological analyses).

## Collection/generation methods
- RHN networks are well established in some countries; ROBIN consolidates efforts to create a globally representative RHN.
- The ROBIN Network conducted workshops to agree criteria for station inclusion and to define Level 1 and Level 2 classifications.
- Level 1 stations emphasize suitability for extreme-flow analyses in pristine or near-pristine catchments; Level 2 stations support monthly, seasonal, and annual analyses with robust metadata.
- Criteria are qualitative to balance global coverage and data quality; Level 1 and Level 2 criteria include disturbance thresholds, data continuity, and metadata requirements.
- Metadata and catchment attributes are augmented using HydroAtlas and CARAVAN-derived data; some data and shapefiles are shared via the ROBIN GitHub repository.

## Nature and Units of recorded values
- ROBIN Public Dataset provides daily streamflow data (cubic meters per second, m3/s) for 2,386 stations; metadata is available for all 3,060 stations.
- Data format: 2,386 CSV files named YYXXXXX.csv (YY = country code, XXXXX = ROBIN ID). Each file contains header robin_id, date [yyyy-mmdd], flow_cumecs [m3/s], with NULL representing missing data.
- Time reference: Local Standard Time.
- Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv, containing fields such as ROBIN_ID, LOCAL_ID, NAME, LAT/LON, AREA (catchment), START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, and derived static attributes (CARAVAN-based).
- Catchment attributes are precomputed (HydroAtlas/CARAVAN) and available in the metadata; catchment boundary shapefiles are on the ROBIN GitHub repository.

## Quality control
- A centralized quality control process was applied after data submission.
- A team of three hydrologists visually screened daily records for change points, methodology changes, or infilled data gaps; identified obvious errors and near-natural regime integrity.
- Stations were removed if they did not exhibit a sufficiently near-natural regime; edits were applied to retain the majority of high-quality data.
- Stations were assigned to Level 1 or Level 2 by local specialists; subsequent quantitative criteria (record length and completeness) determined final Level designations.

## Details of data structure
- Data are delivered as a ZIP file containing 2,386 CSV files (named YYXXXXX.csv; ROBIN ID).
- Each CSV contains: header with robin_id, date [yyyy-mmdd], flow_cumecs [m3/s], followed by data rows; missing values are NULL.
- Timezone: Local Standard Time.
- Metadata file: ROBIN_Station_Metadata_Public_V1-1.csv with ROBIN_ID, LOCAL_ID, NAME, LATITUDE, LONGITUDE, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL, HYDROBELT, KOPPEN, and numerous derived catchment attributes (CARAVAN_AREA, etc.).
- Derived attributes: static catchment attributes from HydroAtlas via CARAVAN; catchment boundary shapefiles and related documentation available on GitHub (ROBIN_pipeline).
- Appendix provides detailed descriptions for the metadata fields (Section 7.1), Hydrobelt (Section 7.2), and Koppen climate classification (Section 7.3).

## References
- Do, H. X., et al. (2022). Identifying hydrologic reference stations to understand changes in water resources across Vietnam.
- Harrigan, S., et al. (2018). UK Benchmark Network of river flow stations: designations and trends.
- Hodgkins, G. A., et al. (2024). Climate-driven trends in historical extreme low streamflows on four continents.
- Jain, S. K. (2015). Reference Climate and Water Data Networks for India.
- Kratzert, F., et al. (2023). Caravan - A global community dataset for large-sample hydrology.
- Murphy, C., et al. (2013). Climate-driven trends in mean and high flows from reference stations in Ireland.
- Whitfield, P. H., et al. (2012). Reference hydrologic networks I. Status and directions for national networks.
- Yeste, P., et al. (2018). Climate-driven trends in streamflow records in Southern Spain.
- Zhang, X. S., et al. (2016). How streamflow has changed across Australia since the 1950s.

## 7.1 Station Metadata Column Information (highlights)
- Key fields: ROBIN_ID, LOCAL_ID, NAME, LATITUDE, LONGITUDE, AREA, START_DATE, END_DATE, COUNTRY, DATA_OWNER_NAME, DATA_PERMISSION, LEVEL.
- Climate and geography fields: HYDROBELT, KOPPEN (Köppen climate codes), CARAVAN_AREA, and other derived variables.
- Data integrity fields: FREE_TEXT comments, DATA_PERMISSION (Open / Restricted / Unavailable), and LEVEL (1 or 2).

## 7.2 Hydrobelt Information
- Codes and descriptions for belt classifications (e.g., Greenland - Ice, BOR - Boreal, NML - Northern Mid Latitude, NDR - Northern Dry, NST - Northern Sub Tropical, EQT - Equatorial, SST - Southern Sub Tropical, SDR - Southern Dry, SML - Southern Mid Latitude).

## 7.3 Koppen Information
- Detailed Köppen climate classifications mapped to codes (e.g., Af, Am, Aw, BWh, BWk, BSh, BSk, Csa, Csb, Csc, etc.), including variations such as Cwa/Cwb/Cwc, Cfa/Cfb, Dsa/Dsb/Dsc/Dsd, Dwa/Dwb/Dwc/Dwd, Dfa/Dfb/Dfc/Dfd, ET, EF, and related distinctions (temperate, arid, tropical, polar, etc.).