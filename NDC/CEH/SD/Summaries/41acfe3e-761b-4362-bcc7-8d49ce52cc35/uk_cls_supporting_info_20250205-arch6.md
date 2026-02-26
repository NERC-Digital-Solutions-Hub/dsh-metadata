# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

- Overview
  - Long-term, near-natural blanket bog site data from Flow Country, Caithness and Sutherland.
  - Measurements of greenhouse gas exchange (CO2 and CH4) and associated meteorological and pedological variables.
  - Time period: 2016-10-19 to 2023-01-01 (half-hourly intervals; data span extends through 2022 with ongoing maintenance).
  - Site operated by UKCEH/James Hutton Institute with support from RSPB, UHI, RESAS, and other funders.

- Data content and scope
  - Primary variables: land–atmosphere exchange including CO2 (NEE, GEP, RECO), CH4 (FCH4, CH4 mole fractions), and related fluxes (H, LE), net radiation, meteorology, and pedology (temperature, humidity, pressure, solar radiation, precipitation, soil moisture/temperature, soil water content, soil heat flux, water table depth).
  - Derived and auxiliary products: footprint metrics (FETCH_10/30/50/70/90/MAX), quality flags (FCH4_QC, H/LE/qc flags, NEE_VUT flags), gap-filled fluxes, and partitioning results (GPP_NT_VUT_USTAR, GPP_DT_VUT_REF, RECO_NT_VUT_REF, RECO_DT_VUT_REF, etc.).
  - Output structure includes gap-filled data and multiple partitioning approaches (daytime and nighttime partitioning; VUT/Ustar-based methods) for robust annual budgets.

- File format and naming
  - File format: CSV
  - File naming convention: UK_$$$_DataProduct.csv (site code based on Fluxnet conventions; site reference UK_CLS)
  - File contents include a comprehensive set of fields such as TIMESTAMP, CH4, CO2, FCH4, FCH4_QC, NEE, NEE_VUT_* variants, GPP_* variants, RECO_* variants, H, LE, PPFD_IN, PAR, air/soil parameters, QC flags (Biomet, EddyPro, REddyProc), and gap-filling indicators.
  - Missing values indicated by -9999

- Data fields (key categories)
  - Gas exchange and photosynthesis/respiration
    - CO2: TIMESTAMP, CH4 (mole fraction), CO2 (mole flux), NEE (net ecosystem exchange)
    - FCH4, FCH4_QC (CH4 flux and quality)
    - Partitioned values: GPP (gross primary production), RECO (ecosystem respiration)
    - NEE variants using VUT (Variable Ustar Threshold) and USTAR-based partitions
  - Fluxes and energy balance
    - H (sensible heat flux), LE (latent heat flux)
    - G (soil heat flux), plus associated QC and gap-filling indicators
  - Meteorology and environment
    - Temperature, humidity, pressure, solar radiation, net radiation, PPFD, precipitation, soil moisture/temperature
    - Footprint metrics, wind-related variables (USTAR, U_SIGMA, VPD, RH, PAR, etc.)
  - Data processing and QC
    - Biomet Flag, EddyPro Flag, REddyProc Flag with defined coding (0 best, higher values less reliable; -9999 missing)
    - Gap-filling indicators (PA_F_NS, P_F_NS, etc.)
    - QC-related metadata for each field
  - Reference and metadata
    - Experimental design and instrumentation details
    - Calibration notes and instrumentation changes (e.g., IRGASON replacement/calibration in 2019; soil heat flux sensor changes in 2019)
    - Processing workflow: raw data → EddyPRO processing → REddyProc gap-filling and partitioning

- Spatial coverage
  - Location: latitude 58.371598, longitude -3.965194
  - OS grid reference: NC 85220 44146
  - Spatial resolution: point measurements (single flux tower footprint)

- Temporal coverage
  - Observations span 2016-10-19 00:30:00 to 2023-01-01 00:00
  - Data are collected at high frequency (eddy covariance at 10 Hz; met/pedology at 5 s; half-hourly aggregations)

- Experimental design and data collection
  - Equipment mounted on ~3 m tripod masts on an undisturbed blanket bog
  - Eddy covariance setup: IRGASON for CO2/H2O, LI-7700 CH4; sonic anemometer; net radiometer; soil sensors; all powered off-grid
  - Data retrieval: remote 4G; monthly site visits; automated processing and archiving
  - Processing workflow: raw data processed with EddyPRO v7.0.6; QC including outlier screening, stationarity checks, range checks, u* filtering; 2D footprint modeling
  - Gap filling and partitioning with REddyProc; H/LE/NEE gap-filled via marginal distribution sampling (MDS)
  - Short gaps interpolated using biomet data; longer gaps filled from nearby sites or station data (kinbrace, Met Office)

- Calibration and quality control
  - IRGASON recalibrated in 2019; no significant deviations, but no recalibration within the dataset period due to Covid
  - Soil heat flux sensors expanded from 1 to 5 sensors in 2019; time series represent averages across sensors post-2019
  - QA procedures include:
    - Outlier removal and physics-based screening
    - Stationarity tests and flux range checks
    - u* threshold exclusion for CO2 flux
    - 2D footprint calculation
    - Gap-filling and partitioning with REddyProc; QC flags track data reliability
  - Flags:
    - Biomet Flag: 00, 01, 02, 13, 14, 22, 32, 23, 03, 04
    - EddyPro Flag: 0 (best) to 2 (discard) and -9999 for missing
    - REddyProc Flag: 0 original, 1 most reliable, 2 medium, 3 least reliable, -9999 missing

- Data provenance and references
  - Documentation and references include standard micrometeorological quality control practices and key literature (e.g., Mauder et al., Reichstein et al., Moncrieff et al.)
  - Data provenance supported by UKCEH network processing and UK Met Office/Kinbrace references
  - Supporting institutions: NERC, RESAS, JHI, UHI, RSPB

- Practical notes for data support
  - File contains comprehensive QC and gap-filled data suitable for annual budgets and cross-site comparisons
  - Important to account for flag semantics when filtering data for analyses
  - Calibration history and sensor changes may influence long-term trend interpretation; consider 2019 sensor updates in analyses
  - Data are suitable for self-serve exploration, dashboards, and reproducible analyses with documented processing steps (EddyPRO, REddyProc)