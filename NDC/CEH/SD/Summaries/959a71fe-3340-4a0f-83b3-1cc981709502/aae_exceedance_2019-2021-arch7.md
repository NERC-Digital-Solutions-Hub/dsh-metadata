# Introduction

- This document describes two 1x1 km raster datasets of Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen (N) deposition for 2019–2021 in the UK.
- AAE summarises exceedances across habitats within each 1x1 km grid cell: AAE = AE / total habitat area, where AE = exceedance (keq ha−1 year−1) × exceeded habitat area (ha). Units are keq ha−1 year−1.
- The two rasters are:
  - acid_aae_2019-2021.tif (acidity AAE)
  - nutn_aae_2019-2021.tif (nutrient nitrogen AAE)
- Projections: British National Grid (EPSG:27700); each file has a single band.

## What is included in the habitats

- Acidity AAE (acid_aae_2019-2021.tif) includes: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen AAE (nutn_aae_2019-2021.tif) includes: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## How AAE is calculated (concept)

- For each habitat in each grid cell, AE = exceedance (keq ha−1 year−1) × habitat area (ha).
- AAE = total AE across all habitats in the cell ÷ total habitat area in the cell.
- This means AAE may be zero if deposition is below the critical load for that habitat.

## Critical loads, exceedances, and interpretation

- Exceedances are determined relative to habitat-specific critical loads for acidity and nutrient nitrogen.
- Acidity is governed by a combined S and N deposition function; exceedances are classified via a “shortest distance” approach from a defined critical-load function (CLmaxS, CLminN, CLmaxN).
- For acidity, two calculation methods:
  - Empirical approach for non-woodland mineral/organomineral soils.
  - Simple mass balance (SMB) for woodland and peat soils.
- For nutrient nitrogen, empirical critical loads (ranges) are assigned to habitat classes (EUNIS) and recently revised in 2022.
- Important interpretation notes:
  - Exceedance indicates potential for harm under steady-state conditions; not an immediate signal of damage.
  - Habitat maps and habitat-area calculations used in these datasets may differ from other national maps.
  - Recovery after reducing deposition can take long time (chemical and biological lags).

## Inputs and data sources

- Deposition data: CBED (Concentration-Based Estimated Deposition) method.
- Land cover: UK CEH Land Cover Map 2019 (1 km summary rasters).

## Data structure and metadata

- Two rasters (acid_aae_2019-2021.tif and nutn_aae_2019-2021.tif) with 1 band each.
- Coverage differs between acidity and nutrient nitrogen datasets due to habitat distributions.
- Values are in keq ha−1 year−1; for nutrient nitrogen, 1 keq ha−1 year−1 equals 14 kg N ha−1 year−1.
- If deposition is below the critical load, AAE is set to zero.

## Quality and provenance

- Methods aligned with national/international guidance under CLRTAP; detailed UK Methods Report (Hall et al., 2015) provides full transparency.
- Summary exceedance statistics and trends are published in related reports (e.g., Rowe et al., 2023) and UK Biodiversity Indicator.

## Practical considerations for GIS use

- The AAE rasters are designed for map-based data visualization to help audiences explore spatial patterns of exceedance.
- When interpreting results:
  - Be aware that AAE and exceedances reflect potential long-term risks, not immediate ecological damage.
  - Data cover only areas with available data for critical-load calculations; may not align exactly with other habitat maps.
  - Time lags in chemical and biological recovery mean reductions in deposition do not guarantee rapid ecosystem recovery.

## End notes

- Methodological context and references are provided (e.g., Hall et al., 2015; Rowe et al., 2023).
- Appendices include detailed equations for acidity (e.g., SMB for woodland) and related parameters.