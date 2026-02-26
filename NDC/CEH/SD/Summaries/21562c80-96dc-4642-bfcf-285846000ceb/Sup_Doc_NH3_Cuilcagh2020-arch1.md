# Sup_Doc_NH3_UWT_Cuilcagh

## Purpose and context
- Observes impact of local ammonia (NH3) levels on vegetation around Cuilcagh in Ireland and Northern Ireland.
- Measurements conducted by Ulster Wildlife Trust; analysis by UK Centre for Ecology and Hydrology (Edinburgh).
- Uses UK CEH ALPHA® samplers to estimate ammonia concentrations in air.

## Sampling method and instruments
- Passive samplers with citric acid coated filter to capture NH3; protected by a white PTFE membrane.
- Membrane facing downwards during exposure.
- Samplers mounted on shelters on poles at about 1.5 m above ground; replicate triplicate samplers per site for reliability.
- Exposed monthly at the beginning of each month.
- Analysis: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetric method (ammonium).
- NH3 in air calculated from sampler ammonium concentration using uptake rate of 0.003241315 m3 h-1, exposure duration, and lab blank values.

## Data quality, validation, and flags
- Data flagged to highlight concerns (details on page 4 of the document).
- Quality assurance rules:
  - Coefficient of variation (CV) of replicates < 15% => data considered valid; flag 103 applied if valid.
  - Values above calibration range may be valid if not re-run; not diluted.
  - Missing data or metadata indicated by -9999.
- Final dataset NH3_Cuilcagh2020.csv contains accepted values with appropriate flags.
- Data are monthly measurements per site; concentration units are micrograms NH3 per cubic metre of air (µg NH3 m-3).
- Data structure includes site identifiers, exposure periods, concentration values, and data quality flags.

## Dataset structure and metadata
- Data fields (examples):
  - Station name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Less than detection flag, verification status, unit id, data capture percentage, validity_id, EMEP code, Month-Year, Comments
- EMEP flags provide context for data status and quality (e.g., contamination, calibration issues, detection limits, representativeness).
- Data status and EMEP flag codes listed (e.g., 103 CV issue, various codes indicating sampling conditions or data validity).

## Site information and geography
- Sites include:
  - Boardwalk
  - Eshvagh
  - Corcashel
  - Grouse Project
  - Shridrinagh
- Start date for all sites: 01/02/2020; End date: ongoing.
- Geographic coordinates (latitude, longitude) and 1.5 m inlet height above ground provided for each site.
- Examples:
  - Boardwalk: 54.218694, -7.823424
  - Eshvagh: 54.190490, -7.846421
  - Corcashel: 54.187536, -7.973599
  - Grouse Project: 54.130905, -7.896038
  - Shridrinagh: 54.119063, -7.995085

## Data handling and transparency
- Data are prepared for discoverability with metadata to enable reuse.
- Dataset aims to support analysis of correlations and potential impacts of NH3 on vegetation, aligning with the analysts’ aim to identify patterns and inform decisions.
- Emphasizes standardisation challenges across datasets and the importance of clear documentation for replicability and interpretation.