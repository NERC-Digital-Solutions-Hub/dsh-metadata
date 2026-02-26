# DigiBog model outputs. Description of data structure for column heights and water-table depths.

## Overview
- Contains two DigiBog model output files from the VNP Peatland Tipping Points project (peer-reviewed context cited).
- Outputs describe column heights and water-table depths over time in a simulated peatland.
- Key scenario: drainage via ditches introduced around year 4900, then restoration by raising water table in ditch columns to 10 cm below the adjoining downslope surface from year 4900 onward; simulation runs to year 5100.
- Units: centimetres (cm) for all values; negative water-table depths indicate surface ponding.
- Large time-series dataset: yearly outputs across 5,100 time steps.

## Data structure and format
- Spatial layout: transect of 100 x 2 m x 2 m columns with boundary conditions at each end and along the sides.
- Data footprint per write-out: 306 values (due to boundary handling), reflecting the combined active transect and boundary positions.
- Grid indexing: described as x = 3, y = 102, where x2,y2 is the first active peat column.
- Data ordering within a write-out: x1,y1; x1,y2; x1,y3; ...; x1,y n; x2,y1; x2,y2; x2,y3; ...; x2,y n; x3,y1; ...
- Time series structure: data written every year.
- Total values per file: 1,560,600 values (306 values per year × 5,100 years).

## Boundary conditions and special values
- Boundary condition columns are written with a value of -999.0.
- When a ditch is added, the affected column becomes a boundary condition; subsequent data for that column is recorded as -999.0.

## Data content details
- Variables captured: column heights and water-table depths across the grid.
- Depth sign convention: negative water-table depths indicate ponding at the surface.

## Data management and usage notes for Data Leaders
- Data governance: clearly documented structure, including sentinel value -999.0 for boundaries, is essential for discoverability and proper interpretation.
- Metadata requirements: include grid layout (x=3, y=102), boundary logic, time step cadence (annual), units (cm), and the restoration scenario details.
- Data volume considerations: large time-series (5,100 time steps × 306 values per step per file); plan for storage, indexing, and efficient retrieval.
- Quality and interoperability: aware of potential gaps due to boundary columns and restoration events; ensure users understand how the ditching/restoration scenario affects data continuity.
- Reuse potential: suitable for analyzing hydrological responses and tipping-point dynamics in peatlands, cross-referencing with social-outcomes research as part of ecosystem-service studies.