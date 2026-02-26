# Discovery metadata: Simulation_A_ #.csv, Simulation_B_ #.csv

## Overview
- Files contain results from numerical simulations of river bed dynamics for a hypothetical sand-bed river modeled on the South Saskatchewan River, Canada.
- Two simulations (A and B) explore how different representations of bed roughness and sediment transport influence morphodynamics in large sand-bed rivers.
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith.

## Data and file structure
- Files: Simulation_A_ #.csv, Simulation_B_ #.csv where # denotes the results file number.
- Each file contains eight columns:
  - Column 1: Model domain downstream (x) coordinate (m)
  - Column 2: Model domain cross-stream (y) coordinate (m)
  - Column 3: Model domain bed elevation (m)
  - Column 4: Model domain water depth (m)
  - Column 5: Modelled unit discharge component downstream (x) (m/s)
  - Column 6: Modelled unit discharge component cross-stream (y) (m/s)
  - Column 7: Modelled unit sediment transport rate component downstream (x) (m/s)
  - Column 8: Modelled unit sediment transport rate component cross-stream (y) (m/s)

## Temporal context
- Simulations represent 28 years, with two time slices per year.
- Time slice convention: odd-numbered slices = low flow; even-numbered slices = high flow.

## Experimental design and methods
- Objective: assess how changes in bed roughness representation and sediment transport formulation affect river morphodynamics.
- Model type: 2D depth-averaged numerical model solving the shallow water equations, coupled with sediment transport and bed level change (mass conservation).
- Simulation A: van Rijn sediment transport formulation with depth-dependent Chezy roughness.
- Simulation B: Engelund-Hanson sediment transport formulation with constant (depth-independent) Chezy roughness.
- Initialization: flat bed with banklines digitized for an 8 km reach downstream of Outlook, Saskatchewan.
- Domain and resolution: 800 downstream cells × 300 cross-stream cells; cell size 10 m (downstream) × 5 m (cross-stream).
- Inflow boundary: inlet hydrograph based on gauged flow conditions for the South Saskatchewan River.

## Data provenance and authorship
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith.
- Contextual metadata indicates the same file sets (Simulation_A_ #.csv, Simulation_B_ #.csv) correspond to a time slice sequence over a 28-year simulation horizon.

## Relevance to monitoring and data governance (for monitoring framework context)
- Provides detailed metadata and structured data for evaluating how methodological choices (sediment transport formulations and roughness prescriptions) influence environmental outcomes (morphodynamics) in river systems.
- Clear file naming conventions, time-slice mapping, and column definitions support traceability, replicability, and future decision support.
- Metadata stored within the data files (coordinates, elevations, flow and transport components, units) aids quality assessment and potential integration with broader environmental health dashboards.
- Potential considerations for monitoring workflows:
  - Accessibility and sharing: data are structured with explicit metadata, but transferability depends on data management practices and openness policies.
  - Metadata completeness: current description includes key parameters; additional metadata (e.g., data provenance, calibration details, error estimates) could further support verification and governance.
  - Data transformation needs: raw simulation outputs are in specified units; downstream use may require unit checks or unit-consistent dashboards.