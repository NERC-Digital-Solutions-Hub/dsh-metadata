# Topsoil nitrogen concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Purpose and geographic scope
- Provides modelled estimates of topsoil nitrogen concentration (% dry weight) for the 0–15 cm soil depth across Great Britain at 1 km² resolution, based on Countryside Survey 2007 data.
- Aimed at map-based data visualization and spatial analysis of soil fertility trends.

## Modelling approach
- Generalized Additive Mixed Model (GAMM) incorporating climate, atmospheric deposition, habitat, soil, and spatial variables.
- Includes a random effect to account for nesting of samples within 1 km survey squares.
- Uses non-linear smooth terms for climate and deposition; two-dimensional tensor product smooths for spatial (latitude/longitude) variation.
- Distribution: Tweedie (variance power = 1.99); implemented with the gamm function in R's mgcv package.
- Builds on prior work but adds climate, deposition, and spatial interactions for improved estimates.

## Data inputs and resolution
- Based on 913 sampling locations across Great Britain, with a random factor for 1 km square nesting.
- Outputs are gridded to 1 km² across GB.

## Data product format and coordinate system
- NetCDF file: CS_topsoil_nitrogen_gam.nc
- Key variable: Soil_N — mean 2007 modelled soil nitrogen concentration (% dry wt)
- Coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); supports mapping with a transverse Mercator reference
- Designed for GIS compatibility and map-based visualization

## Predictor variables included
- Climate: 5-year mean spring, summer, and autumn temperatures (C) at 5 km resolution; 5-year means for related temporal ranges
- Precipitation: 5-year mean summer and autumn precipitation (mm)
- Atmospheric deposition: 3-year mean NO3 deposition (kg ha⁻¹ yr⁻¹)
- Spatial terms: tensor product interactions for Easting/Northing (1 km and other scales)
- Habitat and soil descriptors: Broad Habitat, CACO3 Rank, Soil Group, Soil Parent Material Model, plus related classifications
- Land cover and 2007 habitat/land-use context are incorporated to capture environmental variation

## Data attributes
- Soil_N: Mean soil nitrogen concentration for 2007 modelled via GAM; Units: % dry weight soil
- VAR: Standard error associated with Soil_N divided by the predicted mean; Units: ratio
- Coordinates: x (Easting) and y (Northing) in metres; CRS: OSGB 27700
- transverse_mercator: Mapping CRS indicator (unitless)

## Sampling, calibration, analytical methods and QC
- Sampling with a 15 cm long by 5 cm diameter core, following a field protocol
- Nitrogen concentration measured with a total elemental analyser (CEH UKAS accredited SOP3102)
- Data drawn from 256 'original' survey squares
- Quality control aligned with Defra/NERC Joint Codes of Practice
- Core methodological references: Reynolds et al. 2013; Emmett et al. 2008, 2010; Thomas et al. 2020

## Relevance for GIS work and data integration
- Provides a readily plottable 1 km² gridded surface of topsoil N for GB, suitable for thematic mapping, overlay with other CS datasets (e.g., carbon, pH, land cover), and integration with GB-wide GIS layers.
- Coordinate system (OSGB 27700) facilitates alignment with GB datasets (e.g., Land Cover Map 2007, 1 km grids).
- NetCDF format supports efficient storage and multi-variable handling in GIS environments.

## References and supporting documents
- Thomas et al. (2020): Patterns and trends of topsoil carbon; methodology context
- Reynolds et al. (2013); Emmett et al. (2008, 2010): Countryside Survey soils methods and 2007 soil report
- Henrys et al. (2012); Morton et al. (2014); Dore et al. (2015): related data products and model evaluations
- British Geological Survey soil and material models and related environmental data sources referenced in the model construction