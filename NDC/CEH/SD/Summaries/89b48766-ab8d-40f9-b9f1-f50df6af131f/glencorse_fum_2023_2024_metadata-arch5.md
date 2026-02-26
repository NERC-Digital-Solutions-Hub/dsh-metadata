# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

## Purpose and Context
- Study of effects of elevated atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Experiment conducted in Glencorse woodland near Edinburgh; aim to quantify NH3 deposition under controlled enhancement.
- Ammonia release is wind-controlled to occur only when wind direction is toward monitoring quadrats (275–345 degrees) at threshold speeds (0.3–10 m s^-1).

## Study Site and Experimental Design
- Location: Glencorse woodland (55.8539°N, -3.2151°W), altitude 200 m.
- Setup: NH3 released from three parallel 20 m tubes at heights 0.5, 1.35, and 2.2 m.
- Release mechanism: NH3 from a cylinder via a mass flow controller (MFC) and solenoid valve, injected into a central airflow produced by a fan.
- Monitoring and control: Wind data from a WXT536 weather station; NH3 release is gated by wind direction and speed thresholds.
- Context: This dataset extends the 2021–22 data from the same site (Deshpande et al., 2024b) and supports analyses in Deshpande et al. 2024a ( Atmos. Environ., 2024a) and related data centre entries (2024b).

## Data Collection and Timeline
- Timeframe: 1 January 2023 – 31 December 2024.
- Data recorded: 68,396 measurements across five NH3/meteorological parameters.
- Data format: CSV file with time-stamped records (GMT).
- Instrumentation and data flow:
  - NH3 release status (NH3_status): duration of NH3 release per interval.
  - NH3_flow_set: NH3 flow set point for prevailing wind conditions (slpm).
  - NH3_flow: actual NH3 flow through the MFC into the release manifold (slpm).
  - Wind_speed: below-canopy wind speed (ms^-1).
  - Wind_direction: below-canopy wind direction (degrees).
- Data provenance: complete experimental design and methodology described in associated publications (Deshpande et al. 2024a; 2024b).

## Data Structure and Metadata
- Dataset: CSV with 68,396 rows and five primary measured variables plus time metadata.
- Columns include:
  - Timestamp (dd/mm/yyyy hh:mm, GMT)
  - NH3_status (minutes; solenoid valve Type 6027, Bürkert)
  - NH3_flow_set (slpm; MKS Instruments)
  - NH3_flow (slpm; MKS Instruments)
  - Wind_speed (ms^-1; Vaisala WXT536)
  - Wind_direction (degrees)
  - Additional instrument/manufacturer metadata fields accompany each parameter
- Metadata notes:
  - Time is provided in GMT.
  - Units are specified per column.
  - Data are subject to quality control applied post-collection.

## Quality Control and Data Gaps
- Visual quality checks performed; obvious instrument/malfunction errors removed.
- Some gaps occurred due to replacement of faulty gas-control components.
- Data cleaned for instrument programming issues and power interruptions; remaining gaps reflect operational maintenance.

## Data Availability and Provenance
- Data collection funded by UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).
- Associated publications and data centre records provide full methodological details and deposition context:
  - Deshpande et al. 2024a (Atmospheric Environment) – estimation of ammonia deposition to forest ecosystems.
  - Deshpande et al. 2024b – meteorological data and ammonia concentration/deposition rates at Glencorse (2021–2022).
  - NERC EDS Environmental Information Data Centre entry for 2021–2022 data (DOI provided in 2024b).

## Related Resources and References
- Deshpande, A.G., et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos. Environ., 2024a. DOI: 10.1016/j.atmosenv.2023.120325
- Deshpande, A.G., et al. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Glencorse, UK, 2021-2022. NERC EDS Environmental Information Data Centre, 2024b. DOI: 10.5285/e30ca77b-9118-4279-8b3a-a4c7773d1c43

## Funding
- UKRI GCRF South Asian Nitrogen Hub
- UKCEH National Capability for UK Challenges Programme NE/Y006208/1