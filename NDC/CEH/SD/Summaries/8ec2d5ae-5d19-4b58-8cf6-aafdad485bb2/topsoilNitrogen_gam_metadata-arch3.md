# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Describes a spatially explicit, model-based estimation of topsoil nitrogen concentration (% dry weight) in the 0–15 cm layer across Great Britain for 2007.
- Uses Countryside Survey data (913 sampling locations) at 1 km2 resolution to generate modelled estimates.
- Aims to support monitoring of soil fertility trends and nutrient status in relation to other soil parameters (e.g., C:N ratio).

## Modelling approach
- Generalized Additive Mixed Model (GAMM) implemented in R using the mgcv package (gamm function).
- Response: Soil_N (mean soil nitrogen concentration); error structure employs a Tweedie distribution with variance power 1.99 (not Gaussian) due to data characteristics.
- Random effects: accounts for nesting of samples within 1 km2 survey squares.
- Non-linear smooths: year-long climate and atmospheric deposition variables modeled with smoothed terms.
- Spatial structure: two-dimensional tensor product smooths on latitude/longitude to capture large-scale spatial variation.
- Data inputs: climate, atmospheric deposition, habitat, soil characteristics, and spatial predictors.
- Improvement over prior simple models by incorporating climate, deposition, habitat, soil, and spatial interactions.

## Variables and predictor structure
- Climate: 5-year mean spring, summer, and autumn temperatures (5 km resolution; 2003–2007), derived from Met Office data.
- Climate: 5-year mean summer and autumn precipitation (5 km; 2003–2007).
- Atmospheric deposition: 3-year mean NO3 deposition (various spatial scales, including 5 km and 2005 data source CBED).
- Spatial terms: eastings/northings (OSGB 1936/ British National Grid) and corresponding tensor product smooths to capture spatial variation.
- Broad Habitat and Soil characteristics: qualitative classes and related materials (e.g., Soil Group, CACO3 Rank) with 1 km or model-based classifications (e.g., Land Cover Map 2007).
- Data-driven interactions: two-dimensional tensor product smooths applied to spatial coordinates; several smooth terms (s()) and tensor products (te()) describe combined effects.

## Data attributes and file
- Dataset: CS_topsoil_nitrogen_gam.nc
- Soil_N: mean topsoil nitrogen concentration (%) for 2007.
- VAR: standard error associated with Soil_N divided by the predicted mean (ratio form).
- x: Easting in OSGB 1936/British National Grid (units: metres).
- y: Northing in OSGB 1936/British National Grid (units: metres).
- transverse_mercator: coordinate reference system for mapping.
- Coordinate reference system: OSGB 1936/British National Grid (EPSG:27700).

## Sampling, calibration, and quality control
- Field sampling and analytical methods described in Reynolds et al. (2013) and Emmett et al. (2008, 2010).
- Sampling protocol used a 15 cm long, 5 cm diameter core.
- Soil N concentration measured with a total elemental analyser following CEH Lancaster UKAS-accredited SOP3102.
- Adherence to Defra/NERC Joint Codes of Practice throughout.

## References and supporting documents
- Dore et al. (2015): Evaluation of atmospheric deposition models.
- Emmett et al. (2008, 2010): Countryside Survey soils manuals and 2007 soils report.
- Henrys et al. (2012): Model estimates of topsoil nutrients for Countryside Survey.
- Morton et al. (2014): Land Cover Map 2007.
- Reynolds et al. (2013): Countryside Survey – soil change (1978–2007) for topsoils in Great Britain.
- Thomas et al. (2020): Patterns and trends of topsoil carbon in the UK (context for related modelling).
- British Geological Survey materials (soil parent material models) referenced for soil classifications.