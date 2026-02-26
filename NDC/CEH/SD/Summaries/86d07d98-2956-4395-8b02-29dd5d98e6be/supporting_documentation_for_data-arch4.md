# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

- A high-resolution predictive dataset for Kenya (30 m) modelling soil erosion, nutrient lateral fluxes (SOC, N, P) and topsoil lifespans under predicted erosion, sponsored by UKRI-NERC and part of NC-International.
- Publication date: 17/06/2023. Authors: Feeney et al. (UKCEH) and collaborators. Data available as three multi-band GeoTIFFs:
  - LC16_Results.tif
  - PNV_Results.tif
  - Mitigation_scenarios.tif
- Data are intended to support data-driven soil and land-management planning, with explicit attention to data quality, provenance, and interoperability for use by data leaders and cross-organisational teams.

## What the data represent

- Erosion, nutrient fluxes, and topsoil lifespans are predicted values (not measured) at 30 m resolution across Kenya.
- Predicted outputs include:
  - Long-term annual erosion rate (t ha-1 yr-1)
  - Topsoil lifespan (years)
  - Lateral flux rates via erosion for SOC (t SOC ha-1 yr-1), N (t N ha-1 yr-1), and P (t P ha-1 yr-1)
- Data are stored as integer rasters with conversion factors to retrieve true values, to minimize file sizes while preserving precision.

## Modelling approach and data lineage

- Core model: Revised Universal Soil Loss Equation (RUSLE) applied at national scale (Kenya, 30 m resolution).
  - A = R' × K × LS × C × P'
  - R' (rainfall-runoff erosivity) estimated using rainfall energy and intensity derived from regional regression for East Africa (Moore, 1979) due to sparse high-resolution meteorological data in Kenya.
  - K-factor (erodibility) computed from topsoil properties (OM, M, s, p) using AfSIS/iSDAsoil inputs and FAO soil maps; OM derived from SOC with a standard conversion.
  - LS-factor derived from a 30 m DEM (combined AW3D30, NASADEM, MERITDEM) using a 2D terrain approach; local slope and upslope contributing area computed to represent topography.
  - C-factor for present-day conditions derived from Copernicus Africa land cover map (LC16, 2016). Cropland C-factor calculated via crop-rotation data (FAOSTAT) and 14 crop groups; non-agricultural land C-factor assigned by averaging IGBP type ranges (no MODIS vegetation cover fraction scaling to maintain comparability with East Africa PNV map).
  - P'-factor set to 1 for present-day baseline due to lack of spatial data on agricultural practices; scenarios test mitigation by applying literature-based P' values for tillage and terracing.
- Lateral nutrient fluxes:
  - Nutrient concentrations (SOC, total N, extractable P) from iSDAsoil, combined with erosion rates to estimate soil-associated lateral losses.
  - Convert flux rates to annual t ha-1 values using simple unit conversions (SOC, N, P).
- Topsoil lifespans:
  - Lifespan of the top 20 cm estimated from topsoil mass M' = BD × V, with BD from iSDAsoil and V fixed at 180 m3 per 0.09 ha grid cell (0.2 m depth × 900 m2 area).
  - T = M' / (0.09 × A), noting that this ignores deposition and soil formation processes, so lifespans are conservative estimates of gross erosion impacts.
- Erosion mitigation scenarios:
  - 16 scenario combinations of tillage ( conventional, minimum, mulch, zoned) and terrace/contour practices with associated P'-factors from literature, applied to cropland where LC16 indicates cropland presence.
  - Scenarios quantify potential erosion reductions relative to a baseline “no practices” scenario.

## Data products and structure

- LC16_Results.tif
  - 30 m resolution; coordinate system WGS 1984 Lambert Azimuthal Equal Area (EPSG: 9820)
  - Bands and units:
    1) Erosion rates (t ha-1 yr-1) – 1 decimal place; conversion factor = 10
    2) Lifespans (yr) – 0 decimal places; conversion = 1
    3) SOC flux rates (t SOC ha-1 yr-1) – 1 decimal place; conversion = 10
    4) N flux rates (t N ha-1 yr-1) – 3 decimal places; conversion = 1000
    5) P flux rates (t P ha-1 yr-1) – 3 decimal places; conversion = 1000
- PNV_Results.tif
  - 30 m resolution; same CRS and extent as LC16
  - Same band structure and units as LC16_Results.tif
- Mitigation_scenarios.tif
  - 30 m resolution; same CRS and extent
  - 16 bands, each representing erosion rate reductions for a specific mitigation scenario (t ha-1 yr-1; 1 decimal place; conversion = 10)
- All three files are designed to be loaded in GIS (ArcMap, QGIS) or via R/Python, with clear metadata on spatial resolution, extent, and band meanings.

## Data provenance, quality, and validation

- Quality checks:
  - Consistent spatial resolution, extent, and CRS across all layers (EPSG: 9820).
  - Verified by stacking bands in R; ensured back-convertibility to true values using specified conversion factors.
  - Value ranges checked for positivity; negative values flagged as No-data where present.
  - Cross-validation against Kenya observations compiled by Evans et al. (2020) showed general agreement: lifespans within an order of magnitude, erosion rates within a factor of 2–3 (see Feeney et al. 2023 supplementary materials).
- Data structure and documentation:
  - Detailed metadata provided for each file and band, including units, decimal places, and conversion factors.
  - Documentation includes rationale for RUSLE factor choices, data sources, and limitations (notably that RUSLE gives gross erosion estimates; deposition and soil formation are not accounted for).

## Third-party datasets and data sources

- iSDAsoil soil maps for 0–20 cm layer (SOC, N, OM, bulk density, texture, structure, P extractable, stone content, etc.)
- iSDAsoil covariates: 30 m DEM, 30 m 2016 land cover (Copernicus Africa LC16)
- Africa rainfall/climate data: 1 km monthly rainfall (2007–2018) from SM2RAIN-ASCAT, CHELSA, WorldClim
- FAO datasets: crops/land-use (harvested area, crop groups for C-factor calculation)
- FAO Digital Soil Map of the World and Kenya shapefiles; Potential Natural Vegetation (PNV) map for East Africa
- Supporting literature: foundational methods and parameterisations (Renard et al., Desmet & Govers, Borrelli et al., Panagos et al., Moore 1979, etc.)

## Potential uses for data leaders and organisations

- Strategic data governance and planning:
  - Assess national-scale soil erosion risk and nutrient losses to inform policy and land-management priorities.
  - Compare present-day conditions with natural vegetation baselines (PNV) to identify erosion hotspots and potential conservation opportunities.
- Data interoperability and collaboration:
  - Integrate with partner datasets (soil properties, land use, climate) to support cross-network data products and co-owned tools.
  - Use consistent 30 m spatial framework to align with other high-resolution datasets and decision-support tools.
- Scenario analysis and policy support:
  - Explore erosion mitigation options via the 16 mitigation scenarios; quantify potential gains in erosion reduction and nutrient retention under different practices.
- Data quality and lifecycle:
  - Leverage detailed provenance, conversion factors, and validation notes to maintain data quality and reproducibility; plan for updates when new soil maps or climate data become available.
- Limitations and considerations:
  - RUSLE-based outputs represent gross erosion and exclude deposition/formation processes; lifespans are conservative.
  - R' relies on regression-based estimates due to limited meteorological stations; ongoing data improvements could refine these factors.
  - Present-day C-factor relies on land-cover maps without MODIS vegetation cover fraction adjustments to maintain comparability with East Africa natural vegetation datasets.

## Access and governance notes

- Data are published as openly described GeoTIFF rasters with explicit units, conversions, and documentation to support discoverability and reuse.
- Suitable for integration into organisational data repositories, GIS-based workflows, and analytic pipelines in R, Python, or GIS software.
- For reuse, reference the 2023 Feeney et al. materials and Feeney et al. supplementary materials for methodological details and limitations.