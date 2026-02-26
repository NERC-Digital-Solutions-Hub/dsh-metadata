# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

- Sponsored by the UK Research and Innovation Natural Environment Research Council as part of the NC-International programme; version date 17/06/2023; authors include Feeney, Robinson, Thomas, Borrelli, Cooper, and May (UKCEH) with contributions from Roma Tre University.

## Overview

- Provides high-resolution (30 m) model predictions of soil erosion by water, lateral fluxes of soil nutrients (SOC, N, P), and topsoil lifespans across Kenya.
- Outputs are designed for use in data-driven assessment of erosion risk, nutrient transport, and land-management impacts, with scenarios to explore erosion mitigation.
- Data are organized into three multi-band geotiff files and accompanied by documentation on data structure, quality control, and third-party data sources.

## Methods and data construction

- Erosion modelling framework:
  - Uses the Revised Universal Soil Loss Equation (RUSLE) to estimate gross soil erosion rate (A) for Kenya at 30 m resolution.
  - A = R' × K × LS × C × P', with P' set to 1 for the national-scale Present-day scenario due to lack of spatially explicit P' data; mitigation scenarios test P' with various practices.
- Factor details:
  - R'-factor (rainfall-runoff erosivity): based on rainfall energy, intensity, and event structure; due to sparse high-resolution rainfall data, regressions (Moore 1979) estimate rainfall kinetic energy and R'. Mean annual rainfall (MAR) used as input for MAR-based regressions; MAR rasters derived from downscaled climate data (2007–2018).
  - K-factor (soil erodibility): computed from topsoil properties (OM, M texture, s, p) using a Wischmeier & Smith-type equation; inputs from iSDAsoil AfSIS data; adjustments include caps on OM (≤4%), silt (<70%), and clay/sand proportions; stone content from iSDAsoil modifies erosion via a stone-correction term.
  - LS-factor (slope length and steepness): calculated with a GIS-based approach (Desmet & Govers, 1996) using a 30 m DEM assembled from AW3D30, NASADEM, and MERITDEM; slope-related parameters and local flow accumulate area are used with a cap at high slopes to avoid overestimation.
  - C-factor (cover-management): split between agricultural and non-agricultural land.
    - Present-day croplands: derived from Copernicus Africa LC16 (2016) and harvested crop area (2012–2016) to describe rotations; 14 crop groups mapped to C-values; overall cropland C-factor computed as a weighted sum (Ccrop) across crops (resulting in 0.353 for Kenyan croplands).
    - Non-agricultural land: aggregated into IGBP land-cover types with average C-factor values from literature; no MODIS vegetation fraction applied to preserve comparability with the Potential Natural Vegetation (PNV) map.
- Nutrient lateral fluxes via erosion:
  - Lateral fluxes correspond to nutrients carried away with eroded soil: SOC, total N, and extractable P (converted to total P using a 7.5% factor).
  - Input topsoil concentrations come from iSDAsoil (SOC, N, P); unit conversions applied to yield flux units in t ha-1 yr-1.
- Topsoil lifespans:
  - Definition: time to remove the top 20 cm of soil due to erosion.
  - Calculation: M' = BD × V, where V = 0.2 m × 900 m2 per grid cell; A is soil erosion rate; T = M' / (0.09 × A) with 0.09 ha as grid cell area.
  - Acknowledges that RUSLE provides gross erosion; deposition processes are not modeled, so lifespans are conservative.
- Erosion mitigation scenarios:
  - Tests 16 combinations of tillage and terrace/contour practices by adjusting P' with published coefficients (tillage: conventional, zoned, etc.; terracing/contouring: bench terracing, contouring, strip cropping, etc.).
  - Approach multiplies cropland erosion reductions (P'-factors) by the cropland area and slope to generate scenario-specific erosion reductions; results stored as Mitigation_scenarios.tif.

## Outputs and data interpretation

- Nature of recorded values:
  - Erosion rates (t ha-1 yr-1)
  - Topsoil lifespans (years)
  - Lateral flux rates: SOC (t SOC ha-1 yr-1), N (t N ha-1 yr-1), P (t P ha-1 yr-1)
- Data are stored as integer rasters with conversion factors provided to recover true values; users should divide by the specified conversion factors to obtain the reported units.

## Data structure and formats

- LC16_Results.tif (Geotiff, INT4S): three or more bands including
  - Erosion rates (t ha-1 yr-1; 1 decimal)
  - Lifespans (yr; 0 decimals)
  - SOC flux rates (t SOC ha-1 yr-1; 1 decimal)
  - N flux rates (t N ha-1 yr-1; 3 decimals)
  - P flux rates (t P ha-1 yr-1; 3 decimals)
  - Conversion factors: erosion 10, lifespans 1, SOC 10, N 1000, P 1000
- PNV_Results.tif (Geotiff, INT4S): same band structure for Potential Natural Vegetation scenario
- Mitigation_scenarios.tif (Geotiff, INT4S): erosion rate reductions under 16 mitigation scenarios; 1 decimal precision per band; conversion factor 10
- Each file is 30 m resolution; CRS: WGS 1984/Lambert Azimuthal Equal-Area (EPSG 9820); extents specified per file
- Quality control notes: consistent resolution/extent/CRS; values checked for positivity; negative values indicate No-data in some cells; data validated against Kenya observations (Evans et al., 2020) with reasonable agreement (lifespans within an order of magnitude; erosion rates within 2–3x).

## Third-party data sources

- iSDAsoil digital soil maps for 0–20 cm soil properties (SOC, N, bulk density, texture, clay/sand/silt, OM, P extractable, stone content, USDA texture class)
- iSDAsoil covariates (30 m DEM, 30 m 2016 land cover LC16)
- Monthly rainfall data for 2007–2018 from SM2RAIN-ASCAT, CHELSA, WorldClim (1 km resolution)
- Africa Soil Profiles Database (ISRIC)
- FAO Digital Soil Map of the World
- FAOSTAT crops and Kenya shapefile; PNV map of East Africa

## Validation and limitations

- Model outputs are predictions rather than measured observations; limited ground-truth data in Kenya exist.
- Validation against available Kenyan data shows lifespans broadly consistent (within an order of magnitude) and erosion rates within a factor of 2–3.
- Limitations acknowledged:
  - P'-factor simplified at national scale; mitigation scenarios rely on assumed combinations of practices and their multipliers.
  - Deposition processes not included; lifespans may be conservative.
  - Cropland C-factor derivation avoids MODIS vegetation fraction to align with PNV comparisons, which may influence present-day vs. natural-vegetation differences.

## How analysts can use the data

- Assess spatial patterns of soil erosion risk and nutrient losses at 30 m resolution for policy or management planning.
- Compare present-day erosion and nutrient fluxes with Potential Natural Vegetation scenarios to evaluate land-use change impacts.
- Explore erosion mitigation options by examining the 16 implemented scenarios and identifying effective combinations of tillage and terracing practices.
- Link erosion rates to topsoil lifespans to quantify long-term soil sustainability under different land-use regimes.
- Incorporate lateral nutrient flux estimates (SOC, N, P) into nutrient budgeting, water quality, or carbon cycling analyses.
- Use the provided data structure to reproduce analyses in R/Python/GIS environments and to facilitate data sharing with metadata as part of a decision-support workflow.