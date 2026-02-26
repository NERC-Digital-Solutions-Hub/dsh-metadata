# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

- The document describes modelled predictions of soil erosion rates, lateral fluxes of soil organic carbon (SOC), nitrogen (N) and phosphorus (P), and topsoil lifespans across Kenya at 30 m resolution.
- Data products are intended to support understanding of erosion risks and nutrient losses, and to evaluate erosion mitigation scenarios.

## Data products and contents

- Three multi-band GeoTIFF files:
  - LC16_Results.tif: erosion rates, topsoil lifespans, SOC fluxes, N fluxes, P fluxes (scaled as integer rasters with conversion factors).
  - PNV_Results.tif: present natural vegetation scenario erosion rates, lifespans, SOC, N, P fluxes.
  - Mitigation_scenarios.tif: reductions in erosion rates under 16 mitigation scenarios (various tillage and terracing combinations).
- Each file uses:
  - Spatial resolution: 30 m
  - Coordinate system: WGS 1984 Lambert Azimuthal Equal Area (EPSG 9820)
  - Extents and scaling documented; units and decimal places specified per band.
- Recorded values (before conversion) include:
  - Erosion rate (t ha-1 yr-1)
  - Topsoil lifespan (yr)
  - SOC, N, P lateral fluxes (t ha-1 yr-1 for SOC; t N ha-1 yr-1; t P ha-1 yr-1)
- Conversion factors are provided to retrieve true values from integer rasters.

## Modelling approach and data sources

- Erosion modelling framework:
  - Uses Revised Universal Soil Loss Equation (RUSLE) to predict gross soil erosion rate (A) as A = R' × K × LS × C × P'.
  - R' (annual rainfall-runoff erosivity) derived from rainfall energy and intensity; when detailed data are sparse, KE–R relationships (Moore 1979) estimate KE and R'.
  - MAR (mean annual rainfall) derived from 1 km monthly rasters (2007–2018) downscaled inputs.
  - K-factor calculated from topsoil properties (OM, texture, structure, permeability) using AfSIS/iSDAsoil inputs; adjustments for OM > 4%, silt content (<70%), and stone fragments included.
  - LS-factor computed from a 30 m DEM using Desmet & Govers (1996) methodology; adjusted for maximum slope to avoid overestimation.
  - C-factor: present-day croplands (LC16 2016) with crops grouped into 14 categories to derive a crop-based C-factor (overall cropland C ≈ 0.353). Non-agricultural land uses assigned IGBP-type C-factors (mean of min/max of the range for each type); natural vegetation scenario uses PNV map without cropland C-factor.
- Erosion mitigation scenarios:
  - Baseline P' = 1 (no agricultural support practices) due to lack of spatial data on practices in Kenya.
  - 16 scenario combinations of tillage and terracing/contouring, with P'-factors drawn from literature for humid tropics; scenarios implemented by adjusting cropland erosion rates and comparing to present-day and PNV scenarios.
- Lateral nutrient fluxes:
  - Fluxes defined as nutrients lost from a grid cell via erosion.
  - SOC, N, extractable P concentrations from iSDAsoil used to compute lateral fluxes by multiplying nutrient maps by erosion rates.
  - P concentration estimated from extractable P by assuming total P = extractable P / 0.075 (average 7.5% extractable).
  - SOC and N fluxes converted to t ha-1 yr-1 with specified unit conversions.
- Topsoil lifespans:
  - Defined as time for the top 20 cm to be eroded away.
  - Topsoil mass M' = BD × V, with V = 180 m3 per 0.09 ha cell (0.2 m depth over 900 m2).
  - Lifespan T = M' / (0.09 × A), where A is the gross erosion rate.
  - Depositional processes not included; lifespans are conservative estimates since erosion is gross (not net erosion).
- Third-party datasets:
  - iSDAsoil soil properties (SOC, N, P, bulk density, texture, structure, stone content, etc.).
  - 30 m DEM (from AfSIS covariates and added sources).
  - Copernicus Africa land cover map (LC16, 2016).
  - FAOSTAT crop data and rotation estimates; FAO/World Bank datasets for crops and soils.
  - PNV map for East Africa (natural vegetation baseline).
  - Additional datasets for validation and context (Evans et al., 2020; Hengl et al., 2021; FAO soil maps; etc.).

## Data structure and usage details

- LC16_Results.tif:
  - Band 1: Erosion rates (t ha-1 yr-1), 1 decimal place, conversion factor 10
  - Band 2: Lifespans (yr), 0 decimals, conversion 1
  - Band 3: SOC flux rates (t SOC ha-1 yr-1), 1 decimal place, conversion 10
  - Band 4: N flux rates (t N ha-1 yr-1), 3 decimals, conversion 1000
  - Band 5: P flux rates (t P ha-1 yr-1), 3 decimals, conversion 1000
- PNV_Results.tif and Mitigation_scenarios.tif share similar band structures for erosion, lifespans, and fluxes, with 16 bands in the mitigation file corresponding to each scenario.
- File metadata includes spatial extent, cell size (30 m), CRS, and explicit conversion guidance to obtain true values.
- Data quality checks ensured consistent resolution, extent, CRS, and proper back-conversion to true values; value ranges and positivity checks performed; negative values flagged as No-data in some cases.
- Validation against observed Kenyan data (Evans et al., 2020) showed general agreement: lifespans within an order of magnitude and erosion rates within a factor of 2–3.

## Quality control and provenance

- Quality control:
  - All layers aligned to the same grid, resolution, and CRS; checks performed in R.
  - Back-conversion and decimal precision verified; positive values checked; No-data indicated where applicable.
  - Extents and band information verified for the three output files.
- Provenance and data sources:
  - Original modelling framework based on Feeney et al. (2023) Science of the Total Environment.
  - Third-party inputs from AfSIS/iSDAsoil, Hengl et al. (2021), FAO datasets, FAOSTAT, COPERNICUS LC16, and PNV maps.
- Documentation availability:
  - Detailed methods, data structure, and third-party datasets documented within the dataset package and supplementary materials of the referenced publications.

## Governance, accessibility, and usage notes for Data Stewards

- Purpose and scope:
  - Provides high-resolution, model-based estimates of soil erosion, nutrient losses, and topsoil lifespans to support data governance, planning, and policy analysis.
- Discoverability and sharing:
  - Data are organized as three geotiff files with explicit band definitions, extents, and conversion factors to facilitate reuse and interoperability.
  - Available through the Environmental Information Data Centre (EIDC) with accompanying methodological documentation.
- Metadata and standards:
  - Clear documentation of data structure, units, and conversions aligns with data stewardship aims for discoverability and reusability.
  - Abbreviations and input datasets are catalogued, with case-sensitive handling (e.g., M vs m, P vs p) to maintain data integrity.
- Data quality and limitations:
  - Acknowledges that RUSLE provides gross erosion estimates; lifespans are conservative due to lack of deposition data.
  - Validation indicates reasonable agreement with available Kenyan observations, though regional data gaps exist.
- Future upkeep and updates:
  - Baseline and scenario analyses can inform ongoing monitoring of erosion risk and nutrient losses under changing land-use and management practices.
  - Potential updates could incorporate improved practice data (P-factor spatial layers) to replace the baseline P' = 1 assumption where available.

## Reference and contact

- Authors: Feeney, C.; Robinson, D.; Thomas, A.; Borrelli, P.; Cooper, D.; May, L. (UKCEH and partner institutions)
- Version/date: 17/06/2023
- Sponsor: UK Research and Innovation NERC NC-International programme (NE/X006247/1)