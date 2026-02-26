# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2017) [CHESS-met]

## Overview
- Daily meteorological variables on a 1 km grid over Great Britain, enabling JULES model work with daily disaggregation.
- Variables: air temperature (K), specific humidity (kg kg-1), wind speed (m s-1), downward longwave radiation (W m-2), downward shortwave radiation (W m-2), precipitation (kg m-2 s-1), air pressure (Pa), daily temperature range (K).
- Temporal coverage: 1961–2017; daily mean values from 09:00 GMT to 09:00 GMT the following day.
- Data distributed as netCDF files, CF-compliant, with monthly files for each variable.

## Data Composition and Variables
- Precipitation: CEH-GEAR daily rainfall estimates scaled to required units.
- Other variables: derived from coarser-resolution datasets (MORECS, CRU TS, WATCH).
- File metadata updated for CF-compliance in this release.

## Data Sources and Provenance
- Input data sources:
  - CEH-GEAR for precipitation (1890–2017).
  - MORECS for daily mean air temperature, vapour pressure, hours of bright sunshine, wind speed.
  - CRU TS versions for daily temperature range across periods:
    - 1961–2012: CRU TS 3.21
    - 2013–2015: CRU TS 3.24
    - 2016–2017: CRU TS 4.03
  - WATCH Forcing Data for air pressure.
- Elevation:
  - Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m resolution.
- Wind reference:
  - ETSU 1 km resolution mean wind speeds.

## Methods and Processing
- Precipitation (P): scaled from CEH-GEAR totals to model units (mm/s).
- Temperature (Ta): MORECS temperature interpolated to 1 km grid (bicubic spline) and elevation-adjusted.
- Specific humidity (qa): interpolated from MORECS vapour pressure and adjusted for elevation.
- Cloud impact: cloud cover factor derived from MORECS sunshine hours; used to compute downward shortwave radiation (Sd) and, with Ta and qa, downward longwave radiation (Ld); Sd corrected for slope and aspect.
- Wind (u10): interpolated from MORECS and adjusted to long-term ETSU wind climatology.
- Pressure (p*): mean-monthly climatology (WFD) adjusted for 1 km grid elevation.
- Daily temperature range (DTR): reprojected from CRU TS datasets (no spatial interpolation) for respective periods.
- All years 1961–2015 use the same values as the previous CHESS-met release; metadata updated to ensure CF compliance.

## File Format and Structure
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data organized monthly; one file per variable.

## Versioning and Release History
- This release extends CHESS-met to 2016–2017 and supersedes the 2017b version.
- Metadata refreshed for CF compliance; dataset values are not identical to earlier release due to metadata updates.

## Data Availability and Access
- Hosted by the Environmental Information Data Centre (EIDC).
- Download via CEH data catalogue: https://catalogue.ceh.ac.uk/documents/2ab15bf0-ad08-415c-ba64-831168be7293

## Known Issues and Technical Notes
- ArcGIS issue: CF-compliant files with projected coordinate systems may display offsets when the datum is assumed as WGS84; offsets typically 10–100 m. Correctable with ArcGIS tools.

## Use, Reuse, and References
- Intended for climate hydrology and ecology modelling and other research requiring high-resolution meteorological inputs for Great Britain.
- Documentation and methodology available in Robinson et al. 2017a; dataset versioning described in Robinson et al. 2017b and related references (e.g., Keller et al. 2015; Tanguy et al. 2019; Weedon et al. 2011).