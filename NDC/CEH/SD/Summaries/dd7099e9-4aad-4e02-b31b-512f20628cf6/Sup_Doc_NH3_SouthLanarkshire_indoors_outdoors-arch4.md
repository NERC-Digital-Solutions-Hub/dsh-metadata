# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two rural sites in South Lanarkshire: one indoors (hall of a dwelling) and one outdoors (garden), with the garden backing onto grassland on a dairy farm.
- Ammonia (NH3) air concentrations measured using CEH ALPHA® passive samplers; analysis conducted by Centre for Ecology and Hydrology Edinburgh.
- Sampling conducted in monthly cycles; samplers exposed at approximately 1.5 m above ground; replicate samplers used for reliability.

## Methods and Data Processing
- CEH ALPHA® sampler details:
  - Passive sampler with a citric acid coated filter to capture NH3; PTFE membrane protects the filter; membrane oriented downwards during exposure.
  - Replicates deployed on shelters on poles to improve reliability.
  - Samplers protected during transport; site operator duties performed by dwelling owner.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - NH3 quantified by SEAL AA3 using colourimetry; results converted to average NH3 concentration in air using a fixed uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Data quality and flags:
  - Raw data screened with quality rules; data flagged for concerns and detailed on page 4 (not provided here).
  - Key quality checks:
    - Coefficient of variation (CV) of replicates < 15% indicates valid representation (flag 103 if met).
    - Data outside calibration range may be valid if instrument issues prevented rerun.
    - Missing data or metadata denoted by -9999.
  - Final dataset: NH3_SouthLanarkshire_indoors_outdoors.csv containing accepted values with appropriate flags; each row represents one month of data for a single site; concentration units are µg NH3 m-3.

## Dataset Structure and Content
- Dataset title: NH3_SouthLanarkshire_indoors_outdoors.csv.
- Columns (examples):
  - Site name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g).
  - Measurement period: start date/time and end date/time.
  - Ammonia concentration: value in µg NH3 m-3.
  - Flags: less than detection limit, verification status, unit id (µg NH3 m-3), data capture percentage, validity_id, EMEP code.
  - Month-Year for the measurement period.
- Data status codes (EMEP flags) are used to document data capture quality, detection limits, and suitability for inclusion; extensive flag set provided to support traceability and data quality assessment.

## Site Information
- Indoor site: located in the hall of a dwelling; start date 01/01/17; end date ongoing; latitude 55.64072, longitude 3.59705; air inlet height 1.5 m.
- Outdoor site: located in the garden of the dwelling; start date 01/01/17; end date ongoing; identical coordinates; air inlet height 1.5 m.

## Data Governance and Use
- Quality and metadata are explicitly considered; data have been flagged to indicate concerns and ensure transparency.
- The final dataset aggregates validated measurements with site identifiers and geospatial context, enabling integration into broader air quality assessments.
- Documentation references detailed data contents, site identifiers, and a structured flag system to support data discoverability and reuse across networks or partners.

## Implications for Data Leaders
- Demonstrates a structured approach to data collection, QA, and documentation for environmental monitoring data.
- Highlights the importance of replicates, clear metadata (site, coordinates, measurement period, units), and a comprehensive flag system for data quality.
- Offers a ready-to-integrate time-series dataset for broader analytical workflows, with explicit provenance and quality indicators to support governance and cross-site collaboration.