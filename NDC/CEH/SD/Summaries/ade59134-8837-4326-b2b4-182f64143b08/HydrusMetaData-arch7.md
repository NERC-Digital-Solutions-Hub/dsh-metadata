# Simulations were conducted with one-dimensional finite element model Hydrus (Simunek et al., 2003; Simunek et al., 2005)

## Overview
- One-dimensional HYDRUS-1D simulations of soil-water and metal transport in a 100 cm deep lysimeter planted with rice.
- 90-day simulation period with data captured as vertical soil profiles and node-specific time series.

## Data and Formats
- Input data: HydrusInputData.csv containing boundary conditions for the model.
- Column discretization: soil column divided into 101 nodes across 100 cm depth.
- Outputs (column-wide, regular intervals): HydrusOutputDay0.csv to HydrusOutputDay90.csv.
  - Variables per output: soil moisture (cm3/cm3), pressure head (cm), dissolved metal concentration (mg/cm3), sorbed metal concentration (ppm).
- High-resolution node time series (very fine temporal resolution) for selected depths:
  - HydrusOutputNode5.csv, HydrusOutputNode11.csv, HydrusOutputNode22.csv, HydrusOutputNode100.csv.
- Units:
  - Soil moisture: cm3/cm3
  - Pressure head: cm
  - Dissolved metal concentration: mg/cm3
  - Sorbed metal concentration: ppm

## Time and Space Coverage
- Time: 0 to 90 days (simulations run over 90 days; outputs include Day0 to Day90).
- Space: 100 cm soil column; 101 vertical nodes.

## Variables and Outputs
- For all-depth outputs: moisture, pressure head, dissolved metal concentration, sorbed metal concentration.
- For node-specific outputs: same variables tracked with high temporal resolution at nodes 5, 11, 22, and 100.

## How this maps to GIS work
- Enables visualization of vertical (depth-based) soil state and metal transport over time.
- Data can be transformed into depth profiles and animated time-series; potentially integrated with geographic layers if georeferenced (requires conversion from 1D depth to 2D/3D spatial representations).
- Useful for informing policy, client discussions, or public-facing maps about subsurface moisture and contaminant dynamics in a rice-lysimeter context.

## Processing notes and considerations
- The model is 1D (vertical) and does not provide horizontal spatial variation.
- Data are provided at regular 9-day intervals for the full column and at finer temporal resolution for selected depths, which may require resampling for consistent GIS visualization.
- Verification and cleaning steps may be needed when combining with other datasets due to unit consistency and depth alignment.

## References
- Simunek, J., Jarvis, N.J., van Genuchten, M.Th., Gardenas, A. (2003). Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. J. Hydrol. 272, 14-35.
- Simunek, J., van Genuchten, M.Th., Sejna, M. (2005). The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0. Hydrus-1D Software Series 1. University of California Riverside.