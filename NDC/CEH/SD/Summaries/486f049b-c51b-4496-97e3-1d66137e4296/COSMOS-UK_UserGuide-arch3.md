# COSMOS-UK User Guide

- Overview
  - Aims to deliver soil moisture data across the UK in near real-time using cosmic-ray neutron sensors (CRNS), enabling improved meteorological models, water resource information, flood warnings, crop planning, and broader environmental science applications.
  - Data are obtained from a network of automated, non-invasive sites; outputs include both raw and derived data, with ongoing research to refine calibration and interpretation.

- Network and Site Context
  - COSMOS-UK established in 2013 to provide UK-wide soil moisture data; aims to expand sites and services.
  - Site selection focuses on representing diverse UK conditions (climate, soil, land cover, geology) and enabling inter-site comparisons across local, regional, and national scales.
  - Factors considered in site selection include geographic coverage, environmental variables, soil moisture variability, existing monitoring, long-term access, ease of access, vandalism risk, and mobile network coverage.
  - The guide lists numerous sites with start dates and properties; Appendix A provides expanded site details.

- Instrumentation and Data Sources
  - Core instrument: Cosmic-Ray Neutron Sensor (CRNS) that counts fast neutrons; counts are converted to soil moisture after field calibration, with corrections for atmospheric pressure, humidity, and cosmic ray intensity.
  - Supporting instruments across sites include:
    - Rain gauge (OTT Pluvio²)
    - Point soil moisture sensors (TDT; multiple depths)
    - Profile soil moisture sensors (multi-depth TDT in one access tube)
    - Soil heat flux plates
    - Soil temperature sensors
    - Radiometer (four-component)
    - Automatic weather station (temperature, humidity, pressure)
    - Barometric pressure sensor
    - Temperature/humidity sensors
    - 3D and integrated sonic anemometers
    - Phenocam (vegetation and surface conditions)
    - Snow depth and snow water equivalent sensors
    - Data logging and communication equipment
  - Instrument installation varies by site (Table 3.2 indicates presence/absence per site).

- Data Types and Outputs
  - Monitored data (Table 4.1): precipitation, humidity (absolute and relative), air temperature, atmospheric pressure, radiation components (shortwave/longwave; incoming/outgoing), wind (speed, direction, 3D), snow depth/SWE, soil volumetric water content (VWC) from IMKO profile, and soil moisture from TDT sensors (depths 15, 40, 65 cm).
  - Derived data (Table 4.2): net radiation, CRNS-based VWC (and daily vs hourly), typical CRNS footprint depth (D86), corrected neutron counts, and potential evaporation (Penman-Monteith).
  - Data are subject to ongoing quality control and may evolve with processing changes and data processing updates.

- Access, Licensing and Use
  - Data are accessible via the CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk; data are uploaded in annual batches and may lag by 1–2 years behind current date.
  - Data requests for non-available data may be considered if reasonable in effort required.
  - Data are provisional and may be revised; data are supplied under a license specifying usage terms.
  - Visualizations and standard graphs are available on the COSMOS-UK live data page; Appendix D provides examples of standard graphical retrievals.
  - For collaboration or further opportunities, data providers welcome inquiries.

- Data Processing, Quality Control and Gaps
  - Processing is required to ensure data quality and to derive VWC from CRNS counts; raw data are automatically processed into level-2 data after quality checks.
  - Quality control (Section 6.1; Appendix G):
    - Automatic QC tests (level 1 to level 2) for each variable (e.g., zero data, too few samples, low power, sensor fault, out-of-range, spikes, diagnostic flags, error codes).
    - Daily visual inspection of data via automatically generated plots.
  - Gaps: No automatic gap-filling is currently implemented (Section 6.2); missing data may be retrieved by site visits in some cases.
  - Data processing philosophy emphasizes consistency; when processing methods change, all historical data are updated to maintain uniformity across the time series.

- CRNS to Soil Moisture: Methodology and Considerations
  - Counts are corrected for background cosmic ray intensity, altitude, atmospheric pressure, and atmospheric water vapor to yield corrected counts.
  - Soil moisture is derived using one of three methods; COSMOS-UK uses site-specific N0 calibration with a generic silica soil base calibration, and accounts for lattice water and soil organic carbon.
  - The CRNS-derived VWC is a depth-averaged value due to neutron penetration; typical effective depth varies with soil moisture and can range from shallow to tens of centimeters.
  - Noise in CRNS data is significant; hourly values can be unreliable, so averaging (6-hour or daily) is recommended to reduce noise.
  - Processing refinements (by late 2016) improved daily VWC data quality, especially at peat soils where high VWC values were problematic; subsequent revisions further reduced out-of-range daily values.
  - D86 and footprint considerations:
    - Earlier assumptions about a fixed footprint depth/size were revised; a six-distance D86 approach (1, 5, 25, 75, 150, 200 m) is used to characterize depth penetration, though a single indicator (75 m) is often used for illustration.
    - The footprint is non-uniform, with most neutrons originating from the closest meters to the sensor; peat soils and high organic content influence bulk density and effective depth calculations.
  - Correction factor gamma (F_i):
    - Historically gamma was unity; since 2018, site-specific gamma values are derived empirically to address spurious trends and sensor differences, improving consistency across sensors and sites.
  - Methodological evolution:
    - When processing changes occur, they are applied retroactively to all sites to maintain consistency; legacy processing may continue in the background.
  - Cross-validation with TDT sensors:
    - TDT probes provide higher-frequency, less noisy soil moisture measurements at shallow depths; comparisons show broad agreement with CRNS trends but differences exist due to sampling volumes and depths.

- Data Quality, Uncertainty and Guidance for Use
  - CRNS data are noisy; daily mean VWC is generally more reliable than hourly values.
  - Peat soils pose challenges; high VWC values require caution and careful interpretation.
  - TDT sensors offer more reliable short-term comparisons at near-sensor scale; CRNS provides larger-scale soil moisture context and integrates moisture from a wider area.
  - Users should review quality flags and consider data processing histories when interpreting time series; use of daily means is encouraged for robust analyses.

- Visualization and Embedding
  - Standard graphs and dashboards are accessible; examples and embedding options are provided (Appendix E with example URLs for embedding plots on websites).
  - LIVE data graphs have slight delays due to processing and data transfer pipelines.

- Acknowledgements and References
  - Acknowledges funding (NERC) and partner organizations; extensive references detailing CRNS methodology and calibration processes.

- Practical Takeaways for Monitoring Framework Authors
  - COSMOS-UK demonstrates a UK-wide, real-time soil moisture monitoring approach using CRNS with a broad site network designed to capture diverse environmental conditions.
  - Data types span meteorology, soil moisture across depths, surface energy balance components, and derived evaporation metrics, enabling integrated environmental health assessments.
  - Emphasizes the importance of metadata, data provenance, and transparent data governance (provisional data, licensing, versioning).
  - Highlights challenges relevant to monitoring frameworks: data gaps, data access delays, siloing across institutions, the need for robust metadata, data transformation requirements, communication of complex results, and implementation of data governance for sharing and updating datasets.
  - Processing evolution and calibration strategies illustrate how methodological changes can affect long-term time series; governance around versioning and retroactive updates is critical for policy-relevant monitoring.
  - The approach includes cross-instrument validation (CRNS with TDT sensors) to enhance confidence in soil moisture assessments across spatial scales.
  - For policy and decision-making, the guide underscores the value of large-area, open, near-real-time environmental data while acknowledging barriers such as peat-soil behavior, data quality flags, and the need for clear guidance on data suitability for specific applications.