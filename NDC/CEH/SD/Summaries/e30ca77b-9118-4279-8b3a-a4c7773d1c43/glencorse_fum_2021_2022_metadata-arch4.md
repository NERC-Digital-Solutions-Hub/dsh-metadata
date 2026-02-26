# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Purpose: Ammonia (NH3) enhancement experiment to study effects on forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland near Edinburgh (coordinates 55.8539°, -3.2151°, altitude ~200 m).
- Timeframe: 16 September 2021 to 5 January 2023 (GMT data).
- Data scope: 45,538 NH3-related measurements across 5 parameters.
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Reference: Deshpande et al. (2024), Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.

## Data collection and dataset structure
- NH3 enhancement system:
  - Three 20 m long tubes with 110 mm diameter, positioned at 0.5, 1.35, and 2.2 m above ground.
  - NH3 released through holes at 20 cm intervals along each tube.
  - Release controlled by wind conditions: occurs when wind direction is 275–345 degrees and wind speed is 0.3–10 m/s.
  - Delivery via a central fan, a stainless steel manifold, a mass flow controller (MFC), and a solenoid valve.
- Measurement cadence:
  - NH3 flow volume recorded every 20 seconds; 15-minute averages compiled.
  - Wind data collected below-canopy by a WXT536 weather station.
- Data format and fields (CSV):
  - Timestamp (GMT), various descriptor fields, and 5 core parameters:
    - NH3_status (0 = OFF, >0 = ON)
    - NH3_flow_set (set point in slpm)
    - NH3_flow (actual flow in slpm)
    - Wind_speed (ms^-1)
    - Wind_direction (degrees)
  - accompanying metadata for each field: instrument, manufacturer, and description.
- Data granularity: 15-minute timestamps for the 45,538 measurements.

## Data quality, provenance and limitations
- Quality control: visual checks; removal of obvious instrument malfunctions, datalogger programming issues, and power-cut artifacts.
- Gaps: some interruptions due to replacement of faulty gas-control components.
- Time and units: all data recorded in GMT; wind and NH3 measurements tied to the same release gating logic.

## Metadata, discoverability and usage
- Dataset is provided as a CSV with explicit column descriptions, units, and instrument details to support reuse and provenance tracking.
- Clear data lineage: instrumentation (MFC, solenoid valve, WXT536), release logic, and data processing (20 s measurements, 15 min averages).

## Relevance for data leadership and governance
- Demonstrates end-to-end data lifecycle management: instrument provenance, controlled data collection, rigorous QC, and detailed metadata for discoverability and reuse.
- Aligns data collection with research questions through explicit gating by wind conditions, enabling transparent assessment of NH3 deposition studies.
- Highlights the importance of metadata richness (units, instrument names, descriptions) and time-standardization (GMT) to support collaboration across networks and communities.
- Provides a model for documenting data sources, handling gaps, and ensuring traceability and potential for future data products or meta-analyses.