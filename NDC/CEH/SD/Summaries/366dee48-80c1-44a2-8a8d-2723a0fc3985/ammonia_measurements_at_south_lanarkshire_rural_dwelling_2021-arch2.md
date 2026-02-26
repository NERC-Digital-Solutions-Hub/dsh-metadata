# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

- Purpose and setting
  - Data from 2 sites in a rural location in South Lanarkshire: one indoors (hall of dwelling) and one outdoors (garden of dwelling, backing onto grassland on a large dairy farm).
  - Local site operator duties performed by the dwelling owner; analysis by Centre for Ecology and Hydrology (UKCEH) Edinburgh.

- Methodology
  - Instrument: UKCEH ALPHA® passive samplers using a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter.
  - Deployment: samplers mounted on a shelter on a pole at about 1.5 m above ground; replicate samplers used for each site to improve reliability.
  - Exposure: monthly cycles, data collected at the beginning of each month.
  - Analysis: exposed samplers extracted into deionised water; NH3 concentration determined via SEAL AA3 colorimetry (ammonium concentration converted to NH3 in air).
  - Calculation: final air concentration derived using uptake rate of 0.003241315 m3 h-1 and exposure duration.
  - Data handling: raw data quality-assured and flagged (details on page 4 of the source).

- Data quality assurance and flags
  - Validation rules:
    - Coefficient of variation (CV) of replicates must be < 15% for a result to be considered valid (otherwise evaluated for potential discards; otherwise flagged as valid, code 103).
    - Some values exceeding calibration range deemed valid if re-measurement wasn’t possible due to instrument or sample issues.
    - Missing data marked as -9999 where concentration or meta-data are absent.
  - Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv contains accepted data with appropriate flags; includes site names and spatial identifiers.

- Dataset structure and contents
  - Each row corresponds to one month of data for a single site; columns include:
    - Site id and Site name
    - Network id (RSW)
    - Parameter id (alpha_NH3_g)
    - Measurement start/end dates and times
    - Measurement (NH3 concentration in µg NH3 m-3)
    - Data flag (including less-than/detection-limit indicators)
    - Verification id, unit id
    - Data capture percentage, Validity id, EMEP data status code
    - Month-Year
    - Comments
  - Units: NH3 concentration in µg NH3 m-3; monthly averages per exposure period.

- EMEP and data status
  - EMEP flags (with codes such as 103, 781, 780, 653, 652, etc.) indicate verification status, data issues, or contextual factors (e.g., nearby agricultural activity, contamination, or sampling conditions).
  - Data capture and validity indicators accompany each record to support reuse and quality assessment.

- Site information
  - Indoor site: located in hall; start date 01/01/17; ongoing; coordinates 55.64072, 3.59705; air inlet height 1.5 m.
  - Outdoor site: located in garden; start date 01/01/17; ongoing; coordinates 55.64072, 3.59705; air inlet height 1.5 m.
  - Both sites share the same coordinates and altitude specifications, differing only by location relative to the dwelling interior/exterior.

- Outputs and purpose for monitoring
  - Outputs are presented in clear formats (reports, maps, charts) and stored/uploaded to appropriate portals.
  - The dataset supports monitoring environmental ammonia over time and across indoor/outdoor settings, enabling assessment of environmental health and policy performance.

- Key considerations and challenges
  - Increasing the value of monitoring datasets by integrating them with additional relevant data sources.
  - Ensuring accessible underlying data to support external analysis and scrutiny.