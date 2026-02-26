# Metadata for: MultihostCoinfectionData.csv

## Overview
- Data from a 2018 mesocosm experiment at ZSL investigating how host community composition (toad tadpoles vs. common frog tadpoles vs. mixed) and exposure history influence the prevalence and mean intensity of Bd (Batrachochytrium dendrobatidis) and ranavirus (Rv) infections.
- Organisms studied: common frog (Rana temporaria) and common toad (Bufo bufo).
- Key outputs include infection status, infection load, and mortality per individual.

## Experimental design
- Community types: 
  - Bb only (100% toads)
  - Rt only (100% frogs)
  - Mixed (50/50 mix of toads and frogs)
- Exposure regimes (four per community) broken into two phases:
  - Phase 1: Bd exposure via zoospores in media or a sterile media control.
  - Phase 2: Rv exposure via three Rv-positive larval frog corpses or three Rv-negative corpses (control).
- Treatments:
  - Control: Phase 1 sham, Phase 2 sham
  - Bd only: Phase 1 Bd exposure, Phase 2 sham
  - RV only: Phase 1 sham, Phase 2 Rv exposure
  - Coinfection: Phase 1 Bd exposure, Phase 2 Rv exposure
- Experimental resolution: 12 distinct community-exposure treatments, with six replicates each.
- Duration: Experiment ran for six weeks.

## Variables
- tank_ID: Unique tank identifier (mesocosm).
- individual_ID: Unique identifier for each host individual.
- species: Species of the sampled individual.
- community_treatment: Host community composition (Bb only, Rt only, mixed).
- exposure_treatment: Four exposure regimes (Control, Bd only, RV only, Coinfection).
- Phase1_dose: Whether individuals experienced Bd exposure or sham in Phase 1.
- Phase2_dose: Whether individuals experienced Rv exposure or sham in Phase 2.
- death_date: Date of death or euthanasia for the individual.
- bd_status: Bd infection status at end of experiment (0 = uninfected, 1 = infected).
- bd_load: Bd DNA load (genomic equivalents); NA for negative.
- Rv_status: Rv infection status at end of experiment (0 = uninfected, 1 = infected).
- Rv_load: Rv DNA load (genomic equivalents); NA for negative.
- Coinfection_status: 0 = negative for coinfection, 1 = positive for coinfection.

## Measurements and units
- Load measurements (bd_load, Rv_load) are in genomic equivalents.
- death_date recorded as date of death or euthanisation.
- Status fields (bd_status, Rv_status, Coinfection_status) are binary.

## Data structure and relationships
- Per-individual level data linked to:
  - Tank-level context via tank_ID.
  - Species and community_treatment to analyze effects of composition.
  - Exposure history across two phases.
- Multidimensional design enables analysis of:
  - Effects of community composition on pathogen prevalence and load.
  - Interactions between Bd and Rv exposure (coinfection dynamics).
  - Temporal patterns via death_date within six-week period.

## GIS considerations for data visualization
- Spatial mapping would require linking tank_IDs to geolocations (e.g., facility coordinates) to visualize spatial patterns of infection or mortality.
- Potential map-based visualizations:
  - Infection prevalence or coinfection by tank location and community type.
  - Heatmaps of bd_load and Rv_load by tank or replicates.
  - Temporal maps using death_date to show progression over the six weeks.
- Data preparation recommendations:
  - Standardize categorical encodings (e.g., ensure consistent codes for community_treatment and exposure_treatment).
  - Align NA handling for loads (NA where negative tests).
  - Integrate with location data if mapping is required; otherwise, generate non-spatial summaries (e.g., by tank or replicate) for GIS-ready visualization.

## Quality and data handling considerations
- Data are from a single controlled mesocosm experiment; ensure provenance is preserved (authors and affiliations).
- Expect data cleaning needs for:
  - Consistent coding of species and treatment categories.
  - Handling missing or NA load values.
  - Synchronizing death_date with exposure phases for temporal analyses.
- Potential data integration challenges include merging with external spatial datasets or other experiments; maintain clear metadata to support reprojection and standardization.

## Provenance and authorship
- Metadata contributed by:
  - Andy Fenton
  - Dave Daversa
  - Andrea Manica
  - Trent Garner
- Affiliations:
  - Institute of Integrative Biology, University of Liverpool
  - Institute of Zoology, Zoological Society of London
  - Department of Zoology, University of Cambridge
- Context: 2018 mesocosm experiment conducted at ZSL to study Bd and Rv dynamics in relation to host community composition and exposure history.