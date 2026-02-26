# Metadata for: MultihostCoinfectionData.csv

## Authors and Affiliations
- Andy Fenton
- Dave Daversa
  - Institute of Integrative Biology, Biosciences Building, University of Liverpool
  - Institute of Zoology, Zoological Society of London
- Andrea Manica
- Trent Garner
  - Department of Zoology, University of Cambridge

## Background
- Data come from a mesocosm experiment conducted in summer 2018 at ZSL.
- Objective: determine how Bd (Batrachochytrium dendrobatidis) and ranavirus (Rv) infection prevalence and mean intensity are influenced by host community composition (toads Bufo bufo and frogs Rana temporaria) and exposure history to the pathogens.

## Experimental Design
- Communities: tanks containing toad tadpoles, frog tadpoles, or a 50/50 mixed species community.
- Phases: two phases by pathogen type.
  - Phase 1: Bd exposure via zoospores in media or sterile media (control).
  - Phase 2: exposure to three Rv-positive frog corpses in treatment tanks or three Rv-negative corpses in control tanks.
- Duration: experiment run for six weeks.

## Exposure Treatments
- Control
  - Phase 1: 6 × sham exposures to sterile media; sham 2: 1 × sham exposure
  - Phase 2: three Rv-negative corpses
- Bd only
  - Phase 1: 6 × 150,000 Bd zoospores
  - Phase 2: single sham exposure
-Rv only
  - Phase 1: 6 × sham exposures
  - Phase 2: single Rv exposure
- Co-infection
  - Phase 1: 6 × 150,000 Bd zoospores
  - Phase 2: single Rv exposure
- Community × exposure: 12 distinct treatments total, each with six replicates

## Variables (Dataset Columns)
- tank_ID: unique identifier for each mesocosm tank
- individual_ID: unique identifier for each host individual
- species: species of the sampled individual (toad or frog)
- community_treatment: host community composition (Bb = 100% toads; Rt = 100% frogs; mixed = 50/50)
- exposure_treatment: which of the four exposure regimes was applied
- Phase1_dose: Bd exposure status (Bd) or control (sham) in Phase 1
- Phase2_dose: ranavirus exposure status (Rv) or control (sham) in Phase 2
- death_date: date of death or euthanisation
- bd_status: Bd infection status at end of experiment (0 = uninfected, 1 = infected)
- bd_load: Bd DNA load in genomic equivalents (NA if negative)
- Rv_status: ranavirus infection status at end of experiment (0 = uninfected, 1 = infected)
- Rv_load: ranavirus DNA load in genomic equivalents (NA if negative)
- Coinfection_status: coinfection status at end of experiment (0 = negative for coinfection, 1 = positive)