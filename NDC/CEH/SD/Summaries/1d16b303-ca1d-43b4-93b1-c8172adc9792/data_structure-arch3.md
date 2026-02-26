# DigiBog model outputs. Description of data structure for column heights and water-table depths

## Simulation information
- Runtime: 5,100 years
- Mineral layer thickness: 5.0 cm (peat builds on top of this layer; included in column height output)
- Year 4,900: six ditches created with a water-table depth of 60.0 cm
- Year 5,000: restoration scenario implemented by setting the water-table in the ditched columns to 10.0 cm below the surface of the adjoining downslope column
- Simulation continues to year 5,100
- Units: centimetres (cm) for both output files
- Negative water-table depths indicate surface ponding

## File structure and data layout
- The simulated peatland is a transect of 100 columns by 2 m × 2 m, with boundary conditions at each end and along the sides, resulting in 306 values per write-out (100 + 2, the main transect) × 3 (including the two boundary sets along the transect sides)
- The simulation grid is described as x = 3, y = 102; the first active peat column is at x2,y2
- Data are written in the sequence: x1,y1; x1,y2; x1,y3; …; x1,yn; x2,y1; x2,y2; x2,y3; …; x2,yn; and so on
- Data are written every year; each file contains 1,560,600 values (306 values per year × 5,100 years)

## Data content and interpretation
- Boundary condition column values are written as -999.0
- When a ditch is added, the affected column becomes a boundary condition and is subsequently written as -999.0

## Data provenance and context
- Outputs come from a model run associated with the VNP Peatland Tipping Points project (see Linking ecosystem changes to their social outcomes: lost in translation, 2021, Ecosystem Services)
- File structure and data arrangement are described to facilitate use and integration with related datasets and monitoring workflows

## Relevance to environmental monitoring and policy
- Provides a detailed, time-resolved hydrological dataset for peatland columns under natural, ditching, and restoration scenarios
- Useful for evaluating how ditching and restoration influence water-table dynamics and surface ponding across a transect
- Highlights data governance considerations for monitoring frameworks: explicit boundary conditions, clear unit definitions, handling of missing/boundary values (-999.0), and the need for metadata and provenance notes to support reuse in policy evaluation and decision-making