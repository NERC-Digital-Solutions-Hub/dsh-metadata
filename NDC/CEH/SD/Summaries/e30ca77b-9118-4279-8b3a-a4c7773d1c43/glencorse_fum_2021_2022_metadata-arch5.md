# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Study aim: investigate effects of elevated atmospheric ammonia on forest vegetation, bryophytes, lichens, and soil.
- Location: Glencorse woodland near Edinburgh, UK (55.8539°, -3.2151°, altitude 200 m).
- Experimental design: ammonia release triggered by wind direction (275–345°) and threshold wind speeds (0.3–10 m s⁻¹); three horizontal PVC release tubes (20 m long, 110 mm OD) at heights 0.5, 1.35, and 2.2 m.
- NH3 delivery: pure anhydrous NH3 from a cylinder via a manifold, MFC, and solenoid valve; release into wind-diluted air through 4 mm holes along the tubes.
- Control logic: solenoid opens only under correct wind conditions; positive pressure from a central fan drives gas into the tubes.
- Data period and timing: 16 September 2021 to 5 January 2023; all data recorded in Greenwich Mean Time (GMT).

## Data collection and measurement details
- Monitoring and control: NH3 release flow rate logged by a mass flow controller every 20 seconds; 15-minute averages computed from these logs.
- Wind measurements: below-canopy wind speed and direction recorded by a WXT536 weather station (Vaisala).
- Data coverage: 45,538 measurements across 5 parameters.
- Data products: provided as a CSV file with time-stamped measurements and accompanying metadata.

## Data structure and metadata
- Core data fields (per row):
  - Timestamp (15-minute timestamps; format dd/mm/yyyy hh:mm)
  - NH3_status (0 = OFF, >0 = ON)
  - NH3_flow_set (set point for NH3 flow, in slpm)
  - NH3_flow (actual NH3 flow through MFC, in slpm)
  - Wind_speed (below-canopy wind speed, m s⁻¹)
  - Wind_direction (wind direction in degrees)
- Instrumentation and provenance fields included for each parameter (instrument, manufacturer, description), enabling traceability.
- All data are recorded in GMT.
- Location details and site description provided to contextualize measurements and potential extrapolation.

## Quality control and data management
- Quality control: visual inspection to remove obvious errors from instrument malfunction, datalogger programming issues, and power outages; some gaps due to replacement of faulty gas control components.
- Data governance: dataset includes detailed metadata (instrument specifics, units, descriptions) to support reuse, replication, and integration with other datasets.
- Data completeness: gaps exist due to maintenance events; users should account for these in analyses and reproducibility.

## Temporal and spatial context
- Timeframe: data cover 2021-09-16 to 2023-01-05 (GMT).
- Site and environment: Birch plantation within Glencorse woodland; wind-directed enhancement design ties release to local wind conditions.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Related publication: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024; doi:10.1016/j.atmosenv.2023.120325.

## Considerations for data reuse and stewardship
- Data standardization: consistent CSV structure with clear unit definitions and descriptive fields supports interoperability with other datasets.
- Provenance: comprehensive metadata on sensors, controllers, and measurement times enhances auditability and reproducibility.
- Reuse implications: dataset suitable for studies on ammonia enhancement effects, deposition estimates, and wind-driven release dynamics; account for data gaps and operational periods when analyzing trends.
- Updating and maintenance: document indicates a defined end date (Jan 2023); future updates would require coordination with the data producers and funding sources.