# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021

## Overview
- Dataset from the Carbon Storage in Intertidal Environments (C-SIDE) project funded by NERC (NE/R010846/1).
- Captures saltmarsh vegetation composition across the UK (2018–2021) to support understanding of carbon stock in relation to plant communities.
- Intended to enable large-scale analysis and support self-serve data exploration for policymakers and researchers.

## What is in the dataset
- Vegetation composition data for UK saltmarshes from 460 quadrats across 33 sites.
- Measurements include:
  - Plant species coverage by eye (percentage cover per species per quadrat)
  - Mean plant height and standard deviation (from 10 random points per quadrat)
  - Plant species richness per quadrat
  - Plant diversity (Shannon–Wiener index) per quadrat
  - Total plant cover (%)
- Location and site metadata:
  - Marsh_ID, Site_ID
  - Marsh Type: Natural, Historic Breach, Managed Realignment
  - Nation: England, Scotland, Wales
  - Coordinates: Latitude (decimal degrees, WGS84), Longitude (decimal degrees, WGS84)
  - X_Easting and Y_Northing (Irish/UK grid references)
  - Elevation above ordnance datum (m)
  - Survey_Date
- File: UK_saltmarsh_veg_cover.csv
- Data descriptors include detailed field names and formats (e.g., text vs. numeric).

## Methods and data quality
- Sampling design: 1 x 1 m quadrats laid along transects perpendicular to the coastline to capture all marsh zones.
- Data collection:
  - Species coverage estimated by eye within each quadrat
  - Plant height measured at 10 random points per quadrat; mean and standard deviation calculated
  - Species richness counted per quadrat
  - Shannon-Wiener diversity index calculated using species proportions
- Quality assurance:
  - Calibration via expert judgement
  - Two team members independently conducted surveys; results combined
- Notes:
  - Statistical treatment and additional data checking fields are marked NA, indicating standard computations were applied but formal QC metadata is limited in the description.

## Metadata and data structure
- Descriptive fields for each variable are provided, including:
  - Marsh_ID, Site_ID, Marsh Type, Nation
  - Latitude_Dec_Degree, Longitude_Dec_Degree
  - X_Easting, Y_Northing
  - Elevation_above_OD_m
  - Survey_Date
  - Mean_Plant_Height_cm, Plant_Height_SD
  - Plant_species_richness, Plant_S-W_diversity
  - Plant_species_coverage (per species), Plant_total_cover
- Data formats:
  - Primary file format: .csv
  - Column-level descriptions include both content and cell format (Text or Number).

## Location and scope
- Geographic coverage: United Kingdom, with sites chosen across Scotland to enable comparability, and inclusion of England/Wales as applicable.
- Temporal coverage: Surveys conducted during 2018–2021.
- Context: Sites selected to reflect variation in environmental regions, sediment types, and potential organic carbon content.

## How to use and potential applications
- Supports large-scale predictions of saltmarsh carbon stocks when combined with soil and sediment data (as referenced in Ford et al. 2019).
- Enables self-serve analysis of plant community structure and diversity in relation to carbon storage potential.
- Can be integrated into dashboards or reports for policymakers, planners, and researchers.
- Useful for restoration planning and monitoring by comparing vegetation structure with carbon metrics over time.

## References
- Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C. and Skov, M.W., 2019. Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), pp.425-436.
- Pielou, E.C., 1966. Shannon's formula as a measure of specific diversity: its use and misuse. The American Naturalist, 100(914), pp.463-465.