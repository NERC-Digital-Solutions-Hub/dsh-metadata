# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

- Overview
  - Purpose: Data from an ammonia (NH3) enhancement experiment to study effects on forest vegetation, bryophytes, lichens, and soil.
  - Scope: 2023–2024 data, extending the 2021–2022 dataset from the same site.
  - Location: Glencorse woodland, near Edinburgh; coordinates 55.8539 N, -3.2151 W; altitude 200 m.

- Data collection and experimental setup
  - NH3 release system: Three 20 m long tubes (0.5, 1.35, 2.2 m above ground) with holes every 20 cm around the tube circumference.
  - Release mechanism: NH3 delivered from a cylinder via a manifold, mass flow controller (MFC), and solenoid valve; a central fan creates positive pressure to inject NH3 into the airflow.
  - Control logic: NH3 release permitted only when wind direction is 275–345 degrees and wind speeds meet predefined thresholds (0.3–10 m/s).
  - Monitoring: Below-canopy wind data from a WXT536 weather station; NH3 released volumes recorded by the MFC every 20 seconds, averaged to 15-minute intervals.
  - Timeframe: Data cover 1 January 2023 to 31 December 2024; all times in GMT.

- Data structure and variables
  - Format: CSV with 68,396 measurements across 5 parameters.
  - Key columns and meanings (examples):
    - Timestamp: 15-minute intervals (dd/mm/yyyy hh:mm) in GMT.
    - NH3_status: Minutes NH3 is released; captured via solenoid valve (Type 6027; Bürkert).
    - NH3_flow_set: NH3 flow set point for the prevailing wind conditions (slpm); MFC (G series, MKS Instruments).
    - NH3_flow: Actual NH3 flow through the MFC into the release manifold (slpm).
    - Wind_speed: Below-canopy wind speed (ms-1; WXT536; Vaisala).
    - Wind_direction: Below-canopy wind direction (degrees).
  - Instrument and manufacturer details embedded in the dataset (e.g., NH3_status, NH3_flow_set, NH3_flow, Wind_speed) for traceability.

- Data quality and processing
  - Quality control: Visual checks with removal of obvious instrument malfunctions, datalogger issues, and power-cut artifacts.
  - Gaps: Some gaps remain due to time required to replace faulty gas-control components.

- Spatial and temporal context for GIS
  - Temporal coverage: 2023-01-01 to 2024-12-31; data expressed in GMT and aligned to 15-minute intervals.
  - Spatial context: Fixed experimental site coordinates; suitable for spatial mapping of NH3 release events and related wind conditions.
  - Potential GIS use: Visualise NH3 release timing alongside wind speed/direction; analyze deposition potential and exposure patterns across the study area.

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
  - References:
    - Deshpande et al. 2024a: Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
    - Deshpande et al. 2024b: Meteorological data and ammonia concentration and deposition rates from Glencorse site, 2021-2022.
  - Data access: Datasets and related methodology details published in Atmos. Environ. 2024a and NERC EDS Environmental Information Data Centre 2024b (DOIs provided in the references).