# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model.

## Overview
- Dataset provides modelled estimates of topsoil invertebrate density (0–8 cm depth) at 1 km² resolution across Great Britain.
- Based on Countryside Survey (CS) data from 2007, using a Generalized Additive Mixed Model (GAMM) that incorporates climate, habitat, soil, and spatial variables.
- Relies on data from 830 sampling locations; includes a random effect to account for nesting within 1 km² survey squares.
- Outputs are provided in a NetCDF file with density estimates and associated uncertainty.

## Data access and citation
- Data download: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Reuse citation: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/93207428-aace-4bb59073-2eb44ad632d1

## Modeling approach
- Generalized Additive Mixed Model (GAMM) with a Tweedie distribution (variance power = 1.99) to fit soil invertebrate density.
- Non-linear smoothed terms for climate variables; two-dimensional tensor product smooths for spatial location (easting/northing) to capture large-scale spatial variation.
- Random factor to account for nesting of samples within 1 km² CS survey squares.
- Climate predictors and resolutions:
  - 5-year mean Growing Degree Days (5 km resolution; 2003–2007)
  - 5-year mean temperature (5 km)
  - 5-year mean precipitation (5 km)
- Spatial and habitat predictors drawn from multiple sources (see table of variables).

## Data outputs and structure
- File: CS_topsoil_invertdensity_gam.nc
- Primary variable: Soil_invert_density (mean density) in individuals per square meter (m⁻²)
- VAR: Standard error associated with Soil_invert_density divided by the predicted mean (ratio)
- Coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700)
- Mapping geometry: Transverse Mercator reference; supports 1 km² spatial resolution outputs

## Variables and predictors
- Smoothed terms:
  - s(5 year mean Growing Degree Days)
  - s(5 year mean temperature)
  - s(5 year mean precipitation)
- Spatial terms:
  - te(Easting, Northing) at 1 km resolution
- Broad Habitat (qualitative)
- CACO3 Rank (qualitative, 1 km)
- Other parametric terms (as defined in the model)

## Sampling, calibration, and quality control
- Sampling method: 4 cm diameter by 8 cm long white plastic core; surface vegetation removed; litter layer retained.
- Processing: cores knocked into ground, then extracted with dry Tullgren method; invertebrates enumerated under a microscope.
- Original data: from 256 CS squares; methodological details in CS technical reports (Emmett et al. 2008, 2010; 2007 soils manual).
- Quality controls align with Defra/NERC Joint Codes of Practice.

## Context and references
- Related methodological and background sources include:
  - Emmett et al. (2008, 2010) CS Soils Manuals and 2007 soils report
  - Henrys et al. (2012) prior model estimates of topsoil invertebrates
  - Thomas et al. (2020) patterns of topsoil carbon (similar GAMM approach)
  - Land Cover Map 2007 (Morton et al. 2014)
  - UK Met Office climate datasets (5 km resolution for predictor variables)

## Practical considerations for analysts
- Data are model-based estimates with accompanying uncertainty (VAR) suitable for large-scale correlational analyses or integration into ecosystem service assessments.
- Spatially explicit (1 km) predictions enabling local-scale analyses, with predictors spanning climate, habitat, and soil characteristics.
- Be mindful of the underlying sampling design and potential scale mismatches when integrating with finer-scale or differently scaled datasets.
- Ensure proper citation and reference to the dataset when reused.