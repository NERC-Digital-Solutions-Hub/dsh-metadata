# Numerical simulations of river bed dynamics for a hypothetical sand-bed river modelled on the South Saskatchewan River, Canada

## Overview
- Results from numerical simulations of river bed dynamics for a hypothetical sand-bed river based on the South Saskatchewan River, Canada.
- Two simulation setups (A and B) used to investigate how bed roughness representation and sediment transport formulations affect morphodynamics.
- Time span: 28 years with two time slices per year; odd slices = low flow, even slices = high flow.

## Data structure and content
- Files: Simulation_A_#.csv and Simulation_B_#.csv (where # is the time-slice number).
- Time slices: 56 total (28 years × 2 slices/year).
- Each file contains eight columns:
  - Column 1: Model domain downstream (x) coordinate (m)
  - Column 2: Model domain cross-stream (y) coordinate (m)
  - Column 3: Model domain bed elevation (m)
  - Column 4: Model domain water depth (m)
  - Column 5: Modelled unit discharge component downstream (x) (m per second squared)
  - Column 6: Modelled unit discharge component cross-stream (y) (m per second squared)
  - Column 7: Modelled unit sediment transport rate component downstream (x) (m per second squared)
  - Column 8: Modelled unit sediment transport rate component cross-stream (y) (m per second squared)

## Simulation design and parameters
- Numerical framework: 2D depth-averaged model solving shallow water equations, coupled with sediment transport and bed level change (mass conservation).
- Initialization: flat bed with digitized banklines for an 8 km reach downstream of Outlook, Saskatchewan.
- Domain and resolution:
  - 800 cells downstream × 300 cells cross-stream
  - Cell size: 10 m (downstream) × 5 m (cross-stream)
- Simulation setup:
  - Simulation A: van Rijn sediment transport formulation; depth-dependent Chezy roughness
  - Simulation B: Engelund-Hanson sediment transport formulation; constant (depth-independent) Chezy roughness
- Inlet conditions: hydrograph based on gauged flow for the South Saskatchewan River.

## Time-slice and flow-condition conventions
- Each time slice corresponds to a model time step; the slice number maps to a specific model time.
- Odd time slices represent low flow conditions; even time slices represent high flow conditions.

## Metadata and accessibility
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith
- Data format standardized as CSV for straightforward integration with environmental monitoring workflows.
- Designed to enable comparison of different physical representations (sediment transport and bed roughness) and to support combining with additional data sources for enhanced environmental monitoring and policy-relevant analysis.

## Potential uses for environmental monitoring and policy evaluation
- Compare how choices in sediment transport formulations and roughness representations influence river morphodynamics under varying flow regimes.
- Use alongside other river condition data to assess environmental health indicators and policy outcomes related to sediment dynamics and channel evolution.
- Promote data reuse by providing a consistent, openly interpretable dataset structure that can be integrated with broader environmental datasets.