# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

- Purpose: Provides map-ready, model-based estimates of topsoil pH (0-15 cm depth) across Great Britain at 1 km2 resolution for 2007, enabling spatial analysis and visualization of soil acidity and related ecological factors.
- Data product: CS_topsoil_ph_gam.nc (NetCDF) covering GB at 1 km2 resolution, suitable for GIS mapping and analysis.
- Coverage and depth: Great Britain; topsoil pH estimates for the 0-15 cm layer.
- Sampling basis: Model built from 2,446 sampling locations across GB (accounting for nesting within 1 km2 survey squares).

- Modelling approach:
  - Generalized Additive Mixed Model (GAMM) with a Tweedie distribution (variance power 1.01) to fit soil pH.
  - Random effect to account for sample nesting within 1 km2 survey squares.
  - Non-linear smooths for climate and atmospheric deposition variables.
  - Two-dimensional tensor product smooths for spatial (latitude/longitude) to capture large-scale spatial variation.
  - Predictors include climate, atmospheric deposition, habitat, soil, and spatial variables (as detailed in Table 1).
  - Model details and full statistical methodology described in Thomas et al. (2020) and related CS technical reports.

- Data attributes and structure:
  - Soil_pH: Mean modeled soil pH value for 2007; units = pH.
  - VAR: Standard error associated with Soil_pH divided by the predicted mean; units = ratio.
  - Coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); units = metres.
  - Mapping reference: transverse_mercator coordinate reference system.
  - File format and coordinate system ready for GIS ingestion (NetCDF with OSGB 27700 projection).

- Variables included in the model (examples from Table 1):
  - Climate: 5-year mean winter, spring, summer, and autumn temperatures; 5-year mean winter, spring, summer, and autumn precipitation (all at ~5 km spatial resolution; 2003–2007 time window) and sources (Met Office 2014).
  - Atmospheric deposition: 3-year mean NO3, NH4, and SO4 deposition (5 km resolution; 2005; CBED 2015 sources).
  - Spatial terms: te(Easting, Northing) with multiple configurations; broad habitat and soil-related descriptors (qualitative classes and 1 km or model-derived layers).
  - Soil and parent material context: CACO3 Rank, Soil Group, and Soil Parent Material Model (British Geological Survey 2010) as categorical or model-derived terms.
  - Model terms: both smoothed and tensor product terms to capture non-linear relationships and spatial patterns.

- Sampling, calibration, and quality control:
  - Measurement basis: Soil pH data published in Reynolds et al. (2013) with field sampling via a standardized core and 10 g soil in 25 ml water (soil-to-water ratio 1:2.5 by weight).
  - Protocols: Follow Defra/NERC Joint Codes of Practice; detailed methodology in Emmett et al. (2008, 2010) CS technical reports.
  - Prior work: Earlier estimates (Henrys et al. 2012) used simpler models; the current product uses a GAMM approach with broader predictor sets.

- Data provenance and supporting literature:
  - Core references include Reynolds et al. (2013), Emmett et al. (2008, 2010), Henrys et al. (2012), Morton et al. (2014) for land cover, and Thomas et al. (2020) for the GAMM-based approach.
  - Related data and models cited (e.g., atmospheric deposition models, soil maps) to support predictor variables and spatial modelling.

- GIS usage guidance:
  - suitable for map-based visualization of spatial patterns in topsoil acidity across GB.
  - The inclusion of VAR enables assessment of uncertainty at each 1 km2 cell.
  - Model-based estimates should be interpreted with awareness of resolution and the nature of predictive modelling (not direct observations).
  - Data can be integrated with other GIS layers (e.g., land cover, habitat, deposition maps) to support policy, planning, and research discussions.

- References and supporting documents:
  - Dore et al. (2015); Emmett et al. (2008, 2010); Henrys et al. (2012); Morton et al. (2014); Reynolds et al. (2013); Thomas et al. (2020); British Geological Survey materials; Met Office data sources.