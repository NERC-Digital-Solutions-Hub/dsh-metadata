# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

- Purpose and scope
  - Ammonia (NH3) enhancement experiment conducted in the Glencorse woodland near Edinburgh to study effects of elevated atmospheric NH3 on forest vegetation, bryophytes, lichens, and soil.
  - Aims to estimate NH3 deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Dataset covers 2023 and 2024 (1 Jan 2023 to 31 Dec 2024) with data logged in Greenwich Mean Time (GMT); extension of the 2021–2022 dataset from the same site.

- Experimental design and data collection
  - Location and setup: Glencorse woodland (Birch plantation) at 55.8539°, -3.2151°, altitude 200 m.
  - NH3 release system: three 20 m long, 110 mm OD PVC tubes configured to release NH3 through six holes around each tube, spaced along the length.
  - Control logic: NH3 release triggered by wind conditions (275–345° direction with threshold wind speeds of 0.3–10 m/s) measured below the canopy.
  - Gas delivery: NH3 supplied from a cylinder via a manifold, with a mass flow controller (MFC) and solenoid valve; NH3 release enabled only when wind criteria are met.
  - Measurement and logging: below-canopy wind data (speed and direction) from a WXT536 weather station; NH3 release volume recorded every 20 seconds and averaged over 15-minute intervals.
  - Data coverage: 68,396 measurements across 5 parameters, stored in a CSV with detailed per-variable metadata.

- Data fields and structure
  - Timestamp (15-minute intervals in format dd/mm/yyyy hh:mm)
  - NH3_status (minutes): time NH3 is released
  - NH3_flow_set (slpm): NH3 flow set point for the wind conditions
  - NH3_flow (slpm): NH3 flow through the MFC into the release manifold
  - Wind_speed (ms^-1): below-canopy wind speed
  - Wind_direction (degrees): wind direction (below canopy)
  - Each parameter includes instrument and manufacturer metadata (e.g., solenoid valve, Bürkert; MFC, MKS Instruments; wind sensor, Vaisala)

- Quality control and data integrity
  - Data visually checked; obvious instrument malfunctions, datalogger issues, and power cuts removed.
  - Some gaps occurred due to replacement of faulty gas control components.

- Data governance, metadata and accessibility
  - Dataset provides comprehensive instrument-level metadata, enabling traceability of measurements.
  - The data are presented alongside related publications and data centre references for context and reuse (e.g., NERC EDS Environmental Information Data Centre).
  - Funding acknowledges UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub; UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
  - References:
    - Deshpande et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ., 2024a.
    - Deshpande et al. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Glencorse, UK, 2021-2022, NERC EDS Environmental Information Data Centre, 2024b.

- Implications for monitoring frameworks
  - Demonstrates a tightly controlled, wind-driven experimental approach to generate policy-relevant NH3 deposition data.
  - Highlights the importance of detailed metadata, calibration of instruments, and clear data processing (15-minute aggregation) for building trust in monitoring outputs.
  - Illustrates how such structured datasets can support model development, validation, and evaluation of environmental policy decisions related to air-nutrient deposition and forest health.
  - Reflects common challenges for monitoring frameworks: maintaining data quality, ensuring timely data sharing, minimizing data silos, and providing transparent governance and metadata to enable reuse.