# Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model

## Overview
- Provides modelled estimates of topsoil invertebrate density (0–8 cm depth) at 1 km2 resolution across Great Britain for 2007.
- Based on 830 sampling locations from the Countryside Survey; includes a random effect to account for nesting within 1 km2 survey squares.
- Demonstrates a GAMM approach with climate, habitat, soil, and spatial variables to capture non-linear and spatial patterns in density.
- Aims to support environmental health monitoring and policy evaluation by delivering spatially explicit indicators with associated uncertainty.

## Methods and model details
- Statistical approach: Generalized Additive Mixed Model (GAMM) using a Tweedie distribution (variance power = 1.99) to fit topsoil invertebrate density data.
- Predictors and data inputs:
  - Climate: 5-year mean Growing Degree Days, temperature, and precipitation (5 km resolution; 2003–2007).
  - Broad Habitat: qualitative class from Land Cover Map 2007.
  - Soil: CACO3 Rank; Soil Parent Material Model (British Geological Survey, 2010).
  - Spatial terms: 2D tensor product smooths for Easting/Northing (1 km resolution); standard smooths for climate variables.
- Model output: mean invertebrate density (individuals m^-2) and associated standard error ratio (VAR).
- Data format: CS_topsoil_invertdensity_gam.nc (NetCDF); coordinates in OSGB 1936 / British National Grid (EPSG:27700); includes a transverse_mercator reference.

## Data attributes
- Soil_invert_density: mean density (individuals m^-2).
- VAR: standard error divided by predicted mean (dimensionless).
- x, y: spatial coordinates (OSGB 27700 in metres).
- transverse_mercator: coordinate reference system descriptor.

## Sampling, calibration, analytical methods and Quality Control
- Sampling: 4 cm diameter × 8 cm long white plastic cores; surface vegetation removed; litter not removed; cores knocked into ground and extracted.
- Invertebrate extraction: dry Tullgren method; counted under microscope.
- Original sampling units: 256 squares from the Countryside Survey (2007).
- QA/QA procedures: followed Defra/NERC Joint Codes of Practice; detailed methodological references provided (Emmett et al. 2008, 2010; Keith et al. 2015; Henrys et al. 2012).

## Data availability and reuse
- Data access: https://doi.org/10.5285/93207428-aace-4bb5-9073-2eb44ad632d1
- Reuse citation: Keith, A.M.; Thomas, A.R.C.; Henrys, P.A.; Emmett, B.A. (2020). Topsoil invertebrate density estimates from the Countryside Survey of Great Britain, 2007 using a generalized additive model. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/93207428-aace-4bb59073-2eb44ad632d1
- Data are provided with metadata in the NetCDF file; dataset supports transparency and replication, with explicit guidance to cite when reused.

## Relevance for monitoring frameworks
- Delivers a spatially explicit, model-based indicator of soil invertebrate density across GB, enabling trend analyses and policy impact assessments on soil biodiversity.
- Includes uncertainty (VAR) to inform confidence in outputs and decision-making.
- Data can be integrated with other environmental indicators (e.g., soil carbon) for composite monitoring dashboards and governance reporting.

## Considerations and challenges (aligned with monitoring framework themes)
- Coverage: 830 sampling locations; represents 0–8 cm soil depth; may influence spatial extrapolation to unsampled areas.
- Metadata and interoperability: dataset provides key metadata (units, coordinates, model details) to aid verification and reuse; some metadata gaps are common in legacy datasets but are addressed here via explicit attributes.
- Data sharing and governance: data are openly accessible with required citation; governance and provenance are documented through linked methodological reports and references.
- Data transformation: modeling required non-linear fits and spatial smoothing; outputs are provided in a ready-to-use format, with explicit model assumptions and software context (mgcv in R).

## References
- Dore et al. (2015); Emmett et al. (2008, 2010); Henrys et al. (2012); Morton et al. (2014); Keith et al. (2015); Thomas et al. (2020); Met Office data sources.