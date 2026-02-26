# Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

- COSMOS-UK provides daily and sub-daily time series of hydrometeorological and soil moisture data from 51 sites across the COSMOS-UK network, covering 2013–2023.
- The dataset comprises 258 files in total, including site metadata, sub-hourly data and QC/data flags, daily data and corresponding flags, and derived metadata.
- Sites include metadata such as coordinates, altitude, soil type, land cover, and soil properties; several sites have been decommissioned over time.
- Data are stored with explicit QC and data-flag schemes, and infilling and data corrections are documented and updated via reprocessing when needed.

## Data holdings and structure

- Total files: 258
  - 1 x COSMOS-UK SiteMetadata file (COSMOS-UK_SiteMetadata_2013-2023.csv)
  - 51 x Sub-hourly hydrometeorological and soil data files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv)
  - 51 x Sub-hourly QC flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv)
  - 51 x Sub-hourly data flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv)
  - 1 x Sub-hourly metadata file (COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv)
  - 51 x Daily hydrometeorological and soil data files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv)
  - 51 x Daily data flags files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>--2023_Flags.csv)
  - 1 x Daily metadata file (COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv)
- File contents and naming conventions are described in the respective sections and linked tables.
- Access point: NERC Environmental Information Data Centre; COSMOS-UK network information at the project website.

## Sub-hourly data (30-minute resolution)

- Coverage: 2013-10 to 2023-12; 30-minute data points ending at the period, e.g., 12:30 refers to 12:00:01–12:30:00.
- Variables (site-specific): incoming/outgoing radiation (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric pressure (PA), air temperature (TA), wind (WS, WD, UX, UY, UZ), humidity (Q, RH), snow depth (SNOW_DEPTH), soil and wind components, soil heat flux (G1, G2), soil temperature and moisture (TDT#_TSOIL, TDT#_VWC, STP_TSOIL#), and supplementary derived variables (COSMOS_VWC, SWE, PE, GCC, etc.).
- Data quality: Two-stage QC
  - Automatic QC tests with unique flag values; failing data are removed and flags stored in QC_Flags files (structure mirrors data with _QCFLAG names).
  - Daily visual QC review complements automatic QC.
  - If multiple QC tests fail, their flag values are summed to a unique final QC flag per data point.
  - QC flags indicate why data were removed; data flags indicate whether a value is missing, infilled, estimated, or unchecked.
- Data flags: Separate file COSMOS-UK_<SITE>_HydroSoil_SH_..._Flags.csv with M (Missing), U (Unchecked), I (Infilled), E (Estimated). Blank cells indicate no issues.
- Derived QC notes: Net radiation (RN) and absolute humidity (Q) are not QC’d themselves because they are derived from QC’d variables.
- Data continuity: Automatic QC flags and data flags allow traceability of data quality and the exact tests contributing to any data modification.

## Daily data (derived variables and totals)

- Coverage: 2013-2023; includes daily totals/means for derived variables.
- Derived variables: VWC (volumetric water content) via CRNS (COSMOS_VWC), SWE (snow water equivalent), PE (potential evapotranspiration, FAO/Penman-Monteith), and GCC (green colour content from PhenoCam).
- Data composition: 51 daily data files and 51 daily flags, plus a daily metadata file describing variables.
- VWC and SWE methodology:
  - VWC derived from Cosmic-Ray Neutron Sensor counts with site-specific corrections ( CTS_MOD_CORR ) for atmospheric pressure, humidity, and cosmic ray intensity.
  - Correction and calibration accounts for lattice water and soil organic carbon (as per site calibrations and Desilets/Zreda frameworks).
  - A 2018 correction factor adjustment uses Jungfraujoch neutron monitor data to account for cosmic ray fluctuations.
  - D86_75m indicates the effective CRNS depth used to derive VWC at various depths.
- SWE: estimated from daily neutron counts, using albedo-based snow-day detection (10:00–14:00 GMT albedo) and a snow-free reference count to derive SWE (method described in Wallbank et al., 2020).
- PE: calculated daily by summing sub-hourly PE values (Penman-Monteith) when positive; variables used include RN, G1/G2, TA, RH, WS, PA.
- GCC: derived from PhenoCam images; daily GCC is the maximum value among up to five images per day; not quality-checked.
- Data quality: Daily data are derived from QC’d sub-hourly data; daily QC is not applied separately.

## Infilling (gap-filling)

- Purpose: Fill gaps in time series with interpolation where appropriate.
- Methods:
  - Linear interpolation or 2nd-order polynomial interpolation.
  - Gap size thresholds guide method choice; interpolation uses up to 4 surrounding values where possible.
  - RMSE-based evaluation conducted to select the best method for each variable and gap scenario.
- Process: Infilling is applied selectively to variables identified in the documentation; the approach and performance metrics are described in the infilling section.

## Completeness and data quality

- Completeness: Figure-based assessment across sites; metrics combine Met (meteorological) and Soil variables; VWC completeness is derived from CRNS data.
- Completeness indicators help assess data availability per site and variable group over the full period.
- Documentation emphasizes the importance of data governance, standardization across variables, and provenance through QC flags, data flags, and infilling records.

## Instrumentation and site variability

- Instrumentation overview (Section 7.1):
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (COSMOS_VWC, CTS_MOD_CORR, D86_75m, SWE, SNOW, ALBEDO).
  - Rain gauges: OTT Pluvio 2; tipping bucket (TBR); rain[e] sensors at several sites.
  - Soil sensors: Time Domain Transmissometry (TDT) soil moisture and soil temperature sensors at multiple depths.
  - Soil heat flux: Hukseflux HFP01SC plates.
  - Radiometer: Hukseflux NR01 (net radiation from shortwave/longwave components).
  - Meteorological suite: Rotronic and Gill MetPak-based sensors for air temperature, humidity, pressure; 3D/2D sonic anemometers for wind; PhenoCam for GCC; snow depth sensors and SnowFox for snow-derived metrics.
- Site variability (Section 7.2): Differences in site setups over time; some sites upgraded from 2D to 3D sonic anemometers; presence/absence of tipping bucket or rain[e] devices; variations between GILL MetPak and Vaisala sensors; some sites have snow sensors and full TDT arrays, others do not.
- Rain[e] height adjustment (Section 7.2.1): In 2023, rain[e] gauges were raised to 1.0 m rim height to reduce blockage by vegetation; this change affects data comparability across sites and times. The timeline of height adjustments is documented per site.

## Data updates, changes, and provenance

- Changes to data (Section 8):
  - Major reprocessing events and corrections, often affecting entire time series.
  - Examples: March 2024 daily PE data fix; site altitude metadata updates; VWC calibration updates; Hollin Hill VWC reprocessing; various sensor calibrations and 30-minute precipitation updates; midnight heat flux spike removal and infilling updates; CRNS corrections and NMDB data infilling adjustments; SWE and albedo derivations added.
  - Reprocessing ensures consistency and improved accuracy across the full timeseries.
- Data authorship and contributions (Section 9): R. Smith as primary contact; team members responsible for data management, site metadata, instrumentation, calibration, data processing algorithms, and project management.
- References (Section 10): Key methodological and calibration references for CRNS, VWC derivation, SWE estimation, PE calculation, and related radiometric and meteorological standards.

## Metadata, documentation, and access

- Site metadata file: COSMOS-UK_SiteMetadata_2013-2023.csv; includes coordinates, altitude, soil properties, land cover, and site activity status (decommissioned sites noted).
- Sub-hourly and daily metadata: CSVs describing variables, units, aggregation, infilling, and notes; includes depth-specific TDT and VWC variables, and specifics about derived variables.
- Documentation emphasizes traceability: QC flags and data flags provide a transparent record of data quality and data processing steps, enabling data stewards to document changes and maintain audit trails.
- Data are housed within the NERC Environmental Information Data Centre and are linked to the COSMOS-UK website for network context and ongoing updates.

## Practical considerations for data stewards

- Governance and standards:
  - Maintain clear metadata for all datasets, including site metadata, variable definitions, units, aggregations, and flags.
  - Preserve both QC flags and data flags to enable users to distinguish why data were removed and which data have been infilled/estimated.
  - Track reprocessing events and maintain version histories (as demonstrated by the Change to Data log).
- Data quality and interoperability:
  - Monitor completeness metrics and document site-specific data gaps, especially given site variability in instrumentation and maintenance challenges (e.g., rain[e] height changes and blockage issues).
  - Ensure consistent handling of -9999 as missing values across sub-hourly and daily files.
  - Provide guidance on interpreting derived data (VWC from CRNS with CTS_MOD_CORR, SWE estimation methods, GCC from PhenoCam) and any site-specific calibration notes.
- Accessibility and discovery:
  - Maintain and publicize detailed descriptions of data sources, instrumentation, processing steps, and change history to support data reuse.
  - Ensure alignment between raw data, QC flags, data flags, and derived products to minimize confusion for data users.
- End-of-life and decommissioning:
  - Note decommissioned sites (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest) and their impact on long-term time series continuity.