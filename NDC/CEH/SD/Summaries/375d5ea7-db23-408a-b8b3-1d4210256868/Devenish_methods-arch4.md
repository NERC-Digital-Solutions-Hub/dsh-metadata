# Study area: The study was conducted across four sites in June-July 2014 and July-September 2015, when myrmecochorous seeds would naturally be dispersing.

## Overview
- Examines how invasive ants (L. humile) affect ant communities and myrmecochorous seed dispersal.
- Four study sites: two invaded and two non-invaded.
- Vegetation: open cork-oak secondary forest with Quercus and Pinus; presence of herbaceous myrmecochorous plants.
- All data files contain RAW data and have not been transformed or normalised.

## Sites and invasion status
- Invaded sites: Montilivi Campus (Site 1) and Castell d'Aro (Site 2).
- Non-invaded sites: Montilivi Campus (Site 3) and Santuari dels Angels (Site 4).
- Data collected across four experiments targeting ant communities, seed dispersal, and seed fate.

## Data collection approach and RAW data principle
- Data across all experiments are RAW and unmodified.
- Data files use explicit naming to indicate experiment, data type, and RAW status.
- Data capture spans spatial (across four sites) and temporal dimensions (multiple days and times).

## Experiment 1: Pitfall trapping
- Purpose: Assess ant community composition via pitfall traps.
- Methods:
  - At each site: two 100 m transects with traps every 5 m.
  - Traps: 50 ml propylene glycol in 150 ml beakers, buried flush.
  - Traps left for 72 hours; ants identified to species where possible.
- Data file: Devenish_Experiment_1_ant_community_PITFALL_RAW
- Data structure:
  - Column A: Collection Code (text)
  - Column B: Collection location (text)
  - Column C: Sample collection date (date)
  - Column D: Collection reference (Transect Code [8 factors] + Hub # [20 factors])
  - Columns E onward: Ant species (count data)

## Experiment 1: Baiting
- Purpose: Track temporal shifts in ant community at baits.
- Methods:
  - Ten baits per transect at 10 m intervals; bait = 5 g tuna/honey on a card.
  - Bait checks at 7:00, 11:00, 15:00, 19:00; ants collected after 1 hour and identified.
- Data file: Devenish_Experiment_1_ant_community_BAITING_RAW
- Data structure:
  - Column A: Collection Code (text)
  - Column B: Sample collection date (date)
  - Column C: Regional code (eight factors: A–H)
  - Column D: Collection Period (morning, midday, afternoon, evening)
  - Column E: Number of species identified (count data)
  - Columns F–Y: Ant species (three factors: n/a, present, absent)

## Experiment 2: Seed removal
- Purpose: Investigate seed dispersal rates in invaded vs non-invaded sites.
- Methods:
  - Ten seed hubs per site along a transect (10 m intervals); seeds accessible to ants but protected from larger fauna.
  - Each hub: six seeds (three from each of two plant species).
  - Seeds placed at 08:00; surveyed at 0.5, 1, 2, 3, 6, 12, 24 hours; run for six consecutive days.
  - Total seeds used: 869 (439 invaded, 439 non-invaded).
- Data file 1: Devenish_Experiment_2_seed_dispersal_HUB_RAW
  - Data structure:
    - Column A: Seed hub location (transect name + seed hub #)
    - Column B: Ant community invasion status (invaded, non-invaded)
    - Column C: Number of seeds removed (count data)
- Data file 2: Devenish_Experiment_2_seed_dispersal_SurvA_RAW
  - Data structure:
    - Column A: Seed hub location (transect name + seed hub #)
    - Column B: Ant community invasion status (invaded, non-invaded)
    - Column C: Plant species (ten species: listed)
    - Column D: Elaiosome condition (present [1] / absent [0])
    - Column E: Seed status (not-removed [0] / removed [1])
    - Column F: Start time of seed trial
    - Column G: End time of seed trial
    - Column H: Length of time until seed removal/not-removed

## Experiment 3: Nest distribution
- Purpose: Compare nest distribution for dominant seed-dispersing ants across invaded and non-invaded sites.
- Methods:
  - 4 sites (2 invaded, 2 non-invaded); within each site, 5 randomly placed quadrats (30.25 m²).
  - Each quadrat: 144 white cards with 5 g tuna/honey bait; observed 8:00–12:00 for 10 consecutive days.
  - Nests identified by tracking trails back from cards.
  - Nest presence scored (1 = nest present) and number of trails to nest counted.
  - Trails beyond the grid excluded.
- Data file: Devenish_Experiment_3_nest_distribution_RAW
- Data structure:
  - Column A: Grid ID (location status [invaded/non-invaded] + grid #)
  - Column B: Location of the Grid (text)
  - Columns C–DS: Grid reference and score for Rows A–K and Lines 1–11 (count data)
  - Column DU: Total number of grid cells with value > 0 (numeric)

## Experiment 4: Seed fate
- Purpose: Determine depth-related fate of introduced seeds within ant nests.
- Methods:
  - 20 nests in invaded locality (Castell d'Aro) and 20 nests in non-invaded locality (Montilivi Campus).
  - Seeds: 40 seeds per nest (20 Genista monspessulana, 20 Sarothamnus arboreus).
  - Seeds placed within 5 cm of nest entrance; monitored until all seeds were taken (approx. 30 minutes).
  - If seeds remained, covered overnight; next morning surface seeds collected; nest excavated to 10 cm depth; soil sieved to collect buried seeds.
  - Depths beyond 10 cm not explored.
- Data file: Devenish_Experiment_4_seed_fate_RAW
- Data structure:
  - Column A: Plant species (Genista monospessulana, Sarothamnus arboreus)
  - Column B: Nest ID (Nest status [invaded/non-invaded] + number)
  - Column C: Ant community status (invaded, non-invaded)
  - Column D: Total seeds removed into the nest (numeric)
  - Column E: Total seeds retrieved from nest (numeric)
  - Column F: Total seeds retrieved from aboveground refuse piles (numeric)
  - Column G: Total seeds not found; fate unknown (numeric)

## Data governance and notes for Data Leaders
- RAW data: All collected data remain unmodified across experiments, enabling auditability and re-use.
- Data discoverability: File names encode experiment, data type, and RAW status to aid locating and understanding datasets.
- Data structure clarity: Each experiment defines explicit column schemas (counts, presence/absence, times, spatial identifiers), facilitating cross-experiment integration and meta-analysis.
- Invasion-status framing: A consistent INVADED vs NON-INVADDED dichotomy underpins comparisons of ant communities and seed dispersal outcomes.
- Opportunities for data strategy:
  - Documentation of metadata standards to accompany RAW files (locations, dates, transect/hub identifiers, and treatment statuses).
  - Cross-site harmonisation of data schemas to simplify aggregation and comparative analyses.
  - Assessment of data gaps (e.g., variable data richness across experiments) and potential standardisation of measurement units and time points.
  - Potential for building a data catalogue that links these RAW datasets to derived metrics (e.g., nest density, seed removal rates, foraging activity).

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle from field collection to structured RAW datasets across multiple experiments and sites.
- Highlights the importance of consistent metadata, clear file naming, and explicit data schemas to support multi-site data integration and comparative analytics.
- Provides a basis for developing data governance practices around ecological monitoring, including data quality, provenance, and discoverability in multi-partner networks.