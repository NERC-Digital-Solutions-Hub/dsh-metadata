# Study area: The study was conducted within the Jonkershoek Nature Reserve (33°55'51"S, 18°51'16"E), in November 2014 - February 2015 and January - February 2017, when myrmecochorous seeds were naturally dispersing.

## Overview
- Study location: Jonkershoek Nature Reserve within the Boland Mountain Complex, CFR, South Africa.
- Focus: Interactions between invasive Argentine ants (Linepithema humile), Australian wattles (Acacia spp.), and myrmecochorous seed dispersal.
- Data scope: RAW (unmodified) data collected across all trials.
- Experimental scope: Three related experiments examining ant communities, seed removal, and seed fate across invaded and non-invaded sites.
  
## Datasets and data structures

- Experiment 1: Pitfall trapping
  - File: Devenish_Jonkershoek_Experiment_1_ant_community_PITFALL_RAW
  - Data structure (typical fields):
    - Collection_code
    - Collection_location (Transect Code, 11 factors)
    - Collection_date
    - Invasion_status (invaded vs non-invaded)
    - Sample_number (Transect Code + Hub #)
    - Ant species counts (columns F-AT)
- Experiment 1: Baiting
  - File: Devenish_Experiment_Jonkershoek_1_ant_community_BAITING_RAW
  - Data structure:
    - Collection_code
    - Plot_ID (Transect Code + Hub #)
    - Collection_date
    - Collection_period (morning, midday, afternoon)
    - Invasion_status
    - Collection_location (Transect Code)
    - Ground_temperature_C
    - #_of_Species
    - Ant species presence/absence (I-X; 1/0)
- Experiment 2: Seed removal
  - File: Devenish_Jonkershoek_Experiment_2_seed_dispersal_HUB_RAW
  - Data structure:
    - seedhub_id (Transect Code + Hub #)
    - locality (Transect factors)
    - plant_species
    - ant_community
    - period (Morning, Afternoon)
    - elaiosome (Present/Absent)
    - seed_number_removed (0/1)
    - start_time, end_time, duration_min, duration_hr
- Experiment 3: Seed fate
  - File: Devenish_Jonkershoek_Experiment_3_nest_seed_removal_FATE_RAW
  - Data structure:
    - ant_status (native/invasive)
    - nest_id
    - ant_genus
    - plant_species
    - plant_status (native/invasive)
    - on_surface (numeric)
    - removed_into_nest (numeric)
    - 0_12_cm, 13_24_cm, >25_cm (numeric)

## Spatial and GIS considerations
- Location identifiers: transect codes and hub numbers enable spatial linking across datasets.
- Spatial outputs possible: maps of invasion distribution, trap locations, baiting points, seed hubs, ant nests, and seed fate outcomes.
- Temporal aspects: timestamps, collection dates, survey periods, and durations enable spatiotemporal analyses.

## Data quality, preparation, and challenges
- RAW data: no transformations or normalisations applied; require cleaning, standardisation, and documentation.
- Data are distributed across multiple files with varying schemas and naming conventions.
- Challenges include: data held in many places, potential resolution mismatches, and need for consistent data standards.

## How GIS specialists can use this data
- Create spatial layers for:
  - Invaded vs non-invaded areas (based on invasion_status)
  - Transects, hubs, pitfall locations, baiting plots
  - Seed hubs and nest locations with time attributes
- Combine datasets to analyze:
  - Ant species richness and community composition by location and time
  - Seed removal rates by site invasion status and plant species
  - Seed fate by ant status (native vs invasive) and nest depth locations
- Integrate environmental context:
  - Ground temperature as a contextual layer for baiting outcomes
- Support mapping and visualization for policy, stakeholders, or public communication

## Practical recommendations for data handling
- Establish a common metadata framework aligning field identifiers (transect, hub, plot) across experiments.
- Normalize column naming conventions and document data dictionaries for cross-dataset joins.
- Use join keys such as Transect Code, Hub #, and collection_location to harmonize datasets.
- Process time-related fields (start_time, end_time, duration) into unified timestamps where needed.
- Create quality checks to identify missing or inconsistent invasion_status and species identifiers.

## Endnotes on scope and use
- Data are designed for map-based, spatially explicit analyses of ant invasion and seed dispersal processes.
- A careful data integration plan is essential to leverage the full set of experiments for GIS-based visualization and spatial statistics.