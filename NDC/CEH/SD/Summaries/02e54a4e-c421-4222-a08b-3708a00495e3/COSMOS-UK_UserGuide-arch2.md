COSMOS-UK User Guide

## Overview for Analysts
- Purpose: deliver soil moisture data across the UK in near real-time using a cosmic-ray neutron sensing (CRNS) system.
- Key advantage: non-invasive, large-area measurements (up to tens of hectares), automated, suitable for integration into meteorology, hydrology, water resources, flood forecasting, and ecosystem studies.
- Outputs: site-calibrated volumetric water content (VWC) from CRNS, plus a broad suite of co-located environmental measurements (precipitation, air temperature, humidity, pressure, radiation, wind, etc.) and derived products (net radiation, potential evaporation, etc.).
- Data quality and access: ongoing quality control, data are provisional upon delivery, and access is via CEH’s Environmental Information Data Centre (EIDC) with a typical lag of 1–2 years.

## Network and Sites
- UK-wide network designed to sample diverse physical and climatic conditions (land cover, soils, geology, climate), with some site clustering to explore variability at multiple scales.
- Site list and properties are provided (Appendix A; Table 2.1 includes installation dates, coordinates, altitude, soil type, etc.).
- Site selection criteria include: broad geographic coverage, diverse environmental variables, high soil moisture variability, long-term access, proximity to open water (negative), vandalism risk (negative), and mobile network coverage (positive).
- Not all sites carry every instrument; instrumentation can vary by site and over time (see Table 3.2).

## Instrumentation
- Cosmic-Ray Neutron Sensor (CRNS): Hydroinnova CRS-2000/CRS-1000/B; measures fast neutrons to derive soil moisture after calibration; typical CRNS sensing depth is 15–40 cm; footprint can extend tens to hundreds of metres.
- Raingauge: OTT Pluvio² for precipitation (with on-board corrections for temperature/wind).
- Point Soil Moisture Sensors (TDT): time-domain transmissometry sensors at various depths; use generic calibration.
- Profile Soil Moisture Sensor: multi-depth (0.15, 0.40, 0.65 m) with access tube; TDT-based.
- Soil Heat Flux Plates: two per site (0.03 m depth) with self-calibration.
- Radiometer: four-component (shortwave and longwave, upward and downward) for net radiation.
- Automatic Weather Station: measures air temperature, humidity, and other standard meteorological variables; shielded temperature/humidity probe; barometric pressure sensor.
- Barometric Pressure Sensor, Temperature/Humidity Sensor, 3D Sonic Anemometer, Phenocam (vegetation/land-cover observations), Snow Depth Sensor, Snow Water Equivalent, Micrologger (data logger electronics).
- Instrument presence varies by site (Table 3.2 documents installation status).

## Available Data
- Monitored data (Table 4.1): precipitation, absolute humidity, relative humidity, air temperature, atmospheric pressure, incoming/outgoing shortwave and longwave radiation, wind speed/direction, 3D wind, snow depth, snow water equivalent, IMKO profile moisture, soil heat flux, soil temperature, and TDT-based soil moisture/temperature.
- Derived data (Table 4.2): net radiation, CRNS-based VWC, corrected CRNS counts, potential evaporation, and other derived metrics.
- Data are subject to ongoing quality control and may change over time as processing evolves; future derived datasets are anticipated.

## Accessing COSMOS-UK Data
- Primary access via the CEH Environmental Information Data Centre (EIDC): data uploaded in annual batches, typically lagging 1–2 years behind the present.
- Data requests: cosmosuk@ceh.ac.uk; data are provisional and licensed under terms defined by CEH.
- Online viewing: live graphs on the COSMOS-UK website ( presently displaying precipitation, air temperature, and CRNS-derived soil moisture/neutron counts for calibrated/un-calibrated sites over a ~6-month window).
- Standard graphical retrievals and Appendix D examples are available; additional data requests can be considered.

## Data Processing
- Processing transforms raw streams into quality-assured data products (notably CRNS-derived VWC) and other derived statistics.
- Raw vs. level-2 data: Level 1 undergoes automatic QC; passing data are moved to Level 2; raw data remain accessible for audit.
- Aggregation: data can be averaged to hourly/daily intervals; missing data handling is considered during aggregation (e.g., allow up to certain hourly gaps for daily means).

## Quality Control
- Two-stage QC process:
  - Automatic QC tests (Table 6.1; variables have specific tests).
  - Daily visual inspection of plots (1-day and 10-day frames) to catch anomalies.
- Level 1 data that fail tests are excluded from Level 2; Level 2 data are the cleaned data used for analysis.
- Quality control tests cover zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range values, and other error codes (Appendix G documents tests per variable).

## Gap Filling
- Current stance: no automatic gap-filling is performed; gaps may be filled via site visits or manual intervention, but there is no automated imputation in the processing pipeline.

## Processing the CRNS Data
- CRNS basics: fast neutrons are moderated by soil moisture; higher soil moisture leads to more energy loss and fewer detected fast neutrons.
- Counts to soil moisture: recorded counts are corrected for atmospheric pressure, humidity, and atmospheric neutron flux (using reference sites like Jungfraujoch); conversion to VWC uses one of several methods (Site-specific N0, universal hydrogen molar fraction, or neutron transport modelling). COSMOS-UK uses site-specific N0 calibration with field calibration data.
- Noise and averaging: CRNS data are inherently noisy; not suitable for hourly VWC without averaging. Daily means are recommended; 6-hour or longer averaging reduces noise.
- CRNS footprint and depth: effective depth and footprint vary with soil moisture; initial footprint around 300 m, with 50% of counts from within ~50 m; depth penetration declines with moisture (10–80 cm range, site-dependent).
- Processing updates: late 2010s saw revisions to averaging, depth estimation (D86 concept), and a new site-specific correction factor (gamma) to remove spurious trends; processing methods are applied across all sites for consistency.
- Comparing CRNS with point sensors (TDT): CRNS is noisier but samples a larger soil volume; TDT sensors offer more stable, less noisy VWC at ~10 cm depth; comparisons show broad agreement but site-to-site differences reflect sampling volumes and timing.
- Practical guidance: use daily mean VWC values; peat soils can yield higher VWC and require cautious interpretation; the updated processing dramatically reduces unrealistically high/low hourly values and improves data completeness.

## The Beginning, Middle, and End (Contextual Highlights)
- Beginning: COSMOS-UK established in 2013 to provide UK-wide, near real-time soil moisture data using cosmic-ray neutron sensing, enabling advances in weather, hydrology, and climate applications.
- Middle: extensive details on network design, instrumentation, data types, calibration methodologies, and data processing workflows; emphasis on data quality, footprint understanding, and evolving processing methods to improve reliability and usefulness.
- End: ongoing data access, quality control, site expansion, and methodological refinement; acknowledgement of collaborators and references guiding the scientific basis; expectation of additional derived data products and use cases.

Appendices (summary)
- Appendix A: Expanded site list with metadata (locations, calib dates, soils, land cover, etc.).
- Appendix B: Data availability by year and variable group.
- Appendix C: Phenocam images for qualitative environmental monitoring.
- Appendix D: Standard graphical retrievals (examples of plotting soil moisture, rainfall, etc.).
- Appendix E: Embedding COSMOS-UK plots in websites via a simple URL API.
- Appendix F: Site layout and site-specific metadata (partial in excerpt).
- Appendix G: Detailed quality control tests per variable.