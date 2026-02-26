# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Data access and reuse
- Data are downloadable from the provided link.
- If reusing the data, cite: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1

## Dataset overview
- Purpose: modelled estimates of topsoil invertebrate density (0–8 cm depth) at 1 km2 resolution across Great Britain using Countryside Survey data from 2007.
- Model: Generalized Additive Mixed Model (GAMM) with a Tweedie distribution (variance power 1.99); implemented with mgcv in R.
- Structure: includes a random factor to account for nesting of samples within 1 km2 survey squares; non-linear smooths for climate variables; two-dimensional tensor product smooths for latitude/longitude to capture large-scale spatial variation.
- Data scope: based on 830 sampling locations across Great Britain.
- Improvements over past work: expands predictors to climate, habitat, soil, and spatial variables beyond the earlier simpler habitat/parent material approach (Henrys et al. 2012).

## Model variables and data details
- Key predictors (from Table 1): 
  - Climate: 5-year mean Growing Degree Days (5-year mean GDD), 5-year mean temperature, 5-year mean precipitation; spatial resolution for climate terms typically 5 km; temporal range 2003–2007; sources include Met Office (2014).
  - Spatial terms: te(Easting, Northing) with 1 km resolution; explicit geographic coordinates to capture spatial structure.
  - Habitat and soil: Broad Habitat (Land Cover Map 2007), CACO3 Rank (Soil Parent Material Model, 1 km).
- Data attributes:
  - File: CS_topsoil_invertdensity_gam.nc
  - Soil_invert_density: mean density of soil invertebrates in 2007, units = individuals m^-2
  - VAR: standard error associated with Soil_invert_density divided by the predicted mean; units = ratio
  - x, y: Easting and Northing coordinates (OSGB 1936 / British National Grid, EPSG:27700)
  - transverse_mercator: mapping reference system indicator
  - Sampling and resolution details: 0–8 cm depth; 1 km2 spatial resolution for predictions; 5 km resolution for climate covariates; 2007 reference year

## Sampling, calibration, analytical methods and Quality Control
- Sampling method: soil cores 4 cm in diameter by 8 cm long; surface vegetation removed to reveal soil surface; litter not removed; cores inserted to full length and capped for transport.
- Invertebrate extraction: dry Tullgren extraction; enumeration by microscope.
- Sampling frame: data drawn from 256 original Countryside Survey squares.
- Documentation and standards: methods follow Defra/NERC Joint Codes of Practice; methodological details provided in CS technical reports (Emmett et al. 2008, 2010; Keith et al. 2015).

## Context and references
- Related methodological and contextual sources:
  - Countryside Survey soils manuals and 2007 soils report (Emmett et al. 2008, 2010)
  - Prior model estimates of topsoil invertebrates (Henrys et al. 2012)
  - Climate/data sources (Met Office 2014; Morton et al. 2014 Land Cover Map 2007)
  - Large-scale soil ecology and ecosystem services context (Keith et al. 2015)
  - Related analytical framework for soil carbon (Thomas et al. 2020)
- Principal data source: Countryside Survey (CS) 2007
- Data product colleagues and repositories cited for broader methodological background.