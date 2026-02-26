# Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

## Overview
- Compilation of multiple datasets (2015/2016 and 2003–2005) on Asellus aquaticus from Chernobyl-affected areas in Belarus and Ukraine.
- Aimed at assessing developmental stability (fluctuating asymmetry), reproductive capacity, and genetic diversity in relation to radiation exposure.
- Spatial context tied to six sampling sites shown in Figure S1, enabling GIS-based spatial analyses alongside environmental and dose-rate data.
- Data collected under the TREE project and associated methodologies described in linked publications.

## Datasets and GIS relevance
- FA_Data_Chernobyl_2015.csv
  - Morphological measurements for five traits, fluctuating asymmetry (FA2), and environmental factors (dose rate, conductivity, oxygen saturation, pH, temperature), plus site and sex.
  - 10 columns; right-left measures averaged; specimens from six sites.
  - GIS use: map FA2 spatial distribution, relate to dose rates and water chemistry; supports gradient analysis and environmental correlation studies.
- Fecundity_Data_Chernobyl.csv
  - Reproductive metrics: eggs per female, egg weight, female weight, site, year, eggs normalized to weight, sampling date, dose rate, and proportion gravid.
  - 9 columns; data across six lakes/sites and two years (2015/2016).
  - GIS use: map fecundity indicators by site and year; analyze spatial patterns relative to contamination gradients.
- FA_Data_Chernobyl_2003.CSV
  - Morphological data (FA2) plus dose rate, antennal segment count, sampling date, temperature, pH, conductivity, oxygen saturation.
  - 11 columns; temporal comparison with 2015 data.
  - GIS use: temporal-spatial comparison of developmental stability across years and sites; overlay with environmental factors.
- Chernobyl_Genetic_Diversity.csv
  - Genetic diversity metrics from Genotyping-by-Sequencing: sample ID, inbreeding coefficient, expected and observed heterozygosity, Tajima's D, nucleotide diversity.
  - 6 columns; samples from 6 sites across 2003–2005 and 2015.
  - GIS use: map genetic diversity patterns across space and time; explore spatial structure in relation to contamination gradients.

## Data collection, methods, and quality
- Sampling and measurement protocols standardized to reduce bias (randomized boxes, two replicate measurements per individual; thousands of measurements across hundreds of organisms).
- Dose rate calculations based on radiocaesium/strontium deposition and lake-water activity data; full methodology published in linked work.
- Environmental variables collected with calibrated instruments (handheld probes, ImageJ measurements for morphology).
- Missing data indicated by blanks; dataset descriptions provide the structure and variables to expect.
- Data provenance: collected by Neil Fuller and collaborators; genetic data generated at Cornell University; TREE project funding noted.

## Temporal and spatial scope
- Geographic focus: Chernobyl-affected areas in Belarus and Ukraine.
- Sites: six sampling locations (as per Figure S1).
- Time frames: 2003–2005 and 2015–2016 (with fecundity data for 2015/2016 and morphological data across two periods).

## Practical GIS considerations and recommendations
- Integrate these datasets with a geospatial framework (alignment of site identifiers to coordinates from Figure S1 or external georeferencing).
- Strategies for GIS use:
  - Create thematic maps of FA2 by site and year alongside dose-rate layers and environmental variables (pH, temperature, conductivity, oxygen).
  - Map fecundity indicators (eggs per female, gravid proportion) by site and year; assess spatial trends with contamination gradients.
  - Compare temporal changes in developmental stability (2015/2016 vs 2003–2005) and relate to changing dose rates and environmental conditions.
  - Visualize genetic diversity metrics across sites and years to identify spatial patterns of diversity loss or recovery.
- Data preparation steps:
  - Standardize site names and ensure consistent temporal stamps.
  - Address missing values and annotate data gaps.
  - If coordinates are not embedded, georeference sites using Figure S1 or supplementary materials.
- Provenance and access: data generated under TREE project; linkage to published methodology enhances traceability for GIS-derived analyses.

## Provenance and references
- Data sources and methodologies described in the accompanying documentation and related publications (e.g., Fuller et al.; TREE project reports).