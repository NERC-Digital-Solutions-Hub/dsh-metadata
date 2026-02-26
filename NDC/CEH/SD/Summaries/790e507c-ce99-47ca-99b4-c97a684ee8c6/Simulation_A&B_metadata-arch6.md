# Results from numerical simulations of river bed dynamics for a hypothetical sand-bed river modelled on the South Saskatchewan River, Canada

## What the data are
- Simulation_A_ #.csv and Simulation_B_ #.csv files containing results from numerical simulations of river bed dynamics.
- Data describe a hypothetical sand-bed river modelled on the South Saskatchewan River, Canada.
- Files are associated with two simulations (A and B); # denotes the results file number.

## Context and experimental design
- Simulations span 28 years with two time slices per year (odd = low flow, even = high flow).
- Banklines digitized for an 8 km reach downstream of Outlook, Saskatchewan.
- Model domain comprises 800 downstream by 300 cross-stream cells; each cell is 10 m (downstream) by 5 m (cross-stream).
- Inlet hydrograph is based on gauged flow conditions for the South Saskatchewan River.
  
## Data structure and content
- Each file contains eight data columns:
  1) Model domain downstream (x) coordinate (m)
  2) Model domain cross-stream (y) coordinate (m)
  3) Model domain bed elevation (m)
  4) Model domain water depth (m)
  5) Modelled unit discharge component in downstream (x) direction (m per second squared)
  6) Modelled unit discharge component in cross-stream (y) direction (m per second squared)
  7) Modelled unit sediment transport rate component in downstream (x) direction (m per second squared)
  8) Modelled unit sediment transport rate component in cross-stream (y) direction (m per second squared)

## Model setup and scenarios
- Two-dimensional depth-averaged numerical model solving shallow water equations coupled with sediment transport and bed level change (via sediment mass conservation).
- Simulation A: van Rijn sediment transport formulation; depth-dependent Chezy roughness.
- Simulation B: Engelund-Hanson sediment transport formulation; constant (depth-independent) Chezy roughness.
- Initial condition: flat bed with digitized banklines for the 8 km reach.
  
## Data accessibility and format
- File naming: Simulation_A_ #.csv and Simulation_B_ #.csv; # indicates the time-slice (result) number.
- Data structure supports comparison of how different bed roughness representations and sediment transport formulations influence morphodynamics over the 28-year period.

## Potential uses and interpretations
- Enable assessment of how sediment transport formulations and roughness representations affect river morphodynamics in large sand-bed rivers.
- Useful for method comparison, model validation exercises, or integration into broader studies of river evolution under varying flow regimes.
- Provides a time-resolved dataset (per time slice) for spatial analysis across the 8 km reach downstream of Outlook.