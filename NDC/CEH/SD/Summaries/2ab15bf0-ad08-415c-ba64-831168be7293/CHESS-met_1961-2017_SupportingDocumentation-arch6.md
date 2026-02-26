# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2017) [CHESS-met] v1.2

## Overview
- Provides daily meteorological variables on a 1 km grid over Great Britain, covering 1961-2017 (extended to 2016-17 in this release).
- Variables include: air temperature (K), specific humidity (kg/kg), wind speed (m/s), downward longwave radiation (W/m^2), downward shortwave radiation (W/m^2), precipitation (kg/m^2/s), air pressure (Pa), and daily temperature range (K).
- Precipitation is scaled from CEH-GEAR; other variables are derived from coarser datasets.
- CF-compliant netCDF format; monthly files per variable; metadata updated for CF compliance.
- Aims to support the Joint UK Land Environment Simulator (JULES) and other data analyses by providing ready-to-use meteorological inputs.

## Data content and variables
- Daily means for most variables (09:00 GMT to 09:00 GMT next day); daily temperature range (DTR) is reprojected with year-specific CRU inputs.
- Variables and their general derivation:
  - Precipitation (P): scaled from CEH-GEAR daily totals (mm/day) to model units (mm/s).
  - Air temperature (Ta): interpolated from MORECS and elevation-adjusted using IHDTM 50 m elevation data.
  - Specific humidity (qa): derived from MORECS vapour pressure and Ta with elevation adjustment.
  - Downward shortwave radiation (Sd) and longwave radiation (Ld): computed from cloud cover factor derived from MORECS sunshine hours, interpolated to 1 km, and adjusted for slope/aspect.
  - 10 m wind speed (u10): interpolated from MORECS wind speed and adjusted with ETSU long-term wind speeds.
  - Surface air pressure (p*): mean-monthly climatology from WFD pressure adjusted for 1 km elevation.
  - Daily temperature range (DTR): reprojected from CRU TS datasets (varying by year).
- Elevation and terrain effects:
  - Elevation-based adjustments for Ta, qa, and radiation.
  - Slope/aspect corrections for Sd, influencing energy receipt.

## Data sources and creation methods
- Input data sources:
  - CEH-GEAR: gridded UK rainfall (1890-2017) for precipitation.
  - MORECS: daily means for temperature, vapour pressure, sunshine hours, wind speed.
  - CRU TS: daily temperature range (various versions by year).
  - WATCH Forcing Data: air pressure.
  - IHDTM: 50 m elevation.
  - ETSU wind speed dataset: long-term wind speeds for adjustment.
- Methods (summarised):
  - P scaled from CEH-GEAR to model units.
  - Ta created via bicubic interpolation of MORECS values, elevation-adjusted.
  - qa derived from vapour pressure and Ta, with elevation adjustment.
  - Sd and Ld derived using cloud cover factor and environmental conditions; Sd corrected for slope/aspect.
  - u10 interpolated from MORECS and scaled by ETSU climatology.
  - p* climatology adjusted for grid elevation.
  - DTR reprojected from CRU TS datasets with year-specific sources.

## File format and structure
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Monthly files, with one file per variable.
- Data stored and distributed by the Environmental Information Data Centre (EIDC).
- Metadata updated for CF compliance; files are not identical to earlier releases due to metadata updates.

## Known issues
- ArcGIS has a known issue reading CF-compliant files with projected coordinate systems because the datum is assumed to be WGS84; CHESS-met uses a different datum, causing small positional offsets (approximately 10–100 meters). Offsets can be corrected with ArcGIS tools; refer to ArcGIS documentation for guidance.

## Data availability and access
- Data hosted by the Environmental Information Data Centre (EIDC).
- Download available via the CEH catalogue: https://catalogue.ceh.ac.uk/documents/2ab15bf0-ad08-415c-ba64-831168be7293

## How this supports data use (Data Support perspective)
- Provides a ready-to-use, self-contained meteorological dataset to enable data exploration and product creation (e.g., inputs for JULES or other models, dashboards, or analyses) across a broad geographic and temporal span.
- Facilitates data combination and transformation workflows (temperature, humidity, radiation, wind, precipitation, pressure) with clear provenance and CF-compliant formatting for interoperability.
- Documentation of data sources, processing steps, and known issues aids data QA, reproducibility, and communication of limitations to end users.
- The extension to 2016-17 and updated metadata enhance data completeness and usability for contemporary analyses.

## References (key sources)
- JULES model and data usage: Best et al. (2011)
- CEH-GEAR rainfall estimates: Keller et al. (2015); Tanguy et al. (2019)
- MORECS dataset: Hough and Jones (1997)
- CRU TS climate datasets: Jones and Harris (2013); Harris et al. (2014)
- WATCH Forcing Data: Weedon et al. (2011)
- IHDTM digital terrain model: Morris and Flavin (1990)
- ETSU wind resource and related methods: Newton and Burch (1985); Burch and Ravenscroft (1992)
- CHESS-met release history: Robinson et al. (2017a, 2017b)