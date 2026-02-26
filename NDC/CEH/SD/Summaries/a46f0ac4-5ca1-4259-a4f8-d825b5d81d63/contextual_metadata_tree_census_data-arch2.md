# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

## Overview
- Multi-site dataset collected between 2017 and 2020 from 27 permanent forest plots (0.5 ha each) along an altitudinal and forest perturbation gradient in Andean Colombia.
- Purpose: investigate factors driving forest change across gradients and evaluate forest composition; within the BioResilience project assessing forest ecosystem resilience after Colombia’s postconflict period.
- Funded by the UK Natural Environment Research Council (NE/R017980/1).

## Study area and gradient
- Five locations spanning altitude categories:
  - Lowlands (0–1200 m): Serranía de las Quinchas, Puerto Boyacá, Boyacá
  - Midlands (1200–2200 m): Encino and Pedro Palo (Santander/Cundinamarca)
  - Highlands (2200–3200 m): Encenillo and Martos (Cundinamarca)
- Altitudinal gradient categories:
  - Lowlands, Midlands, Highlands
- Perturbation gradient categories (forest disturbance and recovery):
  - Low perturbance (>30 years since last disturbance)
  - Medium perturbance (20–30 years)
  - High perturbance (<20 years)

## Plot establishment and monitoring
- 27 permanent plots, each 0.5 ha, divided into 10 x 10 m subplots; GPS coordinates recorded for relocation.
- Subplot corners marked with white/orange PVC tubes; plot corners marked with orange tubes.
- Sampling windows:
  - Quinchas: 2019 measurements
  - Encino: 2020
  - Pedro Palo: 2020
  - Martos: 2017–2019
  - Encenillo: 2019
- Census procedures:
  - Systematic stem numbering; multi-stemmed trees labeled on main stem and branches; recruits labeled relative to nearest tree.
  - Primary measurement at 1.3 m (POM) for DBH; all woody stems with DBH ≥ 5 cm measured.
  - Ten stems per plot height measured with a hypsometer to calibrate other height estimates.
  - Specimens collected for field identification; all identifications validated by an external taxonomic expert (CAV).

## Data collected and metrics
- Measurements and derived metrics:
  - Diameter (D) at POM (mm)
  - Height (m) for ten stems per plot (used to calibrate other height estimates)
  - Above Ground Biomass (AGB) via pantropical models (Chave et al. 2014) using the BIOMASS package in R
  - Taxonomic data: Family (APG III) and Species (Latin binomial)
  - Disturbance gradient category (Transformation: High, Low, Mid)
  - Altitude category (Lowlands, Midlands, Highlands)
  - plot.id (1–27)
- Summary counts:
  - Total individuals measured: 5,225 (lowlands), 9,338 (midlands), 11,824 (highlands)
- Value ranges and units:
  - D: 50–1,634 mm
  - Height: 1–40 m
  - AGB: 0.001–21.164 Mg
  - AGB units: Mg
  - Height units: m
  - D units: mm
  - Altitude categories encoded as described above

## Data structure and access
- Primary dataset file: plot_data_nerc.csv
- Columns: Family, Species, Diameter (D), Height, Transformation, Above Ground biomass (AGB), Altitude, plot.id
- Data formats follow ForestPlots.net field formats for metadata and data capture
- Location and plot coordinates included to enable spatial analyses and future relocation

## Methods: measurement, calibration and computation
- Measurements:
  - DBH measured at 1.3 m (POM) using a diametric tape
  - Height measured for 10 stems per plot; remaining heights calibrated from these measurements
- Biomass estimation:
  - AGB estimated using pantropical models (Chave et al. 2014)
  - Height estimation assisted by retrieveH function (Feldpausch et al. 2012)
- Calibration and quality:
  - Calibration steps include instrument checks and accuracy verification before measurements
  - Calibration and measurement procedures documented to ensure consistency across plots and years

## Field equipment and procedures
- Equipment list includes:
  - Pole pruners, pruning shears
  - Plastic/paper bags for samples; masking tape; indelible markers
  - Tree tags, nails, hammers for stem labeling
  - Diametric tape; hypsometer for height; yellow paint for 1.3 m measurement points
  - Data worksheets for raw field data
- Procedures emphasize standardized marking, sampling, labeling, and specimen collection for taxonomic verification

## Data quality assurance and governance
- Quality control criteria emphasize accuracy, completeness, and consistency
- External review conducted to verify database structure, detect missing/null fields, ensure data completeness, correct typing, and eliminate duplicates
- Metadata validation performed to ensure accuracy and consistency with database contents
- Data management aims to support data sharing and reuse, with attention to enabling access to underlying data for broader analyses

## Context and references
- Part of the BioResilience project, focusing on forest resilience after postconflict periods in Colombia
- Key references used for methods include:
  - Chave et al. (2014) for AGB allometric models
  - Feldpausch et al. (2012) for height estimation
  - Holdridge (1982) and Cuatrecasas (1958) for life zones and forest classification
  - Various regional reports and inventories for site descriptions and ecological context