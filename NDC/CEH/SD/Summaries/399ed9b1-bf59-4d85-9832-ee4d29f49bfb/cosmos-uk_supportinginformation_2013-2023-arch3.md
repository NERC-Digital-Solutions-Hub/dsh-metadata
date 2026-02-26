# Supporting documentation for: Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

- The COSMOS-UK dataset provides daily and sub-hourly hydrometeorological and soil moisture data from 51 sites (2013–2023), totaling 258 files including site metadata, sub-hourly and daily data, QC flags, data flags, and a single sub-hourly metadata file.
- COSMOS-UK is a network supported under the UK-SCAPE program and NERC funding; data are described and updated in a comprehensive data guide and are available via the COSMOS-UK website and NERC EIDC.

## 1) Purpose and scope
- Documents the data collection, structure, processing, quality control, and changes for daily and sub-hourly hydrometeorological and soil data across the COSMOS-UK network.
- Aims to support policy scrutiny, evaluation, and future decision-making by providing transparent, well-documented environmental time-series data and derived variables.

## 2) Data structure and contents
- 51 site metadata file: COSMOS-UK_SiteMetadata_2013-2023.csv (locations, depth, soil properties, land cover, altitude; several sites decommissioned over time).
- 51 sub-hourly data files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv (30-minute resolution; missing values as -9999; GMT ISO timestamps end of 30-minute period).
- 51 QC flags files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv (quality-control failure indicators; structure mirrors data files with _QCFLAG suffix).
- 51 data flags files: COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv (flags for dataPoints: M missing, U unchecked, I infilled, E estimated).
- 1 sub-hourly metadata file: COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv (variable definitions; includes units and aggregation details).
- 51 daily data files: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv (derived VWC, PE, SWE; daily resolution; -9999 missing).
- 51 daily flags files: COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>--2023_Flags.csv (daily data flags; mirrors data files with _FLAG suffix).
- 1 daily metadata file: COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv (daily variable definitions).

## 3) Sub-hourly data details
- Variables span radiation (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), meteorology (PA, TA, WS, WD, Q, RH), snow (SNOW_DEPTH), wind components (UX, UY, UZ), soil and heat flux (G1, G2), soil temperature and moisture (TDT#_TSOIL, TDT#_VWC, STP_TSOIL# etc.), and additional derived/auxiliary variables (COSMOS_VWC, GCC, SWE, PE, albedo, etc.).
- Temporal aggregation: sub-hourly data are 30-minute records; daily data are sums/means (or midday values for SWE/ALBEDO); timestamps end of the 30-minute period (e.g., 12:30 refers to 12:00–12:30).
- Data quality: missing values are denoted as -9999; data flagged for QC failures are removed from data files and summarized in QC flag files; network-wide QC processing combines multiple flags into unique final values for traceability.
- Derived data: daily volumetric water content (COSMOS_VWC, CRNS-based), snow water equivalent (SWE), potential evapotranspiration (PE, Penman-Monteith), albedo, and PhenoCam-based greenness (GCC) derived from mask-based RGB processing; GCC is not quality-controlled.

## 4) Daily data and derived variables
- Daily variables include LWIN, LWOUT, SWIN, SWOUT (all in MJ m-2 day-1), RN (net radiation, MJ m-2 day-1), PRECIP series (mm day-1 split by source), PA (hPa), TA (°C), WS (m s-1), WD (degrees), Q (g m-3), RH (%), G1/G2 (W m-2), TDT sensor outputs (soil temperature and moisture at multiple depths), and STP_TSOIL/STP_TSOIL# (soil temperatures at depths).
- Derived daily data: VWC, SWE, PE (mm), and GCC (daily maximum) with PhenoCam imagery; SWE calculation uses snow-albedo thresholding and snow-free count rates; GCC is based on masked PhenoCam imagery but has no quality control.
- Completeness notes: completeness indicators combine Met (meteorology) and Soil (soil temperature, heat flux, and VWC from TDT) as well as VWC completeness from CRNS.

## 5) Quality control and data flags
- Two-stage QC: 
  - Automatic QC tests run on the data; failed data are flagged and removed; each test has a unique flag value; flags for multi-test failures sum to a unique total.
  - Daily visual inspection of automated plots.
- QC flags detail which tests were failed; some variables are exempt (e.g., RN and Q are not QC'd because they are derived from QC'd values).
- Data flags provide per-value information about data status (M = missing, U = unchecked, I = infilled, E = estimated). Blank cells indicate no issue.
- Distinction: QC flags explain why data were removed; data flags indicate whether data were infilled/estimated, and are often more directly useful for data usage.

## 6) Infilling
- Infilling uses interpolation for gaps deemed reasonable (small gaps or low-variability variables).
- Methods: linear interpolation or order-2 polynomial interpolation (depending on gap size and surrounding data); larger gaps use more surrounding points if available.
- Method selection is guided by RMSE assessments: the best method is chosen per variable/gap scenario by testing artificial gaps and evaluating RMSE against known values.
- Infilling is applied to selected sub-hourly and daily variables as documented in the data sections.

## 7) Completeness and data quality status
- Completeness figures (Met, Soil, VWC) summarize how consistently data exist across sites and time for grouped variables.
- Met: precipitation, humidity, air temperature, atmospheric pressure, radiation, wind speed/direction.
- Soil: soil heat flux, soil temperature, and VWC from TDT sensors.
- VWC completeness focuses on CRNS-derived volumetric water content data.

## 8) Instrumentation and site configuration
- Instruments used (with time-varying configurations):
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (CRNS-2000/1000 models).
  - Pluvio rainfall gauge and tipping-bucket rain gauge (rain[e]).
  - Time-domain reflectometry (TDT) soil moisture sensors at multiple depths.
  - Soil heat flux plates (Hukseflux HFP01SC).
  - Soil temperature sensors (STP01) at multiple depths.
  - Radiometer (NR01) for net radiation; pyranometers/pyrgeometers for shortwave/longwave components.
  - Temperature, pressure, humidity sensors (Rotronic/Vaisala combinations).
  - 3D or 2D sonic anemometers for wind (UX, UY, UZ; WD).
  - PhenoCam imaging for GCC (greenness).
  - Snow sensors (SR50A) and SnowFox for SWE estimation.
  - Data loggers (Campbell Scientific) and central processing at UKCEH.
- Site variations and changes over time are documented; some sites have snow sensors, some have full TDT arrays, and instrument swaps (e.g., 3D vs 2D anemometers, Vaisala vs GILL MetPak) are noted with dates.
- 2023 rain[e] height adjustment: raised rain[e] gauges to 1.0 m to reduce blockages; multiple sites updated accordingly (see Table Instrumentation.9).

## 9) Data processing, governance, and updates
- Data are telemetered hourly to a central system; sub-hourly data are QC'd and flagged before inclusion.
- Major data changes and reprocessing events are documented (e.g., daily PE correction 2024, altitude metadata updates 2024, VWC recalibration 2023, rain[e] height adjustments 2023).
- Reprocessing occurs when improvements are made; time series are updated accordingly to ensure consistency.
- Data and metadata are publicly described, with author contributions and references provided to support traceability and reproducibility.

## 10) Access, references, and provenance
- Primary reference: Smith et al. 2024 (COSMOS-UK daily and sub-daily hydrometeorological and soil data documentation).
- Data hosted and maintained via NERC Environmental Information Data Centre and the COSMOS-UK website (cosmos.ceh.ac.uk).
- The documentation includes explicit guidance on instrument calibration, data corrections, and derivation methods (e.g., CRNS corrections, SWE derivation, PE computation, albedo/GCC processing).

## 11) Relevance for monitoring and policy evaluation
- Provides a robust, well-documented time series of environmental health indicators for policy scrutiny and decision-making.
- Transparent QC and data flags support assessment of data reliability and uncertainty.
- Derived daily metrics (PE, SWE, VWC) and the high-temporal-resolution sub-hourly data enable detailed hydrological and ecological analyses across multiple sites.
- Documentation of data gaps, metadata standards, and data governance helps ensure data reuse, comparability, and integration into monitoring frameworks.