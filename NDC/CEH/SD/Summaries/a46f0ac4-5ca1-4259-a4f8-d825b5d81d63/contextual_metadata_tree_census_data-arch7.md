# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

## Overview
- A multi-location field dataset documenting tree census and above-ground biomass (AGB) across an altitudinal and disturbance gradient in Andean Colombia (2017–2020).
- Aims to analyze factors driving forest change and community composition, within the BioResilience project.

## Study design, locations and gradients
- 27 permanent forest plots (0.5 ha each) distributed along an altitudinal gradient and forest perturbation gradient.
- Altitude categories:
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Five locations include:
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá)
  - Midlands: Reserva biológica Cachalú (Encino, Tena, Santander) and Pedro Palo in Catalamonte (Tena, Cundinamarca)
  - Highlands: Reserva biológica Encenillo (La Trinidad, Guasca, Cundinamarca) and Martos (Guatavita, Cundinamarca)
- Perturbation gradient (recovery time since disturbance):
  - Low, Medium, High
  - Three plots per perturbation level per location, totaling 27 plots
- Each plot subdivided into 10 x 10 m subplots; GPS coordinates recorded for relocation
- All plots coded with a unique plot.id (1–27)

## Data collected and variables
- Measurements collected per tree:
  - Diameter at breast height (D) in millimeters, measured at 1.3 m above ground (POM)
  - Height (m); height measured on 10 stems per plot with a hypsometer; used to calibrate remaining stems
  - Above Ground Biomass (AGB) in megagrams (Mg) via pantropical allometric models
  - Taxonomic information: Family (APG III), Species (Latin binomial)
  - Plot metadata: disturbance gradient, elevation category, and parcel/plot code
- Totals by altitude category:
  - 5225 individuals measured in lowlands
  - 9338 in midlands
  - 11824 in highlands
- Species identifications:
  - Field identifications to morphospecies
  - One botanical specimen per morphospecies per location collected and identified by CAV for consistency

## Data structure and format
- Primary dataset: a single CSV file titled plot_data_nerc.csv
- Eight columns: Family, Species, Diameter (D), Height, Transformation, Above Ground biomass (AGB), Altitude, plot.id
- Data ranges and units:
  - D: 50–1634 mm
  - Height: 1–40 m
  - AGB: 0.001–21.164 Mg
  - Altitude: categorical (Lowlands 0–1200 m; Midlands 1200–2200 m; Highlands 2200–3200 m)
- Coordinates: latitude and longitude recorded for each plot; GPS-based relocation enabled
- Processing steps:
  - AGB computed using Chave et al. (2014) pantropical models via BIOMASS package in R
  - Height estimated with retrieveH (Feldpausch et al. 2012)
  - D measured with a 1.3 m POM; morphospecies identifications supported by herbarium-level verification

## Methods, tools and QA
- Field instruments and procedures:
  - Measurement tools: diametric tape, hypsometer, marking paints (yellow 1.3 m POM), PVC markers, nails, aluminum labels
  - Timber and botanical material collection: pruners, pruning shears, bags (plastic/paper), masking tape, indelible markers
  - Data recording: original data worksheets; standardized ForestPlots.net field formats
- Quality control and metadata validation:
  - Criteria include accuracy, completeness and consistency
  - External review of databases and metadata for structure, missing values, duplicates, typing, and overall reliability

## GIS and data use considerations
- Spatially explicit: plots and subplots are georeferenced with GPS coordinates, enabling map-based visualization of species composition and biomass across altitude and perturbation gradients.
- Standardized units and clear field definitions support integration with other GIS datasets and metadata.
- Data provenance tied to the BioResilience project (UK NERC NE/R017980/1) and published references for methodology and biomass modeling.

## Fieldwork and instrumentation summary
- Key equipment used in the BioResilience tree census includes marking and sampling tools (pole pruners, pruning shears), marking and labeling materials (PVC tubes, tree tags, nails, paint), measurement devices (diametric tape, hypsometer), and data worksheets.
- Calibration and measurement procedures emphasized accuracy and traceability across locations and campaigns (2017–2020).

## References and context
- Data collection and methods align with Pine/Chave-style biomass estimation using pantropical models; taxonomic verification by CAV; various regional ecological references cited for biome classification and site descriptions.
- Related methodological references include Chave et al. (2014) for AGB estimation, Feldpausch et al. (2012) for height, and regional ecological sources for Holdridge, Cuatrecasas, and local land-use context.