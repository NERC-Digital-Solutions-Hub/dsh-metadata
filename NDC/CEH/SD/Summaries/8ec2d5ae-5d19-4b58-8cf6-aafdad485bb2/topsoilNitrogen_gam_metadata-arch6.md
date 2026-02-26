# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Modelled estimates of topsoil nitrogen concentration (% dry weight) for 0-15 cm depth across Great Britain at 1 km² resolution, based on Countryside Survey data from 2007.
- Uses a Generalized Additive Mixed Model (GAMM) that integrates climate, atmospheric deposition, habitat, soil, and spatial variables.
- Includes a random effect for nesting of samples within 1 km² survey squares and non-linear smoothing for climate variables.
- Accounts for large-scale spatial variation with two-dimensional tensor product smooths of latitude and longitude.
- Data are provided as a gridded product with accompanying uncertainty, using a Tweedie distribution (variance power = 1.99); implemented in R mgcv (gamm).

## Data content and modelling approach
- Based on soil nitrogen data from 913 locations; modelled mean Soil_N with standard error expressed as VAR (standard error divided by the predicted mean).
- Output file: CS_topsoil_nitrogen_gam.nc.
- Modelling specifics:
  - Random effects to account for 1 km² survey square nesting.
  - Non-linear smoothed terms for climate and deposition variables.
  - Spatial smoothing via te(Easting, Northing) and related terms to capture broad geographic variation.
  - Tweedie family used due to non-Gaussian response.
  - Full methodological details available in Thomas et al. (2020).

## Variables used (as described in Table 1)
- Climate predictors:
  - s(5 year mean spring temperature), s(5 year mean summer temperature), s(5 year mean autumn temperature) with 5 km spatial resolution; temporal range 2003-07; sources include Met Office (2014).
  - s(5 year mean summer precipitation), s(5 year mean autumn precipitation) with similar resolutions and ranges.
- Atmospheric deposition:
  - s(3 year mean NO3 deposition), with 5 km resolution; temporal reference around 2005; sources include CBED (2015).
- Spatial terms:
  - te(Easting, Northing) and related smooths to capture spatial structure; possibly at 1 km or 5 km scales.
- Habitat and soil-related predictors:
  - Broad Habitat (Qualitative class; 2007 land cover context).
  - CACO3 Rank (qualitative class and 1 km/derived materials).
  - Soil Group (qualitative class and 1 km/derived materials).
  - Soil Parent Material Model (British Geological Survey, 2010).
- Other model components:
  - Parametric terms corresponding to the above categorical/derived factors.

Note: The table lists a mixture of smoothed terms (s(.)) and tensor product terms (te(.)) across these predictors.

## Data attributes and file format
- File: CS_topsoil_nitrogen_gam.nc.
- Soil_N: Mean soil nitrogen concentration (%) for 2007 modelled via GAM.
- VAR: Standard error of Soil_N divided by the predicted mean (describes relative uncertainty).
- Coordinates:
  - x: Easting (OSGB 1936/British National Grid, EPSG:27700; metres).
  - y: Northing (OSGB 1936/British National Grid, EPSG:27700; metres).
  - transverse_mercator: Defines the coordinate reference system (unitless in this context).
  
## Sampling, calibration, analytical methods, and Quality Control
- Sampling followed the Countryside Survey protocols using 15 cm long by 5 cm diameter cores.
- Nitrogen concentration determined with a total elemental analyser on the 256 original survey squares.
- UKAS-accredited method SOP3102 (CEH Lancaster) used.
- Defra/NERC Joint Codes of Practice adhered to throughout.

## Usage and applications
- Provides a ready-to-explore data product for mapping and analysis of topsoil N status across GB, enabling:
  - Spatial visualization and self-service data exploration at 1 km² resolution.
  - Investigation of relationships between soil N, climate, deposition, and habitat/soil factors.
  - Integration into broader policy, land management, and environmental monitoring work.
- Useful for trend analyses by linking 2007 estimates to climate/deposition contexts and to other soil properties.
- Outputs include associated uncertainty (VAR), aiding risk assessment and interpretation.

## Considerations and caveats
- Based on 913 sample locations; generates model-based estimates rather than direct measurements at every grid cell.
- Non-Gaussian data handled via Tweedie distribution; model assumptions and details described in Thomas et al. (2020).
- For methodological depth and data provenance, refer to Reynolds et al. (2013) and Emmett et al. (2008, 2010) technical reports, plus Henrys et al. (2012).

## References / Supporting documents
- Reynolds et al. (2013). Countryside Survey: National 'Soil Change' 1978-2007 for Topsoils in Great Britain — acidity, carbon, and total nitrogen status. Vadose Zone Journal.
- Emmett et al. (2008, 2010). Countryside Survey technical reports: Soils Manual; Soils Report from 2007.
- Henrys et al. (2012). Model estimates of topsoil nutrients [Countryside Survey].
- Thomas et al. (2020). Patterns and trends of topsoil carbon in the UK — complex interactions of land use change, climate, and pollution. Science of the Total Environment.
- Morton et al. (2014). Land Cover Map 2007 (1 km dominant target class, GB).
- CBED and Met Office sources for deposition and climate data.