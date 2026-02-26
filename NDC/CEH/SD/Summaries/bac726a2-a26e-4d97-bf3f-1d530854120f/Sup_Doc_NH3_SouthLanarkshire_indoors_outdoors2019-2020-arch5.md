# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Two rural sites in South Lanarkshire: one indoors (hall of a dwelling) and one outdoors (garden area backing onto grassland of a dairy farm).
- Site operator duties performed by dwelling owner; analysis conducted by Centre for Ecology and Hydrology Edinburgh (CEH).
- Purpose: measure ammonia concentrations in air using CEH ALPHA passive samplers; samplers exposed in monthly cycles at the start of each month.
- Data are compiled into a final dataset (NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv) with quality flags and metadata.

## Sampling Method
- Instrument: CEH ALPHA® passive samplers with citric acid coated filter to capture NH3; protected by a white PTFE membrane; exposed with membrane end facing downwards.
- Deployment: replicates attached to a shelter on a pole at ~1.5 m above ground.
- Analysis workflow: exposed samplers extracted into deionised water, analyzed by SEAL AA3 using colorimetry to determine ammonium concentration; conversion to average NH3 concentration using uptake rate 0.003241315 m3/h and exposure duration.
- Replication: replicates used to improve reliability of air concentration estimates.

## Data Handling & Quality
- Data flagged to highlight concerns; site operator and lab notes inform any data considerations (details referenced on page 4 of the document).
- Quality assessment rules:
  - CV of replicates < 15%: considered valid; data flagged as 103.
  - CV > 15%: results evaluated; if deemed representative, data remain valid and flagged accordingly.
  - Data missing or meta-data missing: indicated by -9999 in the data field.
  - Some data exceed calibration range but are considered valid due to instrument limitations or不可 rerun due to issues.
- Dataset contents: final NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv contains accepted data values with appropriate flags; unit is micrograms of NH3 per cubic meter (µg NH3 m-3).

## Data Format & Metadata
- Data columns (summary): site name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g), measurement start date/time, measurement end date/time, ammonia concentration (µg NH3 m-3), less than detection flag, verification id (Not verified / Preliminary verified / Verified), unit id (24 = µg NH3 m-3), data capture percentage, validity_id (valid / not valid), EMEP code (data status and flags), and Month-Year (mmm-yy).
- EMEP flags provide details on data capture and validity, with coded reasons (e.g., below detection limit, contamination, sampling period representativeness, nearby agricultural activity, etc.).
- Site information:
  - Inside: start 01/01/17, end ongoing; coordinates 55.64072, -3.59705; air intake height 1.5 m; location: hall of dwelling.
  - Outside: start 01/01/17, end ongoing; coordinates 55.64072, -3.59705; air intake height 1.5 m; location: garden of dwelling.

## Data Access & Storage
- Primary dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv, containing per-month measurements for each site with associated flags and metadata.
- Documentation references page numbers for site names, spatial identifiers, and detailed field definitions (pages 3–5), indicating structured metadata and field-level explanations.

## Limitations & Considerations for Use
- Use of flags requires interpretation to assess data usability (e.g., detection limits, CV of replicates, validity codes, and EMEP flag reasons).
- Some data may be flagged as not verified or preliminarily verified; users should rely on the Verifications field for data confidence.
- Potential data quality considerations include calibration-range exceedances, data gaps, and external contamination indicators necessitating careful data handling and provenance checks.

## Governance & Stewardship Implications
- Data provenance is preserved through replication, standardized measurement protocols, and explicit quality control rules (CV thresholds, calibration considerations, missing data handling).
- Rich metadata and EMEP flags support interoperability, traceability, and appropriate reuse in air quality assessments and regulatory reporting.
- Clear data formats, units, and detailed field definitions facilitate discoverability, consistency across datasets, and appropriate updates to the data catalog.