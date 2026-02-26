# Carbon dioxide and methane fluxes and associated environmental observations during use as plantation forest on peat bog, Forsinard Flows RSPB Reserve, Scotland, 2016-2017

- The dataset contains half-hourly measurements of greenhouse gas exchange (CO2 and CH4) and related meteorological and pedological observations from a plantation forest on peat bog at Forsinard Flow Country, Scotland.
- Focus is on the afforestation period (1980s planting and restoration activities) at the Dyke site, with data managed under the SCO2FLUX network and supported by NERC and RESAS funding.
- Data processing and quality control follow established eddy-covariance workflows (EddyPro for flux processing; REddyProc for gap-filling and flux partitioning).

## Spatial and temporal coverage

- Spatial location: latitude 58.427254, longitude -3.96934 (OS grid ref NC85090 50453); canopy height measurements reference height ~18 m.
- Spatial context: site on RSPB Forsinard Reserve, Flow Country, Caithness and Sutherland, Scotland.
- Temporal coverage: 2016-01-01 00:30 to 2018-01-01 00:00 (measurements primarily 2016-01-01 to 2017-12-31; output may extend to 2018-01-01 due to processing).
- Deployment details: tall mast (~20 m) with sensors at ~18 m above canopy; eddy-covariance setup includes LI-7200 CO2/H2O analyser, LI-7700 CH4 analyser, sonic anemometer, net radiation, soil heat flux, soil temperature, soil moisture, PAR, etc.

## Data structure and content

- File format: CSV with a defined naming convention (UK_$$$_DataProduct_%d_%m_%z.csv; site code UK_DKE as per Fluxnet conventions; date in DD_MM_YYYY format).
- Core variables (example highlights):
  - TIMESTAMP (YYYY-MM-DD HH:mm): end of the half-hour interval.
  - Gas fluxes and related terms: NEE (Net Ecosystem Exchange), NEE_VUT_REF, NEE_VUT_USTARxx (xx = 05, 50, 95), GEP (Gross Primary Production), RECO (Ecosystem Respiration) with nighttime/GPP-based partitioning options.
  - Heat and energy fluxes: H (Sensible heat flux), LE (Latent heat flux), NETRAD (Net radiation).
  - Meteorology and pedology: air temperature (TA_F_NS), relative humidity (RH_F_NS), precipitation (P_F_NS), air pressure (PA_F_NS), PPFD (photosynthetic photon flux density), soil temperatures (TS_1_1_1, TS_2_1_1, TS_3_1_1), soil moisture (ML2), VPD, wind parameters (WD, WS), etc.
  - Gap-filled and QC fields: H_F_MDS, LE_F_MDS, NEE_VUT_REF_QC, NEE_VUT_USTARxx_QC, EddyPro Flag, REddyProc Flag, Biomet Flag, and corresponding RANDUNC (random uncertainty) fields.
- Missing values: indicated by -9999.
- Data processing notes:
  - Gap filling and partitioning of NEE into GEP and respiration using REddyProc (v0.8-2/r14).
  - Gap-filling of H, LE, and NEE via marginal distribution sampling (MDS).
  - Short gaps (0.5–1 h) filled with biomet observations; longer gaps filled using nearby sites, Kinbrace Met Office data, or co-located instruments as available.
  - 2D footprint model used to assess representativeness of flux footprints.

## Data quality, processing, and provenance

- Processing and quality control:
  - Eddy data processed with EddyPRO software; standard corrections and quality checks applied.
  - Flux data screened for statistical outliers, stationarity, physically plausible ranges, and low turbulence (u* thresholding).
  - QC flags include:
    - Biomet Flag: 00 raw, 01 primary reviewed, 02 calibrated, 13/14 interpolated gaps, 22/32 model/instrument substitutions, 03 no data, 04 removed faulty data.
    - EddyPro Flag: 0 best quality fluxes; 1 suitable for analysis; 2 fluxes to be discarded; -9999 missing data.
    - REddyProc Flag: 00 original; 01 most reliable; 02 medium; 03 least reliable; -9999 missing.
- Instrumentation:
  - LI-7200 CO2/H2O analyser; LI-7700 CH4 analyser (open-path).
  - Gill Windmaster Pro sonic anemometer; LI-COR components for data integration.
  - Calibration noted for LI-7200 on 18/05/2017; other sensors monitored for drift but not routinely recalibrated during the period.
- Field logistics:
  - Data acquisition via Sutron 9210 datalogger; remote retrieval over 4G; data processed and archived with an R-based UKCEH package; raw data also stored and accessed during site visits.
- Data lineage and accessibility:
  - Managed by James Hutton Institute (Aberdeen) as part of SCO2FLUX; UHI owned infrastructure; RSPB land access; funding through NERC and RESAS.
  - Core dataset described here is designed for integration with GIS analyses and map-based data products; data are provided as time-series with associated geolocation metadata.

## Relevance for GIS specialists and potential GIS uses

- Provides spatially-referenced, time-resolved (half-hour) flux data with accompanying meteorological and pedological measurements suitable for:
  - Mapping seasonal and interannual patterns of CO2 and CH4 exchange at a peatland plantation site.
  - Linking flux data to environmental covariates (temperature, humidity, soil moisture, radiation) for spatial modeling and hotspot analysis.
  - Assessing footprint representativeness and integrating flux footprints into spatial analyses with other land-cover layers.
- Data integration considerations for GIS:
  - Data are delivered as CSV with explicit timestamp and geolocation context; no shapefiles are provided, so join-time alignment by timestamp is required for GIS workflows.
  - Units and parameter naming follow Fluxnet/REddyProc conventions; consistent handling needed when merging with other geospatial datasets.
  - Missing data and quality flags should be used to filter or weight observations in spatial analyses and when creating map-based products.
- Practical GIS workflows:
  - Merge with gridded environmental layers (soil type, elevation, land cover) to explore drivers of gas flux variability.
  - Generate time-aggregated surfaces (e.g., monthly or seasonal summaries) for visualization in maps or dashboards.
  - Use the 2D footprint information to constrain spatial inference to the representativeness area of the flux measurements.

## References and credits

- Data and processing framework align with established micrometeorology and eddy-covariance standards and references (e.g., Mauder et al., Reichstein et al., Foken et al., Baldocchi; REddyProc and EddyPro workflows).
- Institutions involved: UK Centre for Ecology & Hydrology (UKCEH), James Hutton Institute (JHI), University of Highlands and Islands (UHI), RSPB, NERC, RESAS, with project support from SCO2FLUX and CentrePeat initiatives.