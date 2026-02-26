# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Presents modelled estimates of topsoil nitrogen concentration (% dry weight) for the 0–15 cm soil depth across Great Britain at 1 km² resolution, using Countryside Survey (CS) data from 2007.
- Builds on a GAMM approach that integrates climate, atmospheric deposition, habitat, soil, and spatial predictors to map soil nitrogen.

## Modeling approach and data inputs
- Uses a Generalized Additive Mixed Model (GAMM) with a random effect to account for nesting of samples within 1 km² survey squares.
- Non-linear smoothed terms for climate and atmospheric deposition; two-dimensional tensor product smooths for latitude and longitude to capture large-scale spatial variation.
- Distribution: Tweedie with variance power parameter 1.99 (not Gaussian); implemented with the mgcv R package.
- Based on data from 913 sampling locations; full methodological details provided in Thomas et al. 2020.
- Covariates include:
  - Climate: 5-year mean spring, summer, and autumn temperatures (5 km resolution; 2003–2007; Met Office data, 2014).
  - Precipitation: 5-year mean summer and autumn precipitation (5 km, 2003–07).
  - Atmospheric deposition: 3-year mean NO₃ deposition (5 km, 2005–CBED data, 2015).
  - Spatial terms: Easting/Northing coordinates; 1 km or 5 km spatial resolutions depending on variable.
  - Habitat and soil context: Broad Habitat, Soil Group, CACO3 Rank, Land Cover Map 2007, Soil Parent Material Model.
- Model details and data integration are described in the accompanying references.

## Data product and file attributes
- Data product: CS_topsoil_nitrogen_gam.nc
- Main variable: Soil_N — mean topsoil nitrogen concentration (% dry weight) for 2007 modelled using GAM(M).
- Uncertainty metric: VAR — standard error divided by the predicted mean (ratio).
- Spatial coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); units in metres.
- Coordinate system for mapping: transverse_mercator.
- Output resolution and extents align with 1 km² grid across Great Britain.

## Sampling, calibration, analytical methods, and QA
- Soil nitrogen data published in Reynolds et al. (2013); soil sampling and analysis detailed in CEH technical reports (Emmett et al. 2008, 2010).
- Field sampling used 15 cm long, 5 cm diameter cores following a standardized protocol; nitrogen measured with a total elemental analyser.
- UKAS-accredited method SOP3102; adherence to Defra/NERC Joint Codes of Practice.

## Data provenance, references, and supporting materials
- Key references:
  - Thomas et al. (2020): Patterns and trends of topsoil carbon in the UK (context for GAMM approach and covariates).
  - Reynolds et al. (2013): Countryside Survey national soil change for topsoils (acidity, carbon, total nitrogen).
  - Emmett et al. (2008, 2010): Countryside Survey soils manual and soils report.
  - Henrys et al. (2012): Model estimates of topsoil nutrients (Countryside Survey).
  - Additional data sources: Met Office climate data, Land Cover Map 2007, British Geological Survey materials, CBED nitrate deposition data.
- Supporting documents and datasets are cited with DOIs and source URLs.

## Data accessibility and governance
- The dataset is anchored to established CS data products and is supported by multiple peer-reviewed sources; metadata includes units, coordinate reference system, and uncertainty metrics.
- Uses standardized methods and quality controls described in the referenced technical reports and papers, facilitating reproducibility and integration into broader data systems.

## Applications and implications for data leaders
- Enables spatially explicit assessment of soil nitrogen status across Great Britain for 2007, useful for tracking fertility trends and informing land management and policy decisions.
- Demonstrates the integration of heterogeneous data sources (climate, deposition, land cover, soil classes) within a single predictive framework, illustrating a scalable data system for environmental monitoring.
- Highlights the importance of robust metadata (units, coordinate systems, uncertainty) and transparent methodological documentation to support data discoverability, reuse, and cross-network collaboration.

## Limitations and considerations
- Model based on 913 sample points; spatial and temporal coverage limited to 2003–2007 climate and deposition windows.
- 1 km² resolution with covariates that include coarser resolutions (e.g., 5 km) for some predictors; uncertainties captured in VAR, but users should consider downscaling assumptions.
- Dependency on existing datasets and models (e.g., deposition data, land cover maps) and their corresponding uncertainties.
- Reproducibility relies on access to the MGCV-based modeling approach and the underlying CS documentation and datasets cited.