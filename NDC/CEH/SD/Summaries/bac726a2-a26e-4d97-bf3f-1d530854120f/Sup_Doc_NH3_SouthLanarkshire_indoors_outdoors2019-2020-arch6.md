# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two sites in a rural area of South Lanarkshire: one inside the hall of a dwelling, and one outside in the garden.
- Analysis conducted by the Centre for Ecology and Hydrology Edinburgh using CEH ALPHA® passive samplers to measure ammonia (NH3) in air.
- Samplers are exposed monthly, at the beginning of each month.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv, containing monthly NH3 concentration data per site with quality flags.

## Sampling Method (CEH ALPHA® Sampler)
- Passive sampler using a citric acid coated filter to capture ammonia; protected by a white PTFE membrane.
- Membrane oriented downwards during exposure; samplers mounted ~1.5 m above ground on poles or shelters.
- Replicates used to improve reliability of air concentration estimates.
- Protective plastic containers used for sampler storage.
- Two sites sampled indoors and outdoors; both share the same general setup.

## Analysis
- Exposed samplers are extracted into deionised water.
- Extracts analyzed by SEAL AA3, which uses colourimetry to determine ammonium concentration.
- Ammonia concentration in air calculated from ammonium concentration using a fixed uptake rate (0.003241315 m3 h-1) and exposure duration.

## Data Quality and Flagging
- Data flagged to indicate concerns (details on page 4).
- Quality rules applied:
  - Coefficient of Variation (CV) of replicates < 15%: results considered valid; if CV > 15%, replicates reviewed; if retained, data flagged as valid (103).
  - Values above calibration range but deemed valid: reported when rerun isn’t possible due to instrument failure or sample loss.
  - Missing data or metadata: indicated with -9999; if date/time metadata missing, concentration cannot be calculated.
- Final dataset contains accepted values with appropriate flags. Site names and spacing details are provided on dedicated pages.
- Dataset structure includes a data flag for each row, alongside other metadata.

## Dataset Structure
- File: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv.
- Each row represents one month of data for a single site.
- Columns include:
  - Site name (station name), unique site identifier, network_id (RSW)
  - Parameter_id (type: alpha_NH3_g)
  - Measurement start/end date and time (exposure period)
  - Measured ammonia concentration (units: µg NH3 m-3)
  - Less than flag (detection limit)
  - Verification id (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code and related flags (data status, calibration, contamination, etc.)
  - Month-Year (exposure period)

## EMEP Flags (examples)
- 999: Data Capture = 0; Validity = -1; Reasoning = Missing measurement.
- 781, 780: Validity = 1; Reasoning = Value below detection limit or below quantification/limit.
- 653-652-651: Various reasons (sampling period characteristics or nearby influences).
- 259-260, 559-557, 555, etc.: Flags indicating contamination, nearby activities, or other local influences; many are considered valid but carry specific reasoning.
- 103: CV of replicates >15%; still treated as valid measurement in final dataset.

## Site Information
- Inside (hall of dwelling):
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet above ground: 1.5 m
  - Further details: Located in hall of dwelling
- Outside (garden of dwelling):
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet above ground: 1.5 m
  - Further details: Located in garden of dwelling

## Notes for Data Use
- Data aim to enable end users to self-serve analyses through dashboards or pivot tables; outputs may be promoted and iterated with user feedback.
- Outputs can support broader data use including potential advocacy for improved data collection and sharing.
- The dataset provides explicit structure for traceability, including site identifiers, exposure periods, flags, and quality indicators to support reliable interpretation.