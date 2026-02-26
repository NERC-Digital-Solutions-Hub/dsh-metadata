# The Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met] provides daily meteorological variables on a 1km grid over Great Britain

## Overview
- Provides daily meteorological variables on a 1 km grid across Great Britain, suitable for running the JULES model with daily disaggregation.
- Variables include: air temperature (tas), specific humidity (huss), wind speed (sfcWind), downward longwave radiation (rlds), downward shortwave radiation (rsds), precipitation (precip), air pressure (psurf), and daily temperature range (dtr).
- Temporal coverage: 1961–2012; data are prepared as netCDF files following CEH conventions.
- Precipitation data are CEH-GEAR-based and scaled to required units; other variables are derived from coarser-resolution inputs.

## Input data sources
- Met Office MORECS dataset for daily mean air temperature, vapour pressure, hours of bright sunshine, and wind speed.
- CRU TS 3.21 for daily temperature range.
- WATCH Forcing Data for air pressure.
- Elevation data from the Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m resolution.
- 1 km resolution mean wind speeds from ETSU dataset.

## Data construction methods
- Precipitation (P) is scaled from CEH-GEAR daily totals to the units used by JULES.
- Air temperature (Ta) is created by interpolating MORECS Ta with a bicubic spline and adjusting for 1 km grid elevation using IHDTM.
- Specific humidity (qa) is derived by interpolating MORECS vapour pressure and using Ta, with elevation adjustments; valid at 1.2 m reference height.
- Cloud cover factor is derived from MORECS hours of sunshine and used to compute downward shortwave (rsds) and longwave (rlds) radiation, including cloud corrections.
- Downward shortwave radiation is slope- and aspect-adjusted; southern slopes receive more energy.
- Wind speed at 10 m (u10) is interpolated from MORECS and adjusted with long-term ETSU wind data.
- Surface air pressure (psurf) is a mean-monthly WFD climatology adjusted for grid elevation.
- Daily temperature range (dtr) is reprojected from CRU TS 3.21 with no spatial interpolation.

## File format and access
- Data are distributed in netCDF format, CF-compliant, following CEH gridded dataset conventions.
- NetCDF variable names: tas, huss, sfcWind, rlds, rsds, precip, psurf, dtr.
- Downloading via an Order Manager returns subset files containing required variables and specified temporal/spatial aggregations; original files are monthly per variable named chess_<var>_<year><month>.nc.

## Data quality, metadata and governance
- Uses multiple established data sources with documented methodologies; full method details referenced (Robinson et al., in prep).
- Ensures traceability of inputs and processing steps; netCDF CF-compliant formatting facilitates interoperability and data governance.
- Metadata considerations include elevation adjustments, slope/aspect corrections, and consistency with reference heights; some details rely on external documentation and references.

## Applications for monitoring frameworks
- Enables high-resolution climate, hydrology, and ecological monitoring across the UK.
- Supports policy scrutiny and decision-making by providing consistent, auditable meteorological inputs for modeling and impact assessment (e.g., hydrological responses via JULES).
- Facilitates reproducibility and transparency through standardized data formats, naming conventions, and documented data sources.

## References (selected)
- Best et al. (2011) on JULES model description (Part 1: Energy and water fluxes).
- Hough & Jones (1997) and related MORECS documentation.
- Jones & Harris (2013, 2014) on CRU TS datasets.
- Keller et al. (2015) and Tanguy et al. (2014) on CEH-GEAR rainfall estimates.
- Morris & Flavin (1990) on the digital terrain model for hydrology.
- Newton & Burch (1992) on UK wind energy resource modelling.
- Weedon et al. (2011) on WATCH Forcing Data.
- Robinson et al. (in prep) on trends in evaporative demand using high-resolution meteorological data.