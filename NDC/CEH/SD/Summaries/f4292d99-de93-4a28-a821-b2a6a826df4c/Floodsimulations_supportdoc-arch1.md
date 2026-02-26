# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- 12 GLOF (glacial lake outburst flood) scenarios simulated for Tsho Rolpa Lake using a simple dam breach model.
- A high-performance 2-D hydrodynamic model predicts flood hydrodynamics for each scenario.
- Data include dam breach flow results for all 12 scenarios and 2-D flood hydrodynamics results for the worst-case scenario.
- Study area: downstream of Tsho Rolpa Lake (27°30′–27°51′ N, 86°10′–86°29′ E); map projection: WGS 1984 Transverse Mercator.
- The worst-case scenario flood maps are presented (maximum inundation depth and maximum flow velocity along the main channel from the lake to Manthali).

## Data collection methods
- Numerical modeling: fully hydrodynamic model based on 2-D depth-averaged shallow water equations (SWEs) with a finite volume Godunov-type scheme and shock-capturing capability.
- Computational efficiency: model implemented on GPUs using NVIDIA CUDA for parallel processing.
- Governing equations and variables are defined for depth, discharges, velocities, bed elevation, and bed roughness (Manning n).

## Scenarios and variables
- 12 GLOF scenarios with varying:
  - Final breach depth values (10, 20, 30 m)
  - Current water levels (10, 20, 30 m) and variations with “3m” and “5m” labels
  - Final average breach width (60, 87, 102 m) and other parameter combinations
  - Initial lake volume above final breach bottom (x10^6 m^3 values)
  - Total failure time (hours)
- Key outputs per scenario: maximum inundation depth and maximum flood velocity along the main channel.
- Worst-case scenario visuals: Fig 1 showing maximum inundation depth and maximum flow velocity.

## Data structure and contents
- 1 CSV file: Breach_flow_under_different_GLOF_scenarios
  - 25 columns: Time (s); 12 columns for water depth under each scenario; 12 columns for discharge (unit-width) under each scenario.
- 24 TIFF files:
  - 12 TIFFs for maximum water depth per scenario
  - 12 TIFFs for maximum water velocity per scenario
- Units: water depth in meters; velocity in meters per second.

## Calibration and quality control
- Calibration: no validation performed; minimal parameters with reliance on conservation of mass and momentum as in previous studies.
- Quality control stance: no validation described; methodological choice noted as part of the modeling approach.

## Nature and interpretation of results
- Analytical extraction: maximum water depth and maximum velocity are derived from time-series outputs of the hydrodynamic simulations.
- Data allow comparison of how breach depth, water level, and breach width influence flood magnitude and speed across scenarios.
- Useful for hazard assessment, scenario planning, and understanding flood dynamics downstream of the Tsho Rolpa Lake.

## Practical considerations for analysts
- Data accessibility: a single CSV plus multiple TIFFs enables per-scenario analysis of depth, discharge, and velocity.
- Spatial context: results pertain to the downstream area specified; ensure alignment with local boundary definitions if integrating with other datasets.
- Modeling caveats: results are not validated against observed events; interpretation should consider the simplified breach model and lack of validation.