# COSMOS-UK User Guide

## Overview
- COSMOS-UK provides near real-time soil moisture data from a UK-wide network using cosmic-ray neutron sensing, offering area-average measurements over tens of hectares.
- Data are intended to support environmental research, weather and flood forecasting, agricultural water management, and ecosystem studies.
- Outputs include both raw sensor data and derived soil moisture products, with plans for broader data services and ongoing methodological improvements.

## Data and Outputs

- Monitored data (Table 4.1) include:
  - Precipitation (1 min), Absolute humidity, Relative humidity, Air temperature, Atmospheric pressure
  - Incoming/outgoing shortwave and longwave radiation, Net radiation (derived), Wind (direction, speed, 3D), Snow depth
  - Snow water equivalent, Volumetric water content from IMKO Profile sensors (at multiple depths), Soil heat flux, Soil temperature (multiple depths), Weather variables
  - TDT-based soil moisture and temperature (approx. depths from 2 cm to 50 cm)
- Derived data (Table 4.2) include:
  - Net radiation (derived), CRNS-based volumetric water content (VWC) and corresponding daily/hourly values, Corrected CRNS neutron counts, Potential evaporation
- Data cadence and delivery:
  - Most data are recorded at 30-minute intervals; rainfall typically at 1-minute intervals
  - Data are uploaded from field sites to CEH and undergo quality control to produce Level 2 (cleaned) data
  - Data availability lags: typically up to 1–2 years behind the upload date; provisional and subject to revision
- Access and use:
  - Data available via the CEH Environmental Information Data Centre (EIDC) at http://eidc.ceh.ac.uk
  - Data requests for non-EIDC items considered on a reasonable-effort basis
  - Data are released under a license; COSMOS-UK welcomes collaborative opportunities
  - Live graphs and standard graphical retrievals are available on the COSMOS-UK website
- Products and tools:
  - Standard graphical retrievals (Appendix D) and embedding tools (Appendix E) to display COSMOS-UK plots on websites
  - Quality control plots (1-day and 10-day) are produced and archived
  - Data can be viewed in graphs with delays dependent on processing and transmission

## Sites and Selection

- The COSMOS-UK network spans multiple sites across the UK (Table 2.1 and Appendix A Expanded Site List), with start dates ranging from 2013 onward.
- Site selection criteria aim to cover diverse UK conditions:
  - Geographic coverage for spatial representativeness
  - Variation in climate, soil type, geology, land cover
  - High soil moisture variability and strong research potential
  - Long-term access, ease of access, low vandalism risk, and robust mobile coverage
- Some sites host multiple instruments; not all instruments are deployed at every site (Table 3.2).

## Instrumentation

- Cosmic-Ray Neutron Sensor (CRNS): measures fast neutron counts; soil moisture derived after field calibration; effective depth ~15–40 cm; footprint up to several hundred meters, with sensitivity varying with soil moisture
- Raingauge (OTT Pluvio²): measures precipitation
- Point soil moisture sensors (TDT) at various depths (~2 cm to ~50 cm)
- Profile soil moisture sensor (IMKO PICO-PROFILE): 0.15, 0.40, 0.65 m depths
- Soil heat flux plates (two per site)
- Soil temperature sensors (multiple depths)
- Radiometer (four-component: shortwave and longwave)
- Automatic weather station (air temperature, humidity, wind, radiation shields)
- Barometric pressure sensor
- Temperature and humidity sensor
- 3D sonic anemometer
- Phenocam (two hemispheric cameras for vegetation, cloud, ponding observations)
- Snow depth (sonic sensor) and Snow water equivalent (SnowFox)
- Micrologger (data logger)
- Note: All instruments are not necessarily present at every site; refer to Tables 3.1 and 3.2 for deployment details

## Data Processing and Quality Control

- Processing is required to convert raw sensor data into usable soil moisture and other metrics
- Level 1 to Level 2 QC:
  - Two-stage QC: automatic tests (Level 1) and daily visual inspection of plots (Level 2)
  - QC tests cover zero data, too few samples, low power, sensor fault, diagnostic flags, out-of-range values, secondary variable dependencies, spikes, and error codes (Table 6.1; see Appendix G)
  - Level 2 data preserve the original Level 1 data for traceability
- Gap filling:
  - No automatic gap filling is currently performed
- Averaging and data derivation:
  - Hourly CRNS counts are averaged to reduce noise; daily means are typically used due to high variability in UK soils
  - VWC derived from corrected CRNS counts using methods such as site-specific N0, hydrogen molar fraction (hmf), or neutron transport models; COSMOS-UK uses site-specific N0 calibration with field reference soil moisture
  - Corrections account for atmospheric pressure, humidity, altitude, and cosmic ray intensity (using a Jungfraujoch reference)
- The CRNS processing and data products have evolved:
  - Revised daily averaging method reduces out-of-range VWC values and improves data completeness
  - Negative VWC values are set to zero; values above 100% are flagged for user caution
  - Effective depth and footprint revisions (D86) provide distance-based depth estimates; 75 m distance used as a representative indicator for footprint depth
  - A new site-specific correction factor ɣ was introduced in 2018 to address spurious trends
- Comparison with other sensors:
  - CRNS data are noisier than TDT sensors; TDT sensors provide less noisy measurements and generally align with CRNS within uncertainties
  - Comparisons with TDT data help characterize spatial variability and sensor sampling differences
- Processing continuity:
  - When model updates occur, the new processing is applied to the entire dataset for consistency
  - Legacy methods may continue in the background for reference

## Accessing COSMOS-UK Data

- Primary access via the EIDC portal; data are uploaded in annual batches and may lag by 1–2 years
- Data are provisional and subject to revision; CEH disclaims liability for data use
- Data licensing is provided with data releases
- Graphs and standard retrievals:
  - Live data can be viewed on the COSMOS-UK website
  - Standard graphical retrievals and embedded plotting are available (Appendix D and E)
- Data requests:
  - Requests for non-EIDC data may be considered on a case-by-case basis
  - Collaboration inquiries are welcome (cosmosuk@ceh.ac.uk)

## Data Availability and Limitations

- Availability and completeness vary by site and variable; Appendix B provides period-of-record data availability
- Data gaps can arise from instrument faults, logging issues, telecommunications, or quality control
- Some peat soils pose challenges, particularly for VWC accuracy and daily averaging
- Users should exercise caution with high VWC values, especially in peat-dominated sites
- Peering and data latency depend on processing steps and network transmission; typical delays are up to a couple of hours for graphs, longer for full data access

## Appendices and Tools (Highlights)

- Appendix A: Expanded Site List with site properties, soil types, bulk density, land cover, and coordinates
- Appendix B: Data availability and completeness by year and site
- Appendix C: Phenocam images and metadata
- Appendix D: Standard graphical retrievals (e.g., monthly summaries, period-of-record plots)
- Appendix E: Embedding COSMOS-UK data plots on websites using query parameters
- Appendix F: Site layout details
- Appendix G: Quality control tests and descriptions (detailed QC parameter codes and criteria)

Note: This summary focuses on core concepts, data products, processing workflows, and access mechanisms relevant to Data Support professionals enabling data discovery, integration, and user-facing data products.