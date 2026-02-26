# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

- Overview
  - Measurements of greenhouse gas exchange (CO2 and CH4) over a plantation forest on peat bog at Forsinard Flows, Flow Country, Scotland.
  - Site: Dyke, on RSPB Forsinard Reserve; former blanket bog drained and afforested in the 1980s with non-native conifers; harvested in late 2017 with perimeter drains blocked.
  - Temporal scope: meteorological and pedological observations for 2016-01-01 to 2017-12-31 (half-hourly intervals); dataset represents data from the afforestation period.
  - Management and funding: originally set up by UHI with JHI and RSPB, currently managed by the James Hutton Institute as part of the SCO2FLUX network; funded by NERC and RESAS.

- Dataset scope and variables
  - Land-atmosphere exchange metrics: net ecosystem exchange (NEE) of CO2, CH4 fluxes, atmospheric turbulence, latent and sensible heat fluxes (LE and H), net radiation.
  - Meteorology and pedology: air temperature, relative humidity, air pressure, solar radiation, precipitation, soil water content, soil temperature.
  - Derived/related fluxes and diagnostics: GPP (gross primary production) estimates, RECO (ecosystem respiration), various NEE variants (e.g., NEE_VUT_REF, NEE_VUT_USTAR05/50/95), and related quality flags.
  - Data gaps and quality flags accompany many parameters.

- Data formats and file structure
  - File format: CSV.
  - File naming convention: UK_$$$_DataProduct_%d_%m_%z.csv, where $$$ is the Fluxnet-based site code (UK_DKE) and %d_%m_%z encodes the preparation date.
  - Data columns include: TIMESTAMP (YYYY-MM-DD HH:mm), CH4, CO2, various soil heat flux terms (G_...), H, LE, NEE and multiple NEE variants, NETRAD, precipitation, pressure, PPFD, RH, SW_IN, TA, TS, VPD, WD, WS, etc.
  - Missing values are indicated by -9999.

- Spatial and temporal coverage
  - Location: latitude 58.427254, longitude -3.96934 (OS grid NC85090 50453).
  - Temporal coverage: 2016-01-01 00:30 to 2018-01-01 00:00 (dataset notes include 2016–2017 observations with end-of-2017 data; some elements reference 2018 end).

- Data collection and processing
  - Methodology: eddy-covariance measurements for gas and energy exchanges; turbulence measured with a Gill Windmaster Pro; CO2/H2O with Licor LI-7200; methane with LICOR LI-7700.
  - Instrumentation: tall mast (~18 m sensing height), data loggers (Sutron 9210), remote retrieval via 4G; sensors for air temperature, humidity, solar radiation, net radiation, soil heat flux, soil temperature, and soil moisture.
  - Processing: raw data processed with EddyPRO for flux calculations; gap-filling and partitioning performed with REddyProc in R; gap-filling for H, LE, and NEE using marginal distribution sampling (MDS); short gaps filled by interpolation; longer gaps filled using co-located instruments or nearby stations.
  - Calibration: LI-7200 calibrated on 18/05/2017; other sensors generally not recalibrated during the monitoring period but validated against network data.
  - Data resolution: fluxes computed at 30-minute intervals; raw EC data at 10 Hz; met and ped data at 10 s intervals; half-hourly summaries stored.

- Calibration, quality control, and data flags
  - Quality control: standard procedures include outlier screening, stationarity checks, and physical range checks; 2D footprint modeling; u* threshold filtering (u* < 0.12 m/s leads to exclusion).
  - Flags
    - Biomet Flag: codes for data quality of biomet variables (e.g., 00 raw, 01 reviewed, 02 calibrated, 13 interpolated gap, 32 modelled, 03 no data, 04 removed faulty, etc.).
    - EddyPro Flag: 0 best quality, 1 suitable for general analysis, 2 should be discarded, -9999 missing.
    - REddyProc Flag: 00 original, 01 most reliable, 02 medium, 03 least reliable, -9999 missing.
  - Gap-filling and partitioning: NEE gap-filled and partitioned into GEP and RE using REddyProc; NEE variants (USTAR-based and VUT-based) computed with model efficiency (MEF) evaluations and repeated across time aggregations.
  - Additional QC details: checks for airflow, cospectral corrections, time-lag removal, footprint estimation, and handling of missing/biomet gapfilled data.

- Data access and provenance
  - Networks and stewardship: UKCEH processing network; part of the SCO2FLUX collaboration; land access provided by RSPB; field operations supported by UHI and James Hutton Institute.
  - Funding and affiliations: NERC (NE/V01854X/1, 'MOTHERSHIP', 2022-2027) and RESAS (CentrePeat, 2022-2027) support to process earlier data; affiliations include UHI, JHI, RSPB, and UKCEH.

- Use cases and considerations for analysts
  - Suitable for investigating carbon balance dynamics in afforested peatlands, evaluating CO2 and CH4 fluxes, energy balance components, and responses to restoration strategies.
  - Enables regional or cross-site comparisons within the Flow Country peatlands and related SCO2FLUX datasets.
  - Consider data limitations: localized scale, potential calibration drift for some sensors, data gaps requiring gap-filling; interpretation should account for flag statuses and the MEF-based MEF selections across time aggregations.