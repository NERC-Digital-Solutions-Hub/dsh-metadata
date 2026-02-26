# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Overview
- Modelled estimates of topsoil invertebrate density (0–8 cm depth) across Great Britain for 2007, at a 1 km² resolution, using Countryside Survey data.
- Data product designed for GIS mapping and spatial analysis of soil invertebrate density.
- File: CS_topsoil_invertdensity_gam.nc; coordinate system OSGB 1936 / British National Grid (EPSG:27700); units: individuals per square metre.
- Based on 830 sampling locations with a Generalized Additive Mixed Model (GAMM) that includes climate, habitat, soil, and spatial variables; includes a random effect for nesting within 1 km² survey squares.
- Spatial structure includes 2D tensor product smooths for latitude/longitude to capture large-scale spatial variation.

## What the data are
- Dataset: CS_topsoil_invertdensity_gam.nc
- Core quantity: mean topsoil invertebrate density (individuals m⁻²) for 2007 modeled density.
- Additional data: VAR - standard error associated with the mean divided by the predicted mean (dimensionless ratio).
- Spatial referencing: x (Easting) and y (Northing) in OSGB 27700; transverse_mercator coordinate reference system.
- Coverage: Great Britain, 0–8 cm soil depth; grid cells at 1 km² resolution.

## Modelling approach
- Statistical method: Generalized Additive Mixed Model (GAMM) using a Tweedie distribution (variance power ≈ 1.99) to accommodate data characteristics.
- Predictor components:
  - Non-linear smoothed terms for climate variables: 5-year mean Growing Degree Days, mean temperature, and precipitation (each with 5 km spatial resolution, 2003–2007 period).
  - Spatial terms: two-dimensional tensor product smooths for Easting/Northing to model broad spatial variation (1 km grid).
  - Broad Habitat (qualitative class) from Land Cover Map 2007 (Morton et al. 2014).
  - CACO3 Rank (soil parent material model) at 1 km resolution.
- Random structure: accounts for nesting of samples within 1 km² CS survey squares.
- Modelling context: detailed methodology described alongside related soil carbon analyses (Thomas et al. 2020).

## Data attributes
- Soil_invert_density: mean modeled density (individuals m⁻²) for 2007.
- VAR: standard error associated with Soil_invert_density divided by the predicted mean (dimensionless).
- x: Easting in metres (OSGB 1936 / EPSG:27700).
- y: Northing in metres (OSGB 1936 / EPSG:27700).
- transverse_mercator: coordinate reference parameter (unitless).

## Sampling, calibration, analytical methods and QA
- Sampling method: Countryside Survey soil sampling using a 4 cm diameter by 8 cm long white plastic core; surface vegetation removed; litter layer not removed.
- Processing: cores knocked into the ground, capped at ends, and mailed to the lab; invertebrates extracted with a dry Tullgren apparatus and enumerated via microscope.
- Original data: gathered from 256 “original” CS survey squares.
- Standards: Defra/NERC Joint Codes of Practice followed throughout; methodological details available in CS technical reports (Emmett et al. 2008, 2010) and related methodological papers.

## Access, reuse and citations
- Data access: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Reuse citation: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre (Dataset). https://doi.org/10.5285/93207428-aace-4bb59073-2eb44ad632d1
- Usage note: When reusing, please cite the dataset as above.
- Scope: dataset is model-derived (not a direct inventory) and suitable for GIS-based mapping and analyses of spatial patterns in soil invertebrate density.

## Related references
- Henrys, P.A.; Keith, A.M.; Robinson, D.A.; Emmett, B.A. (2012). Model estimates of topsoil invertebrates [Countryside Survey]. NERC Environmental Information Data Centre. https://doi.org/10.5285/f19de821-a4364b28-95f6-b7287ef0bf15
- Emmett, B.A., et al. (2008, 2010). Countryside Survey technical reports on soils and soils methodology.
- Morton, R.D.; Rowland, C.S.; Wood, C.M.; et al. (2014). Land Cover Map 2007 (1 km dominant target class, GB) v1.2.
- Thomas, A.; Cosby, B.J.; Henrys, P.; Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: complex interactions of land use change, climate and pollution. Science of the Total Environment.