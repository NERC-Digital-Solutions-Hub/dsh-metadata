# Dynamic modelling shows substantial contribution of ecosystem restoration to climate change mitigation

## Overview
- Investigates global mitigation potential of five ecosystem-based land management pathways: Forest Restoration, Reforestation, Reduced Harvest, Agroforestry, and Silvopasture.
- Uses a Dynamic Global Vegetation Model (DGVM) to quantify potential contributions to meeting the 1.5°C target.
- Demonstrates spatial analysis of pathway distribution and alternative quantification of land restoration benefits at a global scale.

## Data and modelling framework
- Global datasets identify spatial distribution for each pathway:
  - Forest pathways: Global map of forest condition.
  - Agricultural pathways: ESA-CCI Landcover maps (year 2000) for cropland and grazing lands.
- Additional overlays incorporate precipitation, biodiversity, and social constraints to reduce land area available for restoration.
- Modelling platform: JULES (BE branch) with a 1.875° x 1.25° grid (N96e).
  - Converts primary datasets to uniform resolution (1% of N96e cell size) and to cell percent values.
  - Includes an additional land-use class for agroforestry and auto-planting capabilities.
- Forcing and timelines:
  - Meteorological forcing from UKESM1; historical 1880–2014, SSP1-2.6 2015–2100; 3-hourly timesteps.
  - Baseline land use from IMAGE (HYDE-based) for historical; 2015–2020 for SSP period.
  - 2021–2030: natural land conversion to crops/pasture decelerates linearly to a fixed level by 2030.
- Scenario design:
  - Post-2030: seven simulations (control with no land-cover change; one per pathway P1–P5; and all pathways combined).
  - Pathway area expansion: linearly increases to full extent by 2040, then remains constant.
  - Extended scenario: continued growth to 2150, using 2091–2100 meteorology looped five times (data availability necessitates repetition).

## Data generation and structure
- Output data: raw model results in netCDF format; one file per year per simulation.
- File naming: jules.oneearth.v4_<simulation>.carbon.<year>.nc
  - Simulations include hist (historical LUH2-based), noluc (no land-use change through 2030, then fixed), all (sum of P1–P5), and P1–P5 (Forest Restoration, Reforestation, Reduced Harvest, Agroforestry, Silvopasture).
  - Years: hist (1881–2000), noluc (2001–2150), all/P1–P5 (2001–2150).
- Variables:
  - frac: fractional cover of each surface type.
  - cs: soil carbon per pool (kg m^-2).
  - c_veg: total vegetation carbon per Plant Functional Type (PFT) (kg m^-2) at period end.
  - cv: gridbox mean vegetation carbon (kg m^-2).
- Dimensions and types:
  - Spatial: x, y; type (surface cover type); time (yearly means).
  - Types mapped to surface categories (natural and plantation variants, crops, pasture, urban, water, bare soil, ice, etc.).
- Temporal and geographic scope: annual means; coordinates provided; global coverage.

## Data provenance and accessibility
- This dataset underpins the publication: Littleton, E.W., Dooley, K., Webb, G., et al. (2021) Dynamic modelling shows substantial contribution of ecosystem restoration to climate change mitigation. Environmental Research Letters, 16, 124061.
- JULES model code publicly available via the Met Office Science Repository Service (registration required).
  - Version used: r12164_biotiles_harvest (repository branch specified in documentation).

## Quality and reproducibility
- JULES is maintained to high standards with emphasis on numerical stability and accuracy, aligned with operational Met Office atmospheric models.
- Data structure and metadata are comprehensive to support reproducibility and cross-study use.

## Practical implications for Data Leaders
- Global, high-resolution, time-evolving scenario data require robust governance around:
  - Data provenance and versioning (clearly documented simulations, file naming, and years).
  - Standardized spatial resolution and downsampling procedures to ensure comparability across pathways.
  - Clear metadata for variables, units, and surface-type definitions to support discoverability and reuse.
  - Open access to model code and clear citation of data sources to enable reproducibility and cross-team collaboration.
- The framework demonstrates how multiple interacting data sources (land-use, climate forcing, biodiversity, social constraints) can be integrated to evaluate strategy-level data products for policy guidance.