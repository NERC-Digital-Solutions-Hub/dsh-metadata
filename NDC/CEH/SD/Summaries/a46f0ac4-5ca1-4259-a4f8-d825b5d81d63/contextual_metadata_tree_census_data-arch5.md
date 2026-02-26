# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

## Aim and scope
- Data from 2017–2020 across 27 permanent forest plots (0.5 ha each) in five locations along an altitudinal gradient (lowland, mid-elevation, highland) and a forest perturbation gradient (low, medium, high).
- Focus on factors influencing forest change and evaluating forest composition in Andean Colombia as part of the BioResilience project.
- Supported by the UK Natural Environment Research Council (NE/R017980/1).

## What the dataset contains
- Measurements for each tree including:
  - Diameter (D) in millimeters
  - Height in meters
  - Above Ground Biomass (AGB) in megagrams
  - Taxonomic names (scientific and family; APG III)
  - Disturbance gradient, altitude category, and plot code
- Metadata describing sites, plot arrangement, and sampling timelines
- A single CSV file (plot_data_nerc.csv) with eight columns: Family, Species, Diameter (D), Height, Transformation, Above Ground biomass (AGB), Altitude, plot.id
- Total counted individuals: 5225 (lowlands), 9338 (midlands), 11824 (highlands)

## Study sites and gradient details
- Altitudinal gradient:
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Locations:
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá)
  - Midlands: Cachalú (Encino, Santander) and Tenasucá de Pedro Palo (Catalamonte, Tena, Cundinamarca)
  - Highlands: Encenillo (La Trinidad, Guasca, Cundinamarca) and Martos (Monquentiva, Guatavita, Cundinamarca)
- Perturbation gradient (recovery time since disturbance):
  - Low (>30 years since last disturbance)
  - Medium (20–30 years)
  - High (<20 years)

## Field methods and data generation
- Plot design and labor
  - 27 permanent plots of 0.5 ha each, subdivided into 10×10 m subplots; GPS coordinates recorded for relocation
  - Systematic stem numbering; multi-stemmed trees labeled with main stem and branches; recruits labeled relative to nearest tree
- Measurements and identification
  - Diameter at the defined point of measurement (POM) at 1.3 m; DBH ≥ 5 cm
  - Height measured on ten stems per plot with a hypsometer; used to calibrate other height estimates
  - Morphospecies identified in the field; one specimen per morphospecies per location collected for proper identification
  - Specimens identified by CAV to ensure consistency in diversity assessments
- Biomass estimation
  - AGB calculated using pantropical allometric models (Chave et al. 2014) via the BIOMASS R package
  - Height estimates obtained with the retrieveH method (Feldpausch et al. 2012)
- Data recording and standards
  - Field data recorded using ForestPlots.net formats
  - Calibration steps and instrument checks performed to ensure measurement accuracy
  - Data quality control included external review of database structure, completeness, data typing, absence of duplicates, and metadata validation

## Data structure and units
- Variables in the dataset:
  - Family: taxonomic family (APG III)
  - Species: Latin binomial name
  - D: Diameter (mm); D = 0 if the tree is dead; range 50–1634 mm
  - Height: Tree height (m); range 1–40 m
  - Transformation: Disturbance gradient category (High, Low, Mid)
  - AGB: Above Ground Biomass (Mg)
  - Altitude: Altitude category (Lowlands, Midlands, Highlands)
  - plot.id: Plot identifier (1–27)
- Typical value ranges:
  - D: 50–1634 mm
  - Height: 1–40 m
  - AGB: 0.001–21.164 Mg

## Data collection and processing workflow
- Data collection
  - Remote relocation via recorded GPS coordinates; fixed subplot grid; precise labeling for reproducibility
- Processing and analysis
  - Taxonomic standardization (APG III)
  - AGB calculation using pantropical models in R
  - Height calibration using measured stems to estimate overall tree height
- Documentation and provenance
  - Comprehensive metadata describing plots, sampling times, locations, and measurement protocols
  - Data stored in a standardized CSV format with clear column definitions

## Quality assurance and governance
- Quality control
  - Multi-person review of database structure, missing values, data types, duplicates, and metadata completeness
  - Validation of metadata for accuracy and consistency with database contents
- Data governance
  - Metadata and data practices align with the BioResilience project objectives
  - Taxonomic harmonization and standardized measurements support interoperability across sites and studies

## Usage context and references
- Purpose: to analyze how altitude and disturbance gradient influence forest structure and biomass, contributing to resilience assessments in post-conflict Colombia
- Key methodological references:
  - Chave et al. (2014) for AGB estimation
  - Feldpausch et al. (2012) for height estimation
  - APG III for family classifications
- Project context and funding:
  - BioResilience project; funded by UK NERC (NE/R017980/1)