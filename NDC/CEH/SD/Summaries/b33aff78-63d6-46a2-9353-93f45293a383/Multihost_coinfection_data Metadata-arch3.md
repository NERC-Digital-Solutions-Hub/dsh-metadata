# Metadata for: MultihostCoinfectionData.csv

## Overview
- Generated from a mesocosm experiment in summer 2018 at the Institute of Zoology, ZSL.
- Objective: determine how prevalence and mean intensity of Bd (Batrachochytrium dendrobatidis) and ranavirus (Rv) infections are influenced by host community composition (Rana temporaria and Bufo bufo) and history of exposure to the pathogens.

## Experimental design and treatments
- Experimental communities:
  - Toad tadpoles only
  - Frog tadpoles only
  - Mixed 50/50 toad and frog
- Exposure regimes (four, split into two phases by pathogen type):
  - Phase 1: Bd exposure or control (sterile media)
  - Phase 2: Rv exposure or control (Rv-positive or Rv-negative corpses)
- Treatment structure:
  - 12 distinct treatments = 4 exposure regimes × 3 community types
  - Six replicates per treatment
  - Experiment duration: six weeks
- Exposure specifics:
  - Control: Phase 1 sham exposures; Phase 2 sham exposure
  - Bd only: Phase 1 Bd zoospores; Phase 2 sham for Rv
  - Rv only: Phase 1 sham; Phase 2 Rv exposure
  - Coinfection: Phase 1 Bd exposure; Phase 2 Rv exposure

## Measured variables and data schema
- tank_ID: unique mesocosm tank identifier
- individual_ID: unique identifier for each host individual
- species: species of the sampled individual
- community_treatment: host community composition (Bb = 100% toads, Rt = 100% frogs, mixed)
- exposure_treatment: which exposure regime was applied
- Phase1_dose: whether tank received Bd exposure or control in phase 1
- Phase2_dose: whether tank received Rv exposure or control in phase 2
- death_date: date of death or euthanization
- Bd_status (bd_status): 0 = uninfected, 1 = infected
- Bd_load (bd_load): Bd DNA quantity in genomic equivalents (NA if negative)
- Rv_status (Rv_status): 0 = uninfected, 1 = infected
- Rv_load (Rv_load): Rv DNA quantity in genomic equivalents (NA if negative)
- Coinfection_status: 0 = no coinfection, 1 = coinfection detected

## Data quality and governance considerations
- Data are organized with explicit end-of-study infection statuses and loads, including NA for non-detections.
- Clear labeling of phases, doses, and community treatments supports traceability of exposure-history effects.
- Metadata completeness evidenced by explicit variable definitions; however, use in cross-platform contexts may require additional methodological details not specified (e.g., measurement assays beyond the stated units).

## Implications for monitoring frameworks
- Demonstrates the utility of multi-factor experimental designs to evaluate environmental health risks under varying community structures and exposure histories.
- Highlights the need for:
  - Comprehensive metadata: clear variable definitions, dose regimes, phase timing, and outcome measures
  - Data governance: transparent sharing of underlying data while handling NA values and sensitive results
  - Standardization of data formats and units (e.g., genomic equivalents for pathogen loads) to enable interoperability
- Indicates practical data collection considerations for policy-relevant monitoring: linking community composition, exposure regimes, and infection outcomes to inform management decisions and future research directions.