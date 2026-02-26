# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Presents modelled estimates of topsoil nitrogen concentration (0–15 cm depth) across Great Britain at 1 km² resolution for 2007 using Countryside Survey data.
- Nitrogen concentration is a key soil fertility metric and reflects trends in nutrient status and related parameters (e.g., C:N ratio).
- Builds on improved modelling beyond previous simple habitat/parent-material predictors (Henrys et al. 2012) by incorporating climate, atmospheric deposition, habitat, soil, and spatial variables.

## Model and data details
- Method: Generalized Additive Mixed Model (GAMM) with a Tweedie distribution (variance power = 1.99); implemented with mgcv in R (gamm function).
- Basis: Random effect to account for nesting of samples within 1 km² survey squares; non-linear smooths for climate and deposition; two-dimensional tensor product smooths for spatial latitude/longitude.
- Data underpinning the model: 913 sampling locations across GB.
- Key reference for methods: Thomas et al. (2020); full statistical details are provided there.

## Variables included in the model
- Climate: 5-year mean spring, summer, and autumn temperatures (each with 5 km resolution; temporal range 2003–2007; Met Office source, 2014).
- Precipitation: 5-year mean summer and autumn precipitation (5 km; 2003–07; Met Office 2014).
- Atmosphere: 3-year mean NO3 deposition (kg ha⁻¹ yr⁻¹; 5 km; 2005; CBED data).
- Spatial terms: te(Easting, Northing) with multiple scales (1 km, 5 km, etc.) to capture spatial variation.
- Broad Habitat: qualitative classes; 2007 Land Cover Map 2007 as reference.
- Soil-related predictors: CACO3 Rank (qualitative and 1 km / soil material model variants), Soil Group (qualitative and 1 km / material model variants).
- Additional factors: Parametric terms and other descriptors (e.g., mapping to 2007 datasets).
- Overall design uses non-linear smooth terms (s()), tensor product smooths (te()) and cross-variable interactions to capture complex relationships.

## Data attributes and format
- Dataset: CS_topsoil_nitrogen_gam.nc
- Soil_N: mean soil nitrogen concentration (% dry weight) for 2007 modelled values using GAM.
- VAR: standard error relative to the predicted mean (ratio).
- Coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); transverse_mercator coordinate reference.
- Purpose: provides spatially explicit estimates of topsoil N concentration to support assessment of soil fertility status and trends.

## Sampling, calibration, and quality control
- Field sampling: soil nitrogen measurements collected using 15 cm long by 5 cm diameter cores following a standardized field protocol.
- Laboratory analysis: total elemental analysis using an accredited method (CEH Lancaster UKAS SOP3102).
- Data provenance: CS soil data published in Reynolds et al. (2013); full methodological details in Emmett et al. (2008, 2010).
- Quality practices: adherence to Defra/NERC Joint Codes of Practice; standard QA/QC procedures described in cited technical reports.

## Supporting references
- Reynolds et al. (2013): Countryside Survey national soil change for topsoils (acidity, carbon, total nitrogen).
- Emmett et al. (2008, 2010): Countryside Survey soils manuals and 2007 soils report.
- Henrys et al. (2012): prior model estimates of topsoil nutrients.
- Morton et al. (2014): Land Cover Map 2007 data.
- Thomas et al. (2020): Patterns and trends of topsoil carbon; methodological context for the GAMM approach.
- Additional supporting sources: Met Office climate data (2014), BGS Soil/Material models, and related CS technical reports.