# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Overview
- Purpose: Provide modelled estimates of topsoil (0–8 cm) invertebrate density across Great Britain at 1 km² resolution, using Countryside Survey data from 2007.
- Method: Generalized Additive Mixed Model (GAMM) incorporating climate, habitat, soil, and spatial variables; includes a random effect to account for nesting within 1 km² survey squares.
- Output: Spatially explicit estimates with non-linear climate relationships and spatial smooths; implemented via a Tweedie distribution (variance power = 1.99) in R (mgcv package).
- Scale and data origin: Based on 830 sampling locations; 1 km² resolution across GB; 0–8 cm soil depth; references to related soil carbon methods for context.

## Data and model details
- Dataset file: CS_topsoil_invertdensity_gam.nc
- Primary variable: Soil_invert_density (mean density in 2007); Units = individuals m⁻²
- Uncertainty: VAR = standard error divided by the predicted mean (dimensionless ratio)
- Coordinates: x = Easting, y = Northing; OSGB 1936 / British National Grid (EPSG:27700); mapping via transverse Mercator
- Spatial and temporal covariates:
  - Climate: s(5 year mean Growing Degree Days), s(5 year mean temperature), s(5 year mean precipitation) with 5 km spatial resolution and 2003–2007 temporal range (source: Met Office, 2014)
  - Spatial: te(Easting, Northing) with 1 km resolution
  - Habitat and soil context: Broad Habitat (Land Cover Map 2007) and CACO3 Rank (Soil Parent Material Model, 1 km)
- Model specifics:
  - Type: Generalized Additive Mixed Model (GAMM)
  - Distribution: Tweedie (variance power = 1.99)
  - Random effects: Nested structure to account for 1 km² survey square grouping
  - Smoothing: Non-linear smooths for climate variables; 2D tensor product smooths for spatial terms
  - Software: R, mgcv package (gamm function)
- Related references: Thomas et al. 2020 (patterns of topsoil carbon; methodology context), Henrys et al. 2012 (earlier estimates), Emmett et al. 2008/2010 (CS soils methods)

## Data access, provenance and reuse
- Access: Data downloadable from the provided DOI link
- Reuse citation: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. (Dataset). DOI: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Data citation requirements: If reusing, you must cite the above source.

## Sampling, calibration, analytical methods and QC
- Sampling protocol: 4 cm diameter by 8 cm long white plastic cores; surface vegetation cleared; litter left; cores inserted to full depth and retrieved; cores capped and sent to laboratory
- Extraction and counting: Dry Tullgren extraction; invertebrates enumerated under microscope
- Sample scope: Data summarised by habitat types (Keith et al., 2015); original CS sampling involved 256 survey squares
- Quality control and documentation: Full methodological details available in CS technical reports (Emmett et al. 2008, 2010); Joint Codes of Practice followed

## Outputs and monitoring utility
- For analysts monitoring environmental health and policy performance:
  - Provides standardized, comparable estimates of topsoil invertebrate density across GB for 2007
  - Enables spatial and temporal monitoring when combined with other CS or environmental datasets
  - Supports integration with other data sources to increase dataset value and accessibility of underlying data

## Data attributes and schema (Dataset specifics)
- File: CS_topsoil_invertdensity_gam.nc
- Variables:
  - Soil_invert_density: mean density (ind./m²) for 2007
  - VAR: standard error ratio (SE/mean)
  - x: Easting (meters), OSGB 27700
  - y: Northing (meters), OSGB 27700
  - transverse_mercator: coordinate reference for mapping
- Spatial coverage: Great Britain; resolution details as described (1 km for spatial terms, 5 km for climate terms)