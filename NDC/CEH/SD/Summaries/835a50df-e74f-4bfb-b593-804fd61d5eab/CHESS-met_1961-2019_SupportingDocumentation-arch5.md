# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESSmet] Supporting information

## Overview
- CHESS-met provides daily meteorological variables on a 1 km grid across Great Britain for 1961–2019, extended to 2018–2019 in this release, to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- This supporting information accompanies the CHESS-met dataset release and updates metadata for all years.

## Data content and variables
- Variables (daily means from 09:00 GMT to 09:00 GMT next day):
  - Air temperature (K)
  - Specific humidity (kg/kg)
  - Wind speed (m/s)
  - Downward longwave radiation (W/m^2)
  - Downward shortwave radiation (W/m^2)
  - Precipitation (kg/m^2/s)
  - Air pressure (Pa)
  - Daily temperature range (K)
- All variables (except daily temperature range) are daily means; precipitation is scaled from CEH-GEAR daily rainfall estimates.
- File organization: netCDF, CF-compliant, monthly files; one file per variable with specific naming conventions.

## Data provenance and input data sources
- Precipitation: CEH-GEAR daily rainfall estimates (Keller et al., 2015; Tanguy et al., 2021).
- Air temperature, wind speed, humidity: MORECS dataset (Hough & Jones, 1997) and elevation-adjusted interpolations.
- Daily temperature range: reprojected from CRU TS series (various versions by year).
- Elevation: Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m.
- Wind speeds: UK ETSU 1 km mean wind speeds.
- Reference data used to derive grid-scale variables and apply elevation corrections.

## Methods and data processing
- Precipitation: scaled from CEH-GEAR totals to model units (mm/day to mm/s).
- Air temperature: interpolated MORECS values, then elevation-adjusted; valid at 1.2 m height.
- Specific humidity: derived from MORECS vapor pressure and interpolated air temperature; elevation-adjusted.
- Downward shortwave/longwave radiation: derived using cloud cover factor from MORECS sunshine hours, with shortwave corrected for slope/aspect.
- Long-term wind adjustment: u10 interpolated from MORECS and adjusted to long-term ETSU wind speeds.
- Surface pressure: mean-monthly climatology from WFD adjusted for 1 km elevation.
- Daily temperature range: reprojected from CRU TS datasets with year-specific versions; no spatial interpolation.
- Data are stored in monthly netCDF files and follow UKCEH gridded dataset conventions.

## Metadata, documentation, and citation
- CF-compliant netCDF with detailed metadata; Table 1 (variable-file mappings) documents file-name relationships.
- Data availability and citation:
  - Data accessible via Environmental Information Data Centre (EDI): https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
  - Key citation: Robinson et al. (2023), CHESS-met, NERC EDS EIDC dataset DOI above.
- Related references provide model and data provenance context (e.g., Robinson et al. 2017/2023; Best et al. 2011; CRU TS series; CEH-GEAR; MORECS; WATCH Forcing Data).

## Access, usage, and governance
- Access through EIDC with required citation for any publications or outputs.
- Data are intended to be discoverable and usable for researchers and practitioners requiring high-resolution meteorology for GB.
- Documentation aligns with UKCEH conventions to support interoperability and reuse.

## Updates and versioning
- This release supersedes the previous CHESS-met version (Robinson et al., 2020) and extends coverage to 2018–2019.
- Metadata updated for all years; underlying methods and data sources remain documented for reproducibility.

## Known issues and limitations
- ArcGIS reading issue: CF-compliant files with projected coordinate systems may offset display by ~10–100 m due to WGS84 assumption in ArcGIS; adjust layers with ArcGIS tools as documented.

## Data governance considerations for Data Stewards
- Data quality and interoperability:
  - Ensure metadata completeness (variables, units, file mappings, processing steps, and versioning).
  - Maintain provenance trails linking outputs to input datasets (CEH-GEAR, MORECS, CRU TS, WATCH, IHDTM, ETSU).
- Access and sharing:
  - Enforce citation requirements in all outputs.
  - Ensure alignment with UKCEH gridded conventions and CF standards for long-term preservation.
- Update and maintenance:
  - Track version history (this release vs. prior versions) and planned future updates (e.g., additional years or methodological refinements).
- Practical data stewardship actions:
  - Validate coordinate reference system handling and provide guidance for users encountering ArcGIS offset issues.
  - Monitor dataset completeness across years and document any gaps or anomalies in the metadata.