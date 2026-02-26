# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

## Aim
- Provide modelled predictions of soil erosion, lateral nutrient fluxes (SOC, N, P) via erosion, and topsoil lifespans across Kenya at 30 m resolution to support environmental monitoring and policy evaluation over time.

## What is included
- Model outputs and scenarios intended for monitoring environmental health and policy performance.
- Data generation methods, factor calculations, data structures, and quality control details.
- Outputs are designed to be stored in appropriate data portals and used for dashboards, maps, and reports.

## Data and methods

- Modeling framework
  - Revised Universal Soil Loss Equation (RUSLE) used to predict gross soil erosion rates (A) via water.
  - Predictions at national scale for Kenya, 30 m resolution.
  - A = R' × K × LS × C × P', with P' set to 1 for all grid cells in present-day analyses; detailed exploration of mitigation scenarios multiplies erosion rates by P'-factors.

- Factor definitions and data inputs
  - R'-factor (rainfall-runoff erosivity): derived from rainfall energy (E) and intensity (I30). Due to sparse high-resolution meteorological data in Kenya, regression-based estimates for KE, R, and MAR (mean annual rainfall) are used (Moore 1979; MAR from 1 km downscaled rasters).
  - K-factor (soil erodibility): computed from topsoil properties (OM, M, s, p) using the Wischmeier and Smith function; inputs from iSDAsoil (AfSIS) 0–20 cm layer; OM derived from SOC with a 0.1724 conversion; clay/silt/sand content informs M and p; stone correction applied via Rc and a 30 m stone-content map.
  - LS-factor (slope length and steepness): calculated with a GIS-based 2D terrain method (Desmet & Govers 1996) using a 30 m DEM (AW3D30, NASADEM, MERITDEM) resampled to 30 m; slope limitations applied to avoid exaggeration beyond 26.6° (50%).
  - C-factor (cover-management): computed separately for croplands and non-agricultural land. Present-day LC16 (Copernicus Africa land cover map, 2016) drives C for croplands; harvested crop data (2012–2016) from FAOSTAT informs crop rotations across 14 crop groups to assign group-specific C-values; cropland C-factor for Kenya computed as 0.353. Non-agricultural land uses IGBP classes with average C-ranges from literature; natural vegetation scenarios rely on PNV map rather than MODIS surface cover adjustments.

- Spatial inputs and third-party data
  - iSDAsoil data for soil properties (SOC, N, P, BD, clay, silt, sand, OM, USDA texture, etc.).
  - 30 m DEM (AW3D30, NASADEM, MERITDEM).
  - 1 km monthly rainfall data for 2007–2018 (SM2RAIN-ASCAT, CHELSA, WorldClim variants).
  - FAO/FAOSTAT data for crops; Kenyan country shapefile (Natural Earth); PNV map for East Africa.

- Nutrient fluxes via erosion
  - Lateral fluxes of SOC, N, and P estimated by multiplying topsoil nutrient concentrations (SOC, N, extractable P; with P estimated as total P = extractable P / 0.075) by erosion rates.
  - Units conversions: SOC flux (t SOC ha-1 yr-1), N flux (t N ha-1 yr-1), P flux (t P ha-1 yr-1).

- Topsoil lifespans
  - Topsoil lifespan T (years) defined as time to remove top 20 cm due to erosion.
  - Mass of topsoil M' = BD × V, with V = 180 m3 per 30 m grid cell (0.2 m depth × 900 m2 area); BD in g cm-3 corresponds to t m-3.
  - T = M' / (0.09 × A), where A is the erosion rate (t ha-1 yr-1) and 0.09 ha is the grid cell area.
  - Net deposition is not accounted for; lifespans are likely conservative.

- Erosion mitigation scenarios
  - No agricultural P' factor by default (P' = 1) to reflect lack of spatial data on practices, but mitigation scenarios apply published P'-factors for tillage and terrace practices (16 combinations) to croplands.
  - Scenarios test reductions in erosion via combinations such as bench/continuous terracing, conventional/minimum/mulch tillage, with P'-factors multiplied across practices.
  - Cropland area clipped to LC16, slope reclassified, and erosion rates recalculated for each scenario; reductions are the difference from present-day predictions, compared with Potential Natural Vegetation (PNV) cropland.

## Nature and units of recorded values

- Long-term annual erosion rate: t ha-1 yr-1
- Topsoil lifespan: years
- Lateral flux of SOC via erosion: t SOC ha-1 yr-1
- Lateral flux of N via erosion: t N ha-1 yr-1
- Lateral flux of P via erosion: t P ha-1 yr-1
- Data are stored as integer rasters with conversion factors to enable compact storage; true values require dividing by the specified conversion factors.

## Data outputs and structure

- LC16_Results.tif
  - Geotiff, multi-band INT4S, 30 m resolution, EPSG 9820
  - Bands: Erosion rates (t ha-1 yr-1; 1 decimal), Lifespans (yr; 0 decimals), SOC flux rates (t SOC ha-1 yr-1; 1 decimal), N flux rates (t N ha-1 yr-1; 3 decimals), P flux rates (t P ha-1 yr-1; 3 decimals)
  - Conversion factors: 10 for erosion, 1 for lifespan, 10 for SOC, 1000 for N and P fluxes

- PNV_Results.tif
  - Same format and spatial domain as LC16_Results, for the Potential Natural Vegetation scenario

- Mitigation_scenarios.tif
  - 16 bands representing erosion rate reductions for each scenario (t ha-1 yr-1; 1 decimal)
  - Same spatial domain/resolution as above

- Third-party datasets and references
  - iSDAsoil datasets (soil properties and covariates)
  - 1 km monthly rainfall (SM2RAIN-ASCAT, CHELSA, WorldClim)
  - FAOSTAT crops and NA shapefiles; PNV map for East Africa

## Quality control

- Checks performed 25/04/2023 prior to submission:
  - All layers share the same resolution, extent, and CRS (EPSG: 9820)
  - Bands stacked and aligned in R; unit conversions verified
  - Value ranges and decimal precision verified; positive-value checks; No-data values documented
  - Erosion rates and lifespans compared with observations where available (Kenya, Evans et al., 2020) and found generally in reasonable agreement (lifespans within an order of magnitude; erosion rates within a factor of 2–3)

## Data interpretation and caveats for monitoring

- Outputs are model predictions of gross soil erosion (not net erosion after deposition).
- P-factor assumptions for present-day scenarios reflect lack of spatial data on agricultural practices; mitigation scenarios explore plausible practice combinations.
- Topsoil lifespans are conservative due to not accounting for sediment deposition upslope.

## How this supports environmental monitoring

- Provides a harmonised, high-resolution baseline of erosion, nutrient losses, and soil durability for Kenya.
- Enables comparison over time and across scenarios to evaluate soil health, nutrient leakage, and policy performance.
- Datasets are designed for integration into GIS workflows, dashboards, and policy analysis tools for environmental monitoring and planning.