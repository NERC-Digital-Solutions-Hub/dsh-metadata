# Introduction

- Purpose: Describe 1x1 km data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen deposition for 2018–2020, used to summarise exceedances across habitats within grid squares.
- Products: Two raster datasets
  - acid_aae_2018-2020.tif (AAE for acidity)
  - nutn_aae_2018-2020.tif (AAE for nutrient nitrogen)
- Concept: AAE aggregates exceedances for all habitats within a 1x1 km grid square by summing the Accumulated Exceedance (AE) for each habitat and dividing by the total habitat area in the grid square.

## Habitats included

- Acidity (acid_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen (nutn_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data structure and format

- Projections: British National Grid (EPSG:27700)
- Structure: Each dataset is a single-band raster
- Coverage: Slight differences between acidity and nitrogen datasets reflect habitat distributions

## Calculation methodology (high-level)

- AE for each habitat:
  - AE = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
- AAE per grid square:
  - AAE = total AE / total habitat area in the 1x1 km grid square (keq ha-1 year-1)
- Exceedances and critical loads:
  - Acidity: compare deposition to acidity critical loads using CLmaxS, CLmaxN, CLminN; five-region framework for “shortest distance” exceedance on a S–N deposition plot
  - Nutrient nitrogen: exceedances = total N deposition minus habitat-specific nitrogen critical load
- Conversions:
  - For nutrient nitrogen, AAE (keq ha-1 year-1) can be converted to kg N ha-1 year-1 by multiplying by 14
  - Acidity AAE remains in keq ha-1 year-1 (cannot be split into S or N kg values)

## Inputs and data sources

- Deposition data: CBED (Concentration-Based Estimated Deposition)
- Land cover: UK CEH Land Cover Map 2019 1 km summary rasters

## Data quality and interpretation notes

- Based on methods agreed under the UNECE CLRTAP framework (Hall et al., 2015)
- The maps reflect long-term critical loads for steady-state conditions; exceedance indicates potential long-term harm, not immediate damage
- Habitat distribution maps and habitat-area calculations may differ from other UK habitat maps; total habitat areas for acidity and nitrogen may not exactly match
- Recovery after reducing deposition below the critical load can be slow; chemical and biological recovery times may be long

## Use in GIS and practical considerations

- Suitable for map-based visualization and spatial analysis of where acidity and nitrogen exceedances occur at the 1x1 km scale
- Useful for policy briefs, environmental assessments, and habitat risk mapping
- Users should understand the regional and dataset-specific limitations, including dataset coverage and the distinction between grid-based AAE vs catchment-based analyses

## Appendix and methodological details (summary)

- Acidity critical loads:
  - Empirical method for non-woodland mineral/organomineral soils
  - Simple mass balance (SMB) for woodland and peat soils
  - Peat soils use pH buffering-based thresholds (pH ~4.4)
  - Freshwaters use the FAB catchment-based model
- Nutrient nitrogen critical loads:
  - Empirical loads by habitat classes (EUNIS), with ranges (e.g., 10–20 kg N ha-1 yr-1), revised in 2022
- Appendix I (for woodland acidity SMB) provides the SMB equation using Ca:Al ratio and base-cation models

## Documentation and references

- Primary methodological basis: Hall et al. (2015) UK Methods Report; CEH/DEFRA project literature; UNECE CLRTAP practices
- Related outputs: Trends Report (Rowe et al., 2023) and UK Biodiversity Indicator publications
- Data sources: Land Cover Map 2019; CBED deposition data