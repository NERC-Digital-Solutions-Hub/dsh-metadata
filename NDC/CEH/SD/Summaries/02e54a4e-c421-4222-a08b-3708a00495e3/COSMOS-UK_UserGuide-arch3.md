# COSMOS-UK User Guide

- Aims and purpose: Provide near real-time soil moisture data across the UK using a cosmic-ray neutron sensor network; support improved meteorological modelling, water resource information, flood warning capabilities, crop water use efficiency, and fundamental soil moisture science.

- How COSMOS-UK achieves this:
  - UK-wide network design to sample diverse climate, soil types, land covers; include clustering to study variability at local, regional, and national scales.
  - Stakeholder and expert engagement to identify useful measures; data are sourced, validated, and metadata are added or refined; data are quality assured and presented through reports, charts, or dashboards.
  - Data governance and open sharing where possible; commissioning new data where gaps exist; outputs disseminated to users with appropriate caveats.

- Network design and site selection (Section 2):
  - Sites selected to span geographic, climatic, and soil/land-cover diversity; aim to capture variability without excessive duplication.
  - Key factors in site evaluation (positive and negative influences): geographic coverage; environmental variables (climate, soil, geology, land cover, topography); high soil moisture variability; existing monitoring activities; potential model/data assimilation applications; proximity to open water or groundwater (negative); long-term access permissions (positive); ease of access; vandalism risk; mobile network coverage.
  - Site properties: long-running installations since 2013–2018; calibrated sites shown in Appendix A; table of site start dates, coordinates, and elevations.

- Instrumentation (Section 3):
  - Cosmic-Ray Neutron Sensor (CRNS): counts fast neutrons; soil moisture derived after calibration; large measurement footprint (tens to hundreds of meters; typical effective depth ~15–40 cm; footprint up to ~300 m in radius; calibration accounts for atmospheric pressure, humidity, and cosmic ray intensity). Models used: Hydroinnova CRS-2000 and CRS-1000/B.
  - Raingauge: measures precipitation; on-board processing for temperature/wind-induced biases; model OTT Pluvio².
  - Point soil moisture sensors (TDT) and profile soil moisture sensors (three-depth array): absolute volumetric water content and soil temperature; generic calibration (not site-specific).
  - Soil heat flux plates (two per site): measure soil heat flux at 0.03 m; self-calibrating.
  - Soil temperature sensors: five depths (2, 5, 10, 20, 50 cm) with thermocouples.
  - Radiometer: four-component (shortwave and longwave, upward and downward) for net radiation.
  - Automatic weather station: air temperature, relative humidity, and barometric pressure measurements.
  - Barometric pressure sensor, 3D sonic anemometer, phenocam (vegetation/phenology), snow depth sensor, snow water equivalent sensor (SnowFox), and data logging hardware (Micrologger CR3000).
  - Not all instruments are installed at every site; instrument configurations evolve over time (Tables 3.1 and 3.2).

- Available data (Section 4):
  - Monitored data (sampled at 1 minute to 30 minutes, depending on variable):
    - Precipitation, absolute humidity, relative humidity, air temperature, atmospheric pressure, incoming/outgoing shortwave and longwave radiation, wind (speed and direction; 3D components), snow depth, snow water equivalent, and soil moisture metrics from TDT profiles.
  - Derived data (produced from raw/observed data):
    - Net radiation (derived), volumetric water content from CRNS (CRNS VWC), daily/hourly CRNS neutron counts (corrected), potential evaporation, and other related metrics.
  - Data quality and processing: data are subject to ongoing quality control and gap filling; data availability can change as processing evolves; provisional data are supplied with licensing and caveats.

- Accessing COSMOS-UK data (Section 5):
  - Data are available via the CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk.
  - Data are uploaded in annual tranches and typically lag behind real time by 1–2 years (e.g., 2018 data for 2016 period).
  - Data requests beyond the EIDC are possible; contact cosmosuk@ceh.ac.uk.
  - Data are provisional and may undergo further quality control; license terms apply.
  - Web access includes live graphing for precipitation, air temperature, and soil moisture from the CRNS or neutron counts; standard graphical retrievals are available (Appendix D).

- Data processing and quality control (Section 6):
  - Processing ensures quality of streams and enables derived data (notably CRNS-derived VWC).
  - Data streams may be instrument- or logger-derived, with some data averaged or aggregated to longer intervals.
  - Gap filling: currently no automatic gap-filling is performed; missing data can be retrieved or inferred via site visits in some cases.
  - Quality control (Section 6.1):
    - Two-stage QC: automatic QC tests (Level 1) and daily visual inspection of plots (Level 2); raw Level 1 data copied to Level 2 for traceability.
    - QC tests applied to specific variables and documented in Appendix G; common issues include zero data where not possible, too few samples, low power, sensor faults, out-of-range values, diagnostic flags, spikes, and error codes.
  - Data handling and aggregation (Section 6): data can be averaged or accumulated to hourly/daily intervals; missing data handling rules defined (e.g., allow up to two hourly values missing for daily mean, etc.).
  - Gap filling: no automatic gap-filling currently implemented.

- Processing the CRNS data (Section 7):
  - 7.1 About cosmic rays: overview of cosmic-ray interactions, neutron production, moderation by hydrogen (water), and how surface neutrons relate to subsurface moisture.
  - 7.2 Converting counts to soil moisture: counts adjusted for cosmic-ray background, altitude, atmospheric pressure, and water vapor; three methods to derive water content:
    - Site-specific N0 method (COSMOS-UK uses this with field calibration)
    - Universal calibration (hmf) method
    - Neutron transport modelling (MCNP/COSMIC/URANOS)
  - 7.3 Averaging to reduce noise: hourly CRNS counts are noisy; UK conditions (wet soils, high organic content) reduce counts; recommended 6-hour or 24-hour averaging; daily means used for many applications; some hourly data remain in raw form.
  - 7.4 The CRNS footprint: footprint characteristics vary with soil moisture; effective depth and footprint size (D86 and other metrics) discussed; Kohli et al. (2015) suggests 50% of neutrons within 50 m, with notable near-sensor sensitivity; use of a 75 m D86 as a representative footprint indicator.
  - 7.5 Revised method for daily averaging: changes to daily averaging reduce out-of-bounds VWC values; negative values set to zero; >100% values retained with caveats; allow up to two missing hourly values for daily mean; improvements vary by site (notably peat soils).
  - 7.6 Revised effective depth estimation: moves from a single effective depth to D86 values at several distances (1, 5, 25, 75, 150, 200 m); now uses 75 m D86 as a consistent indicator; D86 values are typically greater than the previously estimated effective depth due to revised processing and soil-averaging.
  - 7.6 A new correction factor: correction for geomagnetic effects and sensor differences; introduced site-specific gamma (ɣ) factor in 2018 to remove spurious trends; ongoing development with a paper in preparation.
  - 7.7 Introduction of revised processing: processing updates applied to all data historically to maintain consistency; legacy methods may still run in the background.
  - 7.8 A comparison with data from TDT sensors: CRNS data are noisy; TDT sensors provide more stable, local VWC; general agreement with CRNS data but differences can arise due to sampling volumes, depths, and temporal alignment; CRNS samples a larger soil volume than TDT sensors.

- Practical considerations for monitoring framework authors (drawing from document content):
  - The COSMOS-UK approach demonstrates how to design a monitoring network that balances wide spatial coverage with local detail, including site selection criteria, instrument variety, and long-term governance.
  - Derived data (VWC from CRNS) require careful calibration, correction factors, and thoughtful averaging to produce reliable indicators for policy and model validation.
  - Data accessibility and governance are critical: provisional data with explicit licensing, traceability through Level 1/Level 2 QC, and documentation of processing changes to ensure reproducibility.
  The COSMOS-UK guide serves as a model for documenting data streams, processing workflows, quality controls, and value proposition for environmental monitoring frameworks.