# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESSmet] Supporting information

## Introduction
- CHESS-met provides daily meteorological variables on a 1 km grid across Great Britain (1961-2019) to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Variables include: air temperature (K), specific humidity (kg/kg), wind speed (m/s), downward longwave radiation (W/m^2), downward shortwave radiation (W/m^2), precipitation (kg/m^2/s), air pressure (Pa), and daily temperature range (K).
- All variables (except daily temperature range) are daily means from 09:00 GMT to 09:00 GMT the following day.
- Precipitation is scaled from CEH-GEAR daily rainfall estimates; other variables are derived from multiple coarser-resolution datasets.
- This release extends coverage to 2018-2019 and updates netCDF metadata; supersedes the 2020 version.

## Input meteorological data
- Precipitation: CEH-GEAR daily rainfall estimates (1890-2019; scaled to model units).
- Temperature, humidity, sunshine, and wind: MORECS daily mean values.
- Daily temperature range: CRU TS series (various versions by year).
- Air pressure: WATCH Forcing Data climatology (WFD).

## Other input data
- Elevation: Integrated Hydrological Digital Terrain Model (IHDTM), 50 m resolution.
- Wind speeds: ETSU 1 km resolution dataset.
- Data sources are combined and adjusted to produce gridded meteorological fields.

## Methods used to create meteorological variables
- Precipitation: scaled from CEH-GEAR daily totals to model units (mm/day to mm/s).
- Air temperature: interpolated MORECS values, elevation-adjusted using IHDTM, valid at 1.2 m height.
- Specific humidity: interpolated from MORECS vapor pressure and temperature; adjusted for elevation.
- Downward shortwave radiation: computed from cloud cover factor (derived from MORECS sunshine hours), then adjusted for slope/aspect.
- Downward longwave radiation: derived alongside shortwave radiation using temperature, humidity, and cloud cover.
- Wind speed at 10 m (u10): interpolated MORECS speeds, adjusted to long-term ETSU wind averages.
- Surface air pressure: mean-monthly climatology from WFD, elevation-adjusted.
- Daily temperature range: reprojected from CRU TS monthly datasets (no spatial interpolation).
- Reference heights and adjustments: temperature/humidity referenced to ~1.2 m; elevation corrections applied for all relevant variables.

## File Format
- Data available as CF-compliant netCDF files.
- Monthly files for each variable; file naming follows a defined mapping (tas for air temperature, dtr for daily temperature range, huss for specific humidity, sfcWind for wind speed, rlds for downward longwave, rsds for downward shortwave, precip for precipitation, psurf for air pressure).
- The CHESS-met set includes multiple variables each stored in separate monthly files, with consistent conventions across years.

## Known issues
- ArcGIS reads CF-compliant files with projected coordinate systems as if they are WGS 84, causing a positional offset (approximately 10–100 m) when using CHESS-met data with non-WGS 84 datums.
- Offsets can be corrected within ArcGIS using its tools; no data corrections in the dataset itself.

## Data availability
- Data are available from the Environmental Information Data Centre (EIDC): https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
- Publications using CHESS-met should cite Robinson et al. (2023) and provide the dataset DOI.
- Please cite: Robinson, E.L. et al. (2023). CHESS-met (1961-2019). NERC EDS EIDC.

## Data use and citation
- Users are encouraged to cite the CHESS-met dataset when used in publications, reports, or outputs.
- Documentation and metadata accompany the dataset to aid reuse, transformation, and integration into end-user data products.