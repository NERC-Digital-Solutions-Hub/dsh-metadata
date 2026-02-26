# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- Two measurement sites in a rural area of South Lanarkshire: inside the hall of a dwelling and outside in the garden adjacent to grassland on a large dairy farm.
- Data collected in 2022; analysis by Centre for Ecology and Hydrology Edinburgh (CEH).
- Use CEH ALPHA® passive samplers to measure NH3 concentrations; samplers exposed in monthly cycles at the start of each month.
- Replicate samplers used to improve reliability; data are flagged for quality concerns.

## Methods and data processing (GIS-relevant details)
- CEH ALPHA® sampler setup:
  - Citric acid coated filter with a protective white PTFE membrane, oriented downwards during exposure.
  - Samplers mounted on a shelter on a pole at ~1.5 m above ground.
  - Replicates deployed per site; samplers protected in plastic containers.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - NH3 quantified using SEAL AA3 with colorimetry, converting ammonium concentration to ambient NH3 using a uptake rate of 0.0038422 m3/h and exposure duration.
- Data quality and flags:
  - Raw data screened against QA rules; data flagged for concerns (see dataset metadata).

## Dataset and schema (structure for GIS use)
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2022.csv
- Content: monthly data for a single site per row, with site-specific and temporal attributes.
- Key columns (examples):
  - Station name / unique site identifier
  - network_id (RSW)
  - parameter_id (alpha_NH3_g)
  - measurement start date/time (exposure start)
  - measurement end date/time (exposure end)
  - ammonia concentration (units: µg NH3 m-3)
  - less than flag (indicates below detection limit of 0.03)
  - verification_id (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
  - unit_id (24 = µg NH3 m-3)
  - Data capture (percent)
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP data status code (A-J; includes verification status, data issues, and EMEP flags)
- Data quality flags (examples of codes described in the metadata):
  - 999: Data capture 0; invalid due to missing measurement
  - 781/780: Valid; below detection or between detection ranges; listed as valid
  - 653/652/651: Valid; sampling period anomalies nearby (construction, agricultural activity, or traffic)
  - 103: CV of replicates >15% but still considered valid with notes
- Missing data indicated by -9999 in the measurement field.
- Spatial identifiers:
  - Location coordinates provided (Latitude ~55.64072, Longitude ~3.59705) for both inside and outside, with air inlet height 1.5 m.
  - Inside site: located in hall of dwelling; Outside site: located in garden of dwelling.

## Site information
- Inside:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: -3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in hall of dwelling
- Outside:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: -3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in garden of dwelling

## Notes for GIS stakeholders
- Dataset supports map-based visualization of indoor vs. outdoor NH3 concentrations over time, with QA flags enabling filtering of uncertain data.
- Spatial alignment relies on provided coordinates and consistent site naming to join with other geographic layers (e.g., land use from the nearby dairy farm and grassland).
- Data provenance: measurements aligned with UK-AIR/EMEP flag conventions to support regulatory or policy-oriented analyses.