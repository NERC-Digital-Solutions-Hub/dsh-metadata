# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2017) [CHESS-met]

- Purpose and scope
  - Provides daily meteorological variables on a 1 km grid across Great Britain to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
  - Enables consistent, time-series assessment of environmental health, hydrology, and ecology across the UK.
  - Outputs are suitable for standardised reports, maps, and charts; data are stored and uploaded to appropriate data portals.

- Variables and daily timing
  - Air temperature (K)
  - Specific humidity (kg/kg)
  - Wind speed (m/s)
  - Downward longwave radiation (W/m^2)
  - Downward shortwave radiation (W/m^2)
  - Precipitation (kg/m^2/s)
  - Air pressure (Pa)
  - Daily temperature range (K)
  - All except daily temperature range are daily means from 09:00 GMT to 09:00 GMT the next day

- Release scope
  - This release extends the CHESS-met dataset to cover 2016–2017 and updates netCDF metadata for all years.
  - Supersedes the previous release (2017b) with extended coverage and updated metadata.
  - Data are CF-compliant netCDF files, organized as monthly files for each variable.

- Input data sources and layers
  - Precipitation: CEH-GEAR daily rainfall estimates (1890–2017), scaled to required units.
  - Temperature, humidity, sunshine, wind: MORECS (Met Office Rainfall and Evaporation Calculation System) daily mean values.
  - Daily temperature range: CRU TS datasets (versions 3.21/3.24/4.03) corresponding to temporal coverage.
  - Air pressure: WATCH Forcing Data (WFD) climatology.
  - Elevation: Integrated Hydrological Digital Terrain Model (IHDTM), 50 m resolution.
  - Wind: ETSU 1 km resolution mean wind speeds.

- Methods and data processing
  - Precipitation: CEH-GEAR totals scaled to kg m^-2 s^-1 (mm/day to model units).
  - Temperature: MORECS temperatures interpolated with a bicubic spline and elevation-adjusted using IHDTM; valid at 1.2 m height.
  - Specific humidity: Interpolated from MORECS vapour pressure and combined with modeled temperature; elevation-adjusted.
  - Downward shortwave radiation: Derived from cloud cover factor (from MORECS sunshine hours), then adjusted for grid cell slope and aspect.
  - Downward longwave radiation: Calculated using Ta, qa, and cloud-adjusted shortwave context.
  - Wind: 10 m wind speed interpolated from MORECS and adjusted using long-term ETSU wind averages.
  - Surface air pressure: Mean-monthly climatology from WFD, adjusted for 1 km grid elevation.
  - Daily temperature range: Reprojected from CRU TS datasets with no additional spatial interpolation.
  - All variables are aligned to the 1 km grid for GB and prepared for use with JULES.

- File format and accessibility
  - NetCDF format, CF-compliant, following CEH gridded dataset conventions.
  - Data stored as monthly files for each meteorological variable.
  - Data availability: Environmental Information Data Centre (EIDC) catalog; download via the CEH catalogue page.

- Known issues and caveats
  - ArcGIS reading issue: projected coordinate systems can offset layers by 10–100 m due to WGS84 assumptions in some workflows; adjustments in ArcGIS tools are required to align layers correctly.

- How this supports environmental monitoring
  - Provides a consistent, high-resolution meteorological foundation for evaluating environmental health, hydrological conditions, and ecological processes over time.
  - Enables integration with other datasets and broader analyses, addressing goals of data value enhancement and wider data accessibility.

- Data availability and references
  - Primary data host: Environmental Information Data Centre (EIDC); access via CEH catalogue.
  - Key references for methods and data sources include Robinson et al. (2017a, 2017b) on CHESS-met, and data sources such as CEH-GEAR, MORECS, CRU TS, and WATCH Forcing Data.