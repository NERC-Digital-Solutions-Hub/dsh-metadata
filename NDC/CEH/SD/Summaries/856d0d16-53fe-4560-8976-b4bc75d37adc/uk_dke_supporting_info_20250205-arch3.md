# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

- Purpose and context
  - Dataset of greenhouse gas exchange (CO2 and CH4) from a plantation forest on peat bog, covering afforestation 1980s to 2017 with perimeter drains blocked.
  - Associated meteorological and pedological measurements included for 2016-01-01 to 2017-12-31 at half-hourly intervals.
  - Originally established by UHI with JHI and RSPB; managed by the James Hutton Institute within SCO2FLUX; funded by NERC and RESAS; UHI retained infrastructure and site access support.

- What is measured
  - Land-atmosphere exchange metrics: net ecosystem exchange (NEE) for CO2, CH4 fluxes, atmospheric turbulence, latent and sensible heat fluxes (LE, H), net radiation, and basic meteorology (temperature, humidity, pressure, solar radiation, precipitation) plus pedology (soil water content and soil temperature).

- Data format and structure
  - File format: CSV.
  - File naming: UK_$$$_DataProduct_%d_%m_%z.csv, with site code UK_DKE and date of data product preparation.
  - File contents include TIMESTAMP and extensive flux and meteorological variables, plus quality flags and gap-filling information.
  - Missing values are encoded as -9999.

- Spatial and temporal coverage
  - Location: latitude 58.427254, longitude -3.96934 (OS grid NC85090 50453).
  - Temporal coverage: 2016-01-01 00:30 to 2018-01-01 00:00.

- Experimental design and data collection
  - Eddy-covariance setup on a 20 m mast over the plantation, sensors ~2 m above canopy.
  - Instruments: LI-7200 for CO2/H2O, LI-7700 for CH4, sonic anemometer, net radiometer, soil heat flux plates, soil temperature sensors, soil moisture probes, PAR sensors, wind sensors, and met stations.
  - Data collection: EC data at 10 Hz; met/ped sensors at 10 s; half-hour aggregates stored for retrieval.
  - Power: off-grid system (solar, methanol fuel-cell, wind); data retrieved via 4G or site visits.

- Data processing and gap-filling
  - Primary processing with EddyPRO for standard corrections and quality control.
  - REddyProc used to gap-fill CO2 fluxes and partition NEE into GEP and respiration.
  - Gap-filling for H, LE, NEE via marginal distribution sampling (MDS); short gaps interpolated from biomet observations; longer gaps filled using nearby sites or Kinbrace Met Office data when needed.

- Quality control and data flags
  - Quality control includes outlier screening, stationarity checks, plausible flux ranges, and u* filtering; 2D footprint modeling applied.
  - Flags:
    - Biomet Flag: 00, 01, 02, 13, 14, 22, 32, 23, 03, 04 indicating data review, calibration, gap interpolation, or removal.
    - EddyPro Flag: 0 (best quality) to 2 (discard) and -9999 for missing.
    - REddyProc Flag: 00 (original) to 03 (least reliable) and -9999 for missing.
  - Missing values indicated as -9999.

- Calibration and validation
  - LI-7200 calibration performed on 18/05/2017; other sensors not recalibrated during the monitoring window but assessed across Forsinard sites for drift and faults.

- Data governance and references
  - Part of UKCEH network data processing; processing and QC follow established micrometeorological standards and citations.
  - References underpinning methods include EddyPro, REddyProc, and standard flux-quality protocols; collaborative acknowledgments include NERC, RESAS, JHI, UHI, RSPB, and UKCEH.