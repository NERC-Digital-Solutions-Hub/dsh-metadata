# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Report on initial results validating a new PTFE membrane for ALPHA® passive samplers used to measure atmospheric ammonia (NH3).
- Study conducted by UKCEH Edinburgh with operator support from AFBI (Hillsborough) and Ricardo AEA (Chilbolton); analysis performed by CEH Edinburgh.
- Samplers deployed monthly at four UK sites, with exposure cycles beginning at the start of each month.
- Final data compiled in NH3_New_Membrane_2022.csv, including quality flags and site metadata.

## Sampling and Analysis Method
- UKCEH ALPHA® sampler:
  - Citric acid-coated filter captures NH3; protected by a white PTFE membrane facing downwards; sealed when not exposed.
  - Replicate samplers used on a shelter mounted ~1.5 m above ground to improve reliability.
  - Samples extracted with deionised water and analyzed by SEAL AA3 using colorimetry to determine ammonium concentration.
  - Ambient NH3 concentration calculated from ammonium results using sampler uptake rate with the new membrane: 0.0041741 m3 h-1.
- Sites and timeframe:
  - Four locations in the UKEAP network; site details and coordinates provided in the dataset metadata.
  - Exposure periods run monthly, with start and end dates/times recorded.

## Data Quality and Validation Rules
- Quality assessment applied to raw data:
  - Coefficient of variation (CV) of replicates: CV < 15% considered valid; CV > 15% triggers evaluation for possible discard; such data flagged with 103.
  - Measurements above calibration range: still considered valid when rerun/dilution not possible due to instrument failure; flagged as valid.
  - Missing data: represented by -9999 in concentration or date/time fields.
- Data flags and flags interpretation:
  - A comprehensive set of EMEP flags used to describe data capture, validity, and data issues (e.g., CV issues, detection limits, contamination, sampling anomalies, nearby activities).
  - Flags help determine data usability and context for each monthly measurement.

## Dataset Structure
- Final dataset: NH3_New_Membrane_2022.csv
- Key columns (illustrative):
  - Site identifier and site name
  - network_id (NM)
  - parameter_id (alpha_NH3_g)
  - Measurement start date/time and end date/time
  - Ammonia concentration (units: µg NH3 m-3)
  - Data capture percentage and validity flag
  - Data status code and EMEP flag
  - Month-Year and optional comments
- Data status and flags provide traceability for each monthly measurement and its associated quality considerations.

## Site Information
- Edinburgh uptake rate OTC (start 01/03/2020; ongoing): coordinates 55.863150, -3.209845; inlet height 1.5 m.
- Auch uptake rate (start 01/03/2020; ongoing): coordinates 55.792160, -3.242900; inlet height 1.5 m.
- Hills uptake rate (start 01/03/2020; ongoing): coordinates 54.452500, -6.083340; inlet height 1.5 m.
- Chilbolton uptake rate (start 01/01/2021; ongoing): coordinates 51.149617, -1.438228; inlet height 1.5 m.
- All sites collocated with specified UKEAP references; further details provided in dataset metadata.