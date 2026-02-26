# Study area and experimental data on ant community and seed dispersal in Jonkershoek Nature Reserve

- Location and timeframe
  - Jonkershoek Nature Reserve, Boland Mountain Complex, Cape Floristic Region, South Africa (33°55'51"S, 18°51'16"E)
  - Study periods: November 2014–February 2015 and January–February 2017
  - Focus on interactions between invasive Argentine ant (Linepithema humile) and Australian wattles (Acacia spp.)

- Data characteristics
  - All data are RAW, unmodified across trials
  - Data describe three interconnected experiments and associated data structures
  - File naming reflects experimental role and RAW status (e.g., Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW)

- Experiment 1: Pitfall trapping
  - Objective: Determine ant community composition in invaded vs non-invaded areas
  - Data file: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW
  - Data structure (columns)
    - Collection_code (text)
    - Collection_location (Transect Code; 11 factors)
    - Collection_date (date)
    - Invasion_status (text)
    - Sample_number (Transect Code + Hub; 20 factors)
    - Ant species (count data; columns F onward)

- Experiment 1: Baiting
  - Objective: Assess temporal shifts in ant community at baits (presence/absence by time of day)
  - Data file: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW
  - Data structure (columns)
    - Collection_code (text)
    - Plot_ID (Transect Code + Hub)
    - Collection_date (date)
    - Collection_period (morning, midday, afternoon)
    - Invasion_status (text)
    - Collection_location (Transect Code)
    - Ground_temperature_C (numeric)
    - #_of_Species (count data)
    - Ant species (present/absent; binary 1/0 across columns I-X)

- Experiment 2: Seed removal
  - Objective: Compare dispersal rates in invaded vs non-invaded sites using seed hubs and multiple plant species
  - Data file: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW
  - Data structure (columns)
    - seedhub_id (Transect Code + Hub)
    - locality (Transect factors)
    - plant_species (text)
    - ant_community (text)
    - period (Morning/Afternoon)
    - elaiosome (Present/Absent)
    - seed_number_removed (0/1)
    - start_time (time)
    - end_time (time)
    - duration_min (time)
    - duration_hr (time)
  - Experimental scale and context
    - 60 seed hubs across six transects; 5840 seeds total (1960 invaded, 3880 non-invaded)
    - Seeds from two plant species, with half of seeds having elaiosomes removed

- Experiment 3: Seed fate
  - Objective: Determine seed transport into ant nests and nest occupancy patterns; relate to nest structure
  - Data file: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW
  - Data structure (columns)
    - ant_status (native, invasive)
    - nest_id (text)
    - ant_genus (text)
    - plant_species (text)
    - plant_status (native, invasive)
    - on_surface (numeric)
    - removed_into_nest (numeric)
    - 0_12_cm (numeric)
    - 13_24_cm (numeric)
    - >25_cm (numeric)
  - Nest assessment
    - Twenty nests per ant species (native/invasive) across six transects
    - Seed mix: three invasive and three native plant species
    - Seeds placed around nest entrances; 24-hour assessment of transport into nests
    - Nest casts via plaster to locate seeds within nest depths (0–12 cm, 13–24 cm, >25 cm)

- Data management and usability notes for Data Leaders
  - RAW data across multiple experiments enable cross-experiment analyses of invasion effects on ant communities and seed dispersal
  - Detailed metadata in file and column descriptions support data discoverability and re-use
  - The data are organized by invasion status, transects, hubs, and time periods, with explicit treatment of presence/absence, abundance, and spatial depth

- Relevance to data strategy and governance
  - Illustrates integration of ecological experiments with consistent labeling, provenance, and raw-data integrity
  - Highlights the importance of clear invasion-status delineation and temporal sampling for user-centred data products and analyses
  - Demonstrates how multi-experiment data can inform understanding of data gaps, standardization needs, and cross-field collaboration in invasion ecology