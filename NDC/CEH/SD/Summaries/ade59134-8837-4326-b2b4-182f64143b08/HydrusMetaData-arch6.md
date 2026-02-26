# Simulations were conducted with one-dimensional finite element model HYDRUS (Simunek et al., 2003; Simunek et al., 2005)

## Overview
- One-dimensional HYDRUS-1D simulations to model soil moisture and metal transport in a 100 cm deep lysimeter planted with rice.
- Timeframe: 90 days.
- Soil column discretization: 101 nodes (covers the full 100 cm depth).
- Outputs include both column-wide and node-specific data to analyze temporal and spatial variation.

## Input data and setup
- Boundary conditions are provided in HydrusInputData.csv.
- Plant: rice.
- Measurements focus on soil moisture, dissolved metal concentration, and sorbed metal concentration within the root zone.

## Data and outputs
- Column-wide outputs (every 9 days):
  - HydrusOutputDay0.csv to HydrusOutputDay90.csv (three-letter increments represent 0 to 90 days in steps of 9).
  - Variables stored for the entire soil column: soil moisture (cm3/cm3), pressure head (cm), dissolved metal concentration (mg/cm3), sorbed metal concentration (ppm).
- Node-specific high-temporal-resolution outputs:
  - HydrusOutputNode5.csv, HydrusOutputNode11.csv, HydrusOutputNode22.csv, HydrusOutputNode100.csv
  - Capture temporal variation of soil moisture, pressure head, and dissolved metal concentration at each specified node.
- Units:
  - Soil moisture: cm3/cm3
  - Pressure head: cm
  - Dissolved metal concentration: mg/cm3
  - Sorbed metal concentration: ppm

## Data structure and interpretation
- Full soil column is represented by 101 nodes across 0–100 cm.
- Regular 9-day sampling provides a coarse overview, while selected nodes provide fine temporal resolution for detailed analysis.
- Outputs enable self-serve inspection and analysis of moisture and metal transport dynamics over time and depth.

## References
- Simunek, J., Jarvis, N.J., van Genuchten, M.Th., Gardenas, A., 2003. Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. J. Hydrol. 272, 14-35.
- Simunek, J., van Genuchten, M.Th., Sejna, M., 2005. The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0 Hydrus-1D Software Series 1. Department of Environmental Sciences, University of California Riverside, Riverside, CA, p. 270.