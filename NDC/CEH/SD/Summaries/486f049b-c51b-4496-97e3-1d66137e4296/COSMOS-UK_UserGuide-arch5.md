# COSMOS-UK User Guide

- Overview and aims
  - COSMOS-UK delivers soil moisture data in near real-time across the UK using cosmic-ray neutron sensors (CRNS), covering large spatial footprints (tens to hundreds of meters radius; up to ~12 hectares).
  - Intended to support applied environmental research, weather and climate models, water resources planning, flood risk, and ecosystem studies; aims to enable data-driven insights and model validation.
  - Emphasizes governance, data quality, and accessible information services for a wide user base.

- Network, sites, and governance
  - Established 2013; aims to expand with a UK-wide network sampling diverse conditions (land cover, soils, climate, geology).
  - Site list provides start dates, coordinates, elevations, and calibration status; Appendix A expands site properties.
  - Site selection criteria balance coverage, representativeness, collaboration potential, long-term access, ease of access, and risk factors (e.g., vandalism, water proximity, mobile coverage).

- Instrumentation and data streams
  - Core instrument: Cosmic-Ray Neutron Sensor (CRNS) for soil moisture; counts fast neutrons, corrected for atmospheric pressure, humidity, and cosmic ray intensity.
  - Additional sensors: rain gauge, TDT soil moisture sensors (depths around 10–30 cm), profile soil moisture sensor (0.15, 0.40, 0.65 m), soil heat flux plates, soil temperature at multiple depths, radiometer, automatic weather station (temperature, humidity, pressure), phase 3 barometric and temperature/humidity sensors, 3D and integrated 2D sonic anemometers, phenocam, snow depth and snow water equivalent, data loggers (Micrologger).
  - Data availability depends on site configuration; not all instruments present at every site (Table 3.2).

- Available data and data products
  - Monitored data (Tables 4.1): precipitation, absolute and relative humidity, air temperature, atmospheric pressure, incoming/outgoing shortwave and longwave radiation, wind (speed and direction), snow depth, snow water equivalent, and soil moisture (CRNS-derived volumetric water content, VWC; profile and TDT-based VWC at multiple depths).
  - Derived data (Table 4.2): net radiation, CRNS-derived VWC, corrected neutron counts, potential evaporation.
  - Temporal resolution: most data at 30-minute intervals; precipitation at 1-minute intervals; site-specific processing may yield hourly equivalents for CRNS-derived products.
  - Data streams are provisional and subject to ongoing quality control and methodological updates.

- Access, licensing, and data management
  - Primary data access via the CEH Environmental Information Data Centre (EIDC) at eidc.ceh.ac.uk.
  - Data uploaded in annual tranches; period behind the current upload by approximately 1–2 years (e.g., 2018 data may cover up to 2016).
  - Data provided under a licence with terms governing exploitation; provisional status acknowledged and liability limited.
  - Data requests outside EIDC are considered on a reasonable-effort basis.
  - Live data and standard graphical retrievals are available on the COSMOS-UK website; Appendix D demonstrates typical retrievals.

- Data processing, quality control, and lineage
  - Purpose of processing: convert CRNS neutron counts to soil moisture (VWC) and generate derived data; apply corrections for cosmic ray flux, altitude, atmospheric conditions, and soil properties.
  - Processing approach: multiple methods exist (site-specific N0 calibration, universal hydrogen molar fraction, neutron transport models); COSMOS-UK currently uses site-specific N0 calibration with field-calibrated reference soil moisture.
  - Quality control (Section 6.1; Appendix G): two-stage process
    - Level 1: automatic QC tests applied to variables; failing data removed from level-2 dataset.
    - Level 2: daily visual QC using plots; data labeled LEVEL1 or LEVEL2 for traceability.
  - Data processing notes:
    - Some datasets represent derived values (e.g., VWC from CRNS) that require averaging to reduce noise.
    - Aggregation rules allow for some missing hourly values when deriving daily means.
    - Peat soils can introduce higher VWC variability and greater processing challenges.
  - Gap filling (Section 6.2): currently no automatic gap-filling performed; missing data may be retrievable by site visits or later QC passes.

- CRNS data specifics and methodological evolution
  - 7.1–7.2: Cosmic-ray interactions and neutron moderation; corrected counts depend on reference monitors; three methods exist for converting counts to VWC; COSMOS-UK uses a field-calibrated reference moisture plus a site-specific calibration parameter.
  - 7.3–7.5: Noise mitigation and daily averaging improvements; early methods filtered out out-of-range values (>100% or <0%), which produced gaps; revised daily-averaging method reduces unrealistics and increases data availability (notably at peat-rich sites).
  - 7.6–7.7: Revised effective-depth estimation (D86 distances) and a new site-specific correction factor (gamma) introduced in 2018 to remove spurious trends; processing revisions applied retroactively across the complete data series for consistency.
  - 7.8: CRNS counts are noisy; comparison with TDT sensors shows general agreement but with site- and time-dependent discrepancies due to differing sampling volumes and depths; ongoing validation and objective analyses planned.

- Footprint, depth, and interpretation considerations
  - CRNS samples a relatively large footprint; effective depth and soil moisture estimates depend on moisture and distance from the sensor.
  - Visualization and interpretation guidance emphasize careful treatment of peat vs mineral soils, spatial heterogeneity, and potential contributions from surface water or vegetation to neutron counts.

- Data quality, documentation, and user guidance
  - Data are provisional and may be revised with further quality control and processing updates.
  - Users are cautioned about data gaps, potential anomalies, and the influence of soil type (peat vs mineral) on VWC estimates.
  - Standard graphical retrievals and embedded plots are provided to assist quick-look assessment; more comprehensive analyses and documentation are planned.

- Appendices and additional resources (for data stewardship and governance)
  - Appendix A: Expanded site list with calibration and soil properties.
  - Appendix B: Data availability and completeness by year.
  - Appendix C: Phenocam imagery and purpose (vegetation phenology, ground conditions).
  - Appendix D: Standard graphical retrievals and example plots.
  - Appendix E: Embedding COSMOS-UK plots in external websites.
  - Appendix F–G: Technical details on quality control tests and data validation.
  - Acknowledgments and references documenting methodology and prior work.

- Practical implications for data stewards
  - Ensure metadata completeness: site characteristics, calibration status, soil properties, land cover, and instrumentation at each site.
  - Monitor data provenance and versioning: processing method changes are applied across all sites; track which datasets reflect which processing version.
  - Manage data access and licensing: align usage with EIDC licence terms; communicate provisional status to data users.
  - Maintain governance around data quality: ongoing QC procedures, explicit documentation of changes to processing algorithms and calibration.
  - Plan for interpretation challenges: peat soils require cautious use; account for large CRNS footprints when aligning with point-scale or profile measurements.
  - Facilitate reproducibility: publish processing steps, calibration parameters (N0, gamma), and decision rules for averaging and flagging; provide clear data lineage and change logs.