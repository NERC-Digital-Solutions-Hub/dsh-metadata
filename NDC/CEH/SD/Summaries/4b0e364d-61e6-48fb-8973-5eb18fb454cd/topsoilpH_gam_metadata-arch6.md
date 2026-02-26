# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Provides modelled topsoil pH estimates (0–15 cm depth) across Great Britain at 1 km² resolution using Countryside Survey (CS) data from 2007.
- Based on 2,446 sampling locations with a random effect to account for nesting within 1 km² survey squares.
- Uses a Generalized Additive Mixed Model (GAMM) with non-linear smooths for climate and deposition; two-dimensional tensor product smooths for latitude/longitude to capture large-scale spatial variation.
- Model fitting employed a Tweedie distribution (variance power = 1.01) implemented via mgcv in R; full methodological details are in Thomas et al. (2020).

## Data product
- Dataset: CS_topsoil_ph_gam.nc
- Main variable: Soil_pH
  - Description: Mean soil pH in 2007 modelled with GAM.
  - Units: pH units
- Uncertainty: VAR
  - Description: Standard error of Soil_pH divided by the predicted mean
  - Units: Ratio
- Spatial references: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700)
- Coordinate system: OSGB 1936 / British National Grid; transverse Mercator mapping
- Data coverage: 1 km² resolution across Great Britain; depth 0–15 cm

## Modelling approach and scope
- Modelling framework: Generalized Additive Mixed Model (GAMM)
- Random effects: Accounts for sample nesting within 1 km² survey squares
- Non-linear terms: Smoothed functions for climate and atmospheric deposition variables
- Spatial terms: Two-dimensional tensor product smooths for Easting and Northing to capture broad spatial patterns
- Distribution: Tweedie with variance power 1.01 (not Gaussian)
- Software: R package mgcv (gamm function)
- Key references: Thomas et al. (2020) for patterns, and Reynolds et al. (2013) for sampling; Emmett et al. (2008, 2010) for soil methods

## Inputs and predictors (as used in the model)
- Climate: 5-year mean winter, spring, summer, and autumn temperatures and precipitations (5 km spatial resolution; covering 2003–2007)
- Atmospheric deposition: 3-year mean NO3, NH4, and SO4 deposition (5 km resolution; covering 2005–2007)
- Spatial terms: Easting and Northing (with several parameterizations including 1 km and others)
- Broad Habitat and Soil context: Qualitative broad habitat classes; 2007 land cover; Soil Group and Soil Parent Material models
- Additional predictors: CACO3 Rank and related variables (as 1 km resolution or model-based substitutes)
- Temporal context: Derived from data 2003–2007 for climate/deposition inputs
- Note: Smoothing and interactions are used to capture non-linear and spatially varying effects

## Data attributes and mapping details
- Soil_pH: Mean pH value for 2007 model
- VAR: Standard error associated with Soil_pH divided by the predicted mean (uncertainty metric)
- Coordinates: x (Easting) and y (Northing) in metres; OSGB 27700
- Coordinate system: Transverse Mercator
- Data provenance: Based on Countryside Survey soil sampling and analyses; methodological references provided

## Sampling, calibration, and quality control
- Sampling protocol: Soil cores (15 cm length, 5 cm diameter); field-moist soil measured with 25 ml deionised water (soil-to-water ratio 1:2.5 by weight)
- Analysis: pH measurements following the Defra/NERC Joint Codes of Practice
- Supporting methodological references: Emmett et al. (2008, 2010) soil manuals and CS technical reports; Reynolds et al. (2013) for soil change and acidity status
- Data provenance and validation: Details of sampling and analytical processes documented in CS technical reports

## Practical considerations for data use (Data Support perspective)
- Use case: Build dashboards or reports to explore spatial patterns of topsoil pH across GB and identify areas of acidity/potential biodiversity impact
- Data quality: Model-based estimates with associated uncertainty (VAR) to inform confidence in predictions; consider patchy data and 1 km² nesting structure when aggregating
- Integration potential: Combine with other CS soil/land-use layers or deposition datasets to analyze drivers of pH variation
- Communication: Translate non-linear climate/deposition effects and spatial patterns into accessible visuals or self-serve tools for end users
- Limitations: Model-based estimates depend on 2007 sampling; temporal changes after 2007 are not captured; spatial resolution is limited to 1 km² aggregates with model smoothing

## References / supporting documents
- Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment, 729, 138330.
- Reynolds, B.A. et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal, 12(2).
- Emmett, B.A. et al. (2008, 2010). Countryside Survey Technical Reports: Soils Manual and Soils Report from 2007. CEH.
- Henrys, P.A. et al. (2012). Model estimates of topsoil pH and bulk density [Countryside Survey].
- Morton, R.D. et al. (2014). Land Cover Map 2007 (1 km) v1.2. NEERC EIDC.
- Dore, A.J. et al. (2015). Deposition model inter-comparison (Atmospheric Environment).