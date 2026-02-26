# Study across four sites evaluating the impact of L. humile invasion on myrmecochorous seed dispersal and ant communities

## Overview
- Field study conducted in 2014–2015 across four sites to compare invaded vs non-invaded conditions regarding ant communities and seed dispersal of myrmecochorous plants.
- Two invaded sites (Montilivi Campus and Castell d'Aro) and two non-invaded sites (Montilivi Campus and Santuari dels Angels) across cork-oak secondary forest with Quercus and Pinus species.
- Data are RAW, unmodified, collected across multiple trials and experiments.

## Study area and invasion status
- Sites include:
  - Site 1: Montilivi Campus – invaded by L. humile
  - Site 2: Castell d'Aro – invaded by L. humile
  - Site 3: Montilivi Campus – non-invaded
  - Site 4: Santuari dels Angels – non-invaded
- Vegetation: open cork-oak secondary forest with herbaceous myrmecochorous plants in clearings.

## Experimental design and methods

- Experiment 1: Pitfall trapping
  - Two 100 m transects per site; traps every 5 m.
  - Traps: 50 ml propylene glycol in 150 ml beakers, buried flush; left 72 hours.
  - Ants identified to species where possible; goal to determine community composition by invasion status.
  - Data file: Devenish_Experiment_1_ant_community_PITFALL_RAW

- Experiment 1: Baiting
  - 10 baits per transect at 10 m intervals; bait = 5 g tuna/honey (5:1) on a card.
  - Baits deployed at 07:00, 11:00, 15:00, 19:00; ants collected after 1 hour.
  - Data file: Devenish_Experiment_1_ant_community_BAITING_RAW

- Experiment 2: Seed removal
  - Seed hubs: 10 hubs per site along transects; each hub has six seeds (two plant species, three seeds each).
  - Seeds accessible to ants via dome mesh; survey at 0.5, 1, 2, 3, 6, 12, 24 hours.
  - Six consecutive days; total 869 seeds used (439 invaded, 439 non-invaded).
  - Data files: Devenish_Experiment_2_seed_dispersal_HUB_RAW and Devenish_Experiment_2_seed_dispersal_SurvA_RAW
  - Data structure highlights: hub location, invasion status, seeds removed, plant species, elaiosome presence, seed fate, and timing.

- Experiment 3: Nest distribution
  - For each site, 5 randomly placed quadrats (each 30.25 m²) with 144 baited cards.
  - Cards observed 8:00–12:00 for 10 consecutive days to count nests and trails.
  - Nest density estimated; trails used to infer nest size.
  - Data file: Devenish_Experiment_3_nest_distribution_RAW
  - Data structure highlights: grid ID, location, grid scores, total positive grid cells.

- Experiment 4: Seed fate
  - 20 nests invaded (Castell d'Aro) and 20 nests non-invaded (Montilivi Campus).
  - Each nest received 40 seeds (20 Genista monspessulana, 20 Sarothamnus arboreus); seeds placed within 5 cm of nest entrance.
  - Seeds observed until all taken; surface seeds covered overnight if needed; 72-hour check and excavation to 10 cm depth for seeds.
  - Data file: Devenish_Experiment_4_seed_fate_RAW
  - Data structure highlights: plant species, nest ID, invasion status, seeds removed/retrieved from nest or refuse, and fate unknown.

## Data management and structure
- All experiments provide RAW data files with detailed column-level structures:
  - Experiment 1 Pitfall: Collection code, location, date, transect/hub codes, species counts.
  - Experiment 1 Baiting: Collection code, date, regional code, collection period, species presence/absence counts.
  - Experiment 2 Seed Dispersal: Hub location, invasion status, seeds removed; plant species, elaiosome, seed fate, times.
  - Experiment 3 Nest Distribution: Grid ID, location, grid references/scores, count of positive cells.
  - Experiment 4 Seed Fate: Plant species, nest ID, invasion status, seed removals/retrievals, refuse seeds, unknown fate.
- Data are deliberately untransformed to preserve raw measurements.

## Key aims and potential analyses
- Compare ant community composition between invaded and non-invaded sites using pitfall and bait data.
- Assess seed dispersal efficiency and patterns in invaded vs non-invaded contexts via seed removal and seed fate experiments.
- Quantify nest density and nest size differences through nest distribution data.
- Link seed fate outcomes to the presence of specific ant communities (e.g., L. humile vs P. pallidula) and invasion status.
- Integrate multi-experiment data to identify correlations between invasion status and ecological processes in ant-mediated dispersal.