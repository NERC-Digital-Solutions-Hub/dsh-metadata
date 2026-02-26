# COSMOS-UK User Guide

## Overview
- The COSMOS-UK network provides near real-time soil moisture data across the UK using cosmic-ray neutron sensors (CRNS), offering area-averaged measurements over up to ~12 hectares.
- Data products include soil moisture (CRNS-derived VWC), meteorological variables, and other derived environmental parameters, designed for map-based GIS use and integration with models and remote sensing.
- The aim is to enable applications in weather/climate modelling, water resources, flood forecasting, agriculture, and ecosystem analysis; data are publicly accessible via the CEH Environmental Information Data Centre (EIDC).

## Data and data products relevant to GIS specialists
- Monitored data (Table 4.1): precipitation, humidity (absolute and relative), air temperature, atmospheric pressure, radiation components (shortwave/longwave, incoming/outgoing), wind (direction, speed, 3D components), snow depth, snow water equivalent, soil moisture and temperature at multiple depths, soil heat flux.
- Derived data (Table 4.2): net radiation, CRNS-derived volumetric water content (VWC), daily/hourly VWC, corrected neutron counts, potential evapotranspiration.
- CRNS-specific outputs: corrected counts, D86 (distance depth where 86% of counts originate, indicating footprint penetration), site-specific VWC with averaging to reduce noise.
- Spatial scale and footprint: CRNS produces area-averaged signals with a footprint typically hundreds of meters to a few hundred meters radius, and an effective depth that varies with soil moisture from ~0.08 m (wet soils) to ~0.8 m (dry soils).
- Data formats and access: data are available via the CEH EIDC; data are provisional and subject to quality control revisions; graphs and standard retrievals are accessible online; embedding plots via provided URLs is supported.

## Sites and network design (GIS implications)
- UK-wide network sampling diverse conditions (climate, soil types, land cover) to capture spatial variability at local, regional, and national scales.
- Site selection criteria balance coverage with representation, long-term access, proximity to water, vandalism risk, power/mobile coverage, and existing research activities.
- Site list includes numerous locations with detailed metadata (start date, calibration status, grid coordinates, altitude, soil type, land cover). Not all instruments are present at every site.

## Instrumentation (scope for GIS data layers)
- Core instruments: Cosmic-Ray Neutron Sensor (CRNS), rain gauge, point soil moisture sensors (TDT), profile soil moisture sensor, soil heat flux plates, soil temperature sensors, radiometer, automated weather station, barometric pressure sensor, temperature/humidity sensor, anemometers, phenocam, snow depth/SWE sensors, micrologger.
- Some sites have full instrument suites; others have partial setups (Table 3.2 lists installations by site).
- Instrumentation is periodically updated; CRNS outputs underpin the primary soil moisture product, with ground-based sensors providing additional calibration/validation data.

## Data processing, quality control, and caveats (critical for GIS workflows)
- Processing is required to convert raw measurements into usable data streams and derived variables (e.g., CRNS counts to VWC).
- Quality control (QC): two-stage process
  - Level 1 QC: automated tests (e.g., zero data, too few samples, low power, sensor faults, out-of-range values, spikes, diagnostic flags, error codes).
  - Level 2 QC: daily visual inspection of plots; questionable data retained with QC labels for review.
- Gap filling: currently no automatic gap filling; gaps may exist due to sensor/logging/telemetry issues or QC.
- Data averaging: hourly CRNS-derived VWC is noisy; daily means (and longer) are recommended. COSMOS-UK moved to daily aggregation with revised methods to reduce out-of-range values; some high VWC values (especially peat soils) should be treated with caution.
- Processing revisions (since 2016-2018):
  - Revised daily averaging method reduces unrealistically high/low values and increases data completeness.
  - Revised effective depth estimation (D86) across multiple distances from the sensor to better reflect penetration depth under varying moisture.
  - New site-specific correction factor (gamma) to adjust for geomagnetic and sensor differences; ongoing refinements under publication.
  - When changes are made, new processing applies to the entire historical data for consistency.
- Comparison with TDT sensors: CRNS signals are noisy; TDT sensors provide complementary, less noisy measurements at shallower depths; cross-comparison used to assess consistency and inform interpretation.
- Data provenance and caveats: data are provisional and may be revised; licensing and attribution requirements apply; users should account for variable data completeness across sites and time.

## Accessing and using COSMOS-UK data (GIS integration)
- Primary access: CEH Environmental Information Data Centre (EIDC) at http://eidc.ceh.ac.uk/.
- Data are uploaded in annual tranches and can be requested via cosmosuk@ceh.ac.uk; not all data are available via EIDC immediately due to archival latency.
- Data licensing: data are supplied with usage terms; collaboration opportunities encouraged.
- Live data visualization: standard web pages allow viewing graphs for selected variables (e.g., rainfall, air temperature, CRNS-derived VWC); live data pages may have limited variable support.
- Embedding and plotting: Appendix E provides example URLs and parameters to embed COSMOS-UK graphs on websites; HTML snippets show how to generate graphs and control display parameters (site code, parameter, timespan, image size).
- Data formats and units: tables 4.1 and 4.2 define variables, units, and sampling intervals (e.g., 1 min for rainfall, 30 min for most meteorological and soil measurements, 30 min for CRNS in counts; derived VWC typically daily).
- Documentation and support: ongoing updates to processing methods and data products; data users should reference the guide for method details (Section 7 for CRNS processing; Appendices for data availability, QA tests, and embeddings).

## Considerations for GIS specialists (practical tips)
- Spatial alignment: use site coordinates (East/North grid references) and corresponding site footprints; CRNS footprints can span hundreds of meters, with depth sensitivity depending on soil moisture and distance from the sensor.
- Data quality: account for Level 1 vs Level 2 QC labeling; be mindful of gaps and potential revisions to processed values; peat soils may yield more uncertain VWC values.
- Temporal resolution: hourly CRNS data are noisy; prefer daily means for mapping and analyses requiring robust moisture estimates; consider using TDT data for higher temporal resolution at localized points.
- Data integration: combine COSMOS-UK data with other GIS layers (soil type, land cover, climate data, remote sensing products) for spatial analysis and model validation.
- Validation and uncertainty: use ground-based sensors (TDT, soil moisture probes) and phenocams for qualitative validation; be cautious with surface water and vegetation effects on CRNS-derived VWC (documentation discusses these factors and their impact on interpretation).
- Reproducibility: when processing changes are made, the guide notes that COSMOS-UK applies updates to the entire dataset to maintain consistency; document processing version when using historical data.