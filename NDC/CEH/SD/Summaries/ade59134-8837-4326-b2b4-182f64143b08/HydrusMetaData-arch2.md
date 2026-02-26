# HYDRUS-1D Simulation of Soil Moisture and Metal Transport in a Rice-Lysimeter (100 cm, 90-Day Simulation)

## Overview
- Conducted one-dimensional finite element simulations using HYDRUS-1D to model soil moisture and metal transport in a 100 cm deep lysimeter planted with rice.
- Simulation period: 90 days.
- Objective: capture soil moisture and metal concentration dynamics in the root zone.

## Data and Inputs
- Boundary conditions and other input data are provided in HydrusInputData.csv.
- The soil column is discretized into 101 nodes (0 to 100 cm depth).

## Outputs (Whole Column)
- Variables simulated and recorded for the entire soil profile (100 cm) every 9 days:
  - Soil moisture (cm3/cm3)
  - Pressure head (cm)
  - Dissolved metal concentration (mg/cm3)
  - Sorbed metal concentration (ppm)
- Output files:
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

## Temporal Resolution at Selected Nodes
- Fine temporal variation recorded for nodes 5, 11, 22, and 100:
  - Node 5: HydrusOutputNode5.csv
  - Node 11: HydrusOutputNode11.csv
  - Node 22: HydrusOutputNode22.csv
  - Node 100: HydrusOutputNode100.csv

## Units
- Soil moisture: cm3/cm3
- Pressure head: cm
- Dissolved metal concentration: mg/cm3
- Sorbed metal concentration: ppm

## Context and References
- HYDRUS-1D software package for simulating one-dimensional movement of water, heat, and multiple solutes in variably-saturated media (Version 3.0).
- References:
  - Simunek, J.; Jarvis, N.J.; van Genuchten, M.Th.; Gardenas, A. (2003). Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. J. Hydrol. 272, 14-35.
  - Simunek, J.; van Genuchten, M.Th.; Sejna, M. (2005). The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0. Hydrus-1D Software Series 1. University of California Riverside.