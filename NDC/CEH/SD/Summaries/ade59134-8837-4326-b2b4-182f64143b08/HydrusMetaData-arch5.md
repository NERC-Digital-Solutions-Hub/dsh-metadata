# Simulations were conducted with one-dimensional finite element model Hydrus

## Overview
- Hydrus-1D simulations were conducted to model soil moisture and metal transport in a 100 cm deep lysimeter planted with rice over 90 days.
- Outputs cover the entire soil column and selected nodes, capturing moisture, pressure head, dissolved metal concentration, and sorbed metal concentration.

## Model and Data Setup
- Model: HYDRUS-1D (one-dimensional) for variably-saturated flow and solute transport.
- Domain depth: 100 cm, discretized into 101 nodes.
- Boundary conditions: specified in HydrusInputData.csv.
- Plant and system context: rice plant grown in the lysimeter.

## Outputs and Data Organization
- Whole-column outputs: recorded every 9 days.
  - Files: HydrusOutputDay0.csv through HydrusOutputDay90.csv.
  - Recorded variables per time step: soil moisture (cm3/cm3), pressure head (cm), dissolved metal concentration (mg/cm3), sorbed metal concentration (ppm).
- Node-specific time series: very fine temporal resolution for selected nodes.
  - Nodes: 5, 11, 22, 100.
  - Files: HydrusOutputNode5.csv, HydrusOutputNode11.csv, HydrusOutputNode22.csv, HydrusOutputNode100.csv.
- Units:
  - Soil moisture: cm3/cm3
  - Pressure head: cm
  - Dissolved metal concentration: mg/cm3
  - Sorbed metal concentration: ppm

## Variables and Data Details
- For the entire soil column, records include moisture, pressure head, dissolved metal concentration, and sorbed metal concentration.
- Node-specific files provide temporal variations for nodes 5, 11, 22, and 100.

## Data Provenance and References
- Input data source: HydrusInputData.csv (boundary conditions).
- Model and software references:
  - Simunek, J.; Jarvis, N.J.; van Genuchten, M.Th.; Gardenas, A. 2003.
  - Simunek, J.; van Genuchten, M.Th.; Sejna, M. 2005. The HYDRUS-1D software package (Version 3.0).

## Relevance for Data Stewards
- Data formats: CSV files with clear naming conventions for day-wise and node-wise outputs.
- Metadata considerations:
  - Clear definitions of variables (moisture, pressure head, dissolved and sorbed metal concentrations).
  - Units clearly stated for all variables.
  - Boundary conditions and model setup should be documented (files HydrusInputData.csv and HYDRUS-1D version used).
- Data governance and sharing:
  - Ensure discoverability by indexing input/output file names and their contents.
  - Maintain provenance by recording software version, model configuration, and parent CSV files.
  - Consider providing a data dictionary and a process log describing how outputs were generated and any data transformations applied.
- Potential challenges:
  - Large temporal outputs for multiple nodes; ensure scalable storage and efficient retrieval.
  - Interoperability across systems and formats; maintain consistent units and naming conventions.