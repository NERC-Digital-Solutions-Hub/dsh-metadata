# Jonkershoek Ant Invasion and Seed Dispersal Experiments

## Overview
- Study location: Jonkershoek Nature Reserve, Boland Mountain Complex, Cape Floristic Region, South Africa.
- Timeframe: November 2014–February 2015 and January–February 2017.
- Focus: Myrmecochorous seed dispersal in sites with invasive Argentine ant (Linepithema humile) and Australian wattles (Acacia spp.).
- Data status: All files contain RAW, unmodified data collected across trials.

## Datasets Collected (by Experiment)

### Experiment 1: Pitfall Trapping
- File: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW
- Purpose: Compare ant communities in invaded vs. non-invaded areas (presence of L. humile).
- Data structure (selected columns):
  - Collection_code, Collection_location (Transect Code), Collection_date, Invasion_status (invaded vs. non-invaded), Sample_number, Ant species (count data).
- Notes: Follows methods from Devenish et al. (2019).

### Experiment 1: Baiting
- File: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW
- Purpose: Assess temporal shifts in ant community composition at baits (presence/absence by species).
- Data structure (selected columns):
  - Collection_code, Plot_ID (Transect Code + Hub), Collection_date, Collection_period (morning/midday/afternoon), Invasion_status, Collection_location, Ground_temperature_C, #_of_Species (count), Ant species (presence/absence per time period).
- Notes: Baiting conducted at 08:00, 12:00, 16:00; species identified where possible.

### Experiment 2: Seed Removal
- File: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW
- Purpose: Compare dispersal rates in invaded vs. non-invaded sites using seed hubs.
- Data structure (selected columns):
  - seedhub_id, locality, plant_species, ant_community, period (Morning/Afternoon), elaiosome_present/absent, seed_number_removed (binary), start_time, end_time, duration_min, duration_hr.
- Experimental design: 60 seed hubs across six transects; eight seeds per hub (two species per hub); 5840 seeds total (1960 invaded, 3880 non-invaded).

### Experiment 3: Seed Fate
- File: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW
- Purpose: Determine seed transport to ant nests and nesting depth placement.
- Data structure (selected columns):
  - ant_status (native vs. invasive), nest_id, ant_genus, plant_species, plant_status (native vs. invasive), on_surface, removed_into_nest, 0_12_cm, 13_24_cm, >25_cm.
- Method: For each ant species, twenty nests (≥10 m apart) across six transects; seeds from three invasive and three native plant species placed near nest entrances; 24-hour exposure; nest casts used to locate seeds within nest depths.

## Data Structure, Variables, and Metadata Considerations
- Cross-experiment linkage: Multiple experiments on related topics (invasion status, ant communities, and seed dispersal/fate) using transect and hub codes to identify locations.
- Key variables:
  - Invasion_status and plant_status for distinguishing invaded vs. non-invaded contexts.
  - Ant_species counts and presence/absence indicators for community composition.
  - Temporal factors: collection_date, collection_period, start_time, end_time, duration.
  - Environmental context: ground_temperature_C.
  - Seed fate outcomes: binary transport to nest and depth distribution.
- Units and formats:
  - Dates as date fields; times as time fields; temperatures in Celsius; durations in minutes/hours.
  - Categorical indicators (e.g., presence/absence, invaded/non-invaded) with explicit coding in the data files.

## Data Quality, Governance, and Stewardship Considerations
- RAW status: Data are untransformed; suitable for reproducibility but require careful documentation and standardization before sharing or meta-analysis.
- Metadata gaps: While file names and column headers provide structure, additional metadata is needed (data collection protocols, transect/hub coding schemes, species taxonomy references, units, data processing steps, and any edition history).
- Data standardization:
  - Harmonize transect codes and hub identifiers across experiments.
  - Ensure consistent taxonomic naming conventions for ant species and plant species.
  - Document data collection methods and any deviations from protocol.
- Quality assurance recommendations:
  - Implement data validation rules (e.g., plausible ranges for counts, dates, times).
  - Cross-check invasion status assignments with site records and logs.
  - Record any missing values and rationale for omissions.
- Data sharing and governance:
  - Define a data license, DOI, and citation guidance.
  - Establish a central data portal or repository to host the RAW files with accompanying metadata and a data dictionary.
  - Create version-controlled data releases to support updates and reuse.

## Practical Implications for Data Stewards
- Creating usable datasets from RAW data will require:
  - Comprehensive metadata documentation (data dictionary, protocols, codes, and units).
  - A harmonized schema across all experiments to enable integrated analyses (e.g., linking invasion status to seed dispersal outcomes).
  - Clear data governance policies (licensing, access controls, and update processes) to facilitate discoverability, reuse, and long-term preservation.
- Potential reuse scenarios:
  - Assessing how the presence of L. humile influences ant community structure and seed dispersal dynamics.
  - Analyzing seed fate in relation to ant species, nest depth, and native vs. invasive plant interactions.
  - Integrating with broader CFR datasets to study invasion biology, seed dispersal, and ecosystem impacts.

## Endnotes
- The study explicitly notes that all data are RAW and have not been modified or normalized, underscoring the need for thorough metadata and careful governance to enable robust reuse.