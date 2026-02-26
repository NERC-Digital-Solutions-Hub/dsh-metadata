# Discovery metadata: Simulation_A_ #.csv, Simulation_B_ #.csv

## Overview
- Files: Simulation_A_ #.csv and Simulation_B_ #.csv
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith
- Data description: Results from numerical simulations of river bed dynamics for a hypothetical sand-bed river modeled on the South Saskatchewan River, Canada. The “#” in file names represents the results file number.

## Contextual metadata
- Files: Simulation_A_ #.csv, Simulation_B_ #.csv
- Purpose: Investigate how changes in bed roughness representation and sediment transport affect simulated morphodynamics of large sand-bed rivers.
- Time coverage: Simulations represent 28 years, with two time slices per year. Odd time slices = low flow; even time slices = high flow.
- File time-slice mapping: The # in each file name corresponds to the model time slice number.

## Dataset structure and fields
- Each file contains eight columns:
  1) Model domain downstream (x) coordinate (m)
  2) Model domain cross-stream (y) coordinate (m)
  3) Model bed elevation (m)
  4) Model water depth (m)
  5) Modelled unit discharge component downstream (x) (m per second)
  6) Modelled unit discharge component cross-stream (y) (m per second)
  7) Modelled unit sediment transport rate component downstream (x) (m per second)
  8) Modelled unit sediment transport rate component cross-stream (y) (m per second)
- Model purpose: 2D depth-averaged shallow water equations with sediment transport and bed level change (mass conservation).

## Simulation design and conditions
- Simulations A vs B:
  - Simulation A: van Rijn sediment transport formulation; depth-dependent Chezy roughness.
  - Simulation B: Engelund-Hanson sediment transport formulation; constant depth-independent Chezy roughness.
- Initial conditions: Flat bed; banklines digitized for an 8 km reach downstream of Outlook, Saskatchewan.
- Model domain and resolution: 800 downstream cells by 300 cross-stream cells; cell size 10 m (downstream) by 5 m (cross-stream).
- Inflow: Inlet hydrograph based on gauged flow conditions for the South Saskatchewan River.
- Coverage: 28-year simulations with time-slice outputs across both A and B configurations.

## Data governance and stewardship considerations
- Provenance: Clear authorship and model descriptions provided; two distinct modeling approaches documented (A and B).
- Metadata completeness: Includes file naming conventions, time-slice mapping, coordinate units, and column definitions; clearly links file numbers to time slices.
- Data formats and accessibility: CSV files with explicit column definitions; suitable for reuse but consider providing a data dictionary or schema in a separate metadata record.
- Handling of large data: Long time span and multi-dimensional outputs imply large data volumes; plan for scalable storage, indexing by time slice, and efficient retrieval.
- Reuse and interoperability: Two similar simulation setups enable comparative analyses; ensure explicit licensing, versioning, and any code or parameter details needed for reproducibility.
- Quality and validation: Documentation notes the physical models used; consider additional quality checks (unit consistency, boundary conditions, and cross-validation between A and B results) to support data integrity.