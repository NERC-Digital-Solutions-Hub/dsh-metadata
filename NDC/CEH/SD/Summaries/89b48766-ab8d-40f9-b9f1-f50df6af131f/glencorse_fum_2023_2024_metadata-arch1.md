# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

- Purpose and context
  - Study of how high atmospheric ammonia (NH3) affects forest vegetation, bryophytes, lichens, and soil.
  - Extension of a 2021-22 dataset from the same Glencorse site; aimed at deposition estimation and related analyses.

- Study site
  - Glencorse woodland, near Edinburgh, coordinates 55.8539° N, -3.2151° W; altitude ~200 m.
  - Birch plantation used for the enhancement experiment.

- NH3 release system and control
  - NH3 released only when wind direction is 275–345 degrees and wind speed is 0.3–10 m/s.
  - Release occurs from three parallel 20 m tubes at heights 0.5, 1.35, and 2.2 m.
  - NH3 delivered from a cylinder via stainless steel pipe, mass flow controller (MFC), and solenoid valve; fan creates positive pressure in the tubes.
  - Wind data measured below canopy; NH3 flow limited by wind and controlled by the system.

- Data collection and variables
  - Data collected at 15-minute intervals; 68,396 measurements across 2023–01–01 to 2024–12–31 (GMT).
  - Primary variables in the CSV:
    - Timestamp (15-minute intervals)
    - NH3_status: time NH3 is released (minutes)
    - NH3_flow_set: NH3 flow setpoint (slpm)
    - NH3_flow: NH3 flow through the MFC into the release manifold (slpm)
    - Wind_speed: below-canopy wind speed (ms^-1)
    - Wind_direction: wind direction (degrees)
  - Data structure includes metadata fields such as instrument and manufacturer for traceability.

- Quality control and data integrity
  - Visual QA to remove obvious instrument malfunctions, logger issues, and power-outages.
  - Gaps occur due to replacement of faulty gas-control components.

- Data format and access
  - Data provided as a CSV file with 68,396 rows and 5 key measurements plus timestamps and supporting metadata.
  - Times are recorded in Greenwich Mean Time (GMT).

- Related work and references
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments (Atmospheric Environment).
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Glencorse site, 2021–2022 (NERC EDS Environmental Information Data Centre).

- Funding
  - UKRI GCRF South Asian Nitrogen Hub
  - UKCEH National Capability for UK Challenges Programme NE/Y006208/1