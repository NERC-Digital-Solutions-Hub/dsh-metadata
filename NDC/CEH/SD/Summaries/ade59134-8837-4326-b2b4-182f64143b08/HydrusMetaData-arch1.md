# Simulations were conducted with one-dimensional finite element model Hydrus (Simunek et al., 2003; Simunek et al., 2005).

## Overview
- 90-day simulation using HYDRUS-1D for a 100 cm deep lysimeter planted with rice.
- Input boundary conditions provided in HydrusInputData.csv.
- Outputs cover soil moisture, water pressure head, and metal concentrations in the soil profile.

## Simulation setup
- One-dimensional finite element model (HYDRUS-1D).
- Soil column depth: 100 cm, discretized into 101 nodes.
- Focus variables recorded: soil moisture (cm3/cm3), pressure head (cm), dissolved metal concentration (mg/cm3), and sorbed metal concentration (ppm).

## Outputs and data files
- Global time-step data stored every 9 days in:
  - HydrusOutputDay0.csv
  - HydrusOutputDay9.csv
  - HydrusOutputDay18.csv
  - HydrusOutputDay27.csv
  - HydrusOutputDay36.csv
  - HydrusOutputDay45.csv
  - HydrusOutputDay54.csv
  - HydrusOutputDay63.csv
  - HydrusOutputDay72.csv
  - HydrusOutputDay81.csv
  - HydrusOutputDay90.csv
- High-resolution temporal data for specific nodes stored in:
  - HydrusOutputNode5.csv
  - HydrusOutputNode11.csv
  - HydrusOutputNode22.csv
  - HydrusOutputNode100.csv

## Variables and units
- Soil moisture: cm3/cm3
- Pressure head: cm
- Dissolved metal concentration: mg/cm3
- Sorbed metal concentration: ppm
- Units definitions are provided inline (cm3/cm3, cm, mg/cm3, ppm). 

## References
- Simunek, J.; Jarvis, N.J.; van Genuchten, M.Th.; Gardenas, A. (2003). Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. Journal of Hydrology, 272, 14-35.
- Simunek, J.; van Genuchten, M.Th.; Sejna, M. (2005). The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0. Hydrus-1D Software Series 1.