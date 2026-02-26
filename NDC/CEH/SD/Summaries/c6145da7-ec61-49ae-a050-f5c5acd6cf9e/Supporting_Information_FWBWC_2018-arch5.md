# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

## Overview
- Dataset documenting atmospheric ammonia concentrations from CEH ALPHA passive samplers at five moss sites as part of the LIFE project under Site Nitrogen Action Plan (SNAP). 
- Local site operator duties by Natural England (NE); analysis by Centre for Ecology and Hydrology (CEH) Lancaster; data processing by CEH Edinburgh.
- Samplers exposed monthly; data processed to produce annual 2018 measurements dataset.

## Sampling Method and Analysis
- CEH ALPHA® passive samplers with citric acid coated filter to capture NH3; white PTFE membrane protects the filter.
- Samplers exposed at about 1.5 m above ground, in replicate to improve reliability; mounted on shelters.
- Analysis: exposed samplers extracted into deionised water and measured with SEAL AA3 colorimetry (ammonium detection).
- Concentration in air calculated using a known uptake rate (0.0028986 m3 h-1) and exposure duration.
- Final dataset named: FWBWC_ammonia_measurements_2018.csv.
- Data columns include site name, unique site identifier, network_id, parameter_id, exposure window, concentration (µg NH3 m-3), and related flags.

## Data Processing and Quality Assurance
- Raw data quality checks applied:
  - CV of replicates < 15% to validate replicates; if >15%, evaluation of discards; valid data flagged (103).
  - Missing samplers assigned -9999.00 and marked invalid (-1).
  - Sampler duration deviations (longer/shorter than normal) flagged.
  - Local contamination or deviations recorded; non-representative results discarded; reported as average of remaining results.
- Data status and flags:
  - Each row includes a data flag, verification id, unit id, data capture percentage, and validity id.
  - EMEP flagging codes accompany data status (see below for flag meanings).
- Site information and dataset contents are documented (site names listed with spatial identifiers on pages referenced in the source).

## Data Contents and Metadata
- Each row corresponds to one month’s data for a single site (beginning of month to end of month).
- Columns (representative): 
  - site name, unique site identifier, network_id, parameter_id,
  - measurement start date/time, measurement end date/time,
  - ammonia concentration (µg NH3 m-3),
  - less than detection limit flag (1 if < DL, 0 otherwise),
  - verification id (Not Verified / Preliminary Verified / Verified),
  - unit id (e.g., 24 = µg NH3 m-3),
  - data capture (%),
  - validity_id (1 = valid, -1 = not valid),
  - EMEP code (data status and flags),
  - Month-Year (mmm-yy).
- Units: micrograms of ammonia per cubic metre of air (µg NH3 m-3).

## Data Flags and Provenance
- EMEP Flags provide a composite data status and quality rationale (e.g., contamination indicators, detection/quantification considerations, sampling period representativeness, CV checks, etc.).
- Examples of flagging rationale include contamination from local sources, below detection limit, estimated values, sampling period deviations, or validity confirmations.
- Flagging supports data discoverability and appropriate use in analyses and reporting (e.g., UK-AIR/E ME P context).

## Site Information
- MM01: start 01/07/2018; End date Ongoing; Latitude 52.925, Longitude -2.777; Inlet height 1.5 m.
- MM02: start 01/07/2018; End date Ongoing; Latitude 52.932, Longitude -2.751; Inlet height 1.5 m.
- MM03: start 01/07/2018; End date Ongoing; Latitude 52.924, Longitude -2.758; Inlet height 1.5 m.

## Data Governance and Usage
- Responsibilities span NE (operators) and CEH (analysis and data processing); emphasis on data governance, metadata completeness, and transparent QA/QA reporting.
- Dataset supports discoverability and reuse by researchers and managers assessing atmospheric ammonia at the sites; includes detailed metadata, quality flags, and provenance to aid appropriate interpretation and update workflows.