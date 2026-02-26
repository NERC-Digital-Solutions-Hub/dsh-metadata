# Sup_Doc_NH3_UWT_Cuilcagh

- Purpose and scope
  - Data from the area around Cuilcagh in Ireland and Northern Ireland to observe the impact of local ammonia (NH3) on vegetation.
  - Local site operator: Ulster Wildlife Trust; analysis: UK Centre for Ecology and Hydrology (CEH) Edinburgh.
  - Measurements use UK CEH ALPHA samplers; exposed monthly at the start of each month.

- Sampling and measurement method
  - Passive CEH ALPHA sampler with citric acid coated filter to capture NH3; PTFE membrane protects filter; membrane faces downward during exposure.
  - Replicate samplers (triplicates) mounted ~1.5 m above ground on shelter posts.
  - Analysis workflow: extract samplers in deionised water; measure ammonium with SEAL AA3 colorimetry; convert to average NH3 concentration in air using uptake rate (0.003241315 m3 h-1), exposure duration, and lab blanks.
  - Data flagged for quality concerns. Raw data checked against quality rules.

- Data quality and validation
  - Quality assurance rules
    - Coefficient of variation (CV) of replicates < 15% considered valid; if CV > 15%, replicates may be discarded; data may still be flagged as valid (code 103).
    - Some measurements exceed calibration range but are considered valid.
    - Missing data indicated by -9999 (also for missing date/time metadata).
  - Final dataset file: NH3_Cuilcagh2020.csv with accepted values and appropriate flags.
  - Data capture and validity indicators accompany each row (e.g., data capture percentage, validity flag, verification status, detection-limit information).

- Dataset structure and contents
  - Each row represents one month of data for a single site.
  - Key columns
    - Site name, unique site identifier, network_id, parameter_id (alpha_NH3_g)
    - Measurement start date/time and end date/time (exposure window)
    - Measurement value: ammonia concentration (µg NH3 m-3)
    - Less than flag: whether value is below detection limit (0.03)
    - Verification id (0–3 indicating verification status)
    - Unit id (24 = µg NH3 m-3)
    - Data capture (percentage), validity_id (1 = valid, -1 = not valid)
    - EMEP code and related flags
    - Month-Year (format mmm-yy)
    - Comments
  - Example context: final dataset consolidates site-wise, month-by-month NH3 exposure data with quality and provenance metadata.

- EMEP flags and interpretations
  - Codes indicate data status, quality issues, or contextual notes (e.g., contamination, detection limits, sampling period representation).
  - Examples (representative meanings):
    - 103: CV of replicates > 15% but still considered valid
    - 780/781/559/555, etc.: various contamination, detection limit, or local influence notes
    - 652–654, 593, 591: local influences or data adjustments; validity varies
    - 999 family: data capture or validity indicators for missing or special cases
  - Flags provide context for data quality decisions and future data handling.

- Site information
  - Boardwalk: start 01/02/2020; ongoing; lat 54.218694, lon -7.823424; inlet height 1.5 m
  - Eshvagh: start 01/02/2020; ongoing; lat 54.190490, lon -7.846421; inlet height 1.5 m
  - Corcashel: start 01/02/2020; ongoing; lat 54.187536, lon -7.973599; inlet height 1.5 m
  - Grouse Project: start 01/02/2020; ongoing; lat 54.130905, lon -7.896038; inlet height 1.5 m
  - Shridrinagh: start 01/02/2020; ongoing; lat 54.119063, lon -7.995085; inlet height 1.5 m
  - All sites share a similar data collection approach and exposure height; site details and identifiers are included in the dataset.

- Practical notes for data support and reuse
  - The dataset supports time-series analyses of NH3 exposure at multiple sites with standardized measurement methodology.
  - Users should respect data flags (CV issues, detection limits, and EMEP codes) when interpreting concentrations or aggregating data.
  - Missing or invalid entries are explicitly marked (-9999 or negative validity codes), guiding data cleaning and quality control.
  - The data are suitable for ecological impact assessments, trend analyses, and cross-site comparisons within the 2020 dataset.