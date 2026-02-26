# Carbon dioxide and methane fluxes and associated environmental observations from an unmodified blanket bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2022

- Purpose and scope
  - Long-term, near-natural blanket bog site in the Flow Country, Caithness and Sutherland, Scotland.
  - Provides measurements of greenhouse gas exchange (CO2 and CH4) plus associated meteorological and pedological observations to monitor environmental health and policy-relevant performance over time.
  - Supports assessment of target state observations at nearby restored/restored-from-plantation sites; site data contribute to the SCO2FLUX network.

- Data content and key parameters
  - Gas exchange and fluxes
    - CO2: net ecosystem exchange (NEE) and related fluxes; partitioning into gross primary production (GPP) and ecosystem respiration (RECO) under various methods (daytime/nighttime partitioning, VUT/USTAR-based approaches).
    - CH4: methane flux (FCH4) and CH4 mole fraction observations.
    - Derived flux components and quality flags (e.g., NEE_VUT_REF, NEE_VUT_USTAR05/50/95, RECO_VUT, RECO_NT_VUT, etc.).
    - Evapotranspiration (ET); sensible heat flux (H); latent heat flux (LE); net radiation (Rg, SW_IN, PPFD, etc.).
  - Microclimate and pedology
    - Air temperature, relative humidity, barometric pressure, solar radiation, precipitation, soil moisture content, soil temperature, soil heat flux, water table depth.
    - Footprint metrics (FETCH_10, FETCH_30, FETCH_50, FETCH_70, FETCH_90, FETCH_MAX) and stability parameter (ZL).
  - Instrumentation and data quality
    - Turbulence and energy flux measurements ( eddy covariance with IRGASON; CH4 with LI-7700; sonic anemometer).
    - Net radiometer and long/shortwave components; soil and meteorological sensors.
    - Quality flags: Biomet Flag, EddyPro Flag, REddyProc Flag; gap-filling and uncertainty metrics (RANDOMUNC, QC, etc.).

- File structure and contents
  - Format: CSV data files.
  - File naming: UK_$$$_DataProduct.csv, where $$$ is a site reference code; site reference UK_CLS.
  - Data elements include: TIMESTAMP (YYYY-MM-DD HH:mm; end time of half-hour period), CH4 (nmol CH4 mol-1), CO2 (µmol CO2 m-2 s-1), ET (mm), FCH4 and FCH4_QC, and a wide range of derived and auxiliary variables (G, GPP_DT_VUT_REF, GPP_NT_VUT_REF, NEE, NEE_VUT_REF, NEE_VUT_USTARXX, RECO, LE, H, PPFD_IN, TA_F_NS, RH_F_NS, VPD_F_NS, USTAR, WS, WD, etc.).
  - Missing values are indicated by -9999.
  - Documentation sections cover file format, naming conventions, file contents, missing values, metadata flags, and data processing steps.

- Spatial and temporal coverage
  - Spatial: point measurement located at 58.371598, -3.965194 (OS grid NC 85220 44146).
  - Temporal: 2016-10-19 00:30:00 to 2023-01-01 00:00 (30-minute intervals for the primary dataset; high-frequency data at 10 Hz for eddy covariance measurements).

- Data acquisition, processing, and calibration
  - Hardware and setup
    - Instrumentation mounted on tripod masts ~3 m above surface; largely pristine blanket bog with typical pool systems; minimal direct human intervention beyond light deer grazing.
    - Datalogger: Campbell Scientific CR3000; modem: Sierra Wireless RV50X.
    - Gas exchange: IRGASON for CO2/H2O; LI-7700 for CH4; sonic anemometer for turbulence; net radiometer (Kipp&Zonen); PPFD (Skye Instruments); soil sensors (CS616, 105T); soil heat flux (HFP01); water table sensors (Druck).
  - Data collection and processing
    - Eddy covariance data captured at 10 Hz; half-hour aggregated fluxes computed using EddyPro; data retrieved via 4G or site visits; REddyProc used for gap-filling and partitioning.
    - Pre-processing includes quality control, two-dimensional footprint corrections, time lag corrections, and cospectral attenuation corrections.
    - Gap-filling methods: marginal distribution sampling (MDS) for H, LE, NEE; NEE partitioning and MEF-based selection of GPP/RECO versions.
    - Biomet data gap-filled and flagged (Biomet Flag); EddyPro and REddyProc quality flags accompany outputs.
  - Calibration and sensor notes
    - Site refurbished in 2016; IRGASON recalibrated in 2019; some sensors not recalibrated during the Covid period.
    - Soil heat flux sensor changes in 2019 (addition of new plates; time series represent averages across all sensors installed from Aug 2019).
    - CO2 storage considered negligible at observation height; CO2 flux sign convention follows micrometeorological standards (positive from ecosystem to atmosphere).
  - Data processing and quality control (QC)
    - Flux data screened for outliers, physically implausible values, and stationarity issues; fluxes excluded when low turbulent mixing (u*) thresholds not met; 2D footprint model applied.
    - Specific QC: H, LE, NEE gap-filled with REddyProc; short gaps interpolated; longer gaps filled using co-located or nearby station data; PAR, precipitation, and other biomet variables gap-filled with established approaches.
    - QC flags:
      - Biomet Flag values indicate data review/calibration status and data origin (raw, reviewed, calibrated, interpolated gap, etc.).
      - EddyPro Flag values range from best quality (0) to data suitable for general use (1) to discard (2), with -9999 for missing values.
      - REddyProc Flag values indicate data reliability for gap-filled outputs (0 original, 1 most reliable, 2 medium, 3 least reliable, -9999 missing).
  - Limitations and notes
    - Soil moisture data currently under review; final dataset to be released separately.
    - Some sensors changed or upgraded at refurbishment; data continuity carefully annotated.
    - CO2 flux partitioning relies on established methodologies; MEF-based sensitivity used for selecting GPP/RECO estimates.
  
- Access, reuse, and stewardship
  - Part of UKCEH monitoring networks; data are processed and archived through UKCEH workflows.
  - Raw and processed data support long-term environmental monitoring, enabling cross-site comparisons and integration with other datasets to enhance value (e.g., combining with nearby sites or restoration projects).
  - The dataset is designed to be stored and uploaded to appropriate data portals, supporting reuse and policy-monitoring analyses.

- References and methodology foundations
  - Core methodological references include standard eddy covariance processing and QC frameworks, REddyProc gap-filling and partitioning approaches, and footprint analysis methods.
  - Key sources cited in the dataset documentation cover quality control, data processing pipelines, and site-specific calibration notes.