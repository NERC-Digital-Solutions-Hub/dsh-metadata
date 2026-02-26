# Dynamic modelling shows substantial contribution of ecosystem restoration to climate change mitigation

## Objective and approach
- Global-scale assessment of five ecosystem-based land management pathways for carbon mitigation using a Dynamic Global Vegetation Model (DGVM).
- Pathways: Forest Restoration; Reforestation; Reduced Harvest; Agroforestry; Silvopasture.
- Uses JULES (JULES-BE branch) to model plant growth and ecosystem carbon balance on a global grid, allowing analysis of spatial distribution and mitigation potential.

## Pathways analyzed
- Forest Restoration: 541 Mha degraded forests allowed to regenerate.
- Reforestation: 344 Mha deforested land allowed to regenerate.
- Reduced Harvest: 1047 Mha of managed forests allowed to regenerate.
- Agroforestry: 849 Mha of cropland planted with trees.
- Silvopasture: 478 Mha of pasture land planted with trees at 20% cover.

## Data and inputs
- Spatial distributions derived from global datasets:
  - Global map of forest condition for forest pathways.
  - ESA-CCI Landcover (2000) for cropland and grazing lands (agricultural pathways).
- Overlay with additional constraints:
  - Precipitation, biodiversity, social constraints to limit feasible restoration area.
- Land-use distributions on a 3-hourly-forcing grid (N96e, 1.875° x 1.25°) converted to cell-level fractions (percentages).

## Modelling framework and resolution
- Model: JULES v5.1 (JULES-BE) with biotiles/habitat features to represent agroforestry and agricultural expansion.
- Forcing: UKESM1 meteorological output (historical 1880–2014; SSP1-2.6 2015–2100).
- Temporal resolution: 3-hourly time steps; outputs compiled as annual means.

## Simulation design and scenarios
- Baseline: 1880–2014 (historical climatology and LUH2-based land use).
- Future: 2015–2100 (SSP1-2.6 scenario).
- 2021–2030: conversion rates from natural land to cropland/pasture reduced linearly to a fixed level by 2030.
- 2031 onward: seven simulations run in parallel:
  - One control: no further land-cover transitions.
  - One for each pathway (P1–P5).
  - One with all pathways applied together.
- Pathway area expansion: restored/restored land increases linearly over a decade, reaching full extent by 2040; remains fixed thereafter.
- Extended run to 2150: meteorological forcing from 2091–2100 repeated five times to cover an extra 50 years (data beyond 2100 not available).

## Data outputs and structure
- Output format: raw model outputs in netCDF, one file per year per simulation.
- File naming: jules.oneearth.v4_<simulation>.carbon.<year>.nc
- Simulations include: hist; noluc (no land-use change; constant post-2030); all; P1; P2; P3; P4; P5.
- Key variables:
  - frac: fractional cover of each surface type (units: 1).
  - cs: soil carbon per pool (kg m^-2).
  - c_veg: total vegetation carbon per PFT (kg m^-2).
  - cv: gridbox mean vegetation carbon (kg m^-2).
- Spatial and categorical details:
  - Surface-cover types include a wide range from natural evergreen/deciduous trees to grasses (C3/C4), shrubs, urban areas, water, bare soil, land ice, etc.
  - PFTs and surface types aligned with 20 plant functional types (PFTs) and corresponding land-cover categories.
- Outputs are annual means for the calendar year of each file.

## Data provenance and reproducibility
- Data underpin the publication: Littleton et al. (2021) Environmental Research Letters.
- JULES code publicly available via the Met Office repository; specific version used: r12164_biotiles_harvest.
- Detailed methods and data structure provided to enable replication and secondary analyses.

## Relevance for analysts
- Provides spatially explicit estimates of how ecosystem restoration pathways could contribute to climate change mitigation under a 1.5°C pathway.
- Enables comparison of individual pathways vs. combined effects and assessment of land-use change versus business-as-usual scenarios.
- The rich netCDF outputs offer metrics on surface cover, soil carbon pools, and vegetation carbon, suitable for downstream statistical analyses, modeling, and policy assessment.
- Data volume and structure require processing pipelines to extract annual, pathway-specific, and spatially resolved carbon outcomes.