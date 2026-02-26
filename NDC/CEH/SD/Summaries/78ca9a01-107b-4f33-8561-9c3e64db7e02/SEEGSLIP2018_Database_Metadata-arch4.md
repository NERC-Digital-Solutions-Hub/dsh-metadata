# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

## Overview
- Dataset collected by the UK Centre of Ecology & Hydrology (UKCEH) in a BBSRC-funded project to evidence impacts of pasture-fed livestock on grassland parameters (sward composition and soil qualities).
- Context: grasslands are significant for farmers and the public; Pasture Fed Livestock Association (PFLA) certification standards underpin the sampling framework.
- Data cover vegetation species and characteristics, soil quality metrics, and farm management aspects from PFLA member farms.

## Experimental design
- 56 farms across Great Britain (PFLA members), recruited via PFLA.
- Farms sampled May–September 2018; 25 fully certified, 7 provisionally certified, remainder members aiming for certification.
- Plot-level sampling used a large 200 m2 plot per field, with vegetation and soil data collected to enable cross-study comparisons with Countryside Survey methods.
- Each field plot location validated on site; vegetation and soil data collected per field plot.

## Methods

### Vegetation
- Recorded all plant species within the 200 m2 plot and percent covers for nested subplots.
- Each plot assigned a vegetation height category (0–15 cm, 5–15 cm, 15–40 cm, 40 cm–1 m, >1 m).
- Data captured with electronic recording devices.

### Field management
- On-site farmer data collected about current and historic field management, including sward longevity, grazing management, and inputs via a purpose-built questionnaire.

### Soils
- One soil core (15 cm depth, 7 cm diameter) per sampling plot.
- Analyses aligned with Countryside Survey protocols, with some measures omitted.
- Measured properties include: Bulk Density, Carbon (SOC derived from LOI), Total Nitrogen, pH (in water and CaCl2), Olsen and total Phosphorus, soil moisture (where applicable), soil solution electrical conductivity, aggregate stability, and calcite/CaCO3 content.
- LOI used to estimate soil organic matter and carbon concentration; quality control with internal standards.
- Total Carbon and Nitrogen measured via elemental analysis (VarioEL); quality control with in-house references.
- Phosphorus assessed via colorimetric methods; Olsen P measured in arable/improved grassland plots.
- Additional soil properties: bulk density, particle size distribution (laser diffraction and hydrometer methods), calcium carbonate content, and aggregate stability (wet sieving with NaOH treatment for stability).

## Data structure and content
- Four CSV data sheets (anonymised site IDs):
  - SEEGSLIP_PLOTS_2018.csv — basic plot attributes and vegetation data per plot.
  - SEEGSLIP_SPECIES_2018.csv — species-level vegetation data (species name, codes, cover, nesting counts).
  - SEEGSLIP_SOIL_2018.csv — soil metrics (moisture, carbon, nitrogen, pH, phosphorus forms, conductivity, bulk density, texture, stability, CaCO3, etc.).
  - SEEGSLIP_FIELD_MGT.csv — field management data (PFLA membership/certification history, pasture type, grazing and fertilization details, stocking, cuts, lime/herbicide use, etc.).
- Farms anonymised and assigned an ID/site code to preserve landowner confidentiality.

## Data quality and comparability
- Methods aligned with UK Countryside Survey (CS) protocols to enable comparability across national datasets.
- LOI-based carbon estimation uses a defined conversion to maintain compatibility with legacy surveys.
- Rigorous QA measures include internal standards for LOI, duplicate checks, and calibration/standard references for instrumental analyses.
- Quality control procedures applied for pH, conductivity, Olsen P, and other assays (duplicate samples, blanks, and batch controls).

## Relevance to data strategy and governance
- Demonstrates end-to-end data lifecycle: from field data collection to standardized processing, QA, and well-structured, anonymised data delivery.
- Provides a rich, multi-domain data asset (vegetation, soils, and management) suitable for system-level data thinking, cross-study integration, and user-centered product development.
- Emphasizes interoperability with a national monitoring framework (CS) to support long-term trend analysis and evidence-based policy or practice.
- Data organization supports discoverability and potential collaboration with wider data communities through consistent metadata and documentation.

## Key metrics and data domains (highlights)
- Vegetation: species presence, cover percentages, plot-level nesting coverage, and vegetation height categories.
- Soils: LOI and derived soil organic carbon, total soil carbon and nitrogen, phosphorus (total and Olsen), pH (in water and CaCl2), electrical conductivity, bulk density, texture (clay/silt/sand), aggregate stability, and CaCO3 content.
- Field management: tenure with PFLA, certification status, pasture type, grazing regime, length and frequency of grazing, winter grazing, fertilization (mineral and organic), lime, herbicide use, cutting frequency, and stocking levels.

## Summary of the dataset’s utility
- Enables assessment of how pasture-fed practices influence grassland ecology and soil health across Britain.
- Supports cross-site comparisons and integration with Countryside Survey outputs for broader ecological and soil-carbon assessments.
- Serves as a robust data asset for data leaders seeking to model, standardize, and disseminate agricultural and environmental data across networks and partners.