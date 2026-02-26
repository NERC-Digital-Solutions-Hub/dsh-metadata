# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

## Objective and scope
- Provides modeled estimates of gross soil erosion rates, lateral nutrient (SOC, N, P) fluxes via erosion, and topsoil lifespans (0.2 m depth) across Kenya at 30 m resolution.
- Supports monitoring of environmental health, informs policy scrutiny, and tests erosion mitigation scenarios.

## Key outputs (data products)
- LC16_Results.tif: multi-band geotiff with
  - Erosion rates (t ha^-1 yr^-1, 1 decimal)
  - Topsoil lifespans (years, 0 decimals)
  - SOC flux rates (t SOC ha^-1 yr^-1, 1 decimal)
  - N flux rates (t N ha^-1 yr^-1, 3 decimals)
  - P flux rates (t P ha^-1 yr^-1, 3 decimals)
- PNV_Results.tif: natural vegetation scenario with analogous bands
- Mitigation_scenarios.tif: 16 erosion-rate reduction scenarios (1 decimal) illustrating effects of different tillage and terracing practices
- All datasets stored as Geotiff INT4S with documented conversion factors to recover true values

## Methods at a glance
- Based on Revised Universal Soil Loss Equation (RUSLE) applied nationally for Kenya at 30 m resolution
- Core factors:
  - R' (rainfall-runoff erosivity) derived from rainfall data and kinetic energy (KE) estimates using East Africa regression equations due to limited high-resolution records
  - K-factor computed from topsoil properties (OM, M, s, p) using AfSIS/isda soil maps
  - LS-factor derived from a 30 m DEM (Desmet & Govers) with local slope parameters
  - C-factor split for agricultural and non-agricultural land; cropland C-factor = 0.353 based on crop rotations (2012–2016) and land cover (LC16)
  - P'-factor set to 1 for present-day (no explicit spatial data on practices) and varied in mitigation scenarios
- Erosion and nutrient flux calculations:
  - Lateral fluxes = topsoil nutrient concentrations (SOC, N, extractable P) × erosion rates
  - Extractable P converted to total P using an assumed ratio
- Topsoil lifespans:
  - Lifespan T = M' / (0.09 × A), where M' is topsoil mass (BD × V) and A is annual erosion rate
  - Assumes 0.2 m topsoil layer and 0.09 ha area per grid cell; deposition/soil formation not included

## Data inputs and third-party datasets
- iSDAsoil 0–20 cm soil properties (SOC, N, bulk density, texture, organic matter, etc.)
- iSDAsoil covariates: 30 m DEM, 30 m land cover (LC16, 2016)
- 1 km monthly rainfall data (2007–2018) from SM2RAIN-ASCAT/CHELSA/WorldClim integration
- FAOSTAT harvested crop data (for C-factor by crop groups)
- PNV map for East Africa (natural vegetation baseline)
- FAO Digital Soil Map of the World; Kenya shapefile; Africa soils databases
- Observational comparisons: Kenya-basin assessments (Evans et al., 2020) for QA context

## Data structure and units
- LC16_Results.tif, PNV_Results.tif: multi-band INT4S rasters, 30 m resolution, EPSG: 9820
- Bands and units:
  - Erosion rates: t ha^-1 yr^-1 (1 decimal, conversion factor = 10)
  - Lifespans: years (0 decimals, conversion = 1)
  - SOC/N/P flux rates: t ha^-1 yr^-1 or SOC-specific units (N, P with decimals; conversions applied)
- Mitigation_scenarios.tif: 16 bands, each representing erosion-rate reductions (t ha^-1 yr^-1) under specific practice combinations; 1 decimal, conversion = 10
- Detailed metadata on file structure and conversion factors provided to recover true values

## Quality control and validation
- All layers share consistent resolution, extent, and CRS; QA performed in R
- Spatial extents and cell sizes verified; no-data handling documented
- Value checks ensure non-negative values where appropriate; negatives flagged as No-data
- Model outputs compared with observed Kenyan data where available:
  - Lifespans generally within an order of magnitude
  - Erosion rates within a factor of 2–3 of observations (Evans et al., 2020; Bagarello et al., 2012)
- Supplementary materials of Feeney et al. (2023) provide additional validation details

## Implications for monitoring frameworks
- Delivers a high-resolution, policy-relevant suite of indicators for soil health: erosion intensity, topsoil depletion risk, and nutrient (SOC, N, P) mobility
- Enables scenario analysis to evaluate erosion-mitigation strategies (tillage, terracing, contour practices) at national scale with spatially explicit outcomes
- Demonstrates integration of diverse data sources (soil maps, climate data, land cover, crop statistics) and transparent data processing steps, including unit conversions and metadata implications
- Highlights data governance considerations for monitoring:
  - Use of third-party datasets with clear provenance
  - Need for metadata standards and data-sharing practices to ensure reproducibility and transparency
  - Conversion factors and data storage choices to balance file size with usability across GIS and scripting environments