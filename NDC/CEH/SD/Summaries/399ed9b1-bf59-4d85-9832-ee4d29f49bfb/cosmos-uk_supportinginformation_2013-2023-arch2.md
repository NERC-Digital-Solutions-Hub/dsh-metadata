# Supporting documentation for: Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

## Overview
- COSMOS-UK daily and sub-daily hydrometeorological and soil moisture data from 51 sites, covering 2013–2023.
- Total dataset components: 258 files including site metadata, 51 sub-hourly data files, 51 sub-hourly QC flags, 51 sub-hourly data flags, 1 sub-hourly metadata, 51 daily data files, 51 daily data flags, 1 daily metadata, and related documentation.
- Data are time-stamped to end of the 30-minute period (e.g., 12:30 refers to 12:00:01–12:30:00). Values missing are coded as -9999.
- Data are hosted via COSMOS-UK and related portals; project supported by NERC and UK-SCAPE.

## Data files and structure
- 2. COSMOS-UK sites metadata: COSMOS-UK_SiteMetadata_2013-2023.csv (metadata for 51 sites; decommissioned sites noted with end dates).
- 3. Sub-hourly hydrometeorological and soil data: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv
- 3.6 QC flags: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv
- 3.7 Data flags: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv
- 3. Sub-hourly metadata: COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv
- 4. Daily hydrometeorological and soil data: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv
- 4.7 Daily data flags: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>--2023_Flags.csv
- 4. Daily metadata: COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv
- 6. Completeness figures and related notes in document sections.

## Sub-hourly data (HALF-HOUR) and variables
- Resolution: 30-minute data from Oct 2013 to Dec 2023.
- Core variables (per Table 3.1 in the document): radiation components (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric (PA), air temperature (TA), wind metrics (WS, WD, UX, UY, UZ), humidity (Q, RH), snow depth (SNOW_DEPTH), soil heat flux (G1, G2), soil temperature and moisture at multiple depths (TDT#_TSOIL, TDT#_VWC, STP_TSOIL# variations), and derived/auxiliary variables (GCC, COSMOS_VWC, SWE, ALBEDO, PE, etc.).
- Note: RN and Q are not QC-tested.

## Daily data and derived variables
- Derived at daily resolution (Oct 2013–Dec 2023): Volumetric water content (COSMOS_VWC from CRNS), snow water equivalent (SWE), potential evapotranspiration (PE), and greenness proxy (GCC) from PhenoCam.
- Variables include daily totals or means as specified (e.g., LWIN, LWOUT, SWIN, SWOUT as daily totals in MJ/m2/day; RN as daily total; PA, TA, WS, WD, Q, RH, etc. as daily means).
- Albedo and GCC are derived; GCC uses daily max from PhenoCam imagery, with masks per site; GCC has no formal QC.

## Quality control (QC) and data flags
- QC process has two stages:
  - Automatic QC tests applied by a processing script; specific tests per variable; failed data points are flagged and removed; QC flags are stored in *_QCFLAG files.
  - Daily visual inspection of automatically generated plots.
- QC flags file structure mirrors the data file; non-zero indicates removal due to QC failures; 0 indicates pass.
- Data flags file documents data point status (M = missing, U = unchecked, I = infilled, E = estimated); flags accompany the data values and help interpret data provenance.
- Net radiation (RN) and absolute humidity (Q) are not run through QC tests (derived values from QC’d inputs).

## Infilling
- Infilling uses interpolation for gaps deemed reasonable, applied to selected variables.
- Interpolation types: linear or order-2 polynomial; choice depends on gap size and surrounding data.
- Gap assessment criteria (for infilling): gap length, available surrounding data points, and method performance (RMSE estimated via artificial gaps to select best method).
- Infilling is documented per variable and file, with RMSE-based approach described in methodology.

## Completeness
- Figure Completeness (Section 6) summarizes data completeness by site and by variable group:
  - Met data: includes precipitation, humidity, temperature, pressure, radiation, wind; combined as Met.
  - Soil data: soil heat flux, soil temperature, VWC from TDT sensors; combined as Soil.
  - VWC completeness reflects CRNS-derived VWC data quality and coverage.

## Instrumentation and site setup
- COSMOS-UK uses a suite of instruments (CRNS for VWC, rain gauges Pluvio and tipping bucket rain[e], soil moisture sensors via TDT, soil temperature probes, radiometers, anemometers, PhenoCam for GCC, snow sensors, etc.).
- Instrumentation has evolved; section 7.2 details variations by site and changes over time, including snow sensors, full TDT arrays, anemometer types, and rain[e] height adjustments.
- In 2023, rain[e] gauges were raised to 1.0 m to reduce blockage from vegetation; this may affect wind undercatch considerations but improves data reliability.

## Changes to data and reprocessing
- Data are reprocessed when improvements are made; major changes include:
  - 2024: daily PE data fix (negative sub-hourly PE ignored in daily sum); site altitude metadata updated; VWC calibration values updated; bulk density recalculated with updated soil samples; various related variable recalculations.
  - 2023–2022: VWC recalibrations and pressure sensor calibration adjustments; 00:30 and 01:00 heat flux values removed; improved infilling procedures implemented; CRNS-related data adjustments (NMDB infilling, etc.).
  - 2019–2020: SWE added; daily albedo added; PE processing revisions (30-minute to hourly/daily aggregation).
- Change table (Table Changes to data) provides a chronological history of major data processing changes.

## Data accessibility and usage
- Data described here are part of COSMOS-UK and are available via the NERC Environmental Information Data Centre (EIDC) portal and the COSMOS-UK website.
- Data are designed for standardized time-series monitoring, verification, and policy performance analysis, with consistent metadata, QC and flagging to support secondary analyses and data integration with other environmental datasets.

## Author contributions and references
- Core authors include R. Smith and a team responsible for data management, site metadata, field engineering, and processed data development.
- References cited cover calibration methods for cosmic-ray soil moisture, CRNS corrections, SWE estimation, and standard hydrological/meteorological datasets and methods.