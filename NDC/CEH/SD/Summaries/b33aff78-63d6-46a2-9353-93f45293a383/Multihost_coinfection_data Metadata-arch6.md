# Metadata for: MultihostCoinfectionData.csv

## Background
- Data originate from a mesocosm experiment conducted in summer 2018 at the Institute of Zoology, ZSL.
- Objective: determine how Bd (Batrachochytrium dendrobatidis) and ranavirus (Rv) infection prevalence and mean intensity are influenced by host community composition and exposure history.

## Experimental Design
- Communities comprised of toad tadpoles (Bufo bufo), common frog tadpoles (Rana temporaria), or a 50/50 mixed species community.
- Each community type was assigned to one of four exposure regimes, forming 12 distinct treatments in total, with six replicates per treatment (72 mesocosms total).
- Experiment duration: six weeks.
- Two exposure phases:
  - Phase 1: Bd exposure (zoospores) or sham (control) exposure.
  - Phase 2: Rv exposure (Rv-positive frog corpses) or sham exposure (Rv-negative corpses in controls).

## Exposure Treatments
- Control: Phase 1 with six sham exposures; Phase 2 with one sham exposure.
- Bd only: Phase 1 with six Bd zoospore exposures; Phase 2 with one sham exposure.
- Rv only: Phase 1 with six sham exposures; Phase 2 with a single Rv exposure.
- Co-infection: Phase 1 with six Bd zoospore exposures; Phase 2 with a single Rv exposure.
- Community × exposure combinations yield 12 distinct treatments, each with six replicates.

## Variables and Data Collected
- tank_ID: unique identification for each mesocosm tank.
- individual_ID: unique identifier for each host individual.
- species: species of the sampled individual.
- community_treatment: host community composition (Bb = 100% Bufo bufo toads; Rt = 100% Rana temporaria frogs; mixed = 50/50 mix).
- exposure_treatment: which of the four exposure regimes was applied (Control, Bd only, Rv only, Co-infection).
- Phase1_dose: whether sampled individuals were in Bd-exposed tanks or controls during phase 1.
- Phase2_dose: whether sampled individuals were in Rv-exposed tanks or controls during phase 2.
- death_date: date of death or euthanisation of the individual.
- bd_status: binary Bd infection status at end of the experiment (0 = uninfected, 1 = infected).
- bd_load: quantitative Bd DNA load (genomic equivalents); NA for negative samples.
- Rv_status: binary ranavirus infection status at end of the experiment (0 = uninfected, 1 = infected).
- Rv_load: quantitative ranavirus DNA load (genomic equivalents); NA for negative samples.
- Coinfection_status: whether both pathogens were detected at the end (0 = negative for coinfection, 1 = positive for coinfection).

## Notes on Data Use
- Loads are expressed as genomic equivalents; NA indicates samples that tested negative for the respective pathogen.
- The Rv_load variable description mentions Bd DNA in the text, which appears to be a wording artefact; values correspond to the respective pathogen detected.