# Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution

- Purpose: Provide model-based predictions of soil erosion, lateral nutrient fluxes (SOC, N, P), and topsoil lifespans across Kenya at 30 m resolution to support policy, planning, and land-management decisions. Outputs include potential mitigation scenarios to assess erosion-reduction options.

- Outputs overview:
  - Three multi-band GeoTIFF raster files at 30 m resolution:
    - LC16_Results.tif: erosion rates, topsoil lifespans, and nutrient flux rates (SOC, N, P) for present-day conditions.
    - PNV_Results.tif: present-day erosion and lifespans under Potential Natural Vegetation (natural-vegetation baseline) conditions.
    - Mitigation_scenarios.tif: reductions in erosion rates under 16 erosion-mitigation scenarios.
  - Bands and content (per file):
    - Erosion rates (t ha-1 yr-1)
    - Topsoil lifespans (years)
    - Lateral flux rates: SOC (t SOC ha-1 yr-1), N (t N ha-1 yr-1), P (t P ha-1 yr-1)
  - Value units have been stored as integers to reduce file size. True values are recovered by dividing by specified conversion factors in the data structure documentation.

- Geographic and temporal scope:
  - Country: Kenya
  - Spatial resolution: 30 m
  - Baseline inputs span data available up to 2016 for land cover (LC16) and 2007–2018 for rainfall data; models predict long-term annual erosion and related fluxes.

- Methodology (key points):
  - Erosion modelling uses the Revised Universal Soil Loss Equation (RUSLE) to predict gross soil erosion (A) as A = R' × K × LS × C × P'.
  - Factors:
    - R' (rainfall-runoff erosivity): derived from rainfall kinetic energy (E) and intensity using regionally calibrated equations; due to sparse high-resolution rainfall data, regional regression relations (Moore 1979) with MAR as mean annual rainfall are used to estimate KE and R'.
    - K-factor (erodibility): computed from topsoil properties (OM, M, s, p) using Wischmeier and Smith; inputs from iSDAsoil 0–20 cm maps; includes adjustments for organic matter, stone content, and soil structure.
    - LS-factor: computed from a 30 m DEM (Desmet & Govers 1996; 2D terrain approach) using a 30 m grid, with slope limits to avoid unrealistically high values.
    - C-factor: present-day is driven by the 2016 Copernicus Africa land cover map (LC16); crops are categorized into 14 groups to assign crop C-factors; non-cropland land cover is mapped to IGBP types with representative C-factors; for comparability with natural vegetation, the Potential Natural Vegetation (PNV) map is used in separate calculations.
    - P'-factor: assumed to be 1 (no explicit spatial data on agricultural practices); mitigation scenarios test combinations of tillage and terracing practices using published P'-values for humid tropics. Scenarios are applied by adjusting erosion rates and comparing against present-day and PNV baselines.
  - Nutrient flux calculations:
    - Lateral fluxes of SOC, N, and P are obtained by multiplying topsoil concentrations (SOC, N, extractable P from iSDAsoil) by erosion rates.
    - P is scaled from extractable P to total P using an average factor (7.5% of total P equals extractable P).
  - Topsoil lifespans:
    - Lifespan T = M' / (0.09 × A), where M' = BD × V (topsoil mass); BD and V (topsoil volume per grid cell) are used to estimate 0.2 m of soil depth across 0.09 ha cell area; lifespans reflect erosion-driven loss of the top 20 cm without accounting for deposition.
  - Mitigation scenarios:
    - 16 scenarios combining tillage practices (conventional, minimum, mulch, zoned) with terracing/contouring strategies; P'-factors are multiplied to yield scenario-specific erosion reductions, which are subtracted from the present-day erosion to show potential gains.

- Data structure and access details:
  - LC16_Results.tif
    - Raster type: INT4S (Geotiff, multi-band)
    - Bands and conversions:
      - Erosion rates: conversion 10; units t ha-1 yr-1; 1 decimal place
      - Lifespans: conversion 1; units yr; 0 decimal places
      - SOC flux rates: conversion 10; units t SOC ha-1 yr-1; 1 decimal place
      - N flux rates: conversion 1000; units t N ha-1 yr-1; 3 decimal places
      - P flux rates: conversion 1000; units t P ha-1 yr-1; 3 decimal places
  - PNV_Results.tif
    - Similar band structure to LC16_Results.tif but representing Potential Natural Vegetation baseline
  - Mitigation_scenarios.tif
    - 16 bands, each representing erosion-rate reductions for a specific scenario; 1 decimal place
  - Spatial reference:
    - Coordinate system: WGS 1984 Lambert Azimuthal Equal Area (EPSG: 9820)
    - Extents and pixel grid align with a 30 m resolution across Kenya; consistent across all three files
  - Conversion notes:
    - Raster values are stored as integers; to obtain true values, apply per-band conversion factors documented in the data-structure section.

- Quality control and validation:
  - Consistency checks:
    - All layers share the same resolution, extent, and CRS
    - Bands stacked and aligned in R
  - Data checks include forward-back conversion accuracy, value ranges, and non-negative values where appropriate
  - Comparisons with observations (Kenya data collated by Evans et al., 2020) show general agreement: lifespans within an order of magnitude; erosion rates within a factor of 2–3
  - Supplementary materials in Feeney et al. (2023) provide additional validation details

- Third-party datasets and sources:
  - iSDAsoil soil maps (0–20 cm) for SOC, N, extractable P, bulk density, and related properties
  - iSDAsoil covariates set (DEM, 30 m land cover 2016, etc.)
  - 1 km monthly rainfall dataset (2007–2018) from SM2RAIN-ASCAT, CHELSA, and WorldClim
  - FAO datasets (soil map of the world; Crops and Livestock data)
  - Kenya shapefiles and Potential Natural Vegetation maps for East Africa
  - DEM inputs from AW3D30, NASADEM, MERITDEM; SAGA-based LS-factor calculation
  - Crop rotation and harvested area data from FAOSTAT

- Intended users and use cases (data support perspective):
  - Policy makers, land managers, and researchers needing high-resolution erosion and nutrient-flux data to inform soil conservation, land-use planning, and resource management
  - Comparative scenario analysis to evaluate the potential impact of terrace development, tillage intensification/reduction, and other conservation practices on erosion and nutrient losses
  - Integrate outputs with GIS workflows for visualization, spatial planning, and risk assessment
  - Use as a baseline for monitoring and as input to broader biophysical or economic impact assessments

- Limitations and caveats:
  - Outputs reflect gross erosion (not net erosion after deposition) and do not account for sediment deposition upslope
  - P'-factor mitigation scenarios assume multiplicative combination of practices and spatially uniform application within croplands where explicit practice data are unavailable
  - PNV and cropland C-factors rely on land-cover data and aggregated IGBP classes; actual on-the-ground variations may differ
  - Temporal coverage is model-based, with inputs relying on available datasets up to ~2016 for land cover and ~2007–2018 for rainfall; real-world dynamics may vary
  - Negative values in raster outputs indicate no-data areas in certain contexts

- How to use and interpret:
  - Load LC16_Results.tif and/or PNV_Results.tif in GIS to view spatial patterns of erosion, topsoil loss, and nutrient fluxes
  - Use the conversion factors in the data-structure section to obtain true, physical units
  - Compare present-day versus natural-vegetation baseline to assess the impact of land-cover and management on erosion and nutrient losses
  - Examine Mitigation_scenarios.tif to identify which combinations of tillage and terracing yield substantial erosion reductions under different slopes
  - Leverage lateral nutrient flux maps (SOC, N, P) to inform nutrient management and soil health planning

- how to cite:
  - Predicted soil erosion rates, nutrient fluxes and topsoil lifespans, modelled for Kenya at a 30 metre resolution. Version date: 17/06/2023. Authors and affiliations listed in the publication.