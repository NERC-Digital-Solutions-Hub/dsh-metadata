# Devenish_Jonkershoek_Experiment_1_2_3_raw_data

- Study context
  - Location: Jonkershoek Nature Reserve, Boland Mountain Complex, Cape Floristic Region, South Africa.
  - Timeframe: November 2014 – February 2015 and January – February 2017.
  - Focus: interaction between invasive Argentine ant (Linepithema humile), Australian wattles (Acacia species), and myrmecochorous seed dispersal.
  - Data nature: RAW data from three experiments; no transformation or normalisation applied.

- Aims aligned with monitoring frameworks
  - Identify environmental health indicators related to ant invasions, plant-seed interactions, and seed fate.
  - Provide datasets to assess how invasions affect ecosystem processes (e.g., seed dispersal, seed fate) to inform management decisions and monitoring strategies.

- Experimental design overview
  - Experiment 1: Pitfall trapping
    - Objective: characterize ant community composition in invaded vs non-invaded areas.
    - Invocation: Areas defined as invaded if L. humile present at any survey point; non-invaded otherwise.
    - Data type: Ant species counts by pitfall trap; overall community composition by transect.
  - Experiment 1: Baiting
    - Objective: detect temporal shifts in ant community composition (presence/absence at baits) across times of day.
    - Transport: Baits deployed at 08:00, 12:00, 16:00; collected after 1 hour; species identified where possible.
    - Data type: Presence/absence per species at each bait, with environmental metadata (temperature, time of day).
  - Experiment 2: Seed removal
    - Objective: compare seed dispersal rates in invaded vs non-invaded sites using seed hubs.
    - Design: 60 seed hubs across six transects; 8 seeds per hub (two plant species, with/without elaiosome); monitored at 1-hour intervals up to 3 hours; repeated across three weeks, with two daily time points (morning, afternoon).
    - Data type: Seed removal per hub/time, plant_species, ant_community, elaiosome status, and timing metrics.
  - Experiment 3: Seed fate
    - Objective: determine seed transport into ant nests by specific ant species and nest architecture influence.
    - Design: For each ant species, 20 nests (≥10 m apart) across six transects; seeds from six plant species (three invasive, three native) offered near nests; seeds assessed after 24 hours for transport into nests and depth placement via plaster casts.
    - Data type: Seed transport outcome (into nest vs abandoned), nest/seed placement depth (0–12 cm, 13–24 cm, >25 cm), ant_status (native vs invasive), plant_status (native vs invasive), nest identifiers, and nest architecture indicators.

- Data files and data structure (raw)
  - Experiment 1: Ant community – PITFALL_RAW
    - Columns include: Collection_code, Collection_location, Collection_date, Invasion_status, Sample_number, and ant species count data.
  - Experiment 1: Ant community – BAITING_RAW
    - Columns include: Collection_code, Plot_ID, Collection_date, Collection_period, Invasion_status, Collection_location, Ground_temperature_C, #_of_Species, and per-species presence/absence indicators.
  - Experiment 2: Seed dispersal – HUB_RAW
    - Columns include: seedhub_id, locality, plant_species, ant_community, period, elaiosome, seed_number_removed, start_time, end_time, duration_min, duration_hr.
  - Experiment 3: Seed fate – NEST_seed_removal_FATE_RAW
    - Columns include: ant_status, nest_id, ant_genus, plant_species, plant_status, on_surface, removed_into_nest, 0_12_cm, 13_24_cm, >25_cm.

- Key definitions and metadata
  - Invasion_status: invaded if L. humile present at any survey point; non-invaded otherwise.
  - Data provenance: RAW, unmodified data across all trials; methods grounded in Devenish et al. (2019) Biological Invasions.
  - Scope: six transects across the study area; multiple replicates and time points to assess temporal dynamics and spatial variation.

- Relevance for monitoring and policy
  - Provides multi-dimensional indicators for environmental health monitoring:
    - Invasive ant presence/abundance across habitat patches.
    - Temporal dynamics of ant activity (baiting) and its linkage to seed dispersal processes.
    - Quantitative measures of seed removal rates and seed fate relative to ant invasions.
    - Nest-level seed placement and transport patterns informing nest-site risk assessments.
  - Enables comparisons between invaded and non-invaded contexts to guide management actions (e.g., targeting invasions to mitigate disruption of plant regeneration processes).
  - Data standards and governance considerations:
    - RAW data emphasises the need for robust metadata and clear data governance to support reuse.
    - Potential barriers highlighted in monitoring frameworks (e.g., data accessibility, data silos, and the requirement to share underlying data) are relevant for ensuring this dataset is usable for policy and decision-making.
    - Structure of data files with explicit column definitions supports reproducibility and integration into monitoring dashboards or analytic pipelines.

- Practical notes for use in monitoring frameworks
  - Researchers should verify data definitions against the parent Devenish et al. methods to ensure consistent interpretation of invasion status and sampling periods.
  - Metadata completeness (e.g., transect codes, hub identifiers, dates, times, temperatures) is crucial to enable cross-experiment integration and longitudinal analyses.
  - Data cleaning and standardization may be required before integration into monitoring dashboards or policy reports, given the RAW status across experiments.