# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met] Supporting information

## Overview
- Provides daily meteorological variables on a 1 km grid over Great Britain for 1961–2019 to drive the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Variables included: air temperature (K), specific humidity (kg kg-1), wind speed (m s-1), downward longwave radiation (W m-2), downward shortwave radiation (W m-2), precipitation (kg m-2 s-1), air pressure (Pa), and daily temperature range (K).
- Precipitation is scaled from CEH-GEAR; other variables are derived from multiple coarser-resolution datasets. The 2018–19 years have been added to extend the release, with updated netCDF metadata.

## Input meteorological data
- Precipitation: CEH-GEAR gridded daily and monthly areal rainfall for the UK (1890–2019).
- Air temperature, vapor pressure, sunshine hours, wind speed: MORECS dataset.
- Daily temperature range: CRU TS series (varying versions by period: 3.21/3.24/4.03/4.04).
- Air pressure: WATCH Forcing Data (WFD) climatology.

## Other input data
- Elevation: Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m.
- Wind speeds: ETSU 1 km wind-speed dataset.

## Methods used to create meteorological variables
- Pr(cp) precipitation: scaled from CEH-GEAR to CEH units (mm/s).
- Temperature: interpolated MORECS temperature with bicubic spline; elevation-adjusted using IHDTM; valid at 1.2 m reference.
- Specific humidity: interpolated from MORECS vapor pressure and adjusted for elevation.
- Shortwave radiation: cloud cover factor derived from MORECS sunshine hours, interpolated, then adjusted for slope/aspect (south-facing slopes receive more energy).
- Longwave radiation: calculated from temperature, humidity, and cloud factor.
- Wind speed: 10 m wind speed interpolated from MORECS and adjusted to long-term ETSU wind climate.
- Surface pressure: monthly climatology from WFD, elevation-adjusted.
- Daily temperature range: reprojected from CRU TS datasets with no spatial interpolation.
- Output format: netCDF, CF-compliant, monthly files per variable; file-name mapping provided (tas for air temperature, dtr for daily temperature range, huss for specific humidity, sfcWind for wind speed, rlds for downward longwave, rsds for downward shortwave, precip for precipitation, psurf for air pressure).

## Known issues
- Reading CF-compliant files with projected coordinate systems in ArcGIS may offset layers by 10–100 m because the datum is assumed to be WGS 1984. Layers can be adjusted in ArcGIS to correct alignment.

## Data availability
- Data accessible from the Environmental Information Data Centre: https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
- Citation for use: Robinson et al. (2023) CHESS-met dataset, NERC EDS EIDC.

## Citation (references)
- Core methodological and data-source references for CHESS-met and related products, including JULES model description, CRU TS datasets, CEH-GEAR, MORECS, WATCH Forcing Data, and associated meteorological and hydrological work.