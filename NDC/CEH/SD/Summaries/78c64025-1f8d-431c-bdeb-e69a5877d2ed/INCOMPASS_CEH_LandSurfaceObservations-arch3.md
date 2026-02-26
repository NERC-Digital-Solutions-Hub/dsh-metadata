# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

- A dataset of time-series observations describing surface-atmosphere exchanges of sensible heat (H), latent heat (LE), and momentum (τ), plus net ecosystem CO2 exchange (NEE), at three INCOMPASS Land Surface Stations in India, from 2016-01-01 to 2018-01-01.
- Includes ancillary meteorological and soil-physics measurements, as well as atmospheric turbulence metrics and quality indicators for flux observations.
- Three sites: Berambadi (Southern Karnataka; agricultural land), Dharwad (Dharwad UAS, northern Karnataka; agricultural land), and Kanpur (IIT Kanpur, Uttar Pradesh; semi-natural grassland).

- Purpose and context for monitoring frameworks:
  - Provides comprehensive, standardized flux and environmental data to evaluate surface-energy and carbon fluxes in diverse Indian environments.
  - Demonstrates end-to-end data handling from collection through processing, quality control, and documentation to support policy scrutiny and future decision-making.

- Sampling regime and instrumentation:
  - Automated measurements using open-path eddy covariance (EC) systems for H, LE, τ, and NEE, complemented by meteorological and soil-physics sensors.
  - Identical EC instrumentation at all sites; data collected on 10 m masts and logged at 20 Hz, aggregated to 30-minute means.
  - Instruments include Windmaster sonic anemometers, LI-7500A CO2/H2O analysers, barometric pressure sensors, NR01 net radiometer, WindSonic wind sensors, and SBS314 rain gauges.
  - Soil measurements include soil heat flux (0.03 m depth) and soil temperature and volumetric water content at 0.05 m and 0.15 m depths, duplicated at two locations per site.

- Data processing and quality control:
  - Flux calculations performed with EddyPRO v6.1, incorporating: detrending, coordinate rotation, high/low-frequency corrections, density corrections, and storage terms as appropriate.
  - Sign convention: positive fluxes from surface to atmosphere.
  - QC procedures for EC data: outlier removal (MAD), stationarity and integral turbulence tests, site-specific quality flags, minimum data-quality thresholds, footprint checks (ART Footprint Tool), and manual review of time series.
  - QC for meteorological and soil data: basic range checks, spike/dropout filtering, cross-checks between soil sensors, and correlation with rainfall events.
  - Uncertainty indicators and ancillary metrics (e.g., u*, TKE, L, z/L) are computed as part of the processing workflow.

- Data structure, availability, and metadata:
  - Data delivered as separate CSV files for each station, covering 2016-01-01 00:30 to 2018-01-01 00:00.
  - Missing values denoted by -9999; timestamps reflect the end of each 30-minute period.
  - Variables cataloged include: H, LE, τ, NEE, CO2 storage term, atmospheric pressure (Pa), air temperature (Ta), relative humidity (RH), radiation components (SWin, SWout, LWin, LWout, Rnet), precipitation, soil heat fluxes (G1, G2), soil temperature (Tsoil), soil moisture (VWC) across depths, wind metrics (WS_EC, WD_EC; WS_10m, WD_10m), and a suite of turbulence/footprint metrics (Ustar, TKE, T*, L, zL, x_peak, x_10, x_30, x_50, x_70, x_90).
  - Site context provided: coordinates, altitude, dominant land use, climate classification, soil orders, and representative climate data sources.
  - Documentation includes comprehensive site-specific configurations, data processing steps, and references to foundational methods and quality-control standards.

- Relevance to monitoring framework authors:
  - Exemplifies a rigorous, transparent monitoring workflow from sensor deployment to data products, with explicit QC criteria and reproducible processing using established software.
  - Highlights the importance of metadata richness (site characterization, instrument configuration, soil/vegetation context) to support data governance, comparability, and reuse.
  - Demonstrates handling of data gaps, storage terms, and uncertainty estimation within a multi-site monitoring network.
  - Provides a robust template for implementing standardized measurement protocols, data validation, and stakeholder-facing outputs (datasets, methods, and references) in environmental health monitoring programs.

- Notable considerations for data governance and future use:
  - Data are produced with careful QA/QC and documentation to enable reuse in policy evaluation and decision-making.
  - Metadata completeness (site specifics, instrument configurations, and processing parameters) supports verifiability and cross-site comparability.
  - The dataset emphasizes the need for consistent processing, transparent uncertainty accounting, and footprint assessments to ensure representativeness of flux observations across diverse landscapes.