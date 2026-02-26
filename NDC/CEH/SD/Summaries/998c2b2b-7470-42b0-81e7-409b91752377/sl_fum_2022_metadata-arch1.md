# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Study setting: tropical sub-mmontane forest at Queensberry Estate, central Sri Lanka.
- Objective: investigate effects of high ambient NH3 on forest vegetation, bryophytes, lichens, and soil.
- Experimental design: wind-controlled NH3 enhancement facility established in 2022; NH3 release occurs only when below-canopy wind conditions meet predefined directional thresholds and speeds.

## Experimental design and data generation
- Release system: three parallel 20 m PVC tubes (0.5, 1.35, 2.2 m above ground) with six 4 mm holes along each tube; NH3 injected from a cylinder via mass flow controller and solenoid valve into a central fan-driven airflow.
- Control logic: NH3 release triggered only under specific wind direction windows (5–75° and 185–255°) and threshold wind speeds (0.3–10 m s^-1).
- Sensing and timing: below-canopy wind data from a WXT536 weather station; NH3 volume released recorded every 20 s and aggregated to 15-minute intervals.
- Data period: 13 March 2022 to 31 December 2022.
- Data provenance: full experimental design, methodology, analysis, and findings detailed in Deshpande et al. (2024).

## Data structure and contents
- Dataset size: 28,257 measurements covering 5 parameters.
- Provided format: CSV file with the following columns (and metadata fields):
  - Timestamp (date/time in Sri Lanka Standard Time, SLST)
  - NH3_status (0 = OFF, >0 = ON) with instrument details (Type 6027 solenoid valve, Bürkert)
  - NH3_flow_set (set point for NH3 flow, in slpm) with instrument and manufacturer (G series MFC, MKS Instruments)
  - NH3_flow (actual NH3 flow through MFC into the release manifold, in slpm)
  - Wind_speed (below-canopy wind speed, in ms^-1) with instrument and manufacturer (WXT536, Vaisala)
  - Wind_direction (below-canopy wind direction, in degrees) with instrument and manufacturer (WXT536, Vaisala)
- Data quality notes: visual QC performed; obvious instrument malfunction, datalogger issues, and power-cut artifacts removed; some gaps due to replacement of faulty gas-control components.

## Quality, limitations, and considerations for analysis
- Local-scale data: suitable for analyzing correlations between NH3 release dynamics, wind conditions, and downstream environmental responses within this site.
- Data gaps: some missing intervals due to component replacement; consider handling gaps in time-series analyses (e.g., imputation or gap-aware modeling).
- Data provenance and reproducibility: detailed metadata included; dataset designed to be traceable to hardware (valves, MFCs, weather station) and timeline.
- Temporal and spatial scale: measurements are 15-minute aggregates, with 20-second sampling cadence for the release rate; spatial scope limited to near-canopy environment of the Queensberry site.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.