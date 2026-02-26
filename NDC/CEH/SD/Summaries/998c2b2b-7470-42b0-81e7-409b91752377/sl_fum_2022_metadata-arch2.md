# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and scope
  - Data from a 2022 ammonia (NH3) enhancement experiment in a tropical sub-montane forest (Queensberry Estate, central Sri Lanka) to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
  - Experiment designed to understand NH3 enhancement under wind-controlled conditions and to support deposition estimation in forest ecosystems.

- Experimental setup and instrumentation
  - Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693° N, 80.5911° E; altitude 1645 m.
  - NH3 release system: three horizontally aligned PVC tubes (20 m each) at 0.5, 1.35, and 2.2 m above ground; NH3 released via six evenly spaced holes per tube.
  - Gas delivery: pure anhydrous NH3 from a cylinder through a stainless steel conduit (6.35 mm diameter) into a manifold with a mass flow controller (MFC) and solenoid valve; release enabled only under specific wind conditions.
  - Wind control: release triggered when wind direction aligns with monitoring quadrats (5–75° or 185–255°) and wind speeds meet threshold (0.3–10 m/s).
  - Measurement and monitoring: below-canopy wind data via WXT536 station; NH3 flow data recorded by MFC; data logged every 20 seconds and averaged over 15-minute intervals.

- Data collection details
  - Time period: 13 March 2022 to 31 December 2022 (Sri Lanka Standard Time).
  - Data volume: 28,257 measurements.
  - Data focus: five core parameters (NH3 status, NH3 flow set point, NH3 flow, wind speed, wind direction) with associated timestamp and instrument metadata.

- Data structure and format
  - Format: CSV dataset.
  - Columns (examples):
    - Timestamp, Instrument, Manufacturer, Description (15-minute timestamps)
    - NH3_status (0 = OFF, >0 = ON) with details on the solenoid valve
    - NH3_flow_set (slpm) and NH3_flow (slpm) from the G series MFC
    - Wind_speed (ms^-1) and Wind_direction (degrees)
  - Metadata emphasizes units, instrument types, and data descriptions for each field.

- Quality control and data quality
  - Visual quality checks; removal of obvious instrument malfunctions, datalogger issues, and power-cut artifacts.
  - Gaps present due to replacement of faulty gas-control components.

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub.
  - Related literature: Deshpande et al. (2024) Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments (Atmospheric Environment).

- Relevance for environmental monitoring
  - Demonstrates a standardized approach to collecting and curating atmospheric NH3 exposure data under controlled wind conditions.
  - Provides a high-resolution dataset suitable for analyzing NH3 release dynamics, exposure assessment, and deposition modeling in forest ecosystems.
  - Aligns with broader monitoring aims to verify data quality, enable data reuse, and support cross-site environmental health analyses.