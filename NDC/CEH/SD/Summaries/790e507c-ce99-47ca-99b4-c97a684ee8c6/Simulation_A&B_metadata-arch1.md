# Numerical simulations of river bed dynamics for a hypothetical sand-bed river modelled on the South Saskatchewan River, Canada

## Overview
- Study of how different representations of bed roughness and sediment transport affect simulated river morphodynamics in a large sand-bed river.
- Two simulations (A and B) run with a 2D depth-averaged model solving shallow water equations, coupled with sediment transport and bed evolution.
- Initialized on a flat bed with digitized banklines for an 8 km reach downstream of Outlook, Saskatchewan.

## Data files and structure
- Files: Simulation_A_#.csv and Simulation_B_#.csv, where # denotes the time-slice number (model time).
- Time framing: simulations span 28 years with two time slices per year; odd slices = low flow, even slices = high flow.

## Model physics and setup
- Governing equations: 2D depth-averaged shallow water equations with sediment transport and bed level change (mass conservation).
- Initialization: flat bed; banklines digitized for an 8 km reach downstream of Outlook, SK River.
- Inlet conditions: hydrograph based on gauged flow conditions for the South Saskatchewan River.

## Domain and resolution
- Model domain: 800 downstream cells × 300 cross-stream cells.
- Cell size: 10 m downstream × 5 m cross-stream.

## Simulations and configurations
- Simulation A: van Rijn sediment transport formulation; depth-dependent Chezy roughness law.
- Simulation B: Engelund-Hanson sediment transport formulation; constant (depth-independent) Chezy roughness.

## Data content (eight columns per file)
- Column 1: Model domain downstream (x) coordinate (m).
- Column 2: Model domain cross-stream (y) coordinate (m).
- Column 3: Model domain bed elevation (m).
- Column 4: Model domain water depth (m).
- Column 5: Modelled unit discharge component in downstream (x) direction (m per second squared).
- Column 6: Modelled unit discharge component in cross-stream (y) direction (m per second squared).
- Column 7: Modelled unit sediment transport rate component in downstream (x) direction (m per second squared).
- Column 8: Modelled unit sediment transport rate component in cross-stream (y) direction (m per second squared).

## Purpose and implications
- Aims to identify how bed roughness representation and sediment transport formulations influence morphodynamic outcomes in large sand-bed river contexts.
- Data provide time-resolved snapshots over 28 years to assess evolving bed and flow field interactions under differing physical representations.