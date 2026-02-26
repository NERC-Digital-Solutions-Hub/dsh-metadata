# Sup_Doc_NH3_UWT_Cuilcagh

## Overview
- Data describe ammonia (NH3) measurements in the Cuilcagh area (Ireland and Northern Ireland) to assess effects on vegetation.
- Data collection managed by Ulster Wildlife Trust; analysis by UK Centre for Ecology and Hydrology (Edinburgh).

## Sampling and Analysis Methods
- Instrument: UK CEH ALPHA® passive samplers with citric acid coated filters and a PTFE membrane.
- Deployment: replicate samplers (triplicate) mounted on shelters at ~1.5 m height; exposed monthly at the start of each month.
- Analysis: exposed samplers extracted in deionised water; NH3 concentration determined by SEAL AA3 colorimetry (ammonium).
- Calculation: convert to average NH3 concentration in air using uptake rate (0.003241315 m3 h-1), exposure duration, and lab blanks.
- Data quality notes: raw data flagged for concerns; measurements flagged according to QA rules.

## Data Quality and Flags
- Quality checks:
  - Coefficient of variation (CV) of replicates < 15% → data considered valid (flag 103).
  - Values above calibration range may be valid if re-measurement not possible.
  - Missing data indicated by -9999.
- Final dataset: NH3_Cuilcagh2020.csv contains accepted values with appropriate flags.
- Data flags and meta-data: includes verification status, data capture %, validity, and EMEP-related flags (e.g., CV issues, detection limits, contamination indicators).

## Dataset Structure
- Each row represents one month of data for a single site.
- Key fields include:
  - Site name, unique site identifier, network_id, parameter_id
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Less-than indicator (detection limit)
  - Verification id, unit id
  - Data capture percentage, Validity_id
  - EMEP code and Month-Year
  - Comments
- Units for concentration: micrograms of NH3 per cubic metre of air (µg NH3 m-3).

## EMEP Flags (selected meanings)
- 103: CV of replicates >15%; valid measurement.
- 999, 781, 780, 653, 652, 651, 647, 646, 645, 599, 593, 591, 559, 558, 557, 556, 555, 553, 532: various data capture/validity and contamination or representativeness notes (examples include below detection limit, sampling period issues, nearby contamination, or valid observations despite field issues).

## Site Information
- Boardwalk: start 01/02/2020; end ongoing; lat 54.218694, lon -7.823424; inlet height 1.5 m.
- Eshvagh: start 01/02/2020; end ongoing; lat 54.190490, lon -7.846421; inlet height 1.5 m.
- Corcashel: start 01/02/2020; end ongoing; lat 54.187536, lon -7.973599; inlet height 1.5 m.
- Grouse Project: start 01/02/2020; end ongoing; lat 54.130905, lon -7.896038; inlet height 1.5 m.
- Shridrinagh: start 01/02/2020; end ongoing; lat 54.119063, lon -7.995085; inlet height 1.5 m.

## GIS and Data Use Implications
- The dataset provides time-stamped, site-specific NH3 concentrations suitable for GIS mapping and spatial-temporal analysis.
- Can be joined to site point geometries using site identifiers; supports map-based visualization of NH3 exposure trends and spatial patterns.
- QA flags and EMEP codes should be used to filter or annotate data layers (e.g., omit invalid data, highlight detections near detection limits, or note contamination flags).
- Monthly exposure data enable time-enabled (temporal) GIS analyses to assess vegetation impact in relation to NH3 levels.