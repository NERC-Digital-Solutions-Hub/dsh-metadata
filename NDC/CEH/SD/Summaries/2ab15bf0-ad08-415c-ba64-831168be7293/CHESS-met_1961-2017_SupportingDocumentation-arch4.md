# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2017) [CHESS-met]

- Overview
  - CHESS-met provides daily meteorological variables on a 1 km grid covering Great Britain, enabling the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
  - Variables included: air temperature (K), specific humidity (kg/kg), wind speed (m/s), downward longwave radiation (W/m^2), downward shortwave radiation (W/m^2), precipitation (kg/m^2/s), air pressure (Pa), and daily temperature range (K).
  - Coverage: 1961–2017; this release extends to 2016–2017 and updates metadata to CF-compliance. Supersedes the previous CHESS-met release (2017b).

- Data sources (inputs)
  - Input meteorological data:
    - CEH-GEAR: gridded daily/monthly areal rainfall estimates for UK (1890–2017) used for precipitation.
    - MORECS: daily mean air temperature, vapour pressure, sunshine hours, wind speed.
    - CRU TS: daily temperature range from versions 3.21 (1961–2012), 3.24 (2013–2015), 4.03 (2016–2017).
    - WATCH Forcing Data: air pressure.
  - Other input data:
    - IHDTM: 50 m elevation model.
    - ETSU 1 km wind speed dataset.

- Methods and data production
  - Precipitation (P): scaled from CEH-GEAR daily totals to units required by JULES (mm/s).
  - Air temperature (Ta): interpolated from MORECS with bicubic spline; elevation-adjusted using IHDTM; valid at 1.2 m reference height.
  - Specific humidity (qa): interpolated from MORECS vapour pressure, then calculated with Ta and elevation adjustments.
  - Downward shortwave (Sd) and longwave (Ld) radiation: derived from cloud cover factor (from MORECS sunshine hours), with Sd corrected for slope and aspect; Ld computed from Ta, qa.
  - Wind speed (u10): interpolated MORECS values, scaled by long-term ETSU wind speed averages.
  - Surface pressure (p*): mean-monthly climatology of WFD pressure, elevation-adjusted.
  - Daily temperature range (DTR): reprojected from CRU TS monthly datasets (no spatial interpolation), using appropriate CRU version per period.
  - Elevation effects: Ta, qa, Sd, Ld, and radiation calculations adjusted for grid-cell elevation (IHDTM).
  - Reference heights and units: Ta and qa calibrated to a 1.2 m reference height.

- File format and structure
  - Data stored as netCDF, CF-compliant, following CEH gridded dataset conventions.
  - Monthly files; separate file for each variable.

- Known issues and caveats
  - ArcGIS reading CF-compliant netCDF with projected coordinate systems may default to WGS84 datum, causing a 10–100 m positional offset. Offsets can be corrected with ArcGIS tools.

- Data availability and access
  - Hosted by the Environmental Information Data Centre.
  - Download available at the provided CEH catalogue link.

- References and provenance
  - Key sources for methods and data: CHESS-met methodology papers and datasets (CEH-GEAR, MORECS, CRU TS, WATCH, IHDTM, ETSU), and JULES model description.

- Governance and usefulness for data leadership
  - Clear data lineage: multiple established data sources integrated with consistent elevation and slope/aspect corrections.
  - Metadata updates for CF compliance; versioned release (extending coverage to 2016–2017) indicating ongoing dataset maintenance.
  - Structured for reuse in hydrology/climate modelling (e.g., JULES), with explicit data formats and access mechanisms to support discoverability and interoperability.