# Metadata for: MultihostCoinfectionData.csv

- Data origin and purpose
  - Generated from a mesocosm experiment in summer 2018 at the Institute of Zoology, ZSL.
  - Objective: determine how prevalence and mean intensity of Bd (Batrachochytrium dendrobatidis) and ranavirus (Rv) infections are influenced by host community composition (toads Bufo bufo and frogs Rana temporaria) and history of exposure to the pathogens.

- Experimental design
  - Host community compositions: toad tadpoles only, frog tadpoles only, or a 50/50 mixed community.
  - Exposure regimes (four total), across two phases:
    - Phase 1: Bd exposure via zoospores in media or sterile media (control).
    - Phase 2: Ranavirus exposure via three Rv-positive frog corpses or three Rv-negative corpses (control) in treatment tanks.
  - Treatments: 12 distinct combinations (4 exposure regimes × 3 community types), each with six replicates.
  - Duration: six weeks.

- Exposure treatments
  - Control: Phase 1 sham exposure; Phase 2 sham exposure.
  - Bd only: Phase 1 exposure to Bd zoospores; Phase 2 sham exposure.
  - Rv only: Phase 1 sham exposure; Phase 2 exposure to ranavirus.
  - Co-infection: Phase 1 Bd exposure; Phase 2 ranavirus exposure.

- Data collection and variables
  - Tank and individual identifiers:
    - tank_ID: unique mesocosm tank ID
    - individual_ID: unique ID for each host individual
  - Biological and experimental context:
    - species: species of the sampled individual
    - community_treatment: host community composition (Bb = toads; Rt = frogs; mixed)
    - exposure_treatment: four exposure regimes used
    - Phase1_dose: whether Bd exposure or control in phase 1
    - Phase2_dose: whether Rv exposure or control in phase 2
    - death_date: date of death or euthanisation
  - Infection outcomes and loads (end of experiment):
    - bd_status: Bd infection status (0 = uninfected, 1 = infected)
    - bd_load: Bd DNA load (genomic equivalents); NA if negative
    - Rv_status: ranavirus infection status (0 = uninfected, 1 = infected)
    - Rv_load: ranavirus DNA load (genomic equivalents); NA if negative
    - Coinfection_status: whether both pathogens were detected (0 = negative for co-infection, 1 = positive)

- Data structure and interpretation notes
  - The dataset records end-of-study infection status and quantitative loads, alongside per-host and per-tank metadata.
  - NA values indicate negative test results for the corresponding load metrics.
  - The Rv_load description appears to reference Bd DNA; this may indicate a labeling error to verify (Rv_load likely represents ranavirus load).

- Practical relevance for data governance and reuse
  - Clear, named variables and codings support filtering by community type, exposure regime, and infection outcomes.
  - Metadata aligns with two-pathogen host–pathogen dynamics, enabling analyses on how community composition and exposure history drive infection prevalence and intensity.
  - Supports cross-entity collaboration and potential data-product development around host–pathogen interaction datasets, with explicit units and end-state observations to aid discoverability and reuse.