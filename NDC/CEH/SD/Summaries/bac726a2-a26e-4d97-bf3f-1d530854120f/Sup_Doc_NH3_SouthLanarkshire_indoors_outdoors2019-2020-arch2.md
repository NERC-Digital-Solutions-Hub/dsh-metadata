# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

- Overview
  - Location: two NH3 air monitoring sites in a rural area of South Lanarkshire (inside hall of a dwelling and outside in the dwelling’s garden).
  - Operator and analysis: site operator duties by the dwelling owner; analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.
  - Purpose: measure ambient ammonia (NH3) concentrations using standardized, replicated sampling to support environmental health monitoring over time.
  - Proximity: garden backs onto grassland farmed by a large dairy farm.

- Sampling Methodology
  - Instrument: CEH ALPHA® passive samplers using citric acid coated filters to capture NH3; PTFE membrane protects the filter.
  - Deployment: samplers mounted on a shelter on a pole at ~1.5 m height; replicate samplers used per site for reliability.
  - Exposure cycle: monthly cycles, exposed at the beginning of each month.
  - Analysis: exposed samplers extracted into deionised water; analyzed with SEAL AA3 colorimetry to determine ammonium concentration; NH3 concentration in air calculated from ammonium and a known uptake rate (0.003241315 m3 h-1) and exposure duration.

- Data Quality and QA/QC
  - Data flagging: data flagged to indicate concerns; flagged data described in accompanying documentation.
  - Quality rules:
    - Coefficient of variation (CV) of replicates < 15% required for reliability; if CV > 15%, replicates may be discarded; if deemed representative, data are valid with a 103 flag.
    - Data above calibration range may be valid if reanalysis was not possible due to instrument issues.
    - Missing data represented by -9999.
  - Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv contains accepted data with appropriate flags. Each row represents one month of data for a single site; columns include site name, exposure period, NH3 concentration (µg NH3 m-3), and a data flag.

- Dataset Structure and Key Fields
  - Core columns (examples):
    - Site name and unique site identifier; network_id (RSW); parameter_id (alpha_NH3_g).
    - Measurement start date/time and end date/time; exposure period.
    - Ammonia concentration (units: µg NH3 m-3).
    - Less than flag (indicates value below detection limit).
    - Verification id; unit id (µg NH3 m-3); Data capture percentage; Validity_id (1 = valid, -1 = not valid).
    - EMEP code and related flags (data status codes, capture validity, and reasoning for data status).
  - EMEP flags: detailed codes indicating data capture status, validity, and local influences (e.g., detection limit, contamination, sampling conditions, and nearby activities).

- Site Information
  - Inside site: start date 01/01/17; End date ongoing; coordinates 55.64072, -3.59705; air inlet height 1.5 m; location: hall of dwelling.
  - Outside site: start date 01/01/17; End date ongoing; coordinates 55.64072, -3.59705; air inlet height 1.5 m; location: garden of dwelling.

- Context and Accessibility
  - Data are prepared for standardised monitoring outputs and likely uploaded to appropriate data portals as part of routine environmental monitoring.
  - Location context includes proximity to grassland and a dairy farm, which may influence local NH3 levels.