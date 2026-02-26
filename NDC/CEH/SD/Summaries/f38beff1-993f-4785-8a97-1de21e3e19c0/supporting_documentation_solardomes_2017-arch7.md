# Ozone and meteorology 2017

- Context and location
  - Rural site in North Wales, UK, part of Bangor University farm; near the sea.
  - Coordinates: 53°14′N, 4°01′W; elevation: 15 m.
  - Facility: eight solardomes used for ozone exposure experiments; three heated domes (+7°C) to mimic tropical/subtropical conditions; ozone added via a computer-controlled schedule.

- Experimental design
  - Four replicate pots per species/cultivar.
  - Species include multiple wheat cultivars, pearl millet, beans, cowpea, and finger millet with various varieties.
  - Ozone treatment levels: Low (35 ppb), Medium (80 ppb), High (115 ppb).
  - Temperature conditions: unheated vs heated (+7°C).
  - Each replicate continuously logged for ozone and meteorology; exposure lengths varied by species/growing season.
  - Endpoints: biomass and yield (end-of-exposure collection); ad-hoc plant physiology measurements (stomatal conductance, soil moisture, chlorophyll content index).

- Treatments and sampling regime
  - Treatment descriptions: Low unheated, Medium unheated, High unheated; Low heated, Medium heated, High heated.
  - Measurements included stomatal conductance (AP4 porometer), soil moisture (theta probe), chlorophyll content index (CCM-200), and yield data collected at experiment end.
  - Measurements for ozone and meteorology recorded hourly.

- Data resources and structure
  - Biomass_and_Yield_2017.csv (17 columns, 3112 rows): includes species/variety, treatment, pot and pod counts, weights (pods, beans, seed heads), averages, total grain metrics.
  - Ozone_and_meteorology_2017.csv (11 columns, 18534 rows): includes treatment, day/year, date, hour, hourly ozone (ppb), light, temperature, vapour pressure deficit, air pressure (constant), wind speed (dummy value), precipitation (dummy value).
  - Plant_Physiology_2017.csv (11 columns, 3112 rows): includes treatment, species, pot, date/time, leaf side, stomatal conductance, light, leaf temperature, soil moisture, chlorophyll content index.
  - Blank cells indicate missing readings; few measurements missing due to QA issues.

- Data collection, instrumentation, and QA
  - Ozone/meteorology logged automatically; QA checks for range plausibility; gap filling when needed.
  - Plant physiology collected ad-hoc with QA checks.
  - Instruments:
    - Solardome ozone exposure system controlled by LabView.
    - AP4 porometer for stomatal conductance.
    - Delta-T theta probe for soil moisture.
    - CCM-200 for chlorophyll content index.
  - Calibration:
    - AP4 porometer calibrated daily per manufacturer instructions.
    - Ozone analyzers calibrated by external company.
    - CCM-200 autocalibration on turn-on.

- Gap filling and data processing
  - Gap filling protocol maintained original data; amended copies stored separately as filled/corrected data.
  - Gaps of up to 5 consecutive hours filled by averaging adjacent values.
  - Larger gaps cross-referenced with lab notes; where appropriate, fill using previous/next day values to preserve patterns.
  - If ozone system was not running, missing values replaced with a dummy 5 ppb value.
  - Data validation applied to identify and address unrealistic values (e.g., negative ozone or values above plausible limits).

- Miscellaneous and access
  - Related facility description: CEH solardomes and ozone field release system (website link provided).
  - Data suitability for GIS
    - Hourly temporal resolution with explicit timestamps and treatment metadata.
    - Spatial context: single site with multiple dome-specific measurements; suitable for time-series visualization and spatially aggregated analyses by species, treatment, and dome.
    - Clear column definitions and units enable map-based visualizations of ozone exposure, meteorology, and plant responses.
  
- Notes for GIS use
  - Ensure handling of missing data via gap-filled copies or acknowledge missingness in analyses.
  - Use provided coordinates and dome identifiers to map sensor locations if geometry is available; otherwise, aggregate by dome/treatment for spatial summaries.
  - Temporal alignment across datasets (ozone, meteorology, physiology, and biomass/yield) is hourly to end-of-season, enabling synchronized GIS analyses and time-series mapping.