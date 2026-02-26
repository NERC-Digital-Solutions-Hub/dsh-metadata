# Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]

- Overview
  - A comprehensive COSMOS-UK time series dataset of hydrometeorological and soil moisture data from 50 sites, spanning Oct 2013 to Dec 2018.
  - Includes sub-hourly (30-minute) and hourly data, plus daily aggregates, with derived volumetric water content (VWC), snow metrics, and evapotranspiration estimates.
  - Data organized into multiple file types, plus site metadata, to support data discovery, quality control, and reuse.

- Data Content and Structure
  - Files and data types (201 total files):
    - COSMOS-UK_SiteMetadata_2013-2018.csv: site metadata (location, soil type, land cover, etc.).
    - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv: sub-hourly hydromet and soil data (30-min resolution) per site.
    - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv: QC flags for sub-hourly data (per-site, same structure with _QCFLAG suffix).
    - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv: hourly data, including VWC (COSMOS_VWC) and related variables.
    - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv: daily data, including VWC (COSMOS_VWC), D86_75m, Potential Evapotranspiration (PE), and Snow Water Equivalent (SWE).
  - Common data conventions:
    - Missing values denoted by -9999 for numeric fields.
    - SITE_ID identifies the COSMOS-UK site; timestamps are end-of-interval for sub-hourly data; and daily data use 00:00 GMT for the day start.
  - Key variables by data type:
    - Sub-hourly (SH): radiation components (LWIN, LWOUT, SWIN, SWOUT, RN), Precipitation (PRECIP), atmospheric variables (PA, TA, RH, Q), wind (WS, WD, UX/UY/UZ), snow depth (SNOWD_DISTANCE_COR), soil temperature/VWC at multiple TDT depths, soil heat flux (G1/G2), and related sensor outputs.
    - Hourly: corrected cosmic-ray neutron counts (CTS_MOD_CORR), COSMOS_VWC (soil moisture), D86_75m ( derived metric).
    - Daily: COSMOS_VWC (daily average), D86_75m (daily), PE (Penman-Monteith), SWE (midday), SNOW (snow day flag), ALBEDO (10:00–14:00 window).

- Data Processing, Quality Control, and Provenance
  - Data workflow:
    - Instruments on site feed loggers; data telemetered to CEH Wallingford hourly.
    - Two-stage QC:
      - Automatic QC tests implemented by a processing script; failing data are flagged and removed.
      - Daily visual inspection via plots for quick review.
    - QC flags: per-parameter tests yield unique flags; combined flags indicate exact tests failed; failing values are removed and flags saved in site-specific QC files.
  - Quality control tests (examples):
    - Zero data, Too few samples, Low power, Sensor fault, Diagnostic flag, Out of range, Secondary variable, Spike, and Error codes.
    - Each variable has a defined subset of tests applied; the QC flag values sum to a unique final value for traceability.
  - Data derivation details:
    - VWC from cosmic-ray neutron sensor (CRNS) using corrected counts (adjusted for background cosmic rays, altitude, atmospheric pressure, absolute humidity).
    - VWC derivation uses one of three methods; COSMOS-UK employs the site-specific N0 calibration method with a silica-soil matrix assumption and corrections for lattice water and soil organic carbon.
    - 2018 correction added: site-specific gamma factor to adjust for geomagnetic effects; reprocessed to remove spurious trends.
    - Daily VWC (D-VWC) computed as daily averages of hour- or 30-minute corrected counts; D86_75m derived from hourly/daily VWC as described in referenced literature.
    - SWE estimation uses albedo-based snow days (thresholds 50% for start, 35% for end) and a snow-free count rate to compute SWE (Method 1, Wallbank et al. 2020).
    - PE computed via Penman-Monteith using RN, G (mean of G1+G2), TA, RH, WS, and PA; negative sub-hourly values are ignored for daily totals.
  - Instrumentation and site variation:
    - Documentation provides detailed instrumentation (CRNS, rain gauges, TDT soil moisture sensors, soil heat flux plates, soil thermistors, radiometers, weather stations, anemometers, snow sensors, micrologger).
    - Not all instruments are installed at every site; Section 7 and Table 7.1 describe site-specific instrument configurations and exceptions.

- Completeness and Coverage
  - Site coverage: data from 50 COSMOS-UK sites (2013–2018).
  - Completeness indicators:
    - Section 6 presents per-site completeness for combined Met (meteorology) and Soil variables, with separate completeness for VWC data from CRNS.
    - Data gaps arise from instrument absence, decommissioned sites (e.g., Wytham Woods ended 01/10/2016), and variable data quality across sites.
  - Data quality and gaps:
    - Sub-hourly and hourly datasets include flagged and removed values when QC tests fail.
    - Some parameters are not available at all sites or at all depths/times due to instrumentation layout.

- Access, Reuse, and Versioning
  - Data governance and access:
    - COSMOS-UK data and supporting documentation are hosted by CEH and the NERC Environmental Information Data Centre; project website at https://cosmos.ceh.ac.uk/.
  - Versioning and updates:
    - The dataset undergoes periodic reprocessing when improvements are implemented; notable changes include recalibration of VWC, CRNS count infilling, NMDB data infilling, improvements to PE, and SWE/albedo updates (with specific dates in Changes to data).
  - Usage notes for data leaders:
    - Data are suitable for long-term hydrometeorological and soil moisture analyses, model calibration/validation, and multi-site comparative studies.
    - Be aware of potential biases on snow days, site-specific calibration, and site-by-site instrument configurations when aggregating or comparing across sites.

- Author Contributions and References
  - Author contributions: S. Stanley as primary author; dedicated data managers and calibration/maintenance teams; project management and metadata responsibilities distributed among listed contributors.
  - References cover calibration methods, CRNS methodology, and standard hydrological estimation techniques (e.g., Penman-Monteith, soil moisture calibration approaches, and CRNS processing literature).