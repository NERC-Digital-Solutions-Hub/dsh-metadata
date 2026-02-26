# Overview of data

- Purpose and scope
  - Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of C, N, and P.
  - Field data collected to characterize in situ flow velocity in rivers within the Hampshire Avon catchment; intended to support understanding of freshwater ecosystem processes.

- Data contents and structure
  - 39 CSV data files accompanying this overview, named Flow_<SiteCode>_<Season>_<Location>.CSV.
  - Site codes and locations:
    - CE1: River Ebble (lat 51.027499 N, lon -1.9217089 E)
    - GA2: River Avon (lat 51.318289 N, lon -1.8600020 E)
    - GN1: River Nadder (lat 51.043849 N, lon -2.1118158 E)
    - CW2: River Wylye (lat 51.142475 N, lon -2.2033140 E)
    - AS1 (AP): tributary of River Sem (lat 51.055413 N, lon -2.1568407 E)
    - AS (AS2): River Sem (lat 51.045826 N, lon -2.1104425 E)
  - For each transect, the stream is gridded:
    - 0.25 m segments (stream width < 3 m) or 0.5 m segments (width > 3 m)
    - Flow measured for each segment in 0.1 m depth steps from the riverbed; if 0.1 m steps not possible near surface, 0.05 m steps used
  - NaN values indicate data not collected (e.g., between grid lines or readings too close to banks or water surface)
  - Column headers include:
    - Distance (m) from the stream bank
    - Water depth (m) at each distance
    - Notes (vegetation, bed features, proximity to aquatic eddy covariance)
    - Date of measurements (MM/DD/YYYY)
  - Depth row indicates measurement depths (variables may vary by site/campaign)
  - Data values in subsequent lines: average flow in m/s over 15 s of continuous measurements (n = 15)

- Instrumentation and data collection methods
  - In situ flow velocity measured with Model 801 electromagnetic flow meter by Valeport
  - Instrument serviced throughout project at Lancaster University
  - Detailed instrument information available from Valeport (web link provided in document)
  - Campaigns used to capture seasonal variability across multiple sites

- Campaigns and coverage
  - Four field campaigns:
    - Spring 2013: 23/04 – 09/05/2013
    - Summer 2013: 31/07 – 16/08/2013
    - Autumn 2013: 29/10 – 11/11/2013
    - Winter 2014: 28/01 – 09/02/2014
  - Not all sites measured in every campaign:
    - AP (AS1) not sampled in Summer 2013 due to insufficient flow
    - CE1 and GA2 not sampled in Winter 2014 due to flooding

- File naming conventions and site identifiers
  - Flow_<SiteCode>_<Season>_<Location>.CSV
  - SiteCode mappings and corresponding geographic coordinates provided to aid discovery and mapping
  - Location field indicates upstream or downstream position within the studied reach

- Data quality, limitations, and governance notes
  - Gaps indicated by NaN values (data not collected or not available)
  - Depth and depth-level structure may vary by site and campaign, requiring site-specific interpretation
  - Some seasons/sites have incomplete data due to logistical or environmental reasons (e.g., flooding, insufficient flow)
  - Documentation includes instrument details and measurement protocol, enabling assessment of comparability across sites and campaigns

- Documentation, provenance, and access
  - Dataset described as part of a published project with clear attribution to contributing researchers
  - Instrumentation, measurement procedures, and site coordinates are documented to support reuse
  - Last described access and last update reference in the document (historical context provided)

- Stewardship and recommended actions for data governance
  - Ensure standardized metadata across all 39 files (data dictionary, units, site metadata, coordinate reference, and date formats)
  - Attach a clear data license and versioning to support reuse and proper attribution
  - Create a central metadata record or data dictionary to document site-specific schema variations (e.g., depth levels per site)
  - Preserve the naming convention and site codes to maintain traceability; include a crosswalk table for site codes and coordinates
  - Capture data quality notes, including reasons for missing data (e.g., flooding, insufficient flow) to inform users about data limitations
  - Consider publishing a data product or DOI to improve discoverability and long-term preservation
  - Store and share data in a repository that supports provenance, updates, and discoverability for researchers and data users

- Potential uses for data stewards
  - Support discoverability and reuse by researchers studying riverine flow, stream metabolism, and lateral exchange processes
  - Facilitate interoperability by applying consistent metadata standards and improving data documentation
  - Monitor and plan data updates or remediations (e.g., bridging gaps, harmonizing depth measurements) to enhance dataset usability over time