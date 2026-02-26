# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Overview
- Provides modelled estimates of topsoil invertebrate density (0–8 cm depth) at 1 km2 resolution across Great Britain using Countryside Survey data from 2007.
- Uses a Generalized Additive Mixed Model (GAMM) with climate, habitat, soil, and spatial predictors; includes a random effect for nesting within 1 km2 survey squares.
- Employs a Tweedie distribution (variance power = 1.99) and non-linear smooths, including two-dimensional tensor product smooths for spatial terms.
- Based on 830 sampling locations; related to soil carbon analyses and other Countryside Survey work.

## Data and format
- Dataset file: CS_topsoil_invertdensity_gam.nc
- Primary variable: Soil_invert_density (mean density) in individuals per m2.
- Additional variable: VAR (standard error of Soil_invert_density divided by the predicted mean; ratio).
- Coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); includes transverse_mercator mapping reference.
- Spatial and temporal coverage: 1 km2 resolution; model uses 2003–2007 climate and 2007 habitat data.

## Model and methodology
- Generalized Additive Mixed Model (GAMM) with non-linear smoothed terms and spatial interactions.
- Key predictors:
  - s(5-year mean Growing Degree Days) at 5 km resolution (2003–2007; Met Office 2014)
  - s(5-year mean temperature) at 5 km
  - s(5-year mean precipitation) at 5 km
  - te(Easting, Northing) for 1 km spatial interactions
  - Broad Habitat (Land Cover Map 2007)
  - CACO3 Rank (Soil Parent Material Model)
- Random effect to account for nesting of samples within 1 km2 survey squares.
- Modelling tool: R package mgcv with Tweedie family (variance power = 1.99).

## Data attributes
- Soil_invert_density: mean topsoil invertebrate density (ind m-2).
- VAR: standard error ratio (SE divided by predicted mean).
- Metadata: x and y coordinates in OSGB 1936 (EPSG:27700); transverse_mercator reference.

## Sampling, calibration, analytical methods and quality control
- Sampling method: 4 cm diameter by 8 cm long white plastic cores; surface vegetation removed; litter layer left intact.
- Processing: cores knocked into ground, capped, and sent to laboratories; invertebrates extracted by dry Tullgren method and counted under a microscope.
- Original data basis: 256 original survey squares; 830 locations used for model fitting.
- Adherence to Defra/NERC Joint Codes of Practice during sampling and analysis.
- Methodological context: detailed CS soil sampling and analysis protocols described in Emmett et al. (2008, 2010); related modelling and prior estimates discussed in Henrys et al. (2012) and Thomas et al. (2020).

## Data access and reuse
- Data available for download at: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Reuse requires citation: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/93207428-aace-4bb59073-2eb44ad632d1
- Related references include Emmett et al. (2008, 2010) CS technical reports, Morton et al. (2014) Land Cover Map, and Thomas et al. (2020) on soil carbon.

## Relevance for Data Leaders
- Demonstrates end-to-end data product from field sampling to model-based spatial predictions, enabling landscape-scale assessment of soil biota.
- Integrates multiple data sources (climate, soil, habitat, geography) into a single, reusable dataset with clear metadata and data provenance.
- Highlights the importance of data discoverability, documentation, and citation requirements to enable cross-institutional reuse and networked data stewardship.