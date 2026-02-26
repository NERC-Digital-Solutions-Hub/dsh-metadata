# Study area: The study was conducted within the Jonkershoek Nature Reserve (33°55'51"S, 18°51'16"E), in November 2014 - February 2015 and January - February 2017, when myrmecochorous seeds were naturally dispersing.

## Context and setting
- Location: Jonkershoek Nature Reserve, part of the Boland Mountain Complex in the Cape Floristic Region, South Africa.
- Focus: Interactions between invasive Argentine ants (Linepithema humile) and Australian wattles (Acacia spp.) and their effect on myrmecochorous seed dispersal.
- Data status: All data are RAW (unmodified) across trials.

## Data and formats
- Data are organized into three experiments (pitfall trapping, baiting, seed dispersal) and a seed fate assessment.
- File naming and data structures are provided for each experiment, with explicit column definitions.

## Experiment 1: Pitfall trapping
- Objective: Assess ant community composition in invaded vs non-invaded areas using pitfall traps.
- File: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW
- Data structure (Columns):
  - A: Collection_code (text)
  - B: Collection_location (Transect Code [11 factors])
  - C: Collection_date (date)
  - D: Invasion_status (text)
  - E: Sample_number (Transect Code [11 factors] + Hub # [20 factors])
  - F-AT: Ant species (count data)

## Experiment 1: Baiting
- Objective: Track temporal shifts in ant community composition at baits (presence/absence by species) across times of day.
- File: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW
- Data structure (Columns):
  - A: Collection_code (text)
  - B: Plot_ID (Transect Code [11 factors] + Hub # [20 factors])
  - C: Collection_date (date)
  - D: Collection_period (Morning/Midday/Afternoon)
  - E: Invasion_status (text)
  - F: Collection_location (Transect Code [11 factors])
  - G: Ground_temperature_(C) (value)
  - H: #_of_Species (count data)
  - I-X: Ant species (present=1, absent=0)

## Experiment 2: Seed removal
- Objective: Compare dispersal rates of seeds in invaded vs non-invaded sites using seed hubs and multiple plant species.
- Design: 60 seed hubs (10 per site) across six transects; eight seeds per hub (four per two randomly chosen plant species); elaiosomes removed for half of seeds.
- Repeats: Conducted over three weeks with two time surveys per day (08:00 and 13:00), total 5840 seeds (invaded n=1960; non-invaded n=3880).
- File: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW
- Data structure (Columns):
  - A: seedhub_id (Transect Code [11 factors] + Hub # [10 factors])
  - B: locality (Transect code [6 factors])
  - C: plant_species (text)
  - D: ant_community (text)
  - E: period (Morning/Afternoon)
  - F: elaiosome (Present/Absent)
  - G: seed_number_removed (0 = not removed, 1 = removed)
  - H: start_time (time)
  - I: end_time (time)
  - J: duration_min (time)
  - K: duration_hr (time)

## Experiment 3: Seed fate
- Objective: Determine, for each ant species, whether seeds are transported into nests or left above ground, and quantify nest depth placement.
- Design: For each ant species, 20 independent nests (≥10 m apart) across six transects; seed mix (three seeds each of six plant species; invasive and native) placed around nest entrances; seeds may be transported into nests or abandoned above ground. Nest casts used to assess ultimate seed placement depth.
- File: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW
- Data structure (Columns):
  - A: ant_status (native, invasive)
  - B: nest_id (text)
  - C: ant_genus (text)
  - D: plant_species (text)
  - E: plant_status (native, invasive)
  - F: on_surface (numeric)
  - G: removed_into_nest (numeric)
  - H: 0_12_cm (numeric)
  - I: 13_24_cm (numeric)
  - J: >25_cm (numeric)

## Key data considerations and potential data products
- RAW data: No transformations or normalisations applied; suitable for re-structuring into analysis-ready formats.
- Cross-experiment linking: Potential to merge on transect, hub, invasion_status, and collection_date to compare ant community dynamics with seed removal and fate.
- Data products for end users:
  - Ant community profiles by invasion status (pitfall and baiting data).
  - Seed removal rates by plant species, invasion status, and time of day.
  - Seed fate outcomes by ant species and nest depth occupancy.
- Practical implications for data use:
  - Evaluating how invasive ants influence seed dispersal and plant dynamics in CFR ecosystems.
  - Informing management decisions on invasive species control and native plant restoration.
- Limitations:
  - Data are untransformed RAW values; researchers will need to handle missing values, standardise species naming, and reconcile time formats for analysis.