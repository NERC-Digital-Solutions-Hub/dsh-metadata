# COSMOS-UK User Guide

- Near real-time soil moisture data for the UK, using cosmic-ray neutron sensors (CRNS) across a network of sites. Instrumented data provide area-averaged soil moisture over tens of hectares, not just point measurements.
- Primary goal: enable improved meteorological models, water resources understanding, flood resilience, crop water use efficiency, and fundamental soil moisture science.

## Projects, data types and access

- Data streams: CRNS-based soil moisture (VWC) derived from neutron counts, along with complementary in situ sensors for precipitation, air temperature, humidity, radiation, soil temperature, soil moisture (TDT and profile probes), soil heat flux, wind, and phenology (Phenocam).
- Derived data: CRNS-based volumetric water content (VWC), net radiation, potential evaporation, and other joined datasets. Data are provisional and subject to ongoing quality control.
- Data access: CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk. Data uploaded annually (up to 1–2 years delay). Data requests otherwise considered on a reasonable-effort basis; licensing applies. Live graphs and standard graphical retrievals are available on the COSMOS-UK website.

## Sites and site selection

- UK-wide network designed to sample diverse conditions (climate, soil, land cover, geology) with some site clustering to study local, regional, and national variability.
- Site selection factors include location coverage, environmental variables, high soil moisture variability, existing research, data-assimilation potential, proximity to water or groundwater (negative), long-term permissions, accessibility, vandalism risk, and mobile coverage.
- Table of sites spans numerous locations (e.g., Rothamsted, The Lizard, Easter Bush, Alice Holt, Waddesdon, etc.) with calibration status, coordinates, altitude, and soil/land-cover descriptors.

## Instrumentation

- Cosmic-Ray Neutron Sensor (CRNS): counts fast neutrons; converts to soil moisture after field calibration. Large footprint (tens to hundreds of meters), with effective soil depth typically 15–40 cm; processed to account for atmospheric pressure, humidity, and cosmic-ray intensity.
- Raingauge: precipitation (mm, 1-minute recording; on-board processing for temperature/wind corrections).
- Point Soil Moisture Sensors (TDT): absolute volumetric water content and soil temperature at shallow depths; not site-calibrated to specific soils.
- Profile Soil Moisture Sensor (3 depth points: e.g., 0.15, 0.40, 0.65 m) using TDT technique.
- Soil Heat Flux Plates: measure soil heat flux at 0.03 m depth.
- Soil Temperature Sensors: multiple depths via profile thermocouples (2, 5, 10, 20, 50 cm).
- Radiometer: four-component (shortwave and longwave, up and down) for net radiation.
- Automatic Weather Station: air temperature, relative humidity, shielded air readings; barometric pressure.
- Barometric Pressure Sensor: high-range pressure sensor.
- 3D Sonic Anemometer: wind speed in three dimensions (0–45 m/s).
- Phenocam: two wide-angle cameras for qualitative vegetation/phenology and site conditions (clouds, snow, ponding).
- Snow sensors: snow depth and Snow Water Equivalent (via neutron interactions with snow).
- Micrologger: data logging and communication hardware.
- Note: not all instruments are installed at every site; table shows installations by site and status.

## Data availability and monitoring

- Data types and availability are defined in Tables 4.1 and 4.2 (observations and derived products such as VWC and net radiation). Data are continuously quality controlled and subject to updates as methods evolve.
- Live data viewing and standard graphical retrievals are available via COSMOS-UK site; full data access via the EIDC with provisional status.

## Data processing, quality control, and gap handling

- Processing purpose: convert raw measurements into consistent, usable data streams; derive VWC from CRNS counts; apply quality controls and derive longer-interval products.
- Quality control (QC): two-stage process
  - Level 1: automatic QC tests applied to raw data (e.g., range checks, sensor faults, diagnostics, spike detection, error codes).
  - Level 2: daily visual inspection of plots for additional review.
- Data gaps: no automatic gap-filling currently; gaps remain until data retrieval or manual repair occurs.
- Aggregation: data can be averaged to hourly, daily, or longer intervals; guidance exists on handling missing data when deriving daily means (e.g., allow some missing hours).
- Averaging and VWC processing: due to CRNS noise, 6-hour or 24-hour averaging is recommended; daily means are typically used for most analyses. Historically, some hourly VWC values exceeded 100% or were negative; revised methods reduce such outliers and provide guidance on handling high or unreliable values.
- Site-to-site processing changes: COSMOS-UK has updated processing methods over time (e.g., revised averaging, handling of peat soils, use of bulk density in calibration, and more robust daily VWC derivation). When methods change, the entire dataset at all sites is updated to maintain consistency.

## Processing CRNS data and converting counts to soil moisture

- Cosmic-ray physics: cosmic rays produce neutrons; the presence of hydrogen (water) reduces fast-neutron counts via moderation. Therefore higher soil moisture yields fewer neutrons detected.
- Correction workflow: recorded neutron counts are corrected for variations in background cosmic-ray intensity (using a high-altitude reference like Jungfraujoch), altitude, atmospheric pressure, and atmospheric humidity to yield corrected counts.
- Conversion methods (three options): (1) site-specific N0 method (COSMOS-UK default), (2) universal calibration (hydrogen molar fraction, hmf), (3) neutron transport modeling (MCNP/COSMIC/URANOS). COSMOS-UK uses the site-specific N0 approach with field-calibrated reference soil moisture and a generic calibration function for silica-like soil, including corrections for lattice water and organic carbon content.
- Noise and averaging: CRNS-derived VWC is noisy; 30-minute neutron counts require time-averaging to reveal the signal; daily means are commonly used, with 6- or 24-hour averaging recommended for reliability.
- Cross-validation: CRNS data are compared with TDT soil moisture sensors (less noisy; typically at ~10 cm depth) to assess agreement and understand measurement volume differences.

## Footprint and depth considerations

- Effective depth (D86) and footprint: the sensor samples soil over a footprint that varies with soil moisture; effective depth ranges from about 10 cm (wet soils) to up to ~80 cm (dry soils). About half of detected neutrons originate within tens of meters of the sensor; the footprint is several hundred meters in radius but shows strong near-field sensitivity.
- Field sampling for calibration is adjusted to target representative soils and depths around the sensor, including distance-based sampling distances (1, 5, 25, 75 m; with larger radii for dry or wet conditions).

## Updates to processing, corrections, and best practices

- New correction factor: since 2018, a site-specific gamma-based correction factor has been introduced to account for geomagnetic effects and differences between CRNS sensors and the Jungfraujoch reference monitor; this improves removing spurious trends in VWC.
- Revised daily averaging: updated approach to computing daily VWC reduces out-of-range values; when appropriate, allow a small number of missing hourly counts to derive daily means; peat soils require cautious interpretation due to high organic matter and associated uncertainties.
- Revisions applied across all data: whenever processing changes are made, they are implemented across the entire dataset to maintain consistency; legacy calculations may continue in the background for historical comparisons.

## Visualization, embedding and standard outputs

- Standard graphical retrievals are available (e.g., daily means, 30-minute or hourly data) and can be embedded in websites using provided URLs and example scripts.
- Visualization tools include daily quality control plots and longer-range retrievals; there are dedicated graphical retrievals and example URLs for embedding graphs.

## Contact, acknowledgments, and references

- Data and project contact: cosmosuk@ceh.ac.uk; EIDC for data access.
- Acknowledgements: NERC funding, Jungfraujoch neutron monitor data, and collaborating landowners and institutions across the UK.

- References: foundational papers on cosmic-ray soil moisture methods, calibration, and processing (e.g., Zreda et al., Franz et al., Kohli et al., Evans et al., Bogena et al., Desilets et al., etc.) for deeper methodological context.