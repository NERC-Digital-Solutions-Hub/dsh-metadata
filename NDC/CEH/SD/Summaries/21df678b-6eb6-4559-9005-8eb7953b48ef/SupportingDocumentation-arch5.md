# Groundwater level information for 10 locations within the Gandak River Basin, in Bihar, India

## Overview
- Dataset presents groundwater level information for 10 locations in the Gandak River Basin, Bihar, India.
- Collected under the CHANSE (Coupled Human And Natural Systems Environment) project.
- Recording period: April 2017 to February 2019.
- Measurements made with Troll automatic groundwater level loggers at 15-minute intervals.
- All data corrected to local barometric pressure using a Troll barometer.

## Data structure and variables
- DateTime: date and time of recording.
- Temp: water temperature.
- mbgl: depth to water level (meters below ground level) as logged.
- man_mbgl: manually measured depth to groundwater level (measured with a dip meter).
- PT: pressure transducer.
- Baro: barometer data.
- Data quality note: missing values are recorded as blanks.

## Site locations and metadata
- 10 sites with associated metadata (location, coordinates, depths, installation and last download dates, and recording span).
  - Examples of sites include Chinta Manpur, Bagaha 1, Bagaha, Bagaha 3, Bettiah 1–3, Lalganj Basanta, Bettia4, Chalabhar.
  - For each site: 
    - longitude and latitude (decimal or formatted values present but with some formatting inconsistencies in the table).
    - depth_to_base_mbgl: logger-reported base depth to groundwater (m bgl).
    - depth_to_water_level_on_installation_mbgl: depth to water level at installation (m bgl).
    - date_installed: installation date.
    - date_last_download: last data download date.
    - months_of_record: duration of recording (values such as 10.5 are shown).
- Note on data quality: the site table contains formatting inconsistencies and corrupted values in places (e.g., mixed numbers and placeholders like 88889/94444 in coordinates, inconsistent date formats). This indicates a need for cleaning and standardization before sharing or analysis.

## Data quality and governance considerations
- Corrections: data corrected to local barometric pressure; ensures consistency in water level interpretation.
- Gaps and limitations: some metadata entries appear inconsistent or incomplete; missing values are blank.
- Timeframe: data spans from April 2017 to February 2019; last download dates around early 2019.
- Interoperability concerns: inconsistent coordinate formats and site identifiers require standardization for reliable discovery and reuse.

## Data access, sharing, and use
- The dataset is intended to be uploaded to relevant portals and catalogued, with clear data holdings and sharing policies.
- Metadata and provenance (project CHANSE, instrumentation, correction method) should accompany the data to aid discoverability and reuse.
- Potential need for data quality flags and versioning to support transparent reuse.

## Recommendations for data stewardship
- Standardize site identifiers and metadata fields (e.g., site_id, coordinates with consistent CRS, clearly separated installation and last_download dates).
- Clean and validate the site table to resolve formatting issues and remove ambiguous values (e.g., 88889/94444 placeholders).
- Provide a complete data dictionary and metadata file with units, measurement methods, and QA/QC procedures.
- Implement explicit data quality flags (e.g., good, suspect, missing) for each observation.
- Establish a clear update and maintenance plan to handle new data and corrections, including versioning.
- Ensure interoperability guidelines are followed to facilitate cross-dataset discovery and integration.