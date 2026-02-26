# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- A 2022 study at Queensberry Estate, central Sri Lanka, investigates effects of elevated atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- NH3 release is wind-controlled to target below-canopy monitoring quadrats, enabling assessment of deposition processes under specific wind conditions.
- Data collection supports analysis of ammonia deposition to forest ecosystems, with findings linked to broader research (Deshpande et al., 2024).

## Data collection and experiment design
- Location: Queensberry Estate, tropical sub-montane forest (coordinates and altitude provided).
- Release system: three 20 m long PVC tubes with holes along their length, fed by a manifold and a mass flow controller; NH3 injection via a solenoid valve using pure anhydrous NH3.
- Control logic: NH3 released only when wind direction falls within 5–75° and 185–255°, at threshold wind speeds (0.3–10 m s^-1).
- Measurement and logging: below-canopy wind data captured by a WXT536 weather station; NH3 release rate recorded by the MFC; data logged at 20-second intervals and averaged to 15-minute intervals.
- Timeframe: data collected from 13 March 2022 to 31 December 2022.
- Data provenance: complete experimental design, methodology, analysis, and findings detailed in Deshpande et al. (2024).

## Data structure and content
- Dataset size: 28,257 measurements across 5 parameters.
- Format: CSV file with structured fields, including:
  - Timestamp (SLST) and related metadata per row
  - NH3_status (0 = OFF, >0 = ON)
  - NH3_flow_set (set point for NH3 flow)
  - NH3_flow (actual flow into release manifold)
  - Wind_speed (below-canopy wind speed)
  - Wind_direction (below-canopy wind direction)
- Instrumentation metadata embedded in fields (e.g., solenoid valve type, manufacturer for NH3_status; MFC and manufacturer for flow; wind sensor details).
- Units and descriptions provided to support traceability and reproducibility.

## Quality control and data reliability
- Quality checks performed: visual inspection to remove obvious instrument malfunctions, datalogger issues, and power-cut artifacts.
- Gaps acknowledged: some missing data due to time required to replace faulty gas control components.
- Data cleaned to remove erroneous readings prior to downstream analysis.

## Data governance, access, and usage
- Data are documented with explicit metadata, instrument details, and data collection conditions to support reuse in monitoring frameworks.
- Funding acknowledged from UKRI GCRF South Asian Nitrogen Hub.
- Related reference: Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments (Deshpande et al., 2024), published in Atmos Environ.
- Encourages linkage between datasets and broader monitoring objectives, highlighting the importance of transparent data sharing, metadata completeness, and alignment with standards for environmental health monitoring.

## Limitations and considerations for monitoring frameworks
- Data limited to a 2022 campaign at a single site; applicability to other sites or longer-term trends requires careful extrapolation.
- Some data gaps due to equipment maintenance; completeness of metadata varies across fields.
- The need for robust data governance, timely data sharing, and standardized metadata to enable integration into broader monitoring dashboards and policy evaluations.