# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

## Overview
- Measurements of greenhouse gas exchange (CO2 and CH4) over a plantation forest on peat, Forsinard Flow Country, Scotland (Dyke site) during afforestation period; former blanket bog drained and afforested in the 1980s, harvested in late 2017 with perimeter drains blocked.
- Meteorological and pedological observations included; data span 2016-01-01 to 2017-12-31 at half-hourly intervals (with related notes extending to 2018-01-01 for the submission).
- Managed by the James Hutton Institute within the SCO2FLUX network; funded by NERC and RESAS; infrastructure owned by UHI; land access via RSPB.
- Aims aligned with standardised environmental monitoring: verify data quality, transform to outputs such as NEE and CH4 fluxes, and store datasets for portal access.

## Parameters
- Land-atmosphere exchange: CO2 net ecosystem exchange (NEE), CH4, atmospheric turbulence, latent and sensible heat fluxes (LE, H), net radiation.
- Meteorology and pedology: air temperature, relative humidity, air pressure, solar radiation, precipitation, soil water content, soil temperature.
- Derived outputs and related data streams: NEE_VUT, GEP, ecosystem respiration (RECO), footprint/flux partitioning metrics, PAR, VPD, flux quality flags, and gap-filled time series.

## Data format and contents
- File format: CSV.
- File naming: UK_$$$_DataProduct_%d_%m_%z.csv; site code UK_DKE; date of data product preparation.
- Core contents: half-hourly records with numerous fields, including:
  - TIMESTAMP (YYYY-MM-DD HH:mm), CH4 (nmol CH4 mol-1), CO2 (µmol CO2 mol-1).
  - Fluxes and flux-derived metrics: H (Sensible heat), LE (Latent heat), NEE and NEE_VUT variants, GPP variants, RECO variants.
  - Soil and canopy measurements: soil heat flux (G_1_1_1, G_2_1_1, G_3_1_1), soil temperature (TS_*), soil moisture, VPD, PAR, photosynthetically active radiation.
  - Radiation and meteorology: NETRAD, P_F_NS (precipitation), PA_F_NS (air pressure), PPFD_IN/PPFD_OUT, TA_F_NS, RH_F_NS, SW_IN_F_NS, etc.
  - QC and flags: H_F_MDS_QC, LE_F_MDS_QC, NEE_VUT_REF_QC, REddyProc flags, EddyPro flags, Biomet flags.
  - Gaps and missing: missing values denoted by -9999.
- Data processing notes: gap-filled using REddyProc (MDS for NEE, LE, H); longer gaps filled via alternative site data or Kinbrace Met Office data; short gaps interpolated from biomet observations.
- Mix of detailed column metadata and description blocks to aid interpretation and traceability.

## Spatial coverage
- Location: latitude 58.427254, longitude -3.96934; OS grid reference NC85090 50453.
- Site coordinates correspond to the Forsinard Reserve peatland forest area.

## Temporal coverage
- Data period: 2016-01-01 00:30 to 2018-01-01 00:00 (half-hour intervals); primary focus on 2016-2017 afforestation period with related observations.

## Data acquisition and processing
- Experimental design: eddy-covariance setup mounted on a tall mast (~18 m) above a plantation forest canopy; instruments included LI-7200 CO2/H2O analyzer, LI-7700 CH4, sonic anemometer, net radiometers, soil heat flux plates, soil sensors, and meteorological equipment.
- Instrumentation: LI-7200 (CO2/H2O), LI-7700 (CH4), Gill Windmaster Pro anemometer, Li-Cor data interface; off-grid power (solar, wind, methanol fuel cell); 4G remote data retrieval with local storage.
- Data processing: raw fluxes processed with EddyPro; gap-filled and partitioned using REddyProc (R); QC checks for outliers, stationarity, physical plausibility, and u* filtering; 2D footprint modelling (Kljun et al., 2015).
- Data integration: half-hour fluxes from EC data; meteorology and pedology sensors integrated; long-term processing and archiving performed by UKCEH with scripts in R.
- Related datasets: water table depth and soil moisture dynamics recorded but not finalised in this release; planned separate publication.

## Calibration and quality control
- Calibration: LI-7200 calibrated on 18 May 2017; other sensors not recalibrated during monitoring but assessed across Forsinard network for drift.
- Quality control framework:
  - EddyPro-based QC: standard procedures; stationarity tests; plausible value checks; angle-of-attack corrections; cross-correlation time lag removal; cospectral corrections.
  - u* filtering: fluxes excluded if u* < 0.12 m/s.
  - 2D footprint modelling for spatial representativeness.
  - Gap filling and partitioning: REddyProc (v0.8-2/r14) with Marginal Distribution Sampling (MDS) for H, LE, NEE; short gaps filled with biomet data; longer gaps via nearby towers or Kinbrace data when possible.
- Flags:
  - Biomet Flag: codes indicating raw, reviewed, calibrated, interpolated gaps, etc. (00, 01, 02, 13, 14, 22, 32, 23, 03, 04).
  - EddyPro Flag: 0 (best quality) to 2 (discard), -9999 for missing.
  - REddyProc Flag: 00 (original), 01 (most reliable), 02 (medium), 03 (least reliable), -9999 missing.
- Data products and outputs are designed for insertion into standard monitoring portals and for enabling cross-site comparisons.

## Miscellaneous
- Primary institutions and funders: NERC UK Natural Environment Research Council, RESAS Scottish Government, JHI, UHI, RSPB.
- References provided for standard methodologies and QC procedures (eddy covariance processing, gap-filling, footprint modelling, and flux partitioning).

## Reference and further information
- Dataset references and methodological guidelines cited (e.g., EddyPro, REddyProc, footprint models, quality control standards) to support reproducibility and cross-site analyses.