# Jonkershoek Nature Reserve Ant Community and Seed Dispersal Experiments

- Study goal: Identify correlations and patterns in ant community composition and myrmecochorous seed dispersal in relation to invasion by the Argentine ant (Linepithema humile) and Australian wattles (Acacia spp.), and to use findings for predictive insights on ecological impact.

## Study Area
- Location: Jonkershoek Nature Reserve, Boland Mountain Complex, Cape Floristic Region, South Africa (33°55'51"S, 18°51'16"E).
- Timing: November 2014–February 2015 and January–February 2017.
- Focus: Co-occurrence of invasive L. humile and Acacia species (A. saligna, A. pycnantha).

## Data and RAW Material
- All data files contain RAW, untransformed data collected across trials.
- Files documented across three experiments, plus details on invasive status and community composition.

## Experiments and Key Methods

- Experiment 1: Pitfall trapping
  - Objective: Compare ant community composition in invaded vs non-invaded areas using pitfall traps.
  - Reference method: Devenish et al. 2019 (Biological Invasions).
  - Data file: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW.
  - Data structure highlights:
    - Collection_code, Collection_location (Transect Code), Collection_date, Invasion_status, Sample_number, Ant species (counts).

- Experiment 1: Baiting
  - Objective: Assess temporal changes in ant community (presence/absence at baits) across times of day.
  - Data file: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW.
  - Data structure highlights:
    - Collection_code, Plot_ID, Collection_date, Collection_period (morning/midday/afternoon), Invasion_status, Ground_temperature, #_of_Species, Ant species (present/absent).

- Experiment 2: Seed removal (seed dispersal)
  - Objectives: Compare seed removal by ants in invaded vs non-invaded sites.
  - Design: 60 seed hubs across six transects; eight seeds per hub (two plant species per hub), with/without elaiosome; repeated over three weeks; total seeds ~5,840.
  - Data file: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW.
  - Data structure highlights:
    - seedhub_id, locality, plant_species, ant_community, period (Morning/Afternoon), elaiosome (Present/Absent), seed_number_removed (0/1), start_time, end_time, duration_min, duration_hr.

- Experiment 3: Seed fate
  - Objective: Determine whether seeds are transported into ant nests or abandoned, across ant species and plant species; assess nest placement depth.
  - Seed selection: three invasive and three native plant species; seeds exposed near nests; 24-hour exposure.
  - Nest depth assessment: plaster casts to locate seeds within nest depths (0–12 cm, 13–24 cm, >25 cm).
  - Data file: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW.
  - Data structure highlights:
    - ant_status (native/invasive), nest_id, ant_genus, plant_species, plant_status (native/invasive), on_surface, removed_into_nest, 0_12_cm, 13_24_cm, >25_cm.

## Data Structure and Variables (Across Files)
- Common themes: invasion status, transect/hub identifiers, species presence/absence or counts, timing, and spatial depth metrics.
- Key columns include:
  - Invasion_status (invaded vs non-invaded)
  - ant_species or ant_genus; plant_species
  - Time-related fields (collection_date, collection_period, start_time, end_time, duration)
  - Activity/outcome indicators (seed_removed, removed_into_nest, on_surface, depth categories)

## Temporal Coverage
- Primary fieldwork: 2014–2015
- Follow-up/replication: 2017
- Location scale: six transects with multiple hubs/plots per experiment

## Data Quality, Access, and Use for Analysts
- Strengths:
  - RAW data with explicit, documented structure for cross-dataset integration.
  - Clear invasion-status delineation enabling comparative analyses between invaded and non-invaded contexts.
  - Rich temporal and spatial detail (time of day, transect/hub identifiers, nest depth).
- Considerations:
  - Datasets are untransformed; analysts may need normalization or standardization for cross-experiment comparisons.
  - Some factors (e.g., transect/code factors) are encoded and may require careful decoding to merge with external datasets.
  - Data represent a specific ecological context (Jonkershoek CFR) and may limit broad generalizations without additional sites.
- Potential analyses for decision-relevant questions:
  - Compare ant community composition and species richness between invaded vs non-invaded areas (pitfall and baiting data).
  - Quantify seed removal rates and temporal patterns across invasion status and plant species (seed dispersal dataset).
  - Assess seed fate and nest deposition depth to infer seed survival, transport pathways, and nest architecture influences (seed fate dataset).

## Practical Implications
- The combined suite of experiments enables testing of how invasive ants and Acacia species affect native ant communities, seed dispersal efficiency, and seed fate.
- Data can support predictive modeling of invasion effects on myrmecochory and inform management decisions in conservation areas with similar invasive pressures.