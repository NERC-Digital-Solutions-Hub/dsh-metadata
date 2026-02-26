# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Report of initial results validating a new PTFE membrane for ALPHA® samplers used to measure NH3 in air.
- Field work conducted at four UK UKEAP network sites; sampling and analysis coordinated by UKCEH Edinburgh, AFBI Hillsborough, and Ricardo AEA Chilbolton.
- Samplers exposed monthly, with analysis performed at CEH Edinburgh.

## Methodology and Data collection
- UKCEH ALPHA® sampler design:
  - Citric acid-coated filter captures NH3; protected by a white PTFE membrane during exposure.
  - Membrane oriented facing downwards; samplers mounted at ~1.5 m above ground.
  - Replicates used per site to improve reliability.
- Exposure and analysis workflow:
  - Samplers exposed in monthly cycles; analysis involves extracting filters in deionised water and analyzing NH4+ with SEAL AA3 colorimetry.
  - NH3 concentration in air derived from ammonium concentration using a site-specific uptake rate for the new membrane (0.0041741 m3 hr-1) and exposure duration.
- Data handling:
  - The final dataset NH3_New_Membrane_2022.csv contains accepted data values with appropriate flags.
  - Site identifiers and spatial coordinates provided; data capture and metadata are recorded.

## Data structure and fields
- Dataset: NH3_New_Membrane_2022.csv
- Each row represents one month of data for a single site; columns include:
  - Site id and Site name
  - network_id (NM)
  - parameter_id (alpha_NH3_g)
  - measurement start/end dates and times
  - measurement (NH3 concentration in µg NH3 m-3)
  - less than flag (detection limit indicator)
  - verification id (1 = Verified; 2 = Preliminary verified; 3 = Not verified)
  - unit_id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid; -1 = not valid)
  - EMEP flag code and related interpretation
  - Month-Year
  - Comments
- Data content notes:
  - All concentration data are monthly averages for the exposure period.
  - Data are flagged to indicate concerns or quality decisions (e.g., below detection, data capture issues, validation status).

## Data quality assurance and validation
- Quality rules applied to raw data prior to final acceptance:
  - Coefficient of variation (CV) of replicates < 15%: considered valid; if >15%, replicates may be discarded; otherwise data may be flagged 103.
  - Values above calibration range can be considered valid if reruns are not possible due to instrument issues or sample loss.
  - Missing data are indicated with -9999 in the field (or missing date/time metadata prevents concentration calculation).
- Data flags and status:
  - Data capture and validity flags (EMEP/EU flags) accompany each observation to indicate data lineage, quality issues, or special conditions (e.g., contamination, detection limits, nearby activity, sampling anomalies).

## Flags, interpretation, and metadata
- EMEP flags provide context for data status, including:
  - Missing data or data capture issues
  - Values below detection or quantification limits
  - Validity remarks related to contamination, sampling conditions, or environmental interference
  - Other contextual notes (e.g., nearby agricultural activity, industrial contamination, unusual sampling conditions)
- The dataset includes a mapping of flags to reasons and validity status to support consistent interpretation across data portals and analyses.

## Dataset contents and metadata references
- The final dataset contains accepted NH3 measurements with associated quality flags.
- The dataset contents include:
  - A row per month per site
  - Site names and spatial identifiers detailed in accompanying pages
  - Column-level descriptions for traceability and reuse
- Site-specific details and spatial information are provided (coordinates, sampling height, collocation identifiers) to enable geospatial linking and reproducibility.

## Site information
- Sites and coordinates:
  - Edinburgh uptake rate OTC: latitude 55.863150, longitude -3.209845; height 1.5 m; collocated with UKA00128
  - Auch (Edinburgh uptake rate Auch): latitude 55.792160, longitude -3.242900; height 1.5 m; collocated with UKA00451
  - Hills (Edinburgh uptake rate Hills): latitude 54.452500, longitude -6.083340; height 1.5 m; collocated with UKA00293
  - Chilbolton (Edinburgh uptake rate Chilbolton): latitude 51.149617, longitude -1.438228; height 1.5 m; collocated with UKA00614
- Start dates indicate ongoing monitoring from early 2020 and 2021, with ongoing end dates.

## Data governance implications for Data Stewards
- Enables robust data governance through:
  - Clear lineage: documented sampler method, analysis procedure, and uptake rate for the new membrane
  - Consistent data structure: standardized fields and units across observations
  - Transparent quality controls: explicit CV-based validation, calibration-range handling, and missing-data rules
  - Rich metadata: detailed site information, spatial identifiers, and flag semantics (including EMEP and data-status codes)
  - Facilitation of data sharing and discovery via portals and catalogues, with explicit data flags to indicate data quality and limitations

## Challenges and considerations for data stewardship
- Incomplete user needs: balance between detailed metadata and user-friendly summaries for data discoverability
- Timeliness: ensuring timely upload/update of monthly data and maintenance of site status (ongoing end dates)
- Metadata completeness: maintaining comprehensive site and method metadata to support reuse
- Interoperability: harmonizing with multiple data systems and formats across networks and portals
- Handling large datasets: ongoing accumulation from four sites may require scalable storage and governance workflows

## Practical takeaways for users and data managers
- When using NH3_New_Membrane_2022.csv, refer to:
  - The measurement start/end dates and times for exposure periods
  - The CV-based validity (103) and EMEP/validity flags for data quality context
  - Detection-limit indicators and the -9999 missing data marker
  - Site coordinates and collocation details for spatial analyses
- Data stewards should maintain and communicate the data provenance, QA rules, and flag interpretations to support reliable reuse and integration into broader ambient ammonia datasets.