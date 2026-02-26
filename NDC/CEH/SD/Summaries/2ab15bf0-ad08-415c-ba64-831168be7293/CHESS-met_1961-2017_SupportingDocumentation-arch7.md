# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2017) [CHESS-met] v1.2

## Overview
- Daily meteorological variables on a 1 km grid over Great Britain, suitable for running the JULES model with daily disaggregation.
- Variables included: air temperature (K), specific humidity (kg/kg), wind speed (m/s), downward longwave radiation (W/m2), downward shortwave radiation (W/m2), precipitation (kg/m2/s), air pressure (Pa), daily temperature range (K).
- Coverage extends from 1961 to 2017, with the 2016-17 years added; netCDF metadata updated accordingly.
- Data are CF-compliant and stored in monthly netCDF files, one file per variable.

## Data products and formats (GIS-friendly)
- CF-compliant netCDF files following CEH gridded dataset conventions.
- Monthly files for each meteorological variable.
- Elevation and ancillary data used in processing come from high-resolution sources (IHDTM 50 m, ETSU wind dataset at 1 km).

## Input data sources
- Precipitation: CEH-GEAR daily totals (1890-2017) for scaling to model units.
- Temperature and humidity drivers: MORECS daily mean temperature, vapour pressure, hours of bright sunshine, and wind speed.
- Temperature range: CRU TS 3.21/3.24/4.03 daily temperature range datasets (1961-2017, with updates for later periods).
- Air pressure: WATCH Forcing Data (WFD) climatology.
- Elevation: IHDTM, 50 m.
- Wind: ETSU 1 km mean wind speeds.

## Methods (how variables are generated)
- Precipitation (P): scaled from CEH-GEAR daily totals to model-required units (mm/day to mm/s).
- Air temperature (Ta): interpolated MORECS temperature using bicubic spline, then elevation-adjusted using IHDTM; valid at 1.2 m reference height.
- Specific humidity (qa): interpolated from MORECS vapour pressure and Ta; adjusted for elevation.
- Downward shortwave (Sd) and longwave (Ld) radiation: derived using cloud cover factor from MORECS sunshine hours, interpolated, and adjusted for slope and aspect; Ld uses Ta and qa.
- Slope/aspect adjustments: Sd corrected for 1 km grid cell slope/aspect; south-facing slopes receive more energy.
- Wind at 10 m (u10): interpolated MORECS wind speed, then adjusted using long-term ETSU wind averages.
- Surface pressure (p*): mean-monthly WFD climatology adjusted for 1 km grid elevation.
- Daily temperature range (DTR): reprojected from CRU datasets (no spatial interpolation) for respective periods.
- Metadata updates: CF-compliance improvements; data values unchanged from 1961-2015 relative to prior release, but metadata refreshed.

## Known issues
- ArcGIS read issue: CF-compliant files with projected coordinate systems may offset display because ArcGIS assumes WGS84; offset typically 10–100 m.
- Mitigation: adjust each layer using ArcGIS tools to align with true projection; refer to ArcGIS documentation for details.

## Data availability
- Hosted by the Environmental Information Data Centre (EIDC).
- Access: https://catalogue.ceh.ac.uk/documents/2ab15bf0-ad08-415c-ba64-831168be7293

## Release notes
- This release (v1.2) extends CHESS-met to 2016-2017 and updates metadata across all years; files remain CF-compliant but are not identical to the previous release due to metadata enhancements.

## References
- Key methodological and data source references provided (e.g., JULES model description, CEH-GEAR, MORECS, CRU TS datasets, WATCH Forcing Data, IHDTM, ETSU wind data, and related studies).