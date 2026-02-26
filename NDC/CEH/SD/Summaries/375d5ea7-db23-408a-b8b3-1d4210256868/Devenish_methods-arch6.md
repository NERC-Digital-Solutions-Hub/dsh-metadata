# Study area: The study was conducted across four sites in June-July 2014 and July-September 2015, when myrmecochorous seeds would naturally be dispersing.

## Overview
- A multi-site field study comparing invaded and non-invaded ant communities and their effects on seed dispersal and fate.
- Sites include two invaded and two non-invaded locations, with detailed geographic coordinates provided.
- All data are RAW (unmodified) and organized per experimental file names and data structures.

## Study Sites and Invasion Status
- Site 1: Montilivi Campus, invaded (L. humile) - 41°58'59.20"N, 02°49'29.75"E
- Site 2: Castell d'Aro, invaded (L. humile) - 41°49'04.61"N, 03°04'00.68"E
- Site 3: Montilivi Campus, non-invaded - 41°58'59.20"N, 02°49'29.75"E
- Site 4: Santuari dels Angels, non-invaded - 41°58'31.18"N, 02°54'34.02"E
- Vegetation: Open cork-oak secondary forest with Quercus and Pinus, including herbaceous myrmecochorous plants.
- Data scope: RAW data across all trials, not transformed.

## Experiment 1: Pitfall Trapping
- Aim: Assess ant community composition (species mean relative abundance) in invaded vs non-invaded areas.
- Methods:
  - Two 100 m transects per site; pitfall traps placed every 5 m.
  - Traps: 50 ml propylene glycol in 150 ml beakers, buried flush; 72-hour exposure.
  - Collection and species-level identification where possible.
- Data file:
  - Devenish_Experiment_1_ant_community_PITFALL_RAW
- Data structure (Column Summary):
  - Column A: Collection Code (text)
  - Column B: Collection location (text)
  - Column C: Sample collection date (date)
  - Column D: Collection reference (Transect Code [8 factors] + Hub # [20 factors])
  - Columns E–AI: Ant species (count data)

## Experiment 1: Baiting
- Aim: Capture temporal shifts in ant community composition (presence/absence at baits) throughout the day.
- Methods:
  - Ten baits per transect at 10 m intervals.
  - Bait: 5 g tuna/honey (5:1) on a 10 cm2 card.
  - Collection times: 7:00, 11:00, 15:00, 19:00; ants collected after 1 hour; identified where possible.
- Data file:
  - Devenish_Experiment_1_ant_community_BAITING_RAW
- Data structure (Column Summary):
  - Column A: Collection Code (text)
  - Column B: Sample collection date (date)
  - Column C: Regional code (eight factors: A–H)
  - Column D: Collection Period (morning, midday, afternoon, evening)
  - Column E: Number of species identified (count data)
  - Columns F–Y: Ant species (three factors: n/a, present, absent)

## Experiment 2: Seed Removal
- Aim: Compare dispersal rates of seeds in invaded vs non-invaded sites using seed hubs.
- Methods:
  - Ten seed hubs per site along a transect; each hub accessible to ants but protected from larger fauna.
  - Each hub: white card with dome mesh; six seeds from two random plant species (ten species total used in section 2.2).
  - Seed survey times: 0.5, 1, 2, 3, 6, 12, 24 hours; repeat for six days (869 seeds total; 439 invaded, 439 non-invaded).
- Data files:
  - Devenish_Experiment_2_seed_dispersal_HUB_RAW
    - Column A: Seed hub location (transect name + seed hub #)
    - Column B: Ant community invasion status (invaded, non-invaded)
    - Column C: Number of seeds removed (count data)
  - Devenish_Experiment_2_seed_dispersal_SurvA_RAW
    - Column A: Seed hub location (transect name + seed hub #)
    - Column B: Ant community invasion status (invaded, non-invaded)
    - Column C: Plant species name (ten species)
    - Column D: Elaiosome condition (present=1, absent=0)
    - Column E: Seed status (not removed=0, removed=1)
    - Column F: Start time of seed trial
    - Column G: End time of seed trial
    - Column H: Length of time till seed removed/not-removed (End - Start)

## Experiment 3: Nest Distribution
- Aim: Compare spatial distribution and nest characteristics of dominant seed-dispersing ants in invaded vs non-invaded sites.
- Methods:
  - In each site, 5 randomly placed quadrats (30.25 m2 total); each quadrat contains 144 white cards with 5 g tuna/honey bait.
  - Observations over 4 hours per day for 10 consecutive days; nests located by following ant trails to cards.
  - Nest presence scored (1) vs absence (0) per card; nest density estimated; number of trails used to estimate nest size.
  - Trails beyond grid not included.
- Data file:
  - Devenish_Experiment_3_nest_distribution_RAW
- Data structure (Column Summary):
  - Column A: Grid ID (location status: invaded/non-invaded + grid #)
  - Column B: Location of the Grid (text)
  - Columns C–DS: Grid reference and scores for Rows [A–K] and Lines [1–11] (count data)
  - Column DU: Total number of grid cells with value > 0 (numeric)

## Experiment 4: Seed Fate
- Aim: Determine seed fate and depth outcomes for two non-native plant species within invaded vs non-invaded nests.
- Methods:
  - 20 nests in invaded locality (Castell d'Aro) and 20 nests in non-invaded locality (Montilivi Campus).
  - Each nest received 40 seeds: 20 Genista monspessulana (French broom) and 20 Sarothamnus arboreus (Black broom).
  - Seeds placed within 5 cm of nest entrance; observed for 30 minutes until all seeds taken into nest; surface seeds covered overnight if necessary.
  - After 72 hours, a 20 cm radius around nest entrance inspected; nest excavated to 10 cm depth; soil panned to retrieve seeds; depths >10 cm not excavated.
- Data file:
  - Devenish_Experiment_4_seed_fate_RAW
- Data structure (Column Summary):
  - Column A: Plant species used (Genista monospesulana, Sarothamnus arboreus)
  - Column B: Nest ID (Nest status invaded/non-invaded + number)
  - Column C: Ant community status (invaded, non-invaded)
  - Column D: Total number of seeds removed into the ant nest
  - Column E: Total number of seeds retrieved from the ant nest
  - Column F: Total number of seeds retrieved from aboveground refuse piles
  - Column G: Total number of seeds not found; fate unknown

## Cross-Experiment Data and Product Opportunities
- Core linking variables:
  - Invasion status (invaded vs non-invaded)
  - Site identity (four sites with coordinates)
  - Temporal data points (collection dates and times)
- Potential data products:
  - Ant community profiles by site and invasion status (species abundance, presence/absence)
  - Temporal dynamics of ant activity from baiting data
  - Seed removal rates by species and invasion status, with time-to-removal analyses
  - Nest density and nest size estimates by site/status from nest distribution
  - Seed fate outcomes (retrieval vs not retrieved, depth distribution) across species and nests
- Data considerations:
  - RAW data requires cleaning/normalization prior to cross-experiment integration
  - Differences in data structures across experiments; careful harmonization needed for dashboards or self-serve analyses

## Considerations for Data Use and Quality
- Data are raw and untransformed; users should apply appropriate quality checks, standardization, and potential metadata enrichment.
- Invasive status is tied to specific sites, with two invaded and two non-invaded locations; coordinate-level data support spatial analyses.
- Data collection periods span 2014–2015; date/time fields should be standardized to enable temporal comparisons.