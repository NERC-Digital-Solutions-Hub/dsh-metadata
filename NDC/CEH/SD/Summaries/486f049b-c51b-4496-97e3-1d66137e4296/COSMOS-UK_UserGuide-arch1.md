# COSMOS-UK User Guide

- COSMOS-UK was established in 2013 to deliver soil moisture data in near real-time across the UK using cosmic-ray neutron sensors (CRNS) that cover large areas (up to ~12 hectares). The aim is to support improved weather & climate models, water resources monitoring, flood forecasting, agricultural efficiency, crop yield forecasting, and fundamental science on soil moisture and greenhouse gas emissions. Interpreting CRNS measurements requires calibration, corrections for moisture above/below ground, and careful data processing.

## Key data products and data model
- Monitored data include meteorological variables (precipitation, temperature, humidity, pressure, radiation, wind), soil measurements (soil moisture from TDT sensors, profile soil moisture, soil temperature, soil heat flux), and snow-related data (depth and SWE).
- Cosmic-ray neutron counts from the CRNS are processed to derive volumetric water content (VWC) at the soil scale; VWC is a derived quantity, with counts requiring calibration, atmospheric and environmental corrections, and time averaging to reduce noise.
- Derived data also include net radiation and daily/hourly VWC estimates (from CRNS) and related footprint metrics (D86, effective depth).

## Sites and network design
- The COSMOS-UK network spans the UK with numerous sites (see Table 2.1 and Appendix A for full site list, dates, and coordinates). Sites vary in land cover and soil type to sample the range of conditions across the country.
- Site selection criteria emphasize: broad geographic/climate/soil/topography coverage, high soil moisture variability, opportunity for model/data assimilation validation, long-term access, ease of access, proximity to open water avoidance, and mobile network coverage.

## Instrumentation
- Primary instrument: Cosmic-Ray Neutron Sensor (CRNS; Hydroinnova CRS-2000/CRS-1000/B). Counts fast neutrons; the sensor’s effective measurement depth is typically 15–40 cm, with a large horizontal footprint (tens to hundreds of meters; historically ~300 m radius, with adjustments over time).
- Supplementary instruments (time-synced across sites as available):
  - Rain gauge (OTT Pluvio²)
  - Point soil moisture sensors (TDT; multiple depths, not soil-type calibrated)
  - Profile soil moisture sensor (TDT-based, at 0.15, 0.40, 0.65 m)
  - Soil heat flux plates (HFP01SC)
  - Soil temperature sensors (STP01 at multiple depths)
  - Radiometer (four-component: shortwave/longwave)
  - Automatic weather station (temperature, humidity, shielding, barometric pressure)
  - Barometric pressure sensor (Phase 3)
  - Temperature/humidity sensor (Phase 3)
  - 3D sonic anemometer and integrated 2D sonic anemometer
  - Phenocam (two wide-angle cameras) for vegetation, cloud cover, ponding
  - Snow depth sensor and Snow Water Equivalent (SWE via SnowFox)
  - Data logging and micrologger (CR3000)
- Instrument deployment varies by site; Table 3.2 documents site-specific installations.

## Available data
- Monitored data (Table 4.1) include: precipitation, absolute humidity, relative humidity, air temperature, atmospheric pressure, incoming/outgoing shortwave and longwave radiation, wind (speed, direction, 3D components), snow depth, snow water equivalent, IMKO profile soil moisture (three depths), and soil temperature/volumetric water content at multiple depths.
- Derived data (Table 4.2) include: net radiation, CRNS-derived VWC, D86 footprints (depth to 86% of detected neutrons) at various distances, corrected neutron counts, and potential evaporation estimates.
- Data processing and quality control are ongoing; data may be updated with evolving methods. Data availability increases over time; derived products may appear later than raw measurements.

## Accessing COSMOS-UK data
- Primary data portal: CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk. Data are uploaded in annual batches and may be 1–2 years behind the current date (e.g., 2018 data up to 2016).
- Data requests for unavailable items can be considered if reasonable in scope.
- All data are provisional and may be revised; data are provided under a license with terms of use.
- Live data viewing and standard graphical retrievals are available on the COSMOS-UK website; the site currently supports limited variables in live graphs but is planned for broader display.

## Data processing and quality control
- Processing is required to convert raw sensor data into usable variables (e.g., converting CRNS counts to VWC; aggregating hourly data to daily means; applying calibrations and corrections).
- Data processing also combines multiple instruments (e.g., CRNS with TDT sensors) and can derive longer-interval averages.
- Gap handling: currently, explicit gap filling is not performed; however, data gaps may be retrieved by visiting sites or through data requests.
- Quality control (QC) is applied in two stages:
  - Level 1 automatic QC tests (per variable; see Appendix G and Table 6.1 for details)
  - Level 2 dataset created after automated QC, plus daily manual visual inspection of plots
- Data labeling distinguishes Level 1 and Level 2 data; raw data remain available for review.

## CRNS data processing specifics
- Cosmic-ray physics: fast neutrons interact with hydrogen in soil/air; higher hydrogen content (water) reduces detected fast neutrons; the CRNS counts are corrected for atmospheric pressure, altitude, and atmospheric water vapor.
- Methods for converting counts to soil moisture:
  - Site-specific N0 method (COSMOS-UK standard): calibrates a site-specific N0 using field calibration and a generic silica soil model; also accounts for lattice water and soil organic carbon (especially in peat soils).
  - Other methods (universal hydrogen molar fraction; neutron transport modelling) exist but COSMOS-UK predominantly uses the N0-based approach.
- Averaging to reduce noise:
  - CRNS counts are noisy; UK conditions often require 6-hour or daily averaging to obtain reliable VWC values.
  - Initial hourly VWC values can exceed physically plausible ranges; daily means and censoring strategies are employed to manage outliers.
  - A revised method (late 2010s) reduces improbable values and improves data availability, particularly at peat-containing sites, but care is needed when using peat soils due to high organic matter and lattice water.
- Footprint and effective depth:
  - CRNS has a large footprint; initial estimates suggested ~300 m radius, with significant contributions from near-sensor soil (within about 50 m).
  - Effective depth (penetration depth) varies with soil moisture; a D86 approach (distances of 1, 5, 25, 75 m and extended to 150–200 m) is used to characterize depth penetration; D86 values typically exceed earlier single-depth estimates, influenced by moisture and soil bulk density.
  - A representative 75 m D86 distance is used to illustrate penetration depth changes with soil moisture.
- Correction factor:
  - A correction factor Fi is applied to account for variations in cosmic-ray intensity and geomagnetic effects. Since 2018, site-specific gamma factors (γ) have been introduced to remove spurious trends between sites and the Jungfraujoch reference.
- Processing continuity:
  - When processing method changes are implemented, they are applied to the entire dataset for consistency; older calculations may still exist in the background.

## The CRNS vs. other soil moisture sensors
- CRNS data are noisy and sample a larger soil volume than point sensors like TDT probes.
- TDT-based soil moisture data are generally less noisy and more local, often showing better agreement with in-situ sampling at shallow depths.
- Comparisons between CRNS-derived VWC and TDT-derived VWC show periods of agreement and divergence, reflecting differences in sampling volume, timing, and sensor calibration.
- The guide emphasizes the need for further objective, cross-site analysis to quantify spatial/temporal resolution and to account for surface water (ponding) and vegetation effects on CRNS-derived VWC.

## Practical usage notes and caveats
- Peat soils present particular challenges for CRNS-derived VWC due to high organic matter content and lattice/bound water; daily VWC values for peat soils should be used with caution.
- High hourly VWC values (>100% or <0%) may occur despite averaging; the revised daily averaging approach reduces this issue but awareness is required.
- Data are provisional and subject to revision; users should verify data quality via QC flags and documentation, and acknowledge potential data gaps or changes in processing methods.
- The COSMOS-UK data platform provides standard plots and dashboards; data can be embedded into external websites via provided interfaces, with noted caveats about resolution and data lag.

## Appendices and additional resources
- Appendix A/B: Expanded site lists and data availability timelines by year.
- Appendix C: Phenocam imagery and metadata; qualitative vegetation and surface conditions information.
- Appendix D: Standard graphical retrievals and example figures for quick assessments.
- Appendix E: Embedding COSMOS-UK data plots on external websites.
- Appendix F/G: Detailed site lists and quality control tests applied to data.
- References: Key literature on CRNS methodology, calibration, and footprint considerations.

## Contact and data access
- Primary contact for COSMOS-UK: cosmosuk@ceh.ac.uk
- Data hosted by CEH’s EIDC; licensing governs data usage; users can inquire about collaborative opportunities.