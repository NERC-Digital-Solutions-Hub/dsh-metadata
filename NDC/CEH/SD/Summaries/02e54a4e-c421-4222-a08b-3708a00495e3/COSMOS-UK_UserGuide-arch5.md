COSMOS-UK User Guide

## Introduction
- COSMOS-UK provides soil moisture data in near real-time from a UK-wide network using cosmic-ray neutron sensing (CRNS), a non-intrusive, area-representative method (effective footprint up to several hundred metres).
- Intended to support improved meteorological models, water resources, flood warning, crop water management, and fundamental soil moisture science; acknowledges challenges in interpreting CRNS measurements and relating them to on-site conditions.
- The guide is aimed at current and potential data users, describing sites, instrumentation, data available, processing, quality control, and information products including standard retrievals.

## Data governance and access
- Data are hosted by the CEH Environmental Information Data Centre (EIDC) and uploaded in annual tranches, typically with a delay of 1–2 years behind the upload date (e.g., 2018 data cover up to 2016).
- Data requests for non-available items may be considered if feasible; contact cosmosuk@ceh.ac.uk.
- All data are provisional at delivery and may undergo further quality control; CEH disclaims liability for use.
- Data are provided under a license with terms of exploitation; data can be viewed as graphs on the COSMOS-UK live site.
- Live data graphs currently display precipitation, air temperature, and soil moisture from the CRNS (or neutron counts if not yet calibrated), with plans for broader variable display; standard graphical retrievals are available (Appendix D).

## Data availability and formats
- Monitored data include: precipitation (1 min, mm), absolute humidity (30 min), relative humidity (30 min), air temperature (30 min), atmospheric pressure (30 min), incoming/outgoing shortwave and longwave radiation (30 min), wind direction/speed (30 min), 3D wind components (30 min), snow depth and snow water equivalent, soil moisture and temperature at multiple depths, and soil heat flux (30 min).
- Derived data include: net radiation, CRNS-derived volumetric water content (VWC), corrected neutron counts, and potential evaporation (daily).
- Data are categorized into level 1 (raw) and level 2 (quality-controlled/processed); additional processing can derive longer-interval summaries (hourly, daily).

## Site network and selection
- The network aims to sample UK-wide variability in climate, soils, land cover, and geology; clustering enables inter-site comparisons at multiple scales.
- Site selection factors include geographic coverage, environmental variables, high soil moisture variability, existing monitoring, potential for model/data assimilation use, long-term permissions, accessibility, vandalism risk, and mobile coverage.
- The guide provides an expanded site list (Appendix A) with site properties, coordinates, start dates, soil types, bulk densities, land cover, and other contextual data.

## Instrumentation
- COSMOS-UK uses a suite of instruments, with CRNS as the central sensor. Instruments include:
  - Cosmic-Ray Neutron Sensor (CRNS) – Hydroinnova CRS-2000/CRS-1000/B; measures fast neutron counts for soil moisture derivation.
  - Raingauge – OTT Pluvio²; precipitation measurement.
  - Point soil moisture sensors (TDT) – various depths (2 cm, 5 cm, 10 cm, etc.) using time-domain transmissometry, not site-calibrated to local soils.
  - Profile soil moisture sensor – three-depth TDT (0.15, 0.40, 0.65 m) in access tubes.
  - Soil heat flux plates – two per site (0.03 m depth).
  - Soil temperature sensors – multiple depths (2, 5, 10, 20, 50 cm).
  - Four-component radiometer – shortwave and longwave radiation components.
  - Automatic weather station – air temperature, relative humidity, radiation shielded, barometric pressure.
  - Barometric pressure sensor (Vaisala PTB110).
  - Humidity and temperature probe (Vaisala HUMICAP HMP155A).
  - 3D sonic anemometer (wind speeds in 3D).
  - Phenocam – two hemispheric cameras for vegetation, snow, ponding, clouds.
  - Snow depth sensor (Sonic SR50A) and snow water equivalent (SnowFox).
  - Micrologger (Campbell Scientific CR3000) for data logging and control.
- Site- and instrument-ownership details are provided in Tables 3.1 and 3.2 (with variations over time and across sites).

## Data processing
- Data processing is required to convert raw measurements into usable data streams and derived products (notably CRNS-derived VWC).
- Processing involves applying corrections for atmospheric pressure, humidity, and cosmic-ray intensity; converting neutron counts to soil moisture using calibration methods (site-specific N0, hydrogen molar fraction, or neutron transport modeling). COSMOS-UK uses site-specific N0 calibrations.
- Processing also yields aggregated data (hourly to daily) and combines CRNS with other sensors (e.g., TDT data) to improve reliability.
- Processing methods have evolved; when changes are made, they are applied consistently across the entire dataset (historical back-calculation may occur).

## Quality control
- Quality control is ongoing and consists of two stages:
  - Level 1: automatic QC tests applied to each variable; data failing tests are removed from Level 2; tests are documented (Appendix G details per variable).
  - Level 2: daily visual inspection with plots for 1-day and 10-day windows; Level 1 data are retained with LEVEL1/LEVEL2 labels for provenance.
- QC tests cover ranges, sample counts, power, sensor faults, diagnostic flags, and spike detection, with error codes logged for logger faults.
- Data gaps are acknowledged; no automated gap-filling is currently performed (as of the guide’s version).

## Gap filling
- At the time of the guide, no automatic gap-filling is undertaken; gaps may be addressed later via on-site data collection if possible.

## Processing the CRNS data
- The CRNS method relies on cosmic-ray neutrons; corrected counts account for atmospheric and background variations.
- Three primary methods to derive soil moisture from corrected counts are described; COSMOS-UK uses site-specific N0 calibrations with field calibration references and accounts for lattice water and soil organic carbon effects.
- Averaging is essential due to CRNS noise; daily means (often derived from hourly values) are used to improve reliability, with caveats for peat soils and mineral soils.
- The CRNS footprint and effective depth vary with soil moisture, with typical effective depth around 10–80 cm depending on conditions; recent methods include distance-based D86 values to reflect depth of neutrons contributing to counts.
- A revised correction factor (gamma) was introduced in 2018 to remove spurious trends; site-specific gamma values are being developed.
- The guide discusses comparisons with point-based TDT sensors, highlighting broader CRNS sampling volumes and the benefit of cross-validation with local measurements.

## Data access and visualization
- Data can be accessed via the CEH EIDC, with graphs available on the COSMOS-UK live site.
- Embedding COSMOS-UK plots in websites is possible via provided URLs; sample retrievals include precipitation and radiation data.
- Delays between site data collection and graph display can occur, depending on QC and data transfer processes (often under two hours in best cases, but can be longer).

## Appendices and supporting material
- Appendix A: Expanded site list with metadata for each COSMOS-UK site (site IDs, coordinates, start dates, soils, bulk density, land cover, etc.).
- Appendix B: Period of record data availability by variable groups (MET, SOIL, VWC); data completeness by year.
- Appendix C: Phenocam images and usage notes for vegetation phenology and site screening.
- Appendix D: Standard graphical retrievals (e.g., monthly summaries, period-of-record plots, and examples of VWC/RN retrievals).
- Appendix E: Embedding COSMOS-UK data plots on websites via image URLs.
- Appendix F: Site layout details (where available).
- Appendix G: Quality control tests applied to data (detailed per parameter; references to Appendix F for variable-specific tests).

## Acknowledgements and references
- Acknowledges funding from NERC, Jungfraujoch neutron monitor data, site owners, partner organizations, and landowners.
- References include foundational papers on cosmic-ray soil moisture methods, calibration, footprints, and data processing methodologies (Zreda et al., Franz et al., Kohli et al., Desilets et al., Evans et al., etc.).