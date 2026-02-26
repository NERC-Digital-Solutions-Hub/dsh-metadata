# Metadata for physiology data

- Purpose and scope
  - Metadata for three related data sets describing physiology and behavior of threespine sticklebacks in relation to temperature regimes.
  - Aimed at enabling monitoring of environmental health and policy-relevant environmental conditions over time by standardising data and facilitating cross-study comparison.

- Data sets included
  - Data set 1: Metabolism.csv
    - Generated via respirometry on sticklebacks from multiple populations.
    - Study basis: Pilakouta et al. 2020 (multigenerational exposure to elevated temperatures reduces standard metabolic rate in the wild; Functional Ecology).
    - Method: measuring oxygen consumption in a flow-through chamber over weeks to obtain whole-body metabolism.
    - Columns (six):
      - AcclimTemp: acclimation temperature in Celsius at which the specimen was held
      - PopTemp: habitat type (Cold or Warm) corresponding with ambient/geothermal origin
      - Pop: population site code (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for Warm/Cold
      - PopPair: sympatric or allopatric population relationship
      - Mass: specimen weight in grams
      - SMR: standard metabolic rate in mg O2 per hour
  - Data set 2: Sociability.csv
    - Generated in the lab using wild-caught sticklebacks from geothermal and ambient populations.
    - Study basis: Pilakouta et al. 2023 (A warmer environment can reduce sociability in an ectotherm; Global Change Biology).
    - Method: video tracking to quantify mean distance from the stimulus shoal over 30-minute trials; densities standardized across treatments.
    - Columns (seven):
      - populationpair: allopatric or sympatric depending on geographic association
      - population: population name
      - HabitatTemp: thermal habitat of population origin (Warm or Cold)
      - Temp: acclimation temperature and trial temperature
      - ID: individual fish identifier
      - trial: trial number (1 or 2) for repeated testing at a given temperature
      - sociability: mean distance to stimulus shoal (cm)
  - Data set 3: temperature preference.csv
    - Generated in the lab using wild-caught sticklebacks from geothermal and ambient populations.
    - Study basis: Pilakouta et al. 2023 (Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment; Ecology and Evolution).
    - Method: 24-hour temperature preference chamber to record time spent at each temperature; same observer collected all data to minimise observer differences.
    - Columns (seven):
      - Test date: date of data collection
      - Population: population name (sympatric or allopatric)
      - Popn: population and thermal habitat (as in Data set 1)
      - TempPref: time spent in a preferred temperature (minutes)
      - LogTempPref: log transformation of time spent in a preferred temperature
      - Mass: fish weight in grams
      - LogMass: log transformation of weight in grams

- Population and habitat details
  - Populations originate from geothermal (Warmer environments) and ambient (Cool environments) sites.
  - Pop and PopTemp descriptions link specimen origin to their thermal habitat (Cold vs Warm) and whether populations are sympatric or allopatric.

- Data quality, processing, and handling
  - All data checked for outliers (quality control step).
  - A single collector performed all measurements to minimize observer variation.
  - Data are prepared to support standardised analyses and cross-dataset comparability for environmental monitoring.

- References
  - Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology, 34, 1205-1214.
  - Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution, 13, e9654.
  - Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology, 29, 206-214.