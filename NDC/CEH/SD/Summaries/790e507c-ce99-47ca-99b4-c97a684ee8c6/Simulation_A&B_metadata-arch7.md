# Discovery metadata

## Overview
- Contains results from numerical simulations of river bed dynamics for a hypothetical sand-bed river modeled on the South Saskatchewan River, Canada.
- Two simulation results files are provided: Simulation_A_#.csv and Simulation_B_#.csv (the # denotes the time-slice number).
- Each time slice represents model output for 28-year simulations with two slices per year (odd slices = low flow, even slices = high flow).

## Temporal and spatial context
- Time slices correspond to model time steps; odd-numbered slices are low flow, even-numbered slices are high flow.
- Simulations cover 28 years using an inlet hydrograph based on gauged flow conditions for the South Saskatchewan River.

## Data structure and contents
- Each file contains eight columns:
  - Column 1: Model domain downstream (x) coordinate (meters)
  - Column 2: Model domain cross-stream (y) coordinate (meters)
  - Column 3: Model domain bed elevation (meters)
  - Column 4: Model domain water depth (meters)
  - Column 5: Modelled unit discharge component in the downstream (x) direction (meters per second squared)
  - Column 6: Modelled unit discharge component in the cross-stream (y) direction (meters per second squared)
  - Column 7: Modelled unit sediment transport rate component in the downstream (x) direction (meters per second squared)
  - Column 8: Modelled unit sediment transport rate component in the cross-stream (y) direction (meters per second squared)

## Spatial setup and domain
- Model domain: 800 cells downstream by 300 cells cross-stream.
- Cell size: 10 m (downstream) × 5 m (cross-stream).
- Initial condition: flat bed with banklines digitized for an 8 km reach downstream of Outlook, Saskatchewan.

## Model and scenarios
- Purpose: to investigate how changes in bed roughness representation and sediment transport formulations affect river morphodynamics for large sand-bed rivers.
- Model type: 2D depth-averaged numerical model solving shallow water equations, coupled with sediment transport and bed level change equations.
- Scenarios:
  - Simulation A: van Rijn sediment transport formulation with depth-dependent Chezy roughness.
  - Simulation B: Engelund-Hanson sediment transport formulation with constant (depth-independent) Chezy roughness.

## Data provenance and authors
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith.

## GIS readiness and usage notes
- Suitable for map-based visualization of spatial fields across time slices (bed elevation, water depth, discharges, and sediment transport components).
- Can be integrated with GIS layers to analyze morphodynamics along the 8 km reach downstream of Outlook.
- Considerations for GIS use:
  - Coordinate system: coordinates are in meters, but explicit CRS is not provided; users should assign an appropriate CRS and convert if necessary.
  - Time series handling: 56 time slices in total (28 years × 2 slices/year); time dimension should be managed to create animations or time-enabled layers.
  - Units: ensure consistent interpretation of the provided units (some entries list discharge and transport components with units described as meters per second squared, which may require verification during data processing).
  - Data volume: 2 CSV files per time slice; plan for the cumulative size across all slices when loading into GIS software or downstream processing pipelines.