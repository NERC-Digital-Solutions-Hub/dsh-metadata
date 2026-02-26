# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Dataset from a 2022 ammonia enhancement experiment in a tropical sub-mmontane forest at Queensberry Estate, Sri Lanka, aimed at understanding effects of elevated atmospheric NH3 on vegetation, bryophytes, lichens, and soil.
- Data intended for analysis and visualization within GIS workflows to relate ammonia release with meteorological conditions and environmental responses.

## Spatial and environmental context
- Location: Queensberry Estate, central Sri Lanka.
- Coordinates: 6.9693° (lat), 80.5911° (lon); altitude 1645 m.
- Experimental setup uses below-canopy wind data to trigger NH3 release toward monitoring quadrats.

## Data collection and instrumentation
- Ammonia release system:
  - Three horizontal PVC tubes (20 m long, 110 mm OD) at 0.5, 1.35, and 2.2 m heights.
  - Holes at 20 cm intervals along the tubes for NH3 release.
  - Central manifold with a gas supply, powered by a fan; NH3 injected via a mass flow controller (MFC) and solenoid valve.
  - Release occurs only when wind conditions are detected to be in target directions and speeds.
- Wind and ammonia measurements:
  - Wind data: WXT536 weather station (Vaisala) measuring wind speed and direction.
  - NH3 flow data: NH3_flow_set (set point) and NH3_flow (actual flow) through MKS Instruments MFC.
  - NH3 release status: NH3_status (0 = OFF, >0 = ON) from valve (Type 6027) by Bürkert.
- Timeframe and timezone:
  - Data collected from 13 March 2022 to 31 December 2022.
  - Timestamped in Sri Lanka Standard Time (SLST).

## Data structure and fields
- Format: CSV containing 28,257 measurements across 5 primary parameters, with accompanying instrument metadata.
- Core fields:
  - Timestamp (format: dd/mm/yyyy hh:mm) in SLST.
  - NH3_status (OFF/ON) and related instrument metadata.
  - NH3_flow_set (set point) in standard liters per minute (slpm) with instrument and description fields.
  - NH3_flow (actual flow) in slpm with instrument and description fields.
  - Wind_speed (ms^-1) and Wind_direction (degrees) with instrument and description fields.
- Metadata per parameter includes Instrument, Manufacturer, and Description (e.g., NH3_status from Type 6027 solenoid valve; Wind from WXT536 Vaisala).

## Temporal coverage and time zone
- Period: 13 March 2022 – 31 December 2022.
- Time recorded in Sri Lanka Standard Time (SLST).

## Quality control and data issues
- Visual quality control performed; obvious instrument failures, datalogger issues, and power outages corrected or removed.
- Some gaps remained due to time required to replace faulty gas control components.
- Dataset includes metadata to support data provenance and GIS integration.

## GIS applicability and use cases
- Enables spatial-temporal analysis of ammonia release events in relation to wind fields and site geometry.
- Can be integrated with habitat, vegetation, and soil datasets to model or map ammonia exposure and deposition patterns.
- Suitable for creating time-sliced maps of NH3_release_status, flow settings, and wind conditions; supports validation of dispersion or deposition models.

## Data provenance and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Related publication: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.