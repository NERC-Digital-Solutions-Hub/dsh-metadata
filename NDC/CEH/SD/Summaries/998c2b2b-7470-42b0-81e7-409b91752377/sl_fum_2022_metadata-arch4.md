# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- A 2022 ammonia (NH3) enhancement experiment conducted in a tropical sub-montane forest at Queensberry Estate, central Sri Lanka, to study NH3 effects on vegetation, bryophytes, lichens, and soil.
- Location coordinates: 6.9693°, 80.5911°; altitude 1645 m.
- Focus: controlled NH3 release under specific below-canopy wind conditions to assess deposition and ecosystem responses.
- Data scope: 28,257 measurements captured in 2022, provided as a CSV with detailed per-parameter metadata.

## Data collection and experimental setup
- NH3 enhancement system: three parallel 20 m PVC tubes with holes distributed along their length, releasing NH3 through a central manifold driven by a fan.
- NH3 source and control: pure anhydrous NH3 delivered from a cylinder via a mass flow controller (MFC) and solenoid valve; NH3 release enabled only when wind direction is within 5–75° and 185–255° sectors and wind speeds are within 0.3–10 m s^-1.
- Monitoring and gating: wind data collected by a WXT536 weather station; NH3 flow and release status recorded by the MFC and solenoid valve configuration.
- Data cadence: NH3 release volume logged every 20 seconds; 15-minute averages computed thereafter.
- Timestamp standard: Sri Lanka Standard Time (SLST); data span 13 March 2022 to 31 December 2022.
- Data details: complete experimental design, methodology, analysis, and findings available in Deshpande et al. (2024).

## Data quality and structure
- Quality control: visual checks to remove obvious instrument errors; exclusions due to datalogger problems and power outages; some gaps from replacing faulty gas-control components.
- Dataset size and format: 28,257 measurements; CSV with the following columns (each with instrument, manufacturer, and description fields):
  - Timestamp (dd/mm/yyyy hh:mm)
  - NH3_status (0 = OFF, >0 = ON) with instrument/type
  - NH3_flow_set (slpm) with instrument and description
  - NH3_flow (slpm) with instrument and description
  - Wind_speed (ms^-1) with instrument and description
  - Wind_direction (degrees) with instrument and description
- Metadata emphasis: explicit per-field metadata (instrument, manufacturer) to support discoverability and reuse; units clearly specified (slpm, ms^-1, degrees).

## Data governance, accessibility, and reuse
- Availability and provenance: dataset linked to a broader research effort on ammonia deposition; detailed methodology and usage context provided in the 2024 Atmos Environment paper.
- Funding: UKRI GCRF South Asian Nitrogen Hub supported establishment of the facility.
- Cross-reference: related work includes Estimation of ammonia deposition to forests in Scotland and Sri Lanka using wind-controlled NH3 experiments (Deshpande et al., 2024), indicating potential cross-site comparability and broader applicability.
- Useful for: estimation of NH3 deposition to forest ecosystems, analyzing deposition dynamics under wind-controlled release, and supporting future data integration with ecosystem response studies.

## Key considerations for reuse and limitations
- Granularity: data captured at 20-second NH3 release intervals with 15-minute averaged summaries, enabling high-resolution temporal analysis.
- Gating and context: NH3 release is contingent on specific wind conditions, which should be considered when modeling deposition or comparing to ambient NH3 data.
- Data gaps: some missing periods due to equipment maintenance and component replacements; users should account for these gaps in analyses.
- Completeness: full experimental design, methods, and findings are documented in Deshpande et al. (2024), providing necessary context for reuse and interpretation.