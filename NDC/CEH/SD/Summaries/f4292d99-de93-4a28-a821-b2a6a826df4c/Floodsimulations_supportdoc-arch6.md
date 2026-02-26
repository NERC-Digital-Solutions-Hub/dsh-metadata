# Outburst flood simulations of various dam failure scenarios from Tsho Rolpa glacial lake, Nepal, 2020: supporting document

## Overview
- A study of glacial lake outburst floods (GLOFs) from Tsho Rolpa Lake, Nepal, using a simple dam breach model coupled with a high-performance 2-D hydrodynamic model.
- Produces dam breach flow results for 12 GLOF scenarios and 2-D flood hydrodynamics results (worst-case scenario shown in Figure 1).
- Data focuses on the downstream area (approx. 27.5–27.85 N, 86.10–86.49 E) with a WGS 1984 Transverse Mercator projection.
- Primary outputs: maximum inundation depth and maximum flow velocity maps, plus time-series data for breach flows.

## Data scope and scenarios
- 12 GLOF scenarios defined by combinations of final breach depth (10, 20, 30 m) and water level conditions (10/20/30 m, plus additional variants such as 3 m and 5 m minor variants).
- For each scenario, outputs include:
  - Dam breach flow results
  - 2-D flood hydrodynamics results for the worst-case scenario
- Visuals include maximum flood maps for the worst-case scenario (Figure 1).

## Data collection and modeling approach
- Numerical modeling with 2-D depth-averaged shallow water equations (SWEs) to simulate flood dynamics from dam breach.
- Governing equations solved via a finite-volume Godunov-type scheme with shock-capturing for complex GLOF processes.
- Computational efficiency enhanced through GPU-based parallelization (CUDA).
- Bed effects include bed elevation zb and friction via C_f and Manning coefficient n.
- No validation was performed; calibration is described as minimal and based on model conservation properties and prior applications.

## Analytical methods
- Extraction of maximum water depth and maximum velocity for each scenario from the simulation time series.

## Nature and units of recorded values
- Water depth: meters (m)
- Flow velocity: meters per second (m/s)
- Time series: seconds (s)

## Quality control
- No validation exercises were conducted; emphasis on conservation of mass and momentum with minimal parameters, consistent with prior uses of the model.

## Details of data structure
- Data package includes:
  - 1 CSV file: Breach_flow_under_different_GLOF_scenarios
  - 24 TIFF files: 12 for maximum water depth (one per scenario) and 12 for maximum water velocity (one per scenario)
- CSV structure: 25 columns total
  - 1st column: Time (s)
  - Next 12 columns: water depth for each scenario (12 scenarios)
  - Last 12 columns: discharge (unit-width) for each scenario (12 scenarios)

## Data content specifics (scenario details)
- Table 1 (not reproduced here) provides the detailed parameterization for each scenario, including final breach depths (10, 20, 30 m), various water-level conditions, and corresponding metrics such as:
  - Final average breach width
  - Initial lake volume above final breach bottom
  - Total failure time
- Figure 1 depicts maximum flood maps for the worst-case scenario, showing inundation depth and flow velocity along the main flood pathway from the lake toward downstream areas.