# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Presents modelled estimates of topsoil pH (0–15 cm depth) at 1 km2 resolution across Great Britain for 2007.
- Based on Countryside Survey data from 2446 locations; uses a Generalized Additive Mixed Model (GAMM) that includes climate, atmospheric deposition, habitat, soil, and spatial variables.
- Incorporates a random factor for nesting of samples within 1 km2 survey squares; uses non-linear smooths for climate/deposition and 2D tensor product smooths for spatial coordinates.
- Tweedie distribution (variance power ≈ 1.01) is used for model fitting (via the mgcv package in R); full methodological details are described in Thomas et al. 2020.
- Model outputs are available as a NetCDF file named CS_topsoil_ph_gam.nc; full methodology and data context are linked to in the cited references.
- Data and supporting methods come from multiple sources including Reynolds et al. (2013) and Emmett et al. (2008, 2010); all are associated with Countryside Survey and UK environmental data centres.

## Data content and format
- Dataset: CS_topsoil_ph_gam.nc.
- Core variable: Soil_pH — mean soil pH in 2007 modeled using GAM.
- Associated metadata: VAR — standard error for Soil_pH divided by the predicted mean (a measure of relative uncertainty).
- Spatial referencing: x (Easting) and y (Northing) in OSGB 1936/British National Grid (EPSG:27700), with coordinates stored in metres; includes a transverse_mercator reference.
- Complements: model-fitting context and data attributes described below, enabling mapping and downstream analysis.

## Modelling approach and inputs
- Model type: Generalized Additive Mixed Model (GAMM) with random effects to account for sample nesting within 1 km2 squares.
- Non-linear terms (smoothed functions) for climate and atmospheric deposition variables:
  - Five-year mean winter temperature; five-year mean spring temperature; five-year mean summer temperature; five-year mean autumn temperature.
  - Five-year mean winter, spring, summer, and autumn precipitation.
- Spatial terms: two-dimensional tensor product smooths on latitude/longitude to capture large-scale spatial variation.
- Dependent distribution: Tweedie (variance power ≈ 1.01) rather than Gaussian.
- Key predictor sets include:
  - Climate (temperature, precipitation)
  - Atmospheric deposition (NO3, NH4, SO4)
  - Broad Habitat and Soil Group/CACO3 Rank (categorical/qualitative factors)
  - Land Cover 2007 and related habitat/parent material proxies
  - Spatial positioning (Easting/Northing)
- Temporal/spatial context: predictors drawn from 2003–2007 windows; data sources include Met Office and CBED for deposition, and Land Cover Map 2007 for habitat/land-use context.
- Comprehensive variable definitions and examples are provided in Table 1 of the source document.

## Dataset attributes and metadata
- Primary output variable: Soil_pH (pH units) — mean 2007 modelled pH.
- Uncertainty: VAR (ratio) — standard error of Soil_pH divided by the predicted mean.
- Spatial coordinates: x and y in metres (OSGB 1936/British National Grid); coordinate system descriptor included (transverse_mercator).
- Data lineage: Sampling and QC references include Reynolds et al. (2013) and Emmett et al. (2008, 2010); modelling details in Thomas et al. (2020).
- Access/archival context: Data and supporting materials are linked to Countryside Survey technical reports and Environmental Information Data Centre records; full methodological and data provenance is documented.

## Sampling, calibration, analytical methods and quality control
- Sampling: Soil pH measurements were collected using 15 cm long by 5 cm diameter cores following a standardized field protocol.
- Analytical method: 10 g of field-moist soil with 25 ml deionised water (soil-to-water ratio of 1:2.5 by weight) to determine pH.
- Quality control: Methods adhered to Defra/NERC Joint Codes of Practice; detailed QC and methodological notes are provided in Emmett et al. (2008, 2010) and Reynolds et al. (2013).

## Data provenance and references
- Core modelling and data sources:
  - Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment, 729, 138330.
  - Reynolds et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal.
  - Emmett et al. (2008, 2010). Countryside Survey technical reports: Soils Manual and Soils Report from 2007.
  - Henrys et al. (2012). Model estimates of topsoil pH and bulk density [Countryside Survey].
- Data sources for covariates and references:
  - Met Office (2014) climate data
  - Land Cover Map 2007 (Morton et al., 2014)
  - CBED data for deposition (Dore et al., 2015)
  - British Geological Survey materials for soil parent material models
- Data hosting: Countryside Survey datasets and associated materials are available through the NERC Environmental Information Data Centre and related project pages.