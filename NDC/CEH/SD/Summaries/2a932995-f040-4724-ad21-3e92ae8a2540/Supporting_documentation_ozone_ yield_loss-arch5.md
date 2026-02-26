# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2.

## Aim and scope
- Model-based estimate of annual average percentage yield loss due to ozone for four crops (maize, rice, soybean, wheat) over 2010–2012.
- Grid-based outputs (1° by 1°) with per-grid-cell yield loss to aid understanding of spatial patterns and potential impacts on global crop production.
- Uses FAO GAEZ crop production context and established ozone-response methodologies.

## Data generation and workflow
- Grid construction and inputs
  - Created a 1° by 1° grid; used FAO GAEZ data (2000) for total crop production, distinguishing irrigated vs non-irrigated production.
  - Converted national production data to grid-cell estimates using a factor derived from differences between 1999–2001 and 2010–2012 periods.
  - Included only grid cells with more than 500 tonnes production; classified cells as irrigated if >75% of production was irrigated.
  - Assigned hemisphere (North/South) and climate zone using ESDAC/JRC climate zone raster.
  - Established a 90-day growing period per climate zone/hemisphere, based on main growing seasons (USDA/FAO data); table of growing periods per crop per zone provided (Table S1 in Mills et al. 2018a).
- Ozone impact calculation framework
  - Wheat baseline: calculated daily ozone flux using EMEP MSC-W model (version 4.16) to derive POD3IAM (phytotoxic ozone dose above 3 nmol m-2 s-1).
  - For each grid cell, accumulated 90-day POD3IAM using the crop’s climate-specific growing period; separated for irrigated vs rain-limited (non-irrigated) conditions.
  - Yield loss for wheat: Percent Yield Loss = (POD3IAM - 0.1) × 0.64, where 0.1 mmol/m2 is a pre-industrial/reference POD3IAM, and 0.64 is the slope from the dose-response relationship.
  - For maize, rice, and soybean: since flux-response data are limited, convert wheat yield loss to these crops using relative ozone sensitivity derived from M7 (7-hour mean ozone; ppb) response functions. Relative sensitivity = slope of crop’s M7 response divided by wheat’s slope.
  - Final yield loss for each crop per grid cell: wheat baseline yield loss × crop-specific relative sensitivity.
- Output and storage
  - Results are added to the 1° by 1° grid and saved as GIS shapefiles, with one file per crop (maize, rice, soybean, wheat).

## Data structure and format
- Four GIS shapefiles (one per crop), gridded at 1° by 1° resolution.
- Attributes per grid cell:
  - ID: unique grid cell identifier
  - Zone: climate zone
  - Long_Lat: centre coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South
  - Yloss: annual average percentage yield loss for 2010–2012

## Quality control and validation
- Model validation for EMEP model described in Mills et al. 2018b; comparison with Global Atmosphere Watch (GAW) site data shows good performance in peak ozone periods.
- Key validation metrics:
  - Seasonal Dmax and M7 values compared to observed data across 2012; r^2 between 0.88 and 0.93 after outlier handling.
  - Stomatal uptake proxy (AET/PET versus POD3IAM/M7) shows a strong relationship (r^2 ≈ 0.63), supporting reasonable estimation of stomatal uptake.
- Caveats acknowledged:
  - Flux-response data exist for wheat but are limited for maize, rice, and soybean; use of relative sensitivity introduces additional uncertainty.
  - Limited maize data (only three older varieties) increases uncertainty for that crop.
  - In climates with multiple growing seasons, only the most important season is used.
  - Potential non-interoperability of some climate or cropping systems; global-scale extrapolation noted.

## Data provenance, limitations, and caveats
- Primary data sources:
  - EMEP MSC-W model (v4.16) for ozone flux (POD3IAM) and related calculations.
  - CLRTAP dose–response framework (2017) for wheat yield loss.
  - M7 ozone response functions and related crop sensitivity data.
  - FAO GAEZ crop production data; USDA/FAO references for growing periods.
  - Climate zone raster from ESDAC/JRC.
- Limitations:
  - Use of wheat flux–response as a proxy for other crops due to data gaps; future species-specific flux data recommended.
  - Data reflect the 2010–2012 period; applicability to other periods requires re-analysis with updated inputs.
- Cited references for methodology and validation are Mills et al. 2018a, Mills et al. 2018b, CLRTAP 2017, and related EMEP documentation.

## Data access, usage, and metadata considerations
- Outputs are spatial GIS shapefiles suitable for integration with standard geospatial workflows.
- Metadata should capture:
  - Spatial resolution (1° x 1° grid)
  - Crops covered (maize, rice, soybean, wheat)
  - Period (2010–2012)
  - Data sources and models used (EMEP MSC-W v4.16, POD3IAM, M7-based sensitivity, FAO GAEZ)
  - Growing period assumptions by climate zone and hemisphere
  - Known uncertainties and caveats (flux data gaps for non-wheat crops, data limitations for maize)
- References for traceability and reproducibility:
  - Mills et al. (2018a, 2018b)
  - CLRTAP 2017
  - EMEP model technical descriptions
  - FAO GAEZ dataset and JRC ESDAC climate zones

## Maintenance and potential updates
- Current dataset covers 2010–2012; updates would require:
  - Updated ozone flux modeling (POD3IAM) with fresh climate data
  - New crop-specific flux-response data as it becomes available
  - Recalibration of growing period selections and spatial aggregation if inputs change
- Documentation and supplementary information (T1) provide detailed evaluation and methodological notes for future reference.