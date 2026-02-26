# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Provides modelled estimates of topsoil nitrogen concentration (% dry weight) for the 0–15 cm soil layer across Great Britain at 1 km2 resolution, based on Countryside Survey (CS) 2007 data.
- Aims to indicate soil fertility trends and nutrient status over time in relation to climate, deposition, habitat, and soil factors.
- Builds on a more complex modelling approach than previous simple predictors, incorporating climate, atmospheric deposition, habitat, soil, and spatial variables.

## Data and study design
- Data source: Countryside Survey soil nitrogen measurements from 913 locations; includes data from the 256 original survey squares.
- Depth: 0–15 cm.
- Resolution: 1 km2 across Great Britain.
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700); x (Easting) and y (Northing) in metres.
- Model dataset: CS_topsoil_nitrogen_gam.nc with attributes describing mean nitrogen concentration and associated uncertainty.

## Modelling approach
- Statistical method: Generalized Additive Mixed Model (GAMM) implemented via the R mgcv gamm function.
- Response variable: Soil_N – mean topsoil nitrogen concentration (% dry weight) in 2007.
- Error structure: Tweedie distribution with variance power parameter 1.99 (appropriate for the data).
- Random effects: Accounts for nesting of samples within 1 km survey squares.
- Non-linear effects: Smoothed terms for climate and atmospheric deposition variables.
- Spatial terms: Two-dimensional tensor product smooth interactions for spatial coordinates (Easting, Northing) to capture large-scale spatial variation.
- Explanatory variables (from Table 1): 
  - Climate: 5-year mean spring, summer, and autumn temperatures (5 km spatial resolution; 2003–2007).
  - Climate/precipitation: 5-year mean summer and autumn precipitation (5 km; 2003–07).
  - Atmospheric deposition: 3-year mean NO3 deposition (5 km; 2005; CBED data).
  - Spatial: Easting/Northing terms (1 km or finer references).
  - Broad habitat, CACO3 rank, Soil group with respective spatial/qualitative encodings.
- Data and methods references: Thomas et al. (2020) for patterns and modelling approach; prior CS soil methodologies described in Emmett et al. (2008, 2010) and Reynolds et al. (2013).

## Model outputs and data attributes
- Primary dataset: CS_topsoil_nitrogen_gam.nc.
- Key attributes:
  - Soil_N: Mean topsoil nitrogen concentration for 2007 (% dry wt).
  - VAR: Standard error relative to the predicted mean (unitless ratio).
  - x: Easting (metres); OSGB 1936 / British National Grid (EPSG:27700).
  - y: Northing (metres); OSGB 1936 / British National Grid (EPSG:27700).
  - transverse_mercator: Coordinate reference system identifier (unitless).
- Usage intent: Provide standardized, model-based estimates suitable for monitoring environmental health and policy performance over time; outputs suitable for mapping and reporting.

## Sampling, calibration, and quality control
- Sampling: Soil nitrogen measured from the 256 original survey squares using a CEH Lancaster UKAS-accredited method SOP3102.
- Field protocol: 15 cm long by 5 cm diameter soil cores.
- QA and harmonisation: Adheres to Defra/NERC Joint Codes of Practice; detailed methodological reports available (Emmett et al. 2008, 2010).
- References for methods: Reynolds et al. (2013) on soil change 1978–2007; Emmett et al. (2008, 2010) soil sampling/analysis; related CS technical reports.

## Data use and monitoring implications
- Standardised modelling framework enables consistent, comparable monitoring of soil fertility indicators over time.
- Outputs are designed to be stored and uploaded to appropriate data portals, facilitating broader access and integration with other environmental datasets.
- The combination of robust QA, spatial modelling, and multi-source covariates supports assessment of environmental health and policy outcomes at national scales.

## Supporting references (selected)
- Reynolds et al. (2013). Countryside Survey: National 'Soil Change' 1978–2007 for Topsoils in Great Britain – acidity, carbon, and total nitrogen status.
- Emmett et al. (2008, 2010). Countryside Survey technical reports on soils sampling and analysis.
- Henrys et al. (2012). Model estimates of topsoil nutrients [Countryside Survey].
- Thomas et al. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution.
- CBED, Met Office, Morton et al. (2014) data sources for deposition and land cover variables.