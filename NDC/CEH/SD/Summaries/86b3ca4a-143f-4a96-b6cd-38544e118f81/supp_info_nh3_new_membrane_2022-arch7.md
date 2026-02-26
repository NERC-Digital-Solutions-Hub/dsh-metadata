# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

- Purpose: Report initial results from validating a new PTFE membrane for ALPHA® samplers to measure atmospheric NH3, with monthly exposure cycles and analysis conducted at UKCEH Edinburgh.

- Sampling method (UKCEH ALPHA® Sampler)
  - Passive NH3 sampler using a citric acid–coated filter and a white PTFE membrane to permit diffusion of ammonia.
  - Membrane oriented downwards during exposure; samplers mounted on a shelter on a pole at about 1.5 m above ground.
  - Replicates used per site to improve reliability; samplers protected in plastic containers.

- Analysis
  - Exposed samplers are extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry.
  - NH3 concentration in air for the exposure period derived using the sampler uptake rate with the new membrane (0.0041741 m3 h-1) and exposure duration.

- Data handling and quality checks
  - Raw data are quality-checked with rules including:
    - Coefficient of variation (CV) of replicates < 15%; otherwise replicates may be discarded; valid data flagged as 103.
    - Values above calibration range may be retained as valid when re-analysis isn’t possible.
    - Missing data coded as -9999 (e.g., missing measurement or metadata).
  - Final dataset: NH3_New_Membrane_2022.csv; contains accepted data values with appropriate flags; columns include site identifiers, exposure period dates/times, NH3 concentration (µg NH3 m-3), and a data flag.

- Dataset structure and fields (highlights)
  - Each row corresponds to one month of data for a single site.
  - Key fields include: site_id, site_name, network_id (NM), parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration (µg NH3 m-3), less-than indicator, verification_id, unit_id (24 = µg NH3 m-3), data_capture (%), validity_id (e.g., 1 for valid, -1 for not valid), EMEP flag status, Month-Year, and comments.
  - EMEP flags provide QA/status information (e.g., missing data, below detection, contamination indicators, sampling anomalies, etc.).

- Site information and locations (four UKEAP sites)
  - Edinburgh uptake rate OTC: lat 55.863150, lon -3.209845; height 1.5 m; start 2020-03-01; ongoing; collocated with UKA00128.
  - Auch: lat 55.792160, lon -3.242900; height 1.5 m; start 2020-03-01; ongoing; collocated with UKA00451.
  - Hills: lat 54.452500, lon -6.083340; height 1.5 m; start 2020-03-01; ongoing; collocated with UKA00293.
  - Chilbolton: lat 51.149617, lon -1.438228; height 1.5 m; start 2021-01-01; ongoing; collocated with UKA00614.
  - All sites are part of the UKEAP network and provide monthly NH3 measurements.

- Roles and workflow
  - Local site operators: UKCEH Edinburgh, AFBI Hillsborough, and Ricardo AEA Chilbolton.
  - Analysis: Centre for Ecology and Hydrology, Edinburgh.
  - Purpose: facilitate data quality assurance and generation of map-ready NH3 concentration data for GIS applications.

- GIS-relevance and usage notes
  - Dataset enables spatial visualization of NH3 concentrations across four UK monitoring sites with monthly resolution.
  - QA flags and EMEP codes enable confident filtering for map production and regulatory reporting.
  - Involves integration of site metadata (coordinates, altitude, collocation codes) for accurate spatial analyses.