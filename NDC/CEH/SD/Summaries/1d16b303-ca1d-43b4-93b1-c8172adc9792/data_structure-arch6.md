# DigiBog model outputs. Description of data structure for column heights and water-table depths.

## Overview
- Description of two DigiBog model output files from the VNP Peatland Tipping Points project.
- Records column heights and water-table depths in a simulated peatland transect.

## Simulation information
- Runtime: 5,100 years.
- Mineral layer thickness: 5.0 cm (peat builds on this layer; included in column height output).
- After 4,900 years, six ditches are created with a water-table depth of 60.0 cm.
- After 5,000 years, restoration is simulated by setting the water-table in the ditched columns to 10.0 cm below the surface of the adjoining downslope column.
- Simulation continues to 5,100 years.
- Units: centimetres (cm) for all outputs.
- Negative water-table depths indicate surface ponding.

## Data structure and file layout
- The simulated peatland is a transect of 100 x 2 m x 2 m columns, with boundary conditions at each end of the transect and along its sides. This results in 306 values per write-out (100 + 2 main transect columns) × 3 boundary sets.
- Simulation structure is described as: x = 3, y = 102; x2,y2 is the first active peat column.
- Data are written out in the sequence: x1,y1; x1,y2; x1,y3; …; x2,y1; x2,y2; x2,y3; … (iterating across columns and then to the next along the transect).
- The data are written every year, giving each file 1,560,600 values (306 × 5,100 years).

## Boundary conditions and missing data
- Boundary condition column values are written as -999.0.
- When a ditch is added, the column becomes a boundary condition and, thereafter, its data are written as -999.0.

## Data values and units
- All values are in centimetres (cm).
- Negative water-table depths indicate surface ponding.

## Data provenance and references
- Outputs are from the DigiBog model, linked to the VNP Peatland Tipping Points project.
- See the referenced paper for an overview of the model setup: Linking ecosystem changes to their social outcomes: lost in translation, 2021, Ecosystem Services (link provided in the document).