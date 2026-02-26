# Metadata for: MultihostCoinfectionData.csv

- Background
  - Mesocosm experiment conducted in summer 2018 at the Institute of Zoology, Zoological Society of London.
  - Objective: determine how Bd (Batrachochytrium dendrobatidis) infection prevalence and mean intensity, and ranavirus (Rv) infection, are influenced by host community composition (toads Bufo bufo and frogs Rana temporaria) and history of exposure to the pathogens.

- Experimental design
  - Host communities: toad tadpoles, common frog tadpoles, or a 50/50 mixed community.
  - Four exposure regimes: Control, Bd only, Rv only, Co-infection.
  - Two phases by pathogen type:
    - Phase 1: Bd exposure via zoospores in media or sterile media (control).
    - Phase 2: exposure to Rv-positive frog corpses (treatment) or Rv-negative corpses (control).
  - Duration: six weeks.
  - Treatments and replication: 12 distinct treatments (4 exposure regimes × 3 community compositions) with six replicates each.

- Exposure Treatments
  - Control: Phase 1 sham exposure; Phase 2 sham exposure.
  - Bd only: Phase 1 exposure to Bd zoospores; Phase 2 sham exposure.
  - Rv only: Phase 1 sham exposure; Phase 2 exposure to Rv-positive corpses.
  - Co-infection: Phase 1 Bd exposure; Phase 2 Rv exposure.
  - Note: Each treatment combination yields 12 total treatment groups across replicates.

- Variables (data columns)
  - tank_ID: unique mesocosm tank identifier.
  - individual_ID: unique identifier for each host individual.
  - species: species of the sampled individual.
  - community_treatment: host community composition (Bb only = 100% toads, Rt only = 100% frogs, mixed = 50/50).
  - exposure_treatment: one of the four exposure regimes.
  - Phase1_dose: whether sampled individuals were in tanks with Bd exposure or control in phase 1.
  - Phase2_dose: whether sampled individuals were in tanks with Rv exposure or control in phase 2.
  - death_date: date of death or euthanisation for the sample.
  - bd_status: binary Bd infection indicator at end (0 = uninfected, 1 = infected).
  - bd_load: Bd DNA detected, in genomic equivalents; NA if BD negative.
  - Rv_status: binary Ranavirus infection indicator at end (0 = uninfected, 1 = infected).
  - Rv_load: Ranavirus DNA detected, in genomic equivalents; NA if negative.
  - Coinfection_status: whether both pathogens were detected at the end (0 = negative, 1 = positive).