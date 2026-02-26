# Sentinel project bat and bird survey data, 20202023

- Purpose and scope
  - Part of the Sentinel project to assess ecological impacts of agricultural expansion in Ghana and Zambia.
  - Focuses on community structure and composition of bats and birds across land-use gradients; includes examination of dietary habits to infer changes in ecosystem service delivery.

- Study locations and design
  - Ghana: 3 localities within the Upper Guinean wet evergreen forests, surrounded by cacao and rubber plantations.
  - Zambia: 5 localities with subtropical climate, including dry miombo woodlands and evergreen Cryptocephalum forests, surrounded by maize and cassava cultivation.
  - Site selection aimed to include areas with recent agricultural expansion and baseline references.
  - Sampling framework: two-tier stratified random design on a 1 km × 1 km grid; sites categorized into Not Applicable (NA), Agriculture Only, Forest edge, and Forest.
  - Within each site, survey points along transects were randomly selected and spaced at least 200 m apart.
  - Adjustments were made to the sampling plan when sites were inaccessible or permissions were needed.

- Survey methods (birds and bats)
  - Birds
    - Standardised point counts conducted at dawn, lasting ~3 hours.
    - 10-minute counts within a 50 m radius per point; observers recorded species seen or heard, with counts of individuals and grouping, avoiding double counting.
    - A 1-minute quiet period at arrival allowed disturbance to subside; weather and vegetation data recorded at each point.
    - Subset of sites used mist nets to survey understory birds.
  - Mist nets for birds
    - At least 180 m of net lanes; four nets (30 mm mesh) 6–18 m long.
    - Netting from 5:30 to 10:00 (flexible with conditions); birds netted under 30 minutes before sunrise and after sunset to minimize bat captures.
    - Captured birds identified to species, sexed/aged where possible; held briefly (≤30 minutes) before release; adults or recaptured birds noted.
  - Bats
    - Surveyed at the same locations as bird mist netting, using mist nets and harp traps on separate nights.
    - Sampling from sunset with minimum 4 hours per night; nets/traps checked every 15–30 minutes.
    - Equipment: 1–2 harp traps, 7 mist nets, and a high net system per night.
    - Species identification guided by regional reference materials.

- Data management and quality assurance
  - Data entry performed by multiple individuals; data consolidated, error-checked, and validated to ensure accuracy.
  - Metadata and structured data collection designed to support verification and future reuse.

- Data descriptions and structure
  - Data repository: Sentinel_survey_data.zip containing two dataframes.
  - Bird point counts data (Sentinel_Pointcount_data.csv)
    - Variables include: country, locality, grid, transect, point, site; latitude/longitude; collection date; observer; start time; species (common and scientific names); counts by distance (under 50 m and over 50 m); total counts; observation type (seen, heard, both); weather (temperature, cloud cover, wind, rain); land cover at grid, point, and site; canopy height metrics (Max/Min/Mean Can); visibility; counts of trees by size within 10 m radius.
  - Bat and bird mistnetting data (Sentinel_Mistnetting_data.csv)
    - Variables include: country, locality, site, site type; latitude/longitude; collection date; specimen number; class (Aves or Mammalia); scientific and common names.
  - Missing data coded as NA.

- Documentation and references
  - Methods for bird census and survey techniques cited; regional bat guides used for species identification.
  - Data fields are explicitly described to enable understanding and reuse.

- Accessibility considerations
  - Data include detailed field metadata and variable definitions to support transparency and reuse.
  - Some constraints and adjustments during fieldwork (e.g., accessibility and permissions) are noted, reflecting adaptive monitoring practices.