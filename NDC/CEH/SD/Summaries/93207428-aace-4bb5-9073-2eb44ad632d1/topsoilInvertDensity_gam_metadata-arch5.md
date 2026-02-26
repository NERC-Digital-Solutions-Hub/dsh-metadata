# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Overview
- Provides modelled estimates of topsoil invertebrate density (0–8 cm depth) at 1 km² resolution across Great Britain for 2007, derived from Countryside Survey data.
- Based on 830 sampling locations with a random effect to account for nesting within 1 km² survey squares.
- Employs a Generalized Additive Mixed Model (GAMM) incorporating climate, habitat, soil, and spatial variables; non-linear smooths for climate and two-dimensional tensor product smooths for space.
- Uses a Tweedie distribution (variance power ≈ 1.99) rather than a Gaussian model.
- Model fitting performed in R using the mgcv package.

## Data content and scope
- Dataset: CS_topsoil_invertdensity_gam.nc containing modelled mean invertebrate density values.
- Spatial and temporal scope: Great Britain, 0–8 cm soil depth; predictions across 1 km² cells; climate predictors reflect 5-year means (2003–2007).
- Predictors included in the model (as per Table 1): 
  - s(5-year mean Growing Degree Days) and s(5-year mean temperature) at 5 km resolution (2003–2007)
  - s(5-year mean precipitation) at 5 km resolution (2003–2007)
  - te(Easting, Northing) at 1 km resolution
  - Broad Habitat (Land Cover Map 2007)
  - CACO3 Rank (Soil Parent Material Model, 1 km)
- Data product builds on 830 sample locations with a nested structure and spatial smoothing to capture large-scale variation.

## Data attributes and format
- Primary variables:
  - Soil_invert_density: mean density of soil invertebrates (individuals m⁻²)
  - VAR: standard error associated with Soil_invert_density divided by the predicted mean (units: ratio)
  - x: Easting (OSGB 1936/British National Grid, EPSG:27700; units: metres)
  - y: Northing (OSGB 1936/British National Grid, EPSG:27700; units: metres)
  - transverse_mercator: coordinate reference system for mapping (unitless)
- File and coordinates:
  - File: CS_topsoil_invertdensity_gam.nc (NetCDF)
  - Coordinate system: OSGB 1936 / British National Grid (EPSG:27700)
- Data provenance:
  - Model inputs include Climate (Met Office 5-year means), Land Cover Map 2007, Soil Parent Material Model
  - Sampling summarized by habitat types; 4 cm diameter x 8 cm long cores; dry Tullgren extraction; 256 original survey squares
- Documentation and quality control:
  - Technical methods detailed in Countryside Survey reports (Emmett et al. 2008, 2010) and Henrys et al. 2012
  - Standard quality practices aligned with Defra/NERC Joint Codes of Practice

## Data provenance, sampling and QA
- Sampling protocol: soils collected with white plastic cores, surface litter preserved, cores extracted in lab, invertebrates counted under microscope
- QA and governance: followed Defra/NERC Joint Codes of Practice; linked to Countryside Survey technical reports and methodological papers
- Data sources and references:
  - Countryside Survey soil manuals and reports (Emmett et al. 2008, 2010)
  - Past model estimates from Henrys et al. 2012
  - Related climate and land-cover datasets (Met Office, Land Cover Map 2007)
  - Methodological context in Thomas et al. 2020 (soil carbon, similar GAMM framework)

## Access, reuse and licensing
- Data access and availability: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Reuse citation requirement: 
  Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/93207428-aace-4bb59073-2eb44ad632d1
- Note: The dataset is hosted by the NERC Environmental Information Data Centre. The document specifies that, if data are reused, proper citation is required as above. No explicit licensing terms are described in the provided text; stewardship practice should follow repository guidelines and acknowledge data provenance.

## Related references
- Dore et al. (2015) – evaluation of atmospheric models (contextual reference)
- Emmett et al. (2008, 2010) – Countryside Survey soils manuals and CS soils report
- Henrys et al. (2012) – previous model estimates of topsoil invertebrates
- Morton et al. (2014) – Land Cover Map 2007
- Thomas, Cosby, Henrys, Emmett (2020) – Patterns and trends of topsoil carbon using GAMM framework
- Met Office climate data sources (2003–2007 5-year means) and British Geological Survey soil materials models used as inputs