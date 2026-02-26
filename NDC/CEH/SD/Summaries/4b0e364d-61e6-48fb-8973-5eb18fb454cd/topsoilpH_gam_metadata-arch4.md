# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Modelled topsoil pH estimates (0–15 cm depth) at 1 km2 resolution across Great Britain for 2007, derived from Countryside Survey (CS) data.
- Uses a Generalized Additive Mixed Model (GAMM) that incorporates climate, atmospheric deposition, habitat, soil, and spatial variables to predict pH.
- Based on 2446 sampling locations with a random effect to account for nesting within 1 km2 CS survey squares; includes non-linear smooths and spatial tensor product terms.

## Data product and modelling approach
- Output dataset: CS_topsoil_ph_gam.nc, containing mean pH estimates and associated standard error (VAR).
- Model implementation details:
  - Tweedie distribution (variance power = 1.01) used because a Gaussian model was not appropriate.
  - Non-linear smoothed terms for climate and deposition variables.
  - Two-dimensional tensor product smooths for spatial coordinates (latitude/longitude) to capture large-scale spatial variation.
  - Random effect to account for sampling unit nesting.
  - Implemented in R using the mgcv package (gamm function).

## Predictor variables and structure
- Smoothed terms for 5-year mean winter, spring, summer, and autumn temperatures.
- Smoothed terms for 5-year mean winter, spring, and other seasonal precipitation.
- 3-year mean nitrogen deposition indicators (NO3, NH4) and sulfur deposition (SO4).
- Spatial terms: te(Easting, Northing) with multiple resolutions (1 km, 5 km) to model spatial structure.
- Additional predictors: Broad Habitat, CACO3 Rank, Soil Group (linked to soil properties), plus various parametric terms.
- All predictors are designed to capture climate, deposition, habitat context, soil characteristics, and spatial location.

## Data attributes and provenance
- Location: OSGB 1936/British National Grid (EPSG:27700); x and y in metres.
- Coordinate reference system: transverse Mercator.
- Sampling details: soil pH measured from 10 g of field-moist soil using 25 ml de-ionised water (soil-to-water ratio 1:2.5) following field protocols.
- Major data sources and methodological references:
  - Reynolds et al. (2013) for soil pH measurements.
  - Emmett et al. (2008, 2010) for Countryside Survey soils methodology.
  - Henrys et al. (2012) for prior model estimates of topsoil pH.
  - Met Office data (climate inputs) and Land Cover Map 2007 (Morton et al., 2014) as inputs.
  - Thomas et al. (2020) for broader context on soil carbon and related patterns.

## Data quality, access, and caveats
- Data include a standard error (VAR) associated with each pH prediction, reflecting uncertainty.
- The 2007 dataset provides a snapshot across Great Britain and is designed to be used for assessments of soil acidity, nutrient availability, biodiversity, and related analyses.
- Limitations noted include model dependency on available predictors, potential uncertainties in deposition and climate inputs, and the representativeness of sampling locations for all regions.

## References / Supporting documents
- Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment, 729, 138330.
- Reynolds, B., et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal, 12(2).
- Emmett, B.A., Frogbrook, Z.L., et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual.
- Emmett, B.A., Reynolds, B., et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007.
- Henrys, P.A., Keith, A.M., Robinson, D.A., Emmett, B.A. (2012). Model estimates of topsoil pH and bulk density [Countryside Survey]. NERC Environmental Information Data Centre.
- Morton, R.D., et al. (2014). Land Cover Map 2007 (1 km dominant target class, GB) v1.2. NERC EIDC.
- Dore, A.J., et al. (2015). Evaluation of the performance of different atmospheric chemical transport models (UK deposition estimates). Atmospheric Environment.