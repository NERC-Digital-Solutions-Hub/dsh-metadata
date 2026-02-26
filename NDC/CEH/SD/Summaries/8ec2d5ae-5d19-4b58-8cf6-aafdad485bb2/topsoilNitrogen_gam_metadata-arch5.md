# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Modelled estimates of topsoil nitrogen concentration (% dry weight) for the 0–15 cm soil depth across Great Britain at 1 km² resolution, based on Countryside Survey (CS) data from 2007.
- Builds on a Generalized Additive Mixed Model (GAMM) that integrates climate, atmospheric deposition, habitat, soil, and spatial variables, with a random effect to account for sampling nested within 1 km² survey squares.
- Uses a Tweedie distribution (variance power = 1.99) and non-linear smooth terms for climate/deposition and tensor product smooths for spatial coordinates; implemented in R with mgcv.
- Data provenance: derived from 913 GB locations; full methodologies and datasets described in linked CS technical reports and related publications.

## Data content and format
- Dataset file: CS_topsoil_nitrogen_gam.nc (netCDF).
- Primary data: mean topsoil nitrogen concentration (Soil_N) for 2007, plus a variability descriptor (VAR) defined as the standard error divided by the mean.
- Spatial reference: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); transverse_mercator coordinate system defined for mapping.
- Predictor/auxiliary variables included in the model:
  - Climate: 5-year mean spring, summer, and autumn temperatures; 5-year mean summer and autumn precipitation.
  - Atmospheric deposition: 3-year mean NO3 deposition.
  - Spatial terms: te(Easting, Northing) with multiple resolutions (1 km and 5 km concepts) to capture large-scale spatial variation.
  - Metadata-derived factors: Broad Habitat, CACO3 Rank, Soil Group (each with qualitative/class and 1 km or model-derived refinements).
  - Other: Land cover and soil material model inputs from published sources.
- Temporal/spatial context: predictors built from 2003–2007 data where applicable; predictions cover 1 km² grid cells across GB.

## Modelling approach
- Generalized Additive Mixed Model (GAMM) framework with:
  - Non-linear smooths for climate/deposition variables (s()).
  - Two-dimensional tensor product smooths for spatial coordinates (te()) to capture broad spatial structure.
  - A random intercept to account for nesting of samples within 1 km² CS survey squares.
- Model fitting details:
  - Gaussian is inappropriate for the response; Tweedie distribution used (variance power = 1.99).
  - Implemented using the gamm function in the R mgcv package.
  - Full methodological details and model description are provided in Thomas et al. (2020); data provenance described in Reynolds et al. (2013) and CS Technical Reports (2008, 2010).

## Data attributes and metadata
- SoiI_N: Mean topsoil nitrogen concentration (% dry weight) for 2007 from the GAM.
- VAR: Standard error of Soil_N divided by the predicted mean (dimensionless).
- x, y: Easting and Northing coordinates in OSGB 1936 / British National Grid (EPSG:27700); units: metres.
- transverse_mercator: Coordinate reference system descriptor (unitless in metadata).
- Additional attribute context and variable descriptions are provided to support discoverability and reuse.

## Sampling, calibration, QA
- Sampling protocol: 15 cm long by 5 cm diameter soil cores following CS field procedures.
- Analytical method: total elemental analyser; CS soils analysis method SOP3102; UKAS-accredited; Defra/NERC Joint Codes of Practice followed.
- Original data sources/publications:
  - Reynolds et al. (2013) for soil nitrogen data.
  - Emmett et al. (2008, 2010) for CS soils sampling and 2007 soils reports.
  - Henrys et al. (2012) for model-estimated topsoil nutrients.
  - Supporting materials include Met Office climate data, Land Cover Map 2007, and soil/material models (BSG).

## References / Supporting documents
- Key references include: Reynolds et al. (2013); Emmett et al. (2008, 2010); Henrys et al. (2012); Thomas et al. (2020); Dore et al. (2015); Met Office (2014); Morton et al. (2014); British Geological Survey materials (2010).

## Governance, access, and reuse (Data Steward focus)
- Provenance and documentation: dataset is well-documented with explicit modelling approach, predictor variables, and data sources, enabling reproducibility and traceability.
- Metadata and standards: uses standard GB grid coordinates and established CS data conventions; netCDF format supports interoperability and metadata embedding.
- Data quality and validation: QA/QA processes are embedded in sampling (UKAS-accredited methods, SOP3102, codes of practice) and referenced in technical reports; statistical model assumptions and fitting approach are described in accompanying publications.
- Sharing and updates: the dataset is a derived product from ongoing Countryside Survey work; governance documentation and references are provided to support future updates or re-analyses as new CS data become available.
- Usage considerations for data stewards:
  - Ensure consistent coordinate reference systems when integrating with other GB datasets (OSGB 27700).
  - Maintain alignment of metadata with model version (e.g., 2007 CS data with GAMM approach) to preserve reproducibility.
  - Preserve linkage to primary CS sources and model documentation for auditability.
  - Note potential limitations related to temporal scope (2003–2007 climate/deposition inputs) when applying to other periods.