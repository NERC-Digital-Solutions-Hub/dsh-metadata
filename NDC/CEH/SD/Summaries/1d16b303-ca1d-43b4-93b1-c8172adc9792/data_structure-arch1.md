# DigiBog model outputs. Description of data structure for column heights and water-table depths

- Two DigiBog model output files are included, from the VNP Peatland Tipping Points project (reference linked in the repository).
- Purpose: describe data structure for column heights and water-table depths produced by the DigiBog simulations.

- Simulation information
  - Total runtime: 5,100 years.
  - Mineral layer thickness: 5.0 cm (peat builds on top; included in column height output).
  - Ditching event: at year 4,900, six ditches created with a water-table depth of 60.0 cm.
  - Restoration event: at year 5,000, water-table in ditched columns set to 10.0 cm below the surface of the adjoining downslope column.
  - Simulation end: year 5,100.
  - Units: centimetres (cm) for all outputs.
  - Negative water-table depths indicate surface ponding.

- File structure and layout
  - The simulated peatland is a transect of 100 x 2 m x 2 m columns.
  - Boundaries: a boundary condition at each end of the transect and along its sides.
  - Total values per write-out: 306 values, computed as (100 + 2 main transect) x 3 boundary sets along the sides.
  - Coordinate structure: x = 3, y = 102; x2,y2 is the first active peat column.
  - Data writing order: x1,y1; x1,y2; x1,y3; …; x1,yn; x2,y1; x2,y2; x2,y3; …; x2,yn.
  - Data cadence: written every year; each file contains 1,560,600 values (306 columns x 5,100 years).

- Data values and conventions
  - Boundary condition columns are written as -999.0.
  - When a ditch is added, the affected column becomes a boundary condition and is written as -999.0 thereafter.

- Additional context
  - The repository references a related paper for an overview of how the model can be set up: Linking ecosystem changes to their social outcomes: lost in translation (2011) in Ecosystem Services (link provided in the file).
  - Data scale and interpretation considerations useful for analysts:
    - Long time horizon (5,100 years) with yearly resolution.
    - Boundary columns may influence interpretation near edges.
    - Restoration scenario is explicitly simulated (year 5,000) and reflected in subsequent outputs.
    - All depths are in cm; negative values indicate ponding at the surface.