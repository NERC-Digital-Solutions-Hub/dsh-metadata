# Study area: The study was conducted across four sites in June-July 2014 and July-September 2015, when myrmecochorous seeds would naturally be dispersing.

- Purpose: Investigate ant-mediated seed dispersal and ant community dynamics in invaded (L. humile present) vs non-invaded areas.
- Sites and invasion status:
  - Site 1: Montilivi Campus ( invaded )
  - Site 2: Castell d'Aro ( invaded )
  - Site 3: Montilivi Campus ( non-invaded )
  - Site 4: Santuari dels Angels ( non-invaded )
- Habitat context: Open cork-oak secondary forest with herbaceous myrmecochorous plants.
- Data scope: RAW data collected across all trials; no data transformation or normalisation applied.

## Experimental design and data collection

- Experiment 1: Pitfall trapping
  - Invasion-based site classification (invaded vs non-invaded) derived from L. humile presence during surveys.
  - Design: Two 100 m transects per site with pitfall traps every 5 m.
  - Trap setup: 50 ml propylene glycol in 150 ml beakers, buried flush; exposed 72 hours.
  - Outcome: Ant species identified to the extent possible.
  - Data file: Devenish_Experiment_1_ant_community_PITFALL_RAW
  - Data structure: A: Collection Code; B: Collection location; C: Sample collection date; D: Collection reference (Transect Code [8 factors] + Hub # [20 factors]); E-AI: Ant species (count data).

- Experiment 1: Baiting
  - Purpose: Assess temporal shifts in ant community composition at baits.
  - Design: Ten baits per transect at 10 m intervals; bait = 5 g tuna:honey (5:1) on 10 cm2 card.
  - Sampling times: 07:00, 11:00, 15:00, 19:00; collection after 1 hour; species identified where possible.
  - Data file: Devenish_Experiment_1_ant_community_BAITING_RAW
  - Data structure: A: Collection Code; B: Sample collection date; C: Regional code (eight factors A-H); D: Collection Period (morning, midday, afternoon, evening); E: Number of species identified; F-Y: Ant species (present/absent).

- Experiment 2: Seed removal (dispersal)
  - Design: Seed hubs along transects (10 hubs per site; 40 hubs total). Each hub with six seeds from two plant species; access limited to ants by mesh.
  - Protocol: Seeds surveyed at 0.5, 1, 2, 3, 6, 12, 24 hours; run for six days (one seed from each plant species per hub per day). Total seeds used: 869 (439 invaded, 439 non-invaded).
  - Data files:
    - Devenish_Experiment_2_seed_dispersal_HUB_RAW
      - Data structure: A: Seed hub location; B: Ant community invasion status (invaded/non-invaded); C: Number of seeds removed.
    - Devenish_Experiment_2_seed_dispersal_SurvA_RAW
      - Data structure: A: Seed hub location; B: Invasion status; C: Plant species; D: Elaiosome condition; E: Seed status; F: Start time; G: End time; H: Time until removal or last observation.

- Experiment 3: Nest distribution
  - Design: Compare nest distribution of dominant seed-dispersing ants in invaded vs non-invaded sites.
  - Setup: At each site, 5 random quadrats (30.25 m2) with 144 cards each containing bait; observed 4 hours daily for 10 days.
  - Outcomes: Nest presence/absence on cards; number of ant trails to nests; calculated nest density and inferred nest size from trails.
  - Data file: Devenish_Experiment_3_nest_distribution_RAW
  - Data structure: A: Grid ID (location status [invaded/non-invaded] + grid #); B: Location of the Grid; C-DS: Grid reference and score for Rows [A-K] and Lines [1-11] (count data); DU: Total number of grid cells with a value >0.

- Experiment 4: Seed fate
  - Design: Seed fate and depth assessment near nests; 20 invaded nests (Castell d'Aro) and 20 non-invaded nests (Montilivi Campus).
  - Seeds: 40 seeds per nest (20 Genista monspessulana; 20 Sarothamnus arboreus). Seeds placed within 5 cm of nest entrance.
  - Retrieval protocol: Observe for 30 minutes; cover if needed; inspect next morning; after 72 hours excavate nest to 10 cm depth and sieve for seeds.
  - Data file: Devenish_Experiment_4_seed_fate_RAW
  - Data structure: A: Plant species; B: Nest ID (status and number); C: Ant community status; D: Total seeds removed into nest; E: Seeds retrieved from nest; F: Seeds retrieved from aboveground refuse piles; G: Seeds not found (fate unknown).

## Data governance, quality, and interoperability considerations

- Data provenance and integrity
  - All data are RAW, with no transformations or normalisations applied.
  - Data include precise site coordinates and deployment details, enabling traceability back to field conditions.
  - File naming conventions clearly link data to specific experiments and data types.

- Metadata and standards
  - Consistent but diverse data structures across experiments (counts, presence/absence, time-based observations, and nest-trait metrics).
  - Metadata to capture for stewardship: exact coordinates, site status (invaded vs non-invaded), invasion history, dates of collection, method details (trap types, bait types, seed species, seed counts), units of measurement, taxonomic resolution, and any data exclusions or transformations.

- Data quality and usability
  - Some fields are categorical or binary (e.g., presence/absence, invasion status, elaiosome condition), while others are numeric counts or time intervals.
  - Image-like or coded fields (e.g., Region code, Transect Code, Grid references) require a controlled vocabulary or key to ensure consistency across datasets.
  - Potential ambiguities: identical coordinates used for different sites (e.g., Montilivi Campus appearing in multiple entries as both invaded and non-invaded) may need clarification or disambiguation in metadata.

- Accessibility and sharing
  - Data are described as RAW files; consider providing a standardized metadata schema (e.g., a data dictionary for each file, unit definitions, and a codebook for statuses and species names).
  - If sharing beyond the original researchers, include data dictionaries, species taxonomic references, and methodology notes to facilitate reuse.

- Practical data stewardship notes
  - Alignment of invasion status across experiments is essential for cross-study comparisons.
  - Ensure date formats are unambiguous (ISO 8601) and time-of-day stamps are consistently recorded.
  - Standardise location identifiers to avoid confusion where the same site appears under different statuses; include a site-level metadata row indicating coordinates, habitat type, and invasion history.
  - Document any data gaps, observations not captured, or deviations from the protocol (e.g., missed sampling times, trap loss, or seed hub failures).

## Key takeaways for data governance and future use

- The collection comprises four integrated experiments across four sites with invaded vs non-invaded conditions, focusing on ant communities and seed dispersal dynamics.
- RAW data span pitfall traps, baiting, seed removal, nest distribution, and seed fate, with detailed file-level and column-level structures provided.
- For robust reuse and interoperability, curate comprehensive metadata, unify site/invasion identifiers, and standardise time, date, and coordinate formats.
- The dataset supports comparative analyses of how L. humile invasion influences ant community composition, seed removal rates, nest density, and seed fate, with potential applications in invasion biology, ecology of seed dispersal, and conservation planning.