# Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

- A comprehensive COSMOS-UK data product spanning 51 sites from 2013 to 2023, comprising both sub-hourly (30-minute) and daily time series of hydrometeorological and soil moisture data.
- Total of 258 files, organized into site metadata, 51 sub-hourly data files, QC flag files, data flag files, daily data files, and corresponding metadata files.
- Data are provided with missing values coded as -9999 and include detailed quality control (QC) and data flags to support data provenance and re-use.

## Data structure and contents

- Sub-hourly data (30-minute resolution; Oct 2013 – Dec 2023)
  - 51 site data files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv
  - 51 QC flag files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv
  - 51 data flag files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv
  - 1 site metadata for sub-hourly variables: COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv
  - Variables include radiation components, precipitation (Pluvio and tipping bucket), humidity, temperature, wind (speed/direction), soil temperature/moisture sensors (TDT at multiple depths), soil heat flux, and derived quantities. QC and data flag fields mirror data structure.
  - Automatic QC tests and daily visual QC are applied; RN and Q are not QC-tested (derived values).

- Daily data (resolution = daily; Oct 2013 – Dec 2023)
  - 51 daily data files: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv
  - 51 daily QC flag files: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023_Flags.csv
  - 1 daily metadata: COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv
  - Derived daily variables include volumetric water content (VWC) from CRNS, snow water equivalent (SWE), potential evapotranspiration (PE), and albedo-derived GCC (green color content) from PhenoCam images.
  - Daily data are derived from sub-hourly data and may have their own infilling of gaps.

- Metadata
  - COSMOS-UK_SiteMetadata_2013-2023.csv provides site locations, coordinates, altitude, soil type, land cover, bulk density, soil organic carbon, lattice/bound water, and other site-specific characteristics.
  - Altitude metadata largely sourced from NEXTMap 10 m DTM, with some site-specific adjustments.

- Data provenance and accessibility
  - Data are hosted under NERC Environmental Information Data Centre with accompanying user guide and COSMOS-UK website for context and updates.

## Variables, units, and data quality

- Sub-hourly variables (examples)
  - Radiation: LWIN, LWOUT, SWIN, SWOUT, RN; Precipitation: PRECIP, PRECIP_TIPPING, PRECIP_RAINE
  - Meteorology: PA (hPa), TA (°C), WS (m/s), WD (°), Q (gm^-3), RH (%)
  - Snow: SNOW_DEPTH (mm)
  - Wind components: UX, UY, UZ
  - Soil: G1, G2 (soil heat flux), TDT#_TSOIL, TDT#_VWC, STP_TSOIL#, STP_TSOIL# and related VWC/temperature sensors
  - Other: G1/G2, albedo, GCC (daily PhenoCam-derived greens content), etc.
- Daily variables (examples)
  - Radiative inputs: LWIN, LWOUT, SWIN, SWOUT (daily totals, MJ m^-2 day^-1)
  - Net radiation (RN, MJ m^-2 day^-1)
  - Precipitation components (PRECIP, PRECIP_TIPPING, PRECIP_RAINE)
  - PA, TA, WS, WD, Q, RH
  - Derived: PE (mm), VWC (CRNS-based), SWE (mm), GCC (daily maximum from PhenoCam)
- QC, flags, and completeness
  - QC flags explain why data were removed; data flags describe whether data were infilled or estimated.
  - RN and Q are not QC-tested (derived values from QC’d data).
  - Completeness tracked by site, with separate summaries for Met (met variables) and Soil (soil variables); VWC completeness tracked separately.

## Quality control and data flags

- Two-stage QC
  - Automatic QC tests applied to relevant variables; failed data are flagged and removed.
  - Daily visual inspection of automatically generated plots.
- QC flags
  - QC flag files store the sum of individual test flags; non-zero flags indicate data removed due to QC failures.
  - Data flag files indicate if values were infilled, estimated, missing, or unchecked.
  - Example: a data value replaced by infilling (I flag) with its corresponding QC flag values traceable to the tests failed.
- Important distinctions
  - QC flags explain why data were removed; data flags convey information about the data value (infilled/estimated).
  - Derived variables (RN, Q) are not subjected to QC tests, but are checked via their input QC’d data.

## Infilling and data gaps

- Infilling process
  - Simple interpolation for selected variables and gaps considered reasonable.
  - Interpolation types: linear and order-2 polynomial.
  - Gap handling logic considers gap size, surrounding data points, and uses RMSE to choose best method.
  - RMSE-based evaluation is performed with artificial gaps to determine the best infill method per variable.
- Impact and reporting
  - Infilling is documented in the corresponding _FLAG files; infilled values are distinguished from raw data.

## Completeness and data coverage

- Completeness figures cover October 2013 to December 2023.
- Met data include precipitation, humidity, temperature, pressure, radiation, wind speed/direction.
- Soil data include soil heat flux, soil temperature, and various VWC measurements.
- VWC completeness is specifically reported for the CRNS-derived soil moisture data.

## Instrumentation and site characteristics

- Core instruments
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (VWC) and related CRNS-derived metrics
  - Rain gauges: Pluvio (with rim height adjustments for some sites), tipping bucket (rain[e])
  - Soil moisture sensors (TDT) at multiple depths, soil temperature sensors
  - Radiometer (NR01) for net radiation
  - Temperature, humidity, pressure sensors; 3D or 2D sonic anemometers for wind
  - PhenoCam for GCC (green color content) derived from imagery
  - Snow depth sensors and SnowFox for SWE estimation
  - Data logger system (Campbell Scientific CR3000) with central processing
- Site variations
  - Not all sensors are installed at every site; instrumentation configurations evolve over time
  - Some sites located on forest towers; rain[e] height raised to 1.0 m in 2023 to reduce blockages
  - Table-driven site-by-site instrumentation details provided in the documentation

## Changes to data and data processing

- Major data processing changes (highlights)
  - 2023–2024: daily PE data fix; ensuring negative sub-hourly PE values do not contribute to daily sums
  - Site altitude metadata updates based on latest elevation data
  - VWC calibration updates and gamma values recalibrated; bulk density recalculated
  - Various corrections to CRNS-derived variables and infilling procedures (e.g., heat flux corrections, precipitation updates)
  - SWE, albedo, and GCC derivations updated as part of ongoing data refinement
- Documentation of data evolution
  - A table lists major changes with dates and details (e.g., PE, altitude, VWC, etc.)

## Access, authorship, and references

- Authors and contributions
  - R. Smith (primary author); multiple team members contributed to data management, site metadata, processing algorithms, and field engineering.
- References
  - Foundational methods and calibration papers for CRNS, soil moisture, VWC derivation, SWE estimation, and related instrumentation are cited throughout.

## Practical notes for analysts

- Use caution with snow days and CRNS-derived VWC around snow events; SWE and albedo thresholds are used to identify snow days and adjust analyses accordingly.
- Rely on QC and data flags to filter or adjust datasets; RN and Q are derived and not QC-tested, so consider propagation of input QC through derived data.
- Consider site-specific instrumentation changes and height adjustments (e.g., rain[e] height) when combining data across sites or over time.
- Leverage metadata for site-specific context (altitude, soil type, land cover) and for understanding data completeness by site.
- When building models, account for gaps that are infilled, and use the RMSE-based infilling assessments to gauge uncertainty associated with interpolated values.