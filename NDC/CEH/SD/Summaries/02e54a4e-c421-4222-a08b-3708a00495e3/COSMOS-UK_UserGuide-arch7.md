# COSMOS-UK User Guide

- GIS-relevant aim: Provide map-based data products that enable users to rapidly understand and explore UK soil moisture and related environmental information derived from a national CRNS network.

## Overview and purpose
- COSMOS-UK delivers near real-time soil moisture data from a network of UK sites using cosmic-ray neutron sensing (CRNS), offering a larger, non-invasive footprint (up to hundreds of meters to a few hundred meters) and typical effective soil depth around 15–40 cm.
- Primary motivation: support environmental research, meteorological modeling, water resources, flood warning, crop management, and soil-related science.

## How COSMOS-UK works (data flow and products)
- Instruments and data streams
  - Cosmic-Ray Neutron Sensor (CRNS): counts fast neutrons; raw counts require processing to obtain soil moisture (VWC).
  - Complementary instruments: raingauges, point and profile soil moisture sensors (TDT), soil temperature, soil heat flux, radiometer, automatic weather station, barometer, 3D wind, Phenocam, snow sensors, and data logger.
- Data processing and products
  - Counts corrected for environmental variables (pressure, humidity, cosmic ray flux) to yield corrected counts.
  - Derived products include volumetric water content (VWC) from CRNS, net radiation, CRNS-derived VWC with daily/hourly resolutions, and additional derived variables (e.g., potential evaporation).
  - Standard graphical retrievals and site plots are available; data can be embedded in websites via standard image endpoints.

## Data products and availability
- Monitored data (Table 4.1) include: precipitation, absolute and relative humidity, air temperature, atmospheric pressure, incoming/outgoing shortwave and longwave radiation, wind (speed and direction; 3D), snow depth, snow water equivalent, soil moisture (IMKO Profile, TDT at multiple depths), soil temperature (multiple depths), and soil heat flux.
- Derived data (Table 4.2) include: net radiation, CRNS-based VWC, hourly CRNS counts, and potential evaporation.
- Access to data
  - Primary access via the CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk.
  - Data uploaded in annual tranches; typical delay of 1–2 years behind the upload date (e.g., 2018 data may cover up to 2016).
  - Data are provisional and subject to further quality control; licensing terms apply.
  - Live graphs of select variables are available on the COSMOS-UK website; standard graphical retrievals are provided (Appendix D).

## Site network and coverage
- UK-wide distribution designed to sample diverse climates, soils, land covers, and topography; some clustering to explore regional variability.
- Site selection factors include geography, environment, moisture variability, existing collaborations, access, permissions, and network balance (positive/negative influences for redundancy and coverage).

## Instrumentation and data streams (summary)
- Core instrument: Cosmic-Ray Neutron Sensor (CRNS) with 15–40 cm effective soil depth; footprint expands with soil conditions.
- Support sensors: raingauge, point and profile soil moisture (TDT), soil temperature sensors, soil heat flux plates, radiometer, wind sensors, weather station, barometer, humidity sensors, 3D anemometer, Phenocam, snow depth and SWE sensors, micrologger.
- Not all instruments are present at every site; some sites use multiple sensors for cross-validation.

## Data processing and quality control
- Data processing is essential to convert raw streams into reliable environmental variables; CRNS-derived VWC is particularly processing-intensive and noisy.
- Quality control (QC)
  - Two-stage QC on raw data: automatic QC tests (level 1) and daily visual inspection with plots (level 2); data failing tests are excluded from level-2 datasets.
  - QC tests cover zero data, too few samples, low power, sensor faults, out-of-range values, diagnostic flags, spikes, and error codes (Table 6.1; detailed per-variable applicability in Appendix G).
- Gap filling
  - At present, COSMOS-UK does not perform automatic gap filling.
- Data processing specifics for CRNS
  - Correction factors adjust counts for atmospheric pressure, altitude, and atmospheric water vapor using reference data (e.g., Jungfraujoch reference).
  - Conversion of corrected counts to VWC can be done via three methods; COSMOS-UK uses site-specific N0 calibration with field-calibrated reference soil moisture, incorporating lattice water and organic carbon corrections.
  - Averaging and temporal resolution
    - CRNS data are recorded hourly; VWC is derived and typically averaged to reduce noise (recommended 6-hour or daily averages; hourly data are noisy in UK conditions).
    - Daily VWC values are derived with revised methods to minimize out-of-range values; daily means may tolerate some missing hourly data (original method filtered out-of-range values; revised method allows up to two missing hourly values for daily means).
  - Footprint and depth considerations
    - Sensor footprint is large (up to several hundred meters); the effective depth varies with soil moisture, generally shallower in wet conditions (as low as ~10 cm) and deeper in dry conditions.
    - D86 distances (1, 5, 25, 75 m and larger footprints) are used to characterize depth of soil contributing to counts; a 75 m D86 is used as an indicator for footprint penetration.
  - Corrections and updates
    - A new site-specific gamma (ɣ) correction factor was introduced in 2018 to remove spurious trends; adjustments are applied across all sites and back-calculated to historical data.
  - Processing evolution
    - Processing methods have evolved; when changes occur, they are applied to the entire dataset for consistency, though legacy processing may continue in the background.

## CRNS data vs other sensors
- CRNS provides large-scale soil moisture context but is noisier than localized TDT sensors.
- TDT sensors (at ~10 cm depth) generally yield more stable measurements; cross-comparison shows broad agreement with CRNS-derived VWC but with site- and time-varying differences due to measurement volume and sampling depths.

## Data access and usage for GIS
- Data are suitable for map-based visualization and integration with GIS workflows, including:
  - CRNS-derived VWC (0–100% range, daily and hourly where available)
  - Derived net radiation and potential evapotranspiration
  - Point and gridded soil moisture information at multiple depths (via TDT and profile sensors)
  - Visual site context from Phenocam imagery and weather variables
- Web-based plots and embedding options allow rapid inclusion in dashboards and web maps; data licensing applies.
- Data latency: 2 hours or more from site to graph, depending on automatic QC and data ingestion pipelines.

## Appendices (useful for GIS practitioners)
- Appendix A: Expanded site list with coordinates, site characteristics, soil type, bulk density, organic matter, and land cover (helps with GIS layer categorization and contextual mapping).
- Appendix B: Period of record data availability and variable groups (MET, SOIL, VWC) to gauge data completeness per site and variable.
- Appendix C: Phenocam images – qualitative vegetation and surface condition context; useful for interpreting soil moisture signals with vegetation and snow/ponding.
- Appendix D: Standard graphical retrievals – examples of common plots (e.g., monthly summaries, period-of-record plots) for quick map-based storytelling.
- Appendix E: Embedding COSMOS-UK data plots in websites – URL formats for dynamic graphs; helpful for web GIS dashboards.
- Appendix F/G: Site layouts and quality control tests details (structure for reproducibility and data QA in GIS analyses).

## Access and contact
- Data access: EIDC website (eidc.ceh.ac.uk); data are provisional with licensing terms.
- Data requests not available via EIDC may be considered by ECOSMOS-UK staff; contact cosmosuk@ceh.ac.uk
- Live data and standard plots: COSMOS-UK website; imagery, plots, and metadata available for GIS integration.