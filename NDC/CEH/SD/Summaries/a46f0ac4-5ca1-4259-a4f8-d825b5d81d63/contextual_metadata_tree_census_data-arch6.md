# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

## Overview
- Large-scale ecological data collection (2017–2020) across 27 permanent forest plots (0.5 ha each) in five locations along an altitudinal and perturbation gradient in Andean Colombia.
- Aims: investigate factors driving forest change across gradients and evaluate forest composition; part of the BioResilience transdisciplinary project assessing forest resilience post-conflict.
- Funded by the UK Natural Environment Research Council (NE/R017980/1).

## Location, design, and gradients
- 27 permanent plots (0.5 ha each), organized into 5 locations covering three altitude classes: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
- Disturbance gradient categories: low perturbation (>30 years since last disturbance), medium (20–30 years), high (<20 years); three plots per gradient level, per location where applicable.
- Site details:
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá) and adjacent private properties.
  - Midlands: Reserva biológica Cachalú ( Encino and Charala, Santander) and Pedro Palo area (Tena, Cundinamarca).
  - Highlands: Reserva biológica Encenillo (Guasca, Cundinamarca) and Martos (Guatavita, Cundinamarca).
- Plot relocation and documentation: GPS coordinates recorded; plots subdivided into 10 x 10 m subplots; corner marking with PVC tubes; plot and subplot labeling.

## Data collected and key variables
- Measurements per plot: tree diameter (D) at 1.3 m (POM) for all stems with DBH ≥ 5 cm; height for ten stems per plot (hypsometer); total height used to calibrate remaining stems.
- Biomass: Above Ground Biomass (AGB) estimated using pantropical allometric models (Chave et al., 2014) via the BIOMASS package in R; height estimates via Feldpausch et al. (2012).
- Taxonomy: morphospecies identified in the field; one herbarium voucher per morphospecies per location; identifications validated by CAV to ensure taxonomic consistency.
- Metadata: disturbance gradient, elevation category, plot code; coordinates (GPS) and taxonomic details (Family following APG III, Species).
- Data file: a single CSV named plot_data_nerc.csv with eight columns: Family, Species, Diameter (D), Height, Transformation, Above Ground biomass (AGB), Altitude, plot.id.
- Units and value ranges:
  - D: 50–1634 mm
  - Height: 1–40 m
  - AGB: 0.001–21.164 Mg
  - Altitude: categorized as Lowlands, Midlands, Highlands
  - plot.id: 1–27

## Collection, methods, and instrumentation
- Field procedures: 
  - Systematic stem numbering; multi-stemmed trees labeled with main stem and branch decimals.
  - Recruits labeled with the nearest tree number plus a letter.
  - 1.3 m POM used for diameter measurements with yellow paint marking optimal measurement points.
- Tools and materials: pruning tools, bags for samples, masking tape, indelible markers, tree tags and nails, hammers, diametric tapes, data worksheets, and yellow paint for POM marking.
- Data management: ForestPlots.net field formats used for data recording.

## Collection timeline and site-specific notes
- Quinchas (Lowlands): measurements conducted June–December 2019.
- Encino (Midlands): February–March 2020.
- Pedro Palo (Midlands): January 2020.
- Martos (Highlands): December 2017–May 2019 and November 2019.
- Encenillo (Highlands): August–September 2019.
- Overall total individuals measured by altitude: 5225 (lowlands), 9338 (midlands), 11824 (highlands).

## Quality assurance and data governance
- Calibration and measurement accuracy: equipment prepared and validated prior to use; height calibration and measurement verification steps described.
- Quality control: external review of databases and metadata; checks for missing values, duplicates, data completeness, and correct typing; metadata validation to ensure consistency with database contents.
- Data provenance: specimens and identifications conducted to ensure reliability for diversity measurements; field formats standardized to enable cross-site comparisons.

## Data structure and access
- Structure: one CSV file (plot_data_nerc.csv) with eight columns capturing taxonomic, biometric, gradient, and plot identifiers.
- Usability: data tailored for cross-gradient analyses of AGB, height, diameter, and species composition across altitude and disturbance gradients; suitable for self-service exploration and integration with other datasets (e.g., additional ecological or climatic layers).

## References and models
- Allometric models for AGB: Chave et al. (2014).
- Height estimation: Feldpausch et al. (2012).
- Regional ecological context and life zone classifications referenced (Holdridge, Cuatrecasas, etc.).
- BioResilience project context and Colombian forest ecosystem studies cited for site descriptions.