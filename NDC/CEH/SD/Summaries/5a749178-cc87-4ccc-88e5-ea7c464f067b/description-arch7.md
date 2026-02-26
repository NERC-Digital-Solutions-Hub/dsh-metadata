# Beech tree ring data from hot and dry European distribution edges, 2019

## Overview
- Objective: use the relationship between European Beech growth and environmental factors, including climate, to monitor and forecast drought-related declines in forest growth across Europe.
- Data focus: inter-annual tree growth measured as ring width (dendroecology).

## Sampling and study sites
- 12 sites located in Bulgaria, Albania, Kosovo, and Spain sampled in late 2019.
- Sites chosen at lower elevational ends to represent hot and dry edge conditions of European Beech distribution.
- This sampling addresses climatic gaps in the European Beech Tree Ring Network (EBTRN).

## Field and lab methods
- At least 15 canopy-level trees per site; two cores collected per tree.
- Cores processed using standard dendrology procedures: air-dried, mounted, and sanded through grits 80, 120, 300, 600, and 1200.
- Cores scanned into 2400 PPI images for CDendro measurements with precision of 0.01 mm.
- Cross-dating performed virtually and statistically; COFECH used to control cross-dating quality.

## Data products and structure
- site_meta.csv: metadata for the 12 sites (latitude, longitude, elevation, nearest town/village as of late 2019).
- 12 measurement files: ring width measurements for each site, by year, with units in mm and resolution 0.01 mm.
- File naming: each file corresponds to a site ID.
- Data layout:
  - First column: year.
  - Remaining columns: ring width measurements for each core.
  - Tree core IDs: combination of site ID and tree ID; two cores per tree labeled 'a' and 'b'.
  - 'NA' indicates missing values for a given year.

## Data accessibility and identifiers
- Site-level metadata and per-site measurement files are organized with clear site IDs and consistent year-by-year ring width data.

## GIS relevance and potential uses
- Spatial data: site locations with latitude, longitude, and elevation enable map-based visualization of growth patterns.
- Integrates with climate and environmental datasets to analyze spatial-temporal relationships between growth and drought.
- Useful for policy, client, and public-facing map products illustrating regional drought impacts on Beech forests.

## Notes on data quality and limitations
- NA values indicate data gaps for certain years.
- Cross-dating quality is ensured through virtual/statistical methods and COFECH quality checks.
- Data may require harmonization across sites for cross-site comparative analyses.