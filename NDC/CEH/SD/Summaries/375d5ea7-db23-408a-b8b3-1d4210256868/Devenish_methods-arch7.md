# Devenish Study on Ant Communities and Seed Dispersal Across Invaded and Non-invaded Sites

- Study scope
  - Four study sites surveyed in two periods (June–July 2014 and July–September 2015) to capture myrmecochorous seed dispersal during peak activity.
  - Two sites invaded by Linepithema humile (L. humile) and two non-invaded sites; vegetation described as open cork-oak secondary forest with Quercus and Pinus, plus herbaceous myrmecochorous plants.
  - Exact site coordinates are provided for invaded and non-invaded locations.
  - All data files contain RAW, unmodified data.

- Data design and spatial framing (GIS-relevant)
  - Spatially defined components include transects, seed hubs, nests, and grid/quadrat layouts that support map-based analyses.
  - Four experiments generate multiple spatially-referenced data layers, enabling comparisons between invaded and non-invaded contexts.

- Experiment 1: Pitfall trapping
  - Aim: Characterize ant community composition via pitfall traps along transects.
  - Design: At each site, two 100 m transects with traps every 5 m (two transects per site; four transects per site total across sites).
  - Invasion definition: Invaded areas if L. humile present at any survey point; non-invaded otherwise.
  - Data products: Species counts by trap; location and timing metadata.
  - File: Devenish_Experiment_1_ant_community_PITFALL_RAW
  - Data structure highlights:
    - A: Collection Code; B: Location; C: Sample collection date; D: Transect code + hub factors; E-AI: Ant species counts.

- Experiment 1: Baiting
  - Aim: Assess temporal shifts in ant community at baits across the day.
  - Design: 10 baits per transect (10 m apart); bait exposure at four times (07:00, 11:00, 15:00, 19:00); 1 hour collection window.
  - Data products: Presence/absence or counts of ant species at each bait and time.
  - File: Devenish_Experiment_1_ant_community_BAITING_RAW
  - Data structure highlights:
    - A: Collection Code; B: Sample date; C: Regional code (A–H); D: Collection Period (morning, midday, afternoon, evening); E: Number of species identified; F-Y: Ant species presence/absence.

- Experiment 2: Seed removal
  - Aim: Compare seed dispersal rates between invaded and non-invaded sites using seed hubs.
  - Design: Ten seed hubs per site along transects; hubs allow ant access but exclude larger fauna; six seeds per hub (three from each of two plant species); seeds observed over multiple time points (0.5, 1, 2, 3, 6, 12, 24 hours); total 869 seeds used across four sites.
  - Data products: Seed removal counts; species-specific interactions; timing.
  - Files:
    - Devenish_Experiment_2_seed_dispersal_HUB_RAW
    - Devenish_Experiment_2_seed_dispersal_SurvA_RAW
  - Data structure highlights:
    - Hub-level: A: Seed hub location; B: Invasion status; C: Number of seeds removed; D–H: Species-specific and temporal details.

- Experiment 3: Nest distribution
  - Aim: Compare nest density and foraging trails between invaded and non-invaded sites.
  - Design: In each site, five randomly placed quadrats (30.25 m² total) containing 144 cards with bait; observations over 10 consecutive days (8:00–12:00). Card-level scoring for nest presence and number of trails.
  - Data products: Nest presence (0/1) and nest trail counts; nest density and trail-derived nest-size estimates.
  - File: Devenish_Experiment_3_nest_distribution_RAW
  - Data structure highlights:
    - A: Grid ID (status + grid number); B: Grid location; C-DS: Grid references/scores; DU: Total positive grid cells.

- Experiment 4: Seed fate
  - Aim: Determine seed fate in invaded vs non-invaded nests by deploying French broom (Genista monspessulana) and Black broom (Sarothamnus arboreus) seeds near nests.
  - Design: 20 invaded L. humile nests and 20 non-invaded P. pallidula nests; 40 seeds per nest (two species, 20 each) placed near nest entrances; monitoring to recover seeds from nests, surface, and refuse piles; excavation to 10 cm depth after 72 hours to recover buried seeds.
  - Data products: Counts of seeds removed to nests, retrieved from nests and refuse piles, and seeds with unknown fate.
  - File: Devenish_Experiment_4_seed_fate_RAW
  - Data structure highlights:
    - A: Plant species; B: Nest ID; C: Ant status; D: Total seeds removed; E: Seeds retrieved from nests; F: Seeds retrieved from refuse piles; G: Seeds not found/unknown fate.

- Practical GIS considerations and opportunities
  - Potential to build integrated GIS layers combining:
    - Site invasion status and coordinates
    - Transect lines and hub locations
    - Nest locations and nest density estimates
    - Seed hub positions and seed fate outcomes
    - Temporal sampling points for pitfall and bait experiments
  - Data cleaning and harmonization required to enable cross-experiment analyses and spatial comparisons.
  - Coordinate reference and precise georeferencing would enhance mapping of invasion patterns, movement corridors, and seed dispersal hotspots.
  - RAW data availability supports audit trails and reprocessing for GIS-ready datasets (post-cleaning, standardization, and joining by location identifiers such as site, transect, hub, nest, and grid IDs).

- Key considerations for future GIS work
  - Define consistent location identifiers across experiments (site, invaded status, transect/hub/nest IDs) to enable multi-layer joins.
  - Convert qualitative/categorical timing data (e.g., collection periods) into GIS-friendly time intervals or time stamps for temporal analyses.
  - Create species distribution and interaction rasters or vector layers (e.g., nest density maps, seed removal heatmaps) to visualize spatial patterns and compare invaded vs non-invaded contexts.
  - Document data provenance and ensure alignment with metadata standards to preserve RAW-to-cleaned data lineage.