# COSMOS-UK User Guide

- The COSMOS-UK project provides near real-time soil moisture data from a UK-wide network using cosmic-ray neutron sensing, offering a large, non-invasive measurement footprint (up to tens-hundreds of meters) to support environmental monitoring, meteorology, water resources, flood forecasting, crop management, and greenhouse gas studies.
- Outputs are designed for consistent, scrubbed formats suitable for model validation, policy evaluation, and cross-site comparisons, with data stored and served through CEH’s Environmental Information Data Centre (EIDC).

## 1) Purpose and role for environmental monitoring
- Delivers near real-time soil moisture data to improve weather, flood, drought, and agricultural applications.
- Enables large-scale, area-integrated soil moisture estimates, complementing point sensors and remote sensing.
- Supports integration with models, validation of remote sensing products, and understanding soil moisture dynamics and carbon cycling.

## 2) Network and site selection
- UK-wide array of monitoring sites designed to capture diverse climate, soil, land cover, and topography.
- Site selection factors (with positive/negative influences) include: geographic coverage, environmental variables, high soil moisture variability, existing monitoring activity, data assimilation opportunities, proximity to open water (negative), long-term permission, accessibility, vandalism risk, and mobile network coverage.
- Sites listed with start dates, calibration status, coordinates, altitude, and soil/land-cover characteristics; ongoing expansion and updates planned.

## 3) Instrumentation
- COSMOS-UK uses a suite of instruments; not all are installed at every site. Key instruments include:
- Cosmic-Ray Neutron Sensor (CRNS): measures fast neutrons to infer soil moisture after field calibration; large footprint; typical effective depth ~15–40 cm, expands with soil moisture.
- Rain gauge (OTT Pluvio²): precipitation measurement with temperature/wind corrections.
- Point soil moisture sensors (TDT): time-domain transmissometry at 10 cm and other depths; provide absolute volumetric water content (VWC).
- Profile soil moisture sensor (IMKO PICO-PROFILE): deeper TDT measurements at multiple depths.
- Soil heat flux plates (Hukseflux HFP01SC): determine soil heat flux at 0.03 m.
- Soil temperature sensors: multiple soil depths (2, 5, 10, 20, 50 cm).
- Radiometer: four-component solar radiation and longwave radiation sensors; net radiation derived.
- Automatic weather station: air temperature, relative humidity, barometric pressure.
- Barometric pressure sensor, temperature/humidity sensors, 3D/2D sonic anemometers.
- Phenocam: vegetation and land-cover imagery for phenology; snow/ponding/cloud screening.
- Snow depth and Snow Water Equivalent sensors.
- Data loggers (Micrologger) and communication hardware for remote data transmission.
- Instrumentation varies by site; Tables list which devices are at which site.

## 4) Available data
- Monitored data (with units and recording intervals):
  - Precipitation (mm, 1 min), Absolute humidity (g/m3, 30 min), Relative humidity (% 30 min), Air temperature (°C, 30 min), Atmospheric pressure (hPa, 30 min), Incoming/outgoing shortwave and longwave radiation (W/m2, 30 min), Wind direction (degrees, 30 min), Wind speed (m/s, 30 min), 3D wind components (30 min), Snow depth (mm), Snow water equivalent (mm), Volumetric water content from IMKO profiles (30 min), Soil heat flux (W/m2, 30 min), Soil temperature at five depths (°C, 30 min), TDT soil temperature and VWC at multiple depths (30 min).
- Derived data:
  - Net radiation (derived), Volumetric water content from CRNS (COSMOS_VWC; hourly/daily), Corrected CRNS neutron counts, D86 (depth corresponding to 86% of detected neutrons, at multiple distances), Potential evaporation, and other product as noted.
- Data access and formats:
  - Data are available via the CEH Environmental Information Data Centre (EIDC). Data are provisional and may be revised after quality control.
  - Data are uploaded in annual tranches and can be requested if not available in EIDC.
  - Live graphs and standard retrievals are available on the COSMOS-UK website; data can also be embedded in external sites via provided tools.
  - Data licensing governs usage; requests for data not in EIDC may be considered.

## 5) Accessing COSMOS-UK data
- Primary data portal: CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk.
- Data are uploaded in annual releases; typical lag is 1–2 years behind the upload date (e.g., 2018 data for 2016 data).
- Provisional data and quality-controlled Level 2 datasets are supplied; licensing terms apply.
- Live graphing and standard graphical retrievals available on the COSMOS-UK website; embedding tools provided for website integration.
- Data requests can be made via cosmosuk@ceh.ac.uk; collaboration opportunities encouraged.

## 6) Data processing and quality control
- Processing ensures data quality and enables derived variables (notably CRNS-based VWC).
- Data processing steps include calibration, atmosphere/pressure/humidity corrections, aggregation, and deriving VWC from CRNS counts.
- Gap filling: currently no automatic gap-filling; gaps may be filled later by site visits or manual QC, but the standard practice is to report gaps.
- Quality control (two-stage):
  - Level 1 QC: automatic QC tests applied to specific variables; failing data are removed from level-2 dataset.
  - Level 2 QC: daily visual inspection of plots derived from the data; raw data remain accessible.
- QC tests cover zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range values, secondary variable dependencies, spikes, and logger error codes (see Appendix G and Table 6.1 for details).

## 7) Data processing specifics for CRNS (cosmic-ray soil moisture)
- Cosmic-ray basics: high-energy particles create secondary neutrons; hydrogen content (water) moderates neutrons; more soil moisture yields fewer detected fast neutrons.
- Conversion to soil moisture:
  - Recorded counts are corrected for atmospheric pressure, altitude, and humidity (reference calibration at a high-altitude site).
  - Three methods exist; COSMOS-UK uses the site-specific N0 calibration with a field reference soil water content, adjusted by a silica soil matrix constant and corrections for lattice/ bound water and soil organic carbon.
- Averaging and noise:
  - CRNS-derived VWC is noisy; hourly values are often censored and averaged to daily means to improve reliability.
  - Daily means reduce noise; early processing yielded some VWC > 100% or <0%; revised processing reduces these issues but peat soils remain challenging.
  - Methods have evolved; late-2016 changes increased daily data availability (from ~84% to ~92% on average; peat soils show larger gains).
- CRNS footprint and effective depth:
  - Sensor footprint is large; 50% of neutrons may originate within ~50 m; the effective depth of penetration varies with wetness (10 cm to ~80 cm).
  - D86 values (distance-based depth proxy) are used to describe penetration; 75 m D86 is used as a representative indicator for comparisons.
- Revised processing and corrections:
  - A revised daily averaging method reduces out-of-range VWC values.
  - A revised effective depth estimation strategy (D86 at multiple distances) provides a more nuanced footprint description.
  - A new correction factor gamma (γ) accounts for geomagnetic and sensor differences; a site-specific γ was introduced in 2018 to remove spurious trends.
  - When processing method changes, the entire dataset is updated to maintain consistency.
- Comparison with other sensors (TDT):
  - CRNS is noisy, but TDT sensors provide more stable local measurements; comparisons show broad agreement but differences exist due to sampling volumes and temporal/spatial scales.
  - The CRNS often captures broader soil moisture conditions around the sensor than a single TDT probe.
- Practical implications:
  - The data require careful interpretation; peat soils show higher VWC and more sensitivity to processing choices; mineral soils yield more reliable daily VWC.
  - Users should consult documentation on processing methods and be cautious with high VWC values, especially in peat-dominated sites.

## 8) Data quality, limitations, and guidance
- The CRNS method introduces noise; daily averaging and site-specific calibration are essential for reliable VWC values.
- Peat soils pose particular challenges due to high organic matter and variable bulk density; use peat-site data with caution.
- Data gaps can occur from instrument faults, logging, or QC passes; gaps may be manually filled in some cases but not automatically.
- Changes in data processing (e.g., VWC calculation, depth estimation, gamma correction) are applied across all sites to maintain consistency; legacy processing may still be active in the background.

## 9) Appendices and additional resources
- Appendix A: Expanded site list with installation dates, coordinates, soil and land-cover descriptions.
- Appendix B: Period of record data availability by year for data completeness (met, soil, VWC groups).
- Appendix C: Phenocam imagery overview and implementation details for vegetation phenology and site screening.
- Appendix D: Standard graphical retrievals (examples of plots, e.g., monthly summaries, period-of-record plots).
- Appendix E: Embedding COSMOS-UK data plots on external websites via provided image graph URLs.
- Appendix F/G: Quality control tests and data availability details.
- References: Key literature supporting the methods and calibration approaches.