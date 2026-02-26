# Simulation_A_ #.csv and Simulation_B_ #.csv: Numerical simulations of river bed dynamics for a hypothetical sand-bed river modeled on the South Saskatchewan River, Canada

## Overview
- Two simulations (A and B) use a 2D depth-averaged model to study river morphodynamics, coupling shallow water equations with sediment transport and bed evolution.
- Objective: investigate how different bed roughness representations and sediment transport formulations influence morphodynamics in large sand-bed rivers.

## Data content
- Each file contains eight data columns describing spatial and flow/sediment fields.
- Time context: simulations run for 28 years with two time slices per year; odd slices = low flow, even slices = high flow.
- Results are provided for two simulations (A and B) across time slices. The file number (#) corresponds to the model time slice.

## Model setup and boundary conditions
- Domain: 800 cells downstream × 300 cells cross-stream; cell size 10 m (downstream) × 5 m (cross-stream).
- Initial condition: flat bed with digitized banklines for an 8 km reach downstream of Outlook, Saskatchewan.
- Inlet hydrograph based on gauged flow conditions for the South Saskatchewan River.

## Simulations (A vs B)
- Simulation A: van Rijn sediment transport formulation and depth-dependent Chezy roughness.
- Simulation B: Engelund-Hanson sediment transport formulation and constant (depth-independent) Chezy roughness.

## Data columns (per file)
- Column 1: Model domain downstream (x) coordinate (m)
- Column 2: Model domain cross-stream (y) coordinate (m)
- Column 3: Model domain bed elevation (m)
- Column 4: Model domain water depth (m)
- Column 5: Modelled unit discharge component in downstream (x) direction (m/s)
- Column 6: Modelled unit discharge component in cross-stream (y) direction (m/s)
- Column 7: Modelled unit sediment transport rate component in downstream (x) direction (m/s)
- Column 8: Modelled unit sediment transport rate component in cross-stream (y) direction (m/s)

## Provenance and authors
- Discovery/contextual metadata files are labeled Simulation_A_ #.csv and Simulation_B_ #.csv.
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith.

## Relevance and use for data leadership
- Provides a structured, time-resolved dataset to evaluate how different physical representations (sediment transport formulations and bed roughness treatments) affect river morphodynamics predictions.
- Clear metadata structure (time slices, spatial grid, initial conditions, and model setup) supports data discovery, reuse, and interoperability.
- Suitable for analyses of model sensitivity to transport and roughness parameterizations, as well as for validating data pipelines that ingest multidimensional hydrodynamic and sediment-transport outputs.