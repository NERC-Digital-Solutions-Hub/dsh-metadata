# Jonkershoek Nature Reserve Invasion Experiments: Pitfall Trapping, Baiting, Seed Removal, and Seed Fate (2014–2017)

- Purpose and context
  - Study conducted in the Jonkershoek Nature Reserve (Cape Floristic Region, South Africa) to examine interactions between invasive Argentine ants (Linepithema humile), Australian wattles (Acacia spp.), and myrmecochorous seed dispersal.
  - Timeframe spans November 2014–February 2015 and January–February 2017, focusing on natural seed dispersal processes during myrmecochory.
  - Data are RAW and unmodified across all trials.

- Roles and aims aligned with environmental monitoring
  - Demonstrates environmental conditions and biotic interactions in a consistent format to support monitoring of ecological health and policy performance over time.
  - Uses established data sources and standardized methods to generate outputs (e.g., ant community composition, seed dispersal metrics, seed fate).
  - Outputs are designed for clear presentation (reports, maps, charts) and for storage/upload to appropriate data portals, facilitating reuse and scrutiny.
  - Highlights ongoing challenges: increasing dataset value through data integration and broad data accessibility for others.

- Experiment 1: Pitfall trapping
  - Objective: characterize ant community composition in invaded vs non-invaded areas.
  - Method: pitfall traps following Devenish et al. (2019) to derive species mean relative abundances.
  - Data file: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW
  - Data structure highlights:
    - Collection_code, Collection_location, Collection_date, Invasion_status, Sample_number
    - Ant species abundance across samples

- Experiment 1: Baiting
  - Objective: assess temporal shifts in ant community composition at baits (species presence/absence across the day).
  - Method: baits set at 08:00, 12:00, 16:00; ants collected after 1 hour and identified to species where possible.
  - Data file: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW
  - Data structure highlights:
    - Plot_ID, Collection_date, Collection_period (morning/midday/afternoon), Invasion_status, Collection_location
    - Ground_temperature (C), # of species, presence/absence per ant species

- Experiment 2: Seed removal
  - Objective: compare dispersal rates of seeds in invaded vs non-invaded sites.
  - Design: 60 seed hubs (10 per site) across six transects; each hub with eight seeds from two randomly chosen plant species (12 total species); elaiosomes removed for half the seeds in lab.
  - Timing: seeds placed at 08:00 and surveyed hourly up to 3 hours; a second survey at 13:00 to test temporal effects; run for three weeks.
  - Totals: 5840 seeds used (1960 invaded, 3880 non-invaded).
  - Data file: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW
  - Data structure highlights:
    - seedhub_id, locality, plant_species, ant_community, period (Morning/Afternoon)
    - elaiosome presence/absence, seed_number_removed (0/1), start_time, end_time, duration metrics

- Experiment 3: Seed fate
  - Objective: quantify seed transport and fate mediated by individual ant species.
  - Method: for each ant species, twenty nests across six transects; nest-scale seed mix (three seeds from each of six plant species: three invasive, three native) scattered near nest entrances; seeds in perforated lids weighed and secured to measure removal into nests after 24 hours; nest casts to determine seed placement depth.
  - Seed fate: two outcomes per seed (transport into nest = 1, abandonment above-ground = 0).
  - Nest architecture: plaster casts to locate seeds within nest depths (0–12 cm, 13–24 cm, >25 cm).
  - Data file: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW
  - Data structure highlights:
    - ant_status (native/invasive), nest_id, ant_genus, plant_species, plant_status (native/invasive)
    - on_surface, removed_into_nest, 0_12_cm, 13_24_cm, >25_cm

- Data management and accessibility
  - All experiments report RAW data to preserve original observations for verification and reanalysis.
  - Encouraged practices align with environmental monitoring: standardized methods, rigorous QA/cleaning, and transparent storage for portal upload and downstream analyses.
  - Potential for data integration with other environmental datasets to enhance value and enable broader accessibility beyond the immediate study outputs.

- Implications for environmental monitoring
  - Provides baseline metrics for invaded vs non-invaded environments in terms of ant community structure, seasonal activity, and plant seed dispersal dynamics.
  - Supports assessment of how invasive species influence mutualisms (myrmecochory) and seed fate, informing management and policy decisions in the CFR and similar ecosystems.
  - Highlights the importance of making underlying data openly accessible to enable cross-study comparisons and long-term monitoring.