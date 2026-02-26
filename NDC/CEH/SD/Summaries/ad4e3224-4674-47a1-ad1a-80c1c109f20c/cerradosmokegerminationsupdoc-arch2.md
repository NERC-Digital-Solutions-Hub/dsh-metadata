# CerradoSpeciesGermination_BrazilianSmokeWater.csv

- Purpose and context
  - Data from germination experiments assessing the effect of smoke-water on native Cerrado species.
  - Includes species-level, collection-site, treatment, and daily germination observations suitable for monitoring environmental germination responses over time.

- Data structure and key columns (main CSV)
  - Species: species name; includes notes for Vellozia squamata with site-specific identifiers.
  - Collection_site: site of seed collection (details provided in Table 1).
  - Collection_date: date seeds were collected.
  - Experiment_date: date the germination experiment was conducted.
  - Treatment: Control (Control_SW) or smoke-water treated (SW).
  - Replicate: number of replicates (typically 5 per experiment).
  - Viable_seeds, Dead_seeds, Total_seeds: viability counts used to constrain potential germination.
  
- Smoke treatment and experimental design
  - Smoke solution: seeds exposed to smoke-water at 1:1 concentration; 24 hours imbibition at room temperature.
  - Control: seeds imbibed in distilled water for 24 hours.
  - Smoke preparation: biomass (5 g) from native grasses heated at 200°C for 30 minutes, soaked in 50 ml distilled water for 10 minutes, filtered; solutions prepared separately per replicate.
  - Post-imbibition: seeds placed on double-filter-paper with distilled water; germination chambers set to 27°C with a 12 h light/12 h dark cycle.
  - Observations: monitored every 2 days for up to 30 days; germination defined by radicle emergence.
  - Viability checks: non-germinated seeds tested with 1% tetrazolium solution (pH 7).

- Data collection and quality control
  - Data recorded manually and curated in spreadsheets.
  - Collection seed quality constrained by viability tests, used to bound maximum potential germination.

- Daily germination data (structure highlights)
  - Day: number of days since imbibition.
  - Germinated: number of seeds germinated on that day (non-cumulative).

- Collection sites and metadata (Table 1 overview)
  - Provides site abbreviations, full names, locations, and geographic coordinates for seed sources.
  - Sites include EEI (Itirapina, SP), RNST (Cavalcante, GO), Jalapão (Mateiros, TO), SC (Serr­a do Cipó; MG), Pirenópolis (GO), EESB (Santa Bárbara, SP), PNSV (Diamantina, MG).
  - Coordinates provided for precise geolocation.

- Smoke-treated regeneration dataset (CerradoSpeciesGermination_RegenSmokeWater.csv)
  - Species-level germination data under regeneration-smoke conditions.
  - Treatments: Control, Smoke_I (2.5% smoke-water), Smoke_II (5.0% smoke-water).
  - Replicates: typically 3 to 5 per species/condition.
  - Daily observations: Day and Germinated (daily germination counts, not cumulative).

- Experimental specifics for RegenSmokeWater
  - Seed preparation and incubation: non-scarified diaspores placed in Petri dishes or boxes with smoke solutions or distilled water; 24 hours at 27°C in darkness; post-imbibition adjustments to 12 h photoperiod and 27°C.
  - Volume per replicate: 3 mL (small diaspores) or 5 mL (larger diaspores).
  - Observations: daily up to 30 days or until germination stabilizes (no germination for 10 consecutive days).

- Data sources and references
  - Foundational methods and context from:
    - Le Stradic et al., 2015; Fichino et al., 2016; Jäger et al., 1996; Lakon, 1949; Moreira et al., 2010.
  - Methodologies cover germination testing, smoke-related germination cues, and tetrazolium viability assays.

- Relevance for environmental monitoring
  - Provides standardized, QA-conscious datasets linking seed germination responses to smoke cues across multiple Cerrado species and sites.
  - Outputs are suitable for integration into broader environmental health datasets, enabling temporal trend analyses and policy performance assessments.
  - Emphasizes reproducibility through explicit treatment preparations, replicate handling, and data curation steps.

- Practical considerations for analysts
  - Standardized data capture facilitates cross-site comparisons and longitudinal monitoring.
  - Viability constraints help interpret germination outcomes within environmental health assessments.
  - Site coordinates and metadata support geospatial analyses and integration with other environmental indicators.
  - Explicit replication and treatment details support data sharing and reuse, aligning with environmental data portals and interoperable datasets.