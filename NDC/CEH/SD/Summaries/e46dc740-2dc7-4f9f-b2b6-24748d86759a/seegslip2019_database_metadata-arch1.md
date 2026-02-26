# pasture fed livestock farms across Great Britain, 2019

## Overview
- Data collected by the UK Centre for Ecology & Hydrology (CEH) in a project funded by BBSRC to evidence the impacts of pasture-fed livestock practices on grassland parameters, focusing on sward composition and soil qualities.
- Covers grassland types in the UK (acid, calcareous, neutral, improved) and measures biodiversity, soil health, and resilience under pastoral management.
- Based on 17 farms belonging to the Pasture Fed Livestock Association (PFLA); includes fields under mob grazing and, to a lesser extent, herbal leys.
- Data include vegetation, soil metrics, and aspects of farm management from the second year of sampling (2019).

## Experimental design
- 17 farms across Britain; 10 fully certified and 7 with intentions to certify, recruited via PFLA.
- Sampling period: May–September 2019.
- Field pairing: typically one mob-grazed field with a comparable set-stocked field (14 pairs), or comparisons between fields under species-rich ley vs traditional ley.
- Multiple fields per farm sampled in some cases; fields anonymised with farm ID and site codes.
- Sampling methods included vegetation surveys, soil sampling, and farmer interviews on management practices.

## Data collected and methods

- Vegetation
  - 3 randomly placed quadrats per 2x2 m field plot; data captured on species, cover (%), flowering, vegetation height, wormcasts, soil surface condition, and biomass (in a 25x25 cm sub-sample).
  - W-shaped transect with 10 sampling locations for soil sampling and a 10-point vegetation height capture.
- Biomass
  - Harvest of plant material from the central 25x25 cm sub-plot; dried and weighed by groups (grass, dicot, cereal); total biomass recorded.
- Soils
  - Soil cores (15 cm depth, 5 cm diameter) in each field; additional 10 bulked samples across soil depths (0–5 cm, 5–15 cm, 15–30 cm) along the W transect.
  - Analyses aligned with CS soil protocols; sub-samples for soil DNA (deposited in ENA PRJEB46195).
  - Measured properties include: LOI (loss on ignition), total SOC and N, total P, Olsen P (arable/improved grasslands only), pH (in water and CaCl2), electrical conductivity (EC), bulk density, particle size distribution (laser diffraction and hydrometer method), aggregate stability, CaCO3 content, and various soil moisture and density metrics.
  - Quality control via internal standards and replicates; LOI QA checks; calibration and blanks for chemical assays.
- Field/Farm management
  - On-site farmer questionnaire capturing historic and current management (grazing type, stocking density, rest periods, use of fertilizers/manure, presence of temporary leys, silage, etc.).
- Data structure and metadata
  - Soil and vegetation data linked to field and farm identifiers; fields anonymised yet mappable using internal codes.
  - Primary data files (2019) are seven CSV tables with detailed variable definitions and units.

## Data structure (files)

- SEEGSLIP_PLOTS_2019.csv
  - Vegetation plot-level attributes (Farm_NO, FIELD_ID, PLOT_TYPE, PLOT_NUMBER, survey dates, slope, shade, canopy/ground/shrub heights, signs of animals, soil surface conditions, sampling dates, etc.)
- SEEGSLIP_SPECIES_2019.csv
  - Species-level data per plot (BRC_NAMES, BRC_NUMBER, total cover, flowering status, land classification codes, grid references)
- SEEGSLIP_BIOMASS_2019.csv
  - Dried biomass by plant group (GRASS, DICOT, CEREAL, TOTAL)
- SEEGSLIP_SOIL_2019.csv
  - Soil chemistry and physical properties by depth/position (pH, conductivity, moisture, LOI, bulk density, stones, PSD, C/N contents, P metrics, Olsen P, CaCO3, TOTC, TOTN, etc.)
- SEEGSLIP_FARMDATA_2019.csv
  - Farm-level management data from questionnaires (grazing uniformity, grazing type, set stocking, stocking practices)
- SEEGSLIP_FIELDS_2019.csv
  - Field-level management data (control/managed status, current management, field size, shade, rest, fertiliser use, rest intervals, etc.)
- SEEGSLIP_STOCK_2019.csv
  - Stocking information (supplementary feed usage, bale rolling, livestock types)

## Anonymisation and scope
- Farms anonymised to protect landowner confidentiality; fields identified by site codes.
- Sample includes 17 farms in 2019, with paired-field comparisons and field types designed to illuminate mob grazing and ley practices.

## Potential uses for analysts
- Examine correlations between grazing management (mob grazing vs set-stocking, ley types) and grassland biodiversity, sward composition, and soil health.
- Build predictive models linking field management variables to soil carbon, nutrient status (SOC, N, P), pH, moisture, and aggregate stability.
- Compare soil chemical/physical properties across depths and between managed vs control fields.
- Integrate vegetation composition with soil data and management practices to assess resilience and ecosystem function of pasture-fed systems.

## Context and references
- Background on grassland importance and PFLA certification standards; ongoing research includes:
  - Seaton et al. 2023. Soil bacterial and fungal communities show within-field heterogeneity that varies by land management. Soil Biology and Biochemistry.
  - Wagner et al. 2023. Mob grazing: A nature-based solution for British farms producing pasture-fed livestock. Nature-Based Solutions.
- Methodological references include CS soils manual (Emmett et al. 2008, 2010), ITE Land Classification (Bunce et al., 2007), and standard soil analytical procedures.