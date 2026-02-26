# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Overview
- Initial results from a study to determine the uptake rate for ALPHA® samplers prepared and analysed at UKCEH Edinburgh, for the UK and similar climates.
- Local site operator duties carried out by UKCEH, AFBI (Hillsborough), and Ricardo AEA; analysis by CEH Edinburgh.
- Samplers exposed in monthly cycles at the start of each month to measure ambient NH3 concentrations.

## Methodology
- UKCEH ALPHA® passive sampler: citric acid coated filter captures NH3; protected by a white PTFE membrane; membrane facing downwards during exposure.
- Deployment: replicate samplers attached to shelters on poles at ~1.5 m above ground; replicates improve reliability.
- Analysis: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 (colorimetric ammonium detection); ammonium concentration converted to ambient NH3 concentration using a known uptake rate (0.0038422 m3 h⁻1) and exposure duration.
- Data handling: raw data flagged for quality issues; final dataset is submissions_ED_UR_NH3_2022.csv with accepted values and appropriate flags.
- Units: NH3 concentration reported as micrograms per cubic metre (µg NH3 m⁻3); monthly exposure period values are used.

## Data handling and quality assurance
- Quality assessment rules:
  - Coefficient of variation (CV) < 15% across replicates indicates valid and representative results (flag 103 if accepted).
  - Values beyond calibration range may be reported if instrument issues prevented rerun; still considered valid.
  - Missing data or metadata represented by -9999 in the field.
- Flags and statuses:
  - Data capture: 999 indicates missing capture; 0 or 1 indicates capture present/absent.
  - Validity: 1 = valid; -1 = not valid.
  - Verification: 3 = Not verified; 2 = Preliminary verified; 1 = Verified.
  - EMEP and data-status codes capture additional data quality and provenance information.
- Data contents and structure:
  - Final dataset: submissions_ED_UR_NH3_2022.csv containing accepted data values, with appropriate flags.
  - Each row represents one month of data for a single site; columns include site name, start/end dates, exposure period NH3 concentration, and a data flag.

## Data structure and content
- Core fields in the dataset:
  - Site id, Site name, network_id (ED_UR), parameter_id (alpha_NH3_g)
  - Measurement start date/time and end date/time (exposure window)
  - Measurement (NH3 concentration, µg NH3 m-3)
  - Less than flag (1 if below detection limit 0.03 µg/ m3; 0 otherwise)
  - Verification id (1–3)
  - Unit id (24 = µg NH3 m-3)
  - Data capture (percentage)
  - Validity_id (1 = valid; -1 = not valid)
  - EMEP code and related data-status flags
  - Month-Year and Comments
- Notes:
  - The dataset is organized by month per site; site names and spatial identifiers are listed in the documentation.
  - Data capture and validity flags help identify data gaps and questionable measurements.

## Data quality flags and codes (highlights)
- 999: Data capture = 0; missing measurement or data.
- 781: Value below detection limit; considered valid.
- 780: Value below detection or quantification limit; considered valid; estimated value.
- 103: CV of replicate ALPHA samplers > 15%; measurement still considered valid.
- 460, 647, 646, 645, 599, 593, 591, 559, 558, 557, 556, 555, 553, 532, etc.: various contextual reasons for data validity or invalidity (e.g., contamination, nearby activity, anomalous conditions, missing or unreliable data).
- 653, 652, 651: sampling period adjustments (shorter/longer than normal) with observed values reported.
- -9999: missing data or missing date/time metadata preventing calculation.

## Site information
- Edinburgh uptake rate OTC site details (start: 01/03/2020; ongoing):
  - Edinburgh uptake rate OTC; Latitude 55.863150; Longitude -3.209845; Inlet height 1.5 m; Collocated with UKA00128.
  - Auch site; Latitude 55.792160; Longitude -3.242900; Inlet height 1.5 m; Collocated with UKA00451.
  - Hills site; Latitude 54.452500; Longitude -6.083340; Inlet height 1.5 m; Collocated with UKA00293.
  - Chilbolton site; Latitude 51.149617; Longitude -1.438228; Inlet height 1.5 m; Collocated with UKA00614.
- These sites form four UK Eutrophying and Acidifying Pollutants (UKEAP) network locations used to derive uptake rates and ambient NH3 concentrations.

## Governance, stewardship implications for Data Stewards
- Data provenance and responsibility:
  - Study involves multiple organisations (UKCEH, AFBI, Ricardo AEA) with data collection, processing, and analysis performed by CEH Edinburgh.
  - Clear delineation of responsibilities for sampling, analysis, and data curation supports governance and accountability.
- Standards and metadata:
  - Standardized sampler method, exposure protocol, analysis technique, and uptake-rate calculation.
  - Comprehensive metadata available via the dataset structure and accompanying documentation (site details, coordinates, sampling periods, QA flags, and data-status codes).
- Data quality and usability:
  - Explicit QA criteria (CV < 15%, handling of calibration-range issues, and missing data conventions) support data reliability.
  - Flags capture reasons for data exclusion or potential issues, aiding discoverability and reuse.
- Data sharing and updates:
  - Final dataset is clearly named and flagged (submissions_ED_UR_NH3_2022.csv) with accepted data values and provenance metadata.
  - The system accounts for data updates or re-submissions via verification and EMEP flags, enabling versioning and traceability.
- Practical considerations for data governance:
  - Ensure access to the final dataset and any transformation scripts used to convert raw measurements to ambient NH3 concentrations.
  - Maintain documentation of site-specific contexts (collocations, site identifiers, and measurement periods) for accurate re-use.
  - Monitor and update data capture and validity flags as new data are submitted or re-submitted.

## Summary for action
- For data stewardship, the document provides a complete data lifecycle: from collection with replicates, through QA with explicit criteria and flags, to a final, well-documented dataset ready for dissemination and subsequent use in atmospheric ammonia studies.
- The site-level metadata and standardized data schema facilitate discovery, interoperability, and traceability across collaborating organisations.