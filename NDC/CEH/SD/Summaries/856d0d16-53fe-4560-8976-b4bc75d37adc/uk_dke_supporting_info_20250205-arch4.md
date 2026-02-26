# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

## Executive snapshot
- A half-hourly time-series dataset of greenhouse gas exchange (CO2 and CH4) from a plantation forest on peat bog at Forsinard Flow Country, Scotland, covering 2016-01-01 to 2017-12-31 (with related data up to 2018-01-01 in the file). Includes meteorological and pedological measurements.
- Data processing and quality control follow a standardized eddy-covariance workflow (EddyPro, REddyProc) with gap-filling, flux partitioning, and multiple quality flags. Managed and processed within the SCO2FLUX network and UKCEH framework.

## What data are included
- Gas exchange measurements: CO2 and CH4 fluxes (net ecosystem exchange, NEE; CH4 flux) and related turbulence metrics, heat fluxes (H), latent heat flux (LE), and net radiation.
- Meteorological and pedological measurements: air temperature, relative humidity, barometric pressure, solar radiation, precipitation, soil water content, soil temperature, etc.
- Temporal resolution: half-hourly intervals; dataset spans 2016-01-01 to 2017-12-31 (with metadata extending to 2018-01-01).
- Location: Forsinard Reserve, Flow Country, Caithness and Sutherland, Scotland.

## File format and naming
- Format: CSV
- Naming convention: UK_$$$_DataProduct_%d_%m_%z.csv with $$$ as site code UK_DKE and %d_%m_%z representing submission date in R format.

## File contents (key variables and structure)
- Core fluxes and diagnostics: TIMESTAMP (YYYY-MM-DD HH:mm), CH4, CO2, GPP-related terms, NEE, H, LE, NETRAD, and multiple NEE/RECO/partitioning variants (e.g., NEE_VUT_REF, NEE_VUT_USTARxx, RECO_NT_VUT_REF, RECO_NT_VUT_US...).
- Gap-filled and quality-controlled data: LE_F_MDS, H_F_MDS, NEE_VUT_REF, NEE_VUT_USTARxx, RECO_NT_VUT_REF, RECO_NT_VUT_USTARxx, along with corresponding QC flags (e.g., H_F_MDS_QC, LE_F_MDS_QC, NEE_VUT_REF_QC, RECO_NT_VUT_REF_QC, etc.).
- Additional biomet placeholder/auxiliary fields: precipitation (P_F_NS), air pressure (PA_F_NS), PAR (PPFD_IN, PPFD_IN_F_NS, PPFD_OUT), RH, Ta, soil temperatures (TS_1_1_1, TS_2_1_1, TS_3_1_1, TS_AVG), VPD, WD/WS, and auxiliary flags (VPD_F_MDS_QC, NEE_VUT_USTARxx_QC, etc.).
- Missing values indicator: -9999.

## Spatial coverage
- Latitude/Longitude: 58.427254, -3.96934
- OS grid reference: NC85090 50453
- Site mast details: tower at ~18 m height over canopy; measurements collected atop a 20 m mast with data from ~2016-05-11 to 2017-10-18.

## Temporal coverage
- Primary data period: 2016-01-01 00:30 to 2018-01-01 00:00
- Project timeframe includes 2016-2017 afforestation period and related environmental observations.

## Data collection, generation, and transformation
- Instrumentation:
  - Eddy-covariance setup: Gill Windmaster Pro sonic anemometer; Licor LI-7200 enclosed-path CO2/H2O gas analyzer; LI-7700 open-path CH4 analyzer.
  - Net radiometer (Kipp & Zonen), soil heat flux plates, soil temperature and moisture sensors, PAR sensors, meteorological suite (Li-Cor/ Vaisala instruments), water table monitoring.
  - Datalogger: Sutron 9210; data retrieved via 4G and during site visits.
- Sampling and processing:
  - Turbulence data at 10 Hz; half-hourly aggregated fluxes processed with EddyPRO (v7.0.6) and QC as per micrometeorology best practices.
  - Gap-filling and partitioning performed with REddyProc (v0.8-2/r14) using marginal distribution sampling for H/LE/NEE; NEE partitioning and VUT (variable U-star threshold) methods applied with MEF-based year selection.
  - Calibration: LI-7200 calibrated on 18/05/2017; other sensors not calibrated during the monitoring period but reviewed across Forsinard network for drift.
  - Longer gaps in air temperature, humidity, and solar radiation filled using nearby instruments, nearby EC towers, or Kinbrace Met Office data.

## Quality control and data quality flags
- Processing workflow: UKCEH data processing with standard QC; outlier detection (median absolute deviation), stationarity checks, and bounds on flux values (e.g., H, LE, NEE ranges).
- u* filtering used to exclude periods with low turbulent mixing (u* < 0.12 m/s).
- Footprint filtering (2D footprint) and other standard corrections (cospectral attenuation, warm/cold flux corrections, density corrections).
- Gap-filling: REddyProc-based; MDS for gap-filled parameters with accompanying quality flags:
  - Biomet Flag (e.g., 00 raw, 01 primary reviewed, 02 calibrated, 13 interpolated gap, etc.)
  - EddyPro Flag: 0 best quality; 1 suitable for general analysis; 2 to discard; -9999 missing
  - REddyProc Flag: 00 original; 01 most reliable; 02 medium; 03 least reliable; -9999 missing
- Notes: biomet, eddy-covariance, and REddyProc flags accompany data rows to indicate reliability and suitability for various analyses (annual budgets, site-level comparisons, etc.).

## Data governance, provenance, and references
- Project and data stewardship:
  - Site managed by James Hutton Institute (Aberdeen) within SCO2FLUX network; ownership of infrastructure by UHI; land access via RSPB Forsinard.
  - Data processing and archiving performed by UKCEH; funding from NERC (MOTHERSHIP) and RESAS for related projects; ongoing collaboration with JHI, UHI, and RSPB.
- Processing tools and standards:
  - Eddy capture and QC with EddyPRO (Fratini & Mauder; Mauder et al.) and standard micrometeorology QC tests.
  - Gap-filling and partitioning with REddyProc (Reichstein et al.; Reichstein et al. 2016).
- References and methodological notes included in dataset documentation (e.g., key micrometeorology QC standards, footprint modeling, and published methodological papers).

## Additional notes for data users (parents of the data system perspective)
- The dataset is designed to provide a comprehensive, traceable data product for carbon and greenhouse gas flux analysis, with explicit metadata, QC flags, and multiple NEE/partitioning variants to support robust analysis and cross-study comparability.
- Data gaps and calibration status are clearly indicated; some sensors were not calibrated during the monitoring period and may require cross-site calibration checks for long-term trend analysis.
- Longer-term data products (e.g., soil moisture dynamics) are mentioned as undergoing review and may be published separately.