# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Soil carbon concentration is a key indicator of soil health and a driver of soil processes and ecosystem services.
- The Countryside Survey 2007 provides modelled topsoil carbon concentration estimates across Great Britain at 1 km2 resolution.
- Outputs are designed to enable data-informed exploration and interpretation of soil carbon patterns across the country.

## Data and modeling approach
- Based on soil carbon data from 2446 locations; includes a random effect to account for nesting within 1 km2 survey squares.
- Generalized Additive Mixed Model (GAMM) with non-linear smoothed terms and tensor product smooths:
  - Non-linear smooths for climate and atmospheric deposition variables.
  - Two-dimensional tensor product smooths for spatial coordinates (latitude and longitude) to capture broad spatial variation.
- Distribution and fitting:
  - Tweedie distribution with variance power = 1.99 (not Gaussian), fitted using the mgcv package in R (function gamm).
- Full methodological details are reported in Thomas et al. (2020).

## Variables used (as described in Table 1)
- Climate: 5-year mean summer temperature and precipitation (both 5 km resolution, 2003–2007 range), 5-year mean spring temperature, 5-year mean winter temperature (5 km resolution).
- Atmospheric deposition: 3-year mean SO4, NH4, NO3 deposition (5 km resolution; CBED/related sources; years vary per variable).
- Spatial terms: te(Easting, Northing) (1 km resolution) to capture large-scale spatial variation.
- Habitat and soil predictors: Broad Habitat, CACO3 Rank, Soil Group, Land Cover Map 2007 and related classifications (as qualitative or 1 km predictors).
- Additional notes: The table lists various parametric terms corresponding to the above factors.
- Source references for predictors include Met Office, Land Cover Map 2007, British Geological Survey, and related datasets.

## Data attributes and format
- Dataset: CS_topsoil_carbon_gam.nc
- Main variable: Soil_OrgC_Conc — Mean soil carbon concentration in 2007 as estimated by the GAM (units: g kg-1).
- Uncertainty: VAR — Standard error associated with Soil_OrgC_Conc divided by the predicted mean (units: ratio).
- Spatial referencing: x (Easting) and y (Northing) in OSGB 1936/British National Grid (EPSG:27700), units in metres.
- Coordinate system and mapping: transverse_mercator descriptor provided (unitless in table).

## Sampling, calibration, and quality control
- Sampling method: Soil cores (15 cm long, 5 cm diameter) following field protocol; losses-on-ignition (LOI) on 10 g sub-samples after drying.
- Carbon estimation: Carbon concentration estimated by multiplying LOI by a factor of 0.55, calibrated against total carbon measurements (CEH Lancaster UKAS method SOP3102).
- Standards and governance: Methods align with Defra/NERC Codes of Practice; referenced methodological reports include Emmett et al. (2008, 2010) and related CS documentation.

## Outputs and usage
- Primary output: Spatially explicit model-based estimates of topsoil carbon concentration at 1 km2 across Great Britain for 2007.
- Data product enables self-serve analysis, mapping, and integration with other datasets for policy, planning, or scientific inquiries.
- Potential uses include examining spatial patterns of soil carbon in relation to climate, deposition, land use, and habitat types; informing soil health assessments and carbon accounting.

## References and supporting documents
- Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment, 729, 138330.
- Henrys, P.A., Keith, A.M., Robinson, D.A., Emmett, B.A. (2012). Model estimates of topsoil carbon [Countryside Survey]. NERC Environmental Information Data Centre.
- Reynolds, B.A. et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal.
- Emmett, B.A. et al. (2008, 2010). Countryside Survey technical reports on soils manual and soils data.
- Dore, A.J. et al. (2015). Evaluation of atmospheric deposition models (for UK).
- Morton, R.D. et al. (2014). Land Cover Map 2007 (GB) v1.2.
- British Geological Survey (2010). Soil Parent Material Model. 
- Met Office (2014). Climate data sources for UK analyses.