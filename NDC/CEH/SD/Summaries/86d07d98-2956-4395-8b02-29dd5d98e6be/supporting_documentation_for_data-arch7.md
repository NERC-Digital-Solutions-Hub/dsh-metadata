# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

## Overview
- A high-resolution (30 m) dataset modelling soil erosion, nutrient (SOC, N, P) lateral fluxes, and topsoil lifespans across Kenya.
- Produced under the NC-International programme (NERC/UKRI) with authors from UKCEH and partner institutions; version dated 17/06/2023.

## Data products (GIS-ready outputs)
- LC16_Results.tif: multi-band GeoTIFF of present-day predictions
  - Band 1: Erosion rates (t ha-1 yr-1)
  - Band 2: Topsoil lifespans (yr)
  - Band 3: SOC lateral flux rates (t SOC ha-1 yr-1)
  - Band 4: N lateral flux rates (t N ha-1 yr-1)
  - Band 5: P lateral flux rates (t P ha-1 yr-1)
- PNV_Results.tif: multi-band GeoTIFF under Potential Natural Vegetation (natural baseline)
  - Same band structure as LC16_Results
- Mitigation_scenarios.tif: 16 erosion-reduction scenarios (each band corresponds to a scenario in which erosion rates are reduced by P'-factor based adjustments)
- Notes: raster values stored as integers to minimise file size; users must apply conversion factors to recover true values.

## Modelling approach (RUSLE-based)
- Erosion modelling using Revised Universal Soil Loss Equation (RUSLE):
  - A = R' × K × LS × C × P'
  - Present-day baseline: P' set to 1 (no explicit agricultural practices)
  - R' (rainfall-runoff erosivity) derived from rainfall energy (E) and 30-minute intensity (I30); due to sparse data in Kenya, calibrated via East Africa regression equations to estimate KE and R' from mean annual rainfall (MAR).
  - K-factor derived from topsoil properties (OM, M texture, s, p) using AfSIS/iSDAsoil data; adjusted for OM cap, silt thresholds, and stone fragment corrections.
  - LS-factor computed from a 30 m DEM (Desmet & Govers 1996) using a 2D terrain approach; DEM compiled from AW3D30, NASADEM, MERITDEM; caveats for slopes >50% (exaggeration risk).
  - C-factor separated for agricultural and non-agricultural land; present-day C based on Copernicus Africa LC16 (2016). Cropland rotations (2012–2016) described using FAOSTAT data to assign crop-specific C-values; non-agricultural land cover mapped to IGBP types with representative C-values. Optional MODIS-based vegetation cover adjustment omitted to stay comparable with the Potential Natural Vegetation map.
- Erosion-mitigation scenarios:
  - P'-factor adjustments representing tillage practices and terracing/contouring; 16 combinations tested for croplands, using published P'-factor values for humid tropics.
  - Scenarios implemented by adjusting cropland erosion rates and comparing with present-day and PNV baselines.

## Key inputs and data sources ( GIS data and ancillary datasets)
- iSDAsoil 0–20 cm soil properties (SOC, Total N, Extractable P, bulk density, clay/sand/silt contents, organic matter, USDA texture, stone content, etc.)
- AfSIS Africa soil maps and related covariates (soil structure class, WRB group)
- DEM: 30 m resolution (AW3D30, NASADEM, MERITDEM)
- Copernicus Africa land cover map (LC16, 2016)
- 1 km monthly rainfall for 2007–2018 (SM2RAIN-ASCAT, CHELSA, WorldClim) for MAR-based R' calibration
- FAOSTAT crop area data (for crop rotations), used to derive C-factors for croplands
- Potential Natural Vegetation (PNV) map for East Africa (for natural baseline scenarios)
- FAO Digital Soil Map of the World; Kenya country shapefile; Natural Earth 1:10m shapefile for country boundaries
- Third-party soil datasets and related literature (e.g., Evans et al. 2020 for validation context)

## Outputs: units, conversion, and data structure
- Recorded values and units (as per data structure notes):
  - Erosion rates: t ha-1 yr-1
  - Topsoil lifespans: yr
  - Lateral fluxes: t SOC ha-1 yr-1 (SOC), t N ha-1 yr-1 (N), t P ha-1 yr-1 (P)
- Integer raster storage with conversion factors to recover true values:
  - LC16_Results.tif
    - Erosion rates: conversion factor 10 (divide by 10 to get true value)
    - Lifespans: conversion factor 1
    - SOC flux: conversion factor 10
    - N flux: conversion factor 1000
    - P flux: conversion factor 1000
  - PNV_Results.tif: same structure and conversion factors as LC16_Results
  - Mitigation_scenarios.tif: erosion rate reductions; conversion factor 10
- Spatial properties:
  - Coordinate system: WGS 1984 / Lambert Azimuthal Equal Area (EPSG 9820)
  - Resolution: 30 m
  - Extents aligned with Kenyan grid coverage as described in data structure
- Quality control:
  - Processed to ensure identical resolution/extents and CRS across layers
  - Verified back-conversion to true-values and appropriate decimal precision
  - Positive-only values (with some annotated No-data cases)

## Data structure details (three multi-band GeoTIFFs)
- LC16_Results.tif
  - Band 1: Erosion rates (t ha-1 yr-1); conversion 10
  - Band 2: Lifespans (yr); conversion 1
  - Band 3: SOC flux (t SOC ha-1 yr-1); conversion 10
  - Band 4: N flux (t N ha-1 yr-1); conversion 1000
  - Band 5: P flux (t P ha-1 yr-1); conversion 1000
- PNV_Results.tif
  - Same band configuration and units/conversions as LC16_Results
- Mitigation_scenarios.tif
  - Bands 1–16: erosion-rate reductions for each mitigation scenario; conversion 10

## Spatial validation and limitations
- Modelled erosion rates and lifespans are based on gross erosion (not net erosion after deposition), so lifespans may be conservative.
- Validation against available Kenyan observations shows reasonable agreement (lifespans within an order of magnitude; erosion within a factor of 2–3 where data exist).
- Topsoil properties and K-factor inputs rely on regional soil datasets (iSDAsoil/AfSIS) and carry uncertainties inherent to spatially variable soil properties.
- RUSLE-based approach does not account for all processes (e.g., deposition/soil formation rates) and uses present-day P' factor assumptions unless exploring mitigation scenarios.

## Usage notes for GIS specialists
- Load the three GeoTIFFs in ArcMap, QGIS, or through R/Python GIS workflows.
- To interpret actual values, apply the specified conversion factors to each band as indicated in the data-structure table.
- Ensure use of EPSG 9820 for consistent projection; be mindful of extents and cell size (30 m) when resampling or reprojecting.
- For scenario analysis, compare Mitigation_scenarios.tif against LC16_Results.tif to visualize reductions in erosion rates across Kenya.
- Refer to the Feeney et al. (2023) supplementary materials for methodological details and broader context on data generation and limitations.

## Third-party data and references
- Data sources and RAM-based calibrations drawn from iSDAsoil, AfSIS, Copernicus LC16, FAOSTAT, SM2RAIN-ASCAT CHELSA WorldClim, and the PNV map of East Africa.
- Key literature underpinning RUSLE factors, C- and P-factor derivations, and validation context as listed in the document references.