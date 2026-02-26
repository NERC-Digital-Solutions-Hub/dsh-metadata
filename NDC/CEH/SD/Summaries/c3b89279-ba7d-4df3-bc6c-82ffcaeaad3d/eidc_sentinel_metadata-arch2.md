# Sentinel project bat and bird survey data, 20202023

## About the survey
- Part of the Sentinel project (Social and Environmental Trade-Offs in African Agriculture), funded by UK Research and Innovation through the Global Challenges Research Fund.
- Aims to assess ecological impacts of agricultural expansion in Ghana and Zambia by examining community structure, composition, and dietary habits of bats and birds across land-use gradients.
- Seeks to understand potential shifts in ecosystem service delivery resulting from land-use change.

## Survey methods
- Timeframe and locations: Data collected December 2020 to March 2023 in Ghana (3 localities) and Zambia (5 localities).
  - Ghana: Upper Guinean wet evergreen forests, near cacao and rubber plantations.
  - Zambia: Subtropical climate with dry miombo woodlands and evergreen Cryptocephalum forests, near maize and cassava cultivation.
- Sampling design: Two-tier stratified random sampling within each locality.
  - 1 km x 1 km grid overlay; sites categorized as Not Applicable, Agriculture Only, Forest edge, or Forest.
  - Subset of sites randomly sampled; adjustments made for accessibility and community permissions; survey points at least 200 m apart along transects.
- Birds: Standardised point counts at dawn, ~3 hours per location.
  - 10-minute counts within a 50 m radius, identified to species, with counts of individuals and groupings; recording of presence/absence and weather/vegetation data.
  - Mist nets used at a subset of sites to survey understory birds; netting conditions and timing specified to minimize bat capture and ensure animal welfare.
- Bats: Survey at the same locations using mist nets and harp traps on separate nights.
  - Nightly sampling with nets and traps; equipment included multiple mist nets and harp traps; identification guided by regional references.
- Data capture and quality: Data collected by multiple inputters, then consolidated, error-checked, and validated.

## Data consolidation
- Field data sheets were digitised by several inputters.
- The final dataset was compiled, error-checked, and validated to ensure consistency and accuracy.

## Data description
- Sentinel_survey_data.zip contains two dataframes:
  - Sentinel_Pointcount_data.csv: Bird point-count observations.
    - Key fields: country, locality, grid, transect, point, site; latitude/longitude; collection date; observer; time started; common and scientific names; counts (under 50 m, over 50 m, total); observation type; weather (temp, cloud cover, wind, rain); land cover at grid/point/site; canopy and vegetation metrics (canopy height, visibility, tree counts).
  - Sentinel_Mistnetting_data.csv: Bat and bird mist-netting records.
    - Key fields: country, locality, site, site type; latitude/longitude; collection date; specimen number; class (Aves/Mammalia); scientific and common names.
- All missing data are marked as NA.
- Variables cover location (country, locality, grid, transect, point, site) and spatial data (latitude, longitude), temporal data (collection date), species-level data (common and scientific names), counts and observation type, environmental covariates (weather and vegetation), and land-cover/canopy metrics relevant to the sampling design.

## Data usage context and references
- The methods align with established bird census techniques and bat identification guides cited in the project documentation.
- Data intend to support analyses of how agricultural expansion affects avian and chiropteran communities and related ecosystem services, with datasets stored and made available through appropriate data portals as part of standard monitoring practice.