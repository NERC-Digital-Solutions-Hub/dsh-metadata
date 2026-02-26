# Sentinel project bat and bird survey data, 20202023

- Background and aims
  - Part of the Social and Environmental Trade-Offs in African Agriculture (Sentinel) project, funded by UKRI via the Global Challenges Research Fund.
  - Purpose: assess ecological impacts of agricultural expansion in Ghana and Zambia; analyze community structure and composition across land-use gradients; identify bat and bird species present and investigate dietary habits to understand potential shifts in ecosystem service delivery.

- Survey locations and design
  - Survey period: December 2020 to March 2023.
  - Countries and sites: Ghana (3 localities) and Zambia (5 localities).
  - Ghana sites: Upper Guinean wet evergreen forests, surrounded by cacao and rubber plantations.
  - Zambia sites: Subtropical climate with dry miombo woodlands and evergreen Cryptocephalum forests, surrounded by maize and cassava cultivation.
  - Site selection: mix of recently expanded agricultural areas and baseline references with more intact vegetation.
  - Sampling design: two-tier stratified random design using a 1 km × 1 km grid over each locality; grid cells classified as Not Applicable (urban), Agriculture Only, Forest edge, or Forest; subset of sites from Agriculture, Forest edge, and Forest categories sampled.
  - Field logistics: some sites later found inaccessible, leading to alterations in the sampling plan; survey points along transects were randomly chosen and at least 200 m apart.

- Field methods (birds)
  - Bird surveys conducted at dawn using a standardized point count methodology; typically around 3 hours per sampling session.
  - Observation protocol: 10-minute counts within a 50 m radius, identifying birds to species level, estimating group size, and distinguishing perched versus flying; additional species observed beyond 50 m recorded separately.
  - Pre-count protocol: ~1 minute calm period to allow disturbance to subside.
  - Environmental data: weather and vegetation data recorded at each survey point.
  - Subset surveys: mist nets used to survey understory birds at a subset of sites; netting conducted with minimum 180 m of net lanes, 4 shelves, and specific mesh configurations; attempts to minimize harm and avoid netting near sunrise/sunset to protect birds.
  - Post-capture handling: birds identified to species level, sexed and aged where possible; weighed and held briefly before release.

- Field methods (bats)
  - Bat surveys conducted at the same locations as bird mist netting, using mist nets and harp traps on separate nights.
  - Trapping window: nets opened at sunset and operated for a minimum of 4 hours with checks every 15–30 minutes.
  - Equipment: combination of harp traps and mist nets (various sizes and configurations) tailored per site and night.
  - Species identification: guided by regional reference materials and published guides.

- Data consolidation and management
  - Data were entered by multiple inputters, then compiled, error-checked, and validated to produce a consolidated dataset.
  - Data description: Sentinel_survey_data.zip contains two dataframes—bird observations from 10-minute point counts and mistnetting records for bats and birds.
  - Data quality: missing values are marked as NA; efforts aligned with standard survey techniques and reference guides.

- Data structure and variables
  - Bird point counts dataframe (Sentinel_Pointcount_data.csv)
    - Key fields: country, locality, grid, transect, point, site; latitude/longitude; collection date; observer initials and start time.
    - Species data: common name and scientific name; counts within 50 m (perch, flyover, total under/over 50 m); observation type (seen, heard, or both); environmental context (temperature, cloud cover, wind, rain); land cover at grid/point/site.
    - Canopy and vegetation context: canopy height estimates, visibility, and counts of surrounding trees by size class.
  - Bat and bird mistnetting dataframe (Sentinel_Mistnetting_data.csv)
    - Key fields: country, locality, site, site type, latitude/longitude; collection date; specimen number.
    - Taxonomy: class (Aves or Mammalia), scientific name, common name.
  - Documentation: variable descriptions align with eBird nomenclature and regional references where applicable.

- References and provenance
  - Field methods anchored to established bird census and survey techniques and regional bat/bird guides.
  - Species identification supported by regional reference works and literacy in eBird taxonomy.