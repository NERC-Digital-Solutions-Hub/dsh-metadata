# COSMOS-UK User Guide

- The COSMOS-UK project delivers near real-time soil moisture data from a UK-wide network using cosmic-ray neutron sensors (CRNS). The sensor measures soil moisture over large footprints (tens to hundreds of metres across, up to ~12 hectares) and operates automatically from remote sites, enabling applications in meteorology, hydrology, flood forecasting, water use efficiency, and ecosystem studies. Derived data and standard retrievals support wide data exploration and model validation.

- Data scope and outputs
  - Primary measurements: CRNS neutron counts (hourly, with processing to derive soil moisture content, VWC) and site-specific calibrations; counts are corrected for atmospheric pressure, humidity, altitude, and cosmic ray variations.
  - Additional monitored data: precipitation, relative humidity, air temperature, atmospheric pressure, shortwave/longwave radiation, wind (speed and direction), soil temperature, snow depth, snow water equivalent, and wind/temperature/soil measurements from TDT and profile sensors.
  - Derived products: soil moisture from CRNS (VWC), net radiation, potential evaporation, CRNS-derived VWC depth-averaged values (including D86 footprint estimates), corrected neutron counts, and hourly/daily aggregations.
  - Data quality and processing: data are subject to ongoing quality control and updates; methods for CRNS processing (including VWC derivation and averaging) have evolved over time to reduce noise and improve reliability, with site-specific considerations for peat vs mineral soils.

- Site network and selection
  - UK-wide deployment designed to sample diverse climate, soil types, land covers, and topographic conditions; clustering allows inter-site variability analysis at local to national scales.
  - Site selection factors include geographic coverage, environmental variables, potential for data assimilation and model validation, proximity to open water, long-term installation permissions, accessibility, vandalism risk, and mobile coverage considerations.

- Instrumentation
  - Core instruments include: Cosmic-Ray Neutron Sensor (CRNS), rain gauge, point soil moisture sensors (TDT), profile soil moisture sensors, soil heat flux plates, soil temperature probes, radiometer, automatic weather station, barometric pressure sensor, temperature/humidity sensors, 3D and integrated wind sensors, phenocam, snow depth and SWE sensors, and data loggers.
  - Instrumentation evolves over time; not all sensors are installed at every site. Detailed site-by-site instrument availability is provided in the guide’s appendices.

- Data access and availability
  - Primary data portal: CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk.
  - Data delivery: uploaded annually in tranches, typically lagging 1–2 years behind the current date (e.g., 2018 data for 2016 period).
  - Data access policy: data are provisional and may be revised; users must acknowledge provisional status and CEH liability limitations; data are provided under a license specifying exploitation terms.
  - Graphical data access: live COSMOS-UK graphs are available on the COSMOS-UK website; standard graphical retrievals are described in Appendix D.
  - Data requests: not publicly available via EIDC may be considered on a reasonable, effort-based basis; contact cosmosuk@ceh.ac.uk.

- Data processing and quality control
  - Processing purpose: convert raw measurements to reliable data streams and derive CN/VWC values, smoothing noise, and producing usable time series.
  - Quality control (QC):
    - Two-stage QC: automatic QC tests (level 1) and daily visual inspection of plots (level 2).
    - Data flagged and filtered based on tests such as zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range values, and spikes (Table 6.1; see Appendix G for details).
    - Level 1 data are archived; level 2 data are cleaned, but original level 1 data remain accessible.
  - Gap filling: currently no automatic gap filling; gaps may be addressed by site visits or later manual corrections where feasible.
  - Data aggregation: hourly measurements can be averaged to daily or longer intervals; methods have evolved (including revised daily averaging) to minimize unreal values, with peat soils requiring cautious use.
  - Data processing across sites is unified when changes are made to ensure consistency across the entire time series; legacy processing may still exist in the background.

- CRNS data processing specifics
  - Physical basis: cosmic rays create fast neutrons; soil moisture (hydrogen content) reduces fast neutron flux, altering detected neutron counts. Counts are corrected for atmospheric factors to yield corrected counts.
  - VWC derivation methods: three approaches exist (site-specific N0, universal hydrogen molar fraction, neutron transport modelling). COSMOS-UK uses site-specific N0 calibration with a reference soil moisture value from field calibration, plus lattice water and organic carbon considerations.
  - Averaging to reduce noise: due to intrinsic CRNS noise, UK conditions require averaging (recommended 6–24 hours) to obtain reliable VWC values; hourly values can exceed physical bounds and are censored as needed.
  - CRNS footprint and depth (D86 and effective depth): footprint characteristics depend on soil moisture; initial ~300 m radius; later analyses show substantial near-sensor sensitivity (e.g., within 50 m). Effective depth varies with moisture; D86 values at multiple distances (1, 5, 25, 75 m, plus 150–200 m footprint) are provided to reflect penetration depth changes with moisture.
  - Processing updates: 2018 introduced site-specific correction factor ɣ to account for geomagnetic and sensor differences; processing methods and calibration factors have been updated to reduce spurious trends and improve consistency across the network. When processing changes occur, updates are applied retroactively to all sites for consistency.
  - Comparison with other sensors: CRNS data are noisier than localized TDT sensors; TDT sensors provide less noisy measurements and are often in closer agreement with CRNS-derived VWC, though differences may reflect spatial sampling volume and temporal averaging.

- Visualization, retrievals, and embedding
  - Graphical retrievals: standard graphs of variables (e.g., precipitation, air temperature, soil moisture) are available and can be embedded in websites via provided URLs.
  - Embedding data plots: the guide provides examples and HTML parameter codes to embed COSMOS-UK graphs on websites, enabling dynamic visualization of multiple variables over specified time windows.
  - Quality control plots: 1-day and 10-day QC plots are generated and archived for monitoring data quality.

- Appendices and supporting material
  - Appendix A: Expanded site list with site IDs, coordinates, soil descriptions, land cover, and calibration status.
  - Appendix B: Period of record data availability by year and data group (MET, SOIL, VWC).
  - Appendix C: Phenocam images and interpretation for vegetation changes, snow cover, and ponding; provides guidance on qualitative interpretation of site conditions.
  - Appendix D: Standard graphical retrievals with example figures.
  - Appendix E: Embedding COSMOS-UK data plots on websites, including example URL parameters and usage notes.
  - Appendix F & G: Additional data quality control tests and site-specific parameter mappings (G tests; parameter IDs).
  - Appendix F also includes site layout visuals and mapping information; Appendix G lists quality control tests by parameter group.
  - References: foundational literature supporting CRNS theory, calibration, footprint concepts, and previous COSMOS methods.

- Practical considerations for data users (Data Support perspective)
  - Data are provisional and subject to revision as QC and processing update, so treat outputs as current best estimates with potential revisions.
  - CRNS-derived VWC is a depth-averaged proxy; regional and local soil moisture variability and surface water (ponding) can influence readings, especially in peat-rich soils.
  - For critical analyses, compare CRNS-derived VWC with local TDT profile data and consider site-specific soil properties (bulk density, organic matter) for calibration and interpretation.
  - When using daily or higher-aggregation VWC, be aware of improved reliability with revised processing methods, particularly for peat soils where earlier daily values could exceed 100% or be unreliable.
  - Data access requires acknowledging provisional status and licensing terms; for custom requests or data not on the EIDC, contact cosmosuk@ceh.ac.uk.