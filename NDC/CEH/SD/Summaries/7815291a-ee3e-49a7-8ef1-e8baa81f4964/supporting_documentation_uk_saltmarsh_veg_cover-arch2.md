# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project funded by NERC (NE/R010846/1) with staff including Craig Smeaton and a multi-institution research team (University of Glasgow, St Andrews, York, Bangor, UK CEH, SAS, etc.).
- Objective aligned with environmental monitoring: provide standardized data to assess environmental health and inform carbon storage estimates in intertidal saltmarshes.

## Data Resource Description
- Dataset: Saltmarsh vegetation composition data from 460 quadrats across 33 UK saltmarshes, collected 2018–2021.
- Location: United Kingdom; sites concentrated in Scotland with broader UK representation to capture saltmarsh variation in marsh types and carbon content.
- File format: CSV (UK_saltmarsh_veg_cover.csv and related metadata).

## Variables and Observations
- Spatial and environmental variables:
  - Latitude, Longitude (decimal degrees, WGS84)
  - X_Easting, Y_Northing
  - Elevation above Ordnance Datum (m)
  - Survey_Date
- Vegetation metrics (per quadrat):
  - Mean_Plant_Height_cm and Plant_Height_SD (from 10 height measurements per quadrat)
  - Plant_species_richness (count of species per quadrat)
  - Plant_S-W_diversity (Shannon-Wiener index)
  - Plant_total_cover (total plant cover %)
  - Plant_Species (percentage cover of individual species; 58 species recorded)
- Site and marsh descriptors:
  - Marsh_ID (saltmarsh name)
  - Site_ID (quadrats labeled by site/quadrat)
  - Marsh_Type (Natural; Historic Breach; Managed Realignment)
  - Nation (England; Scotland; Wales)
- Data collection details:
  - 1 x 1 m quadrats arranged along transects perpendicular to the coastline to capture all marsh zones
  - Percentage plant cover estimated by eye; height measured at 10 random points per quadrat
  - Species richness as number of species per quadrat
  - Diversity calculated using Shannon-Wiener index
- Calibration and quality control:
  - Expert judgement used for species coverage where needed
  - Two team members conducted surveys independently; combined results reported
  - Some data quality checks noted as NA in the credit (no additional QA steps specified for all fields)

## Data Use and Standardization
- Outputs support consistent monitoring of saltmarsh vegetation and potential carbon stock estimation.
- Standardized methods enable temporal and spatial comparisons across sites.
- References underpinning methods:
  - Ford et al. 2019 for large-scale predictions of saltmarsh carbon stock (based on vegetation and soil observations)
  - Pielou 1966 for Shannon-Wiener diversity calculation

## Location and Site Details
- Sites chosen to reflect Scotland’s coastline; locations described with precise coordinates and alternative coordinate representations (lat/long and UTM-like easting/northing).
- Marsh types and national classifications provide context for environmental variation and management regimes.

## Relevance for Monitoring Practice
- Demonstrates how to structure and store environmental monitoring data to support policy performance and health assessments over time.
- Addresses common monitoring challenges:
  - Facilitating data reuse by documenting variables, methods, and site descriptors
  - Enabling integration with other datasets (e.g., soil type, carbon measurements) to enhance dataset value

## References
- Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C. and Skov, M.W., 2019. Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), pp.425-436.
- Pielou, E.C., 1966. Shannon's formula as a measure of specific diversity: its use and misuse. The American Naturalist, 100(914), pp.463-465.