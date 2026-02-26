# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

- Purpose and scope
  - Long-term dataset of greenhouse gas exchange (CO2 and CH4) plus associated meteorological and pedological observations from a near-natural blanket bog in Caithness and Sutherland, Scotland.
  - Site maintained within the SCO2FLUX network; used to assess observations at nearby sites and to support peatbog restoration context.
  - Managed by The James Hutton Institute with support from UKCEH, NERC, RESAS, and partners; UHI provides on-site operational support; RSPB grants land access.

- Data coverage and location
  - Temporal coverage: 2016-10-19 to 2023-01-01 (near-continuous half-hourly data; dataset described as 2016-2022 in overview but temporal range includes 2023-01-01 in file contents).
  - Spatial coverage: Forsinard Flows blanket bog, Flow Country; coordinates 58.371598 N, -3.965194 W (OS grid NC 85220 44146); point-based flux measurement site.
  - Site characteristics: small, flat bog with natural pool systems; little direct management beyond light to medium red deer grazing.

- Data types and parameters
  - Gas exchange: CO2 flux (NEE) and CH4 exchange (FCH4) with half-hourly and derived fluxes; CO2 and CH4 mole fractions; evapotranspiration (ET).
  - Turbulence and energy balance: friction velocity (USTAR), sensible heat (H), latent heat (LE), net radiation, soil heat flux (G), air temperature, humidity, radiation components, precipitation, soil moisture (under review for final dataset).
  - Derived/budget products: Gross Primary Production (GPP) estimates (DT_VUT and NT_VUT variants), ecosystem respiration (RECO) estimates, partitioned NEE_VUT and related QC variants; footprint information (FETCH_10 to FETCH_90, FETCH_MAX); several quality-control and gap-filled variables (H_F_MDS, LE_F_MDS, NEE_VUT_* QC, RANDUNC metrics, qcs for NEE and energy fluxes).

- File format and data structure
  - Format: CSV.
  - File naming: UK_$$$_DataProduct.csv where $$$ is a Fluxnet site reference code; site reference for Forsinard is UK_CLS.
  - File contents: columns include TIMESTAMP (YYYY-MM-DD HH:mm), CH4 and CO2 measurements, ET, fluxes (FCH4, NEE, G, H, LE, etc.), footprints (FETCH_*), quality flags (Biomet Flag, EddyPro Flag, REddyProc Flag), gap-filled indicators, and various meteorological/biometric metrics (PPFD_IN, PAR, TA_F_NS, RH_F_NS, VPD_F_NS, etc.).
  - Missing values indicated by -9999.

- Data collection and processing
  - Instrumentation: eddy-covariance system with a Campbell Scientific CR3000 data logger; IRGASON for CO2/H2O and turbulence; LI-7700 for CH4; net radiometer (Kipp & Zonen); additional sensors for meteorology and pedology; 4G data retrieval with on-site occasional visits.
  - Sampling: 10 Hz data for eddy-covariance measurements; met/pedo sensors sample every 5 s; half-hourly values stored for retrieval.
  - Processing workflow: raw data processed with EddyPro; QC applied; time lags removed; gap-filling and partitioning performed with REddyProc; gap-filling of H, LE, NEE via marginal distribution sampling (MDS); longer gaps filled with co-located/instrument data or nearby station data.
  - Documentation and lineage: processing scripts and QC steps follow UKCEH network standards; 30-minute flux products generated from raw data; metadata includes extensive flagging and methodological notes.

- Calibration, maintenance, and provenance
  - Calibration: IRGASON calibrated in 2019; other sensors regularly checked for drift against co-located instruments or nearby sites; Covid-related disruption prevented recalibration within the dataset window.
  - Sensor changes: 2016 refurbishment; 2019 change from single to multiple soil heat flux plates with updated logging; soil heat flux time series represents an average across five sensors post-installation.
  - Field/operational context: equipment mounted ~3 m above surface on tripod masts; off-grid power system; long-term site operation with ongoing maintenance and periodic refurbishments.

- Quality control and data quality flags
  - Biomet Flag: indicates gap-filled biomet parameters with codes such as 00 raw, 01 primary reviewed, 02 calibrated, 13/14 interpolated gap with various exceptions, 32 modelled data, 23 interpolation from alternate site, 03 no data, 04 removed faulty data.
  - EddyPro Flag: quality flag for flux data (0 best quality, 1 suitable for general analyses like annual budgets, 2 fluxes to be discarded; -9999 missing).
  - REddyProc Flag: quality flag for gap-filling and partitioning (0 original data, 1 most reliable, 2 medium, 3 least reliable, -9999 missing).
  - Additional QC filters: stationarity tests, physical plausibility ranges for H, NEE, LE; low turbulence periods identified via u* thresholds; 2D footprint modeling to assess source area; gap-filling and partitioning methods clearly documented.

- Governance, storage, and updates
  - Dataset is part of a larger environmental network and is intended for discovery and reuse by data users, with clear provenance from field deployment to processing pipelines.
  - Data are stored and archived following UKCEH practices; ongoing maintenance and updates are implied, with recognition that soil moisture data are under review for final publication.

- References and context
  - Numerous peer-reviewed sources and standard methodologies underpin data processing and QC (EddyPro, REddyProc, flux foot-print modeling, stationarity and cospectral corrections, u* filtering, etc.).
  - Supporting projects and collaborations include NERC, RESAS, JHI, UHI, RSPB, and Fluxnet conventions.

- Notes for data stewardship and reuse
  - Ensure metadata remains aligned with workflows (EddyPro, REddyProc, MDS gap-filling) and flag semantics are preserved for downstream analyses.
  - Acknowledge potential calibration gaps (IRGASON calibration 2019, Covid-related delays) and sensor change impacts (soil heat flux sensor update in 2019) when interpreting long-term trends.
  - Be aware of ongoing data quality considerations for soil moisture and gap-filled products; verify flag values and handling of -9999 missing values in analyses.