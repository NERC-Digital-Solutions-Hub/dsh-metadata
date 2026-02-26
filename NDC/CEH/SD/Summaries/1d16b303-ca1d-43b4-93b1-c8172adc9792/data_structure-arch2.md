# DigiBog model outputs. Description of data structure for column heights and water-table depths.

## Overview
- Two DigiBog model output files are provided, from a simulation associated with the VNP Peatland Tipping Points project.
- Data describe column heights and water-table depths across a peatland transect, intended for analysis of ecosystem changes and related outcomes.

## Simulation information
- Runtime: 5,100 years (∞ notation used in the description).
- Mineral layer thickness: 5.0 cm (peat builds on top of this layer; included in the column height output).
- Ditching/restoration events:
  - At year 4,900: six ditches created with a water-table depth of 60.0 cm.
  - At year 5,000: restoration simulated by setting the water-table in ditched columns to 10.0 cm below the surface of the adjoining downslope column.
- Output units: centimetres (cm) for all data.
- Water-table depths: negative values indicate surface ponding.
- Simulation end: year 5,100.

## Data structure and layout
- Model area: transect of 100 columns by 2 m by 2 m, with boundary conditions at both ends and along the sides.
- Total values per write-out: 306 (100 main transect columns plus boundary columns) × 3 boundary positions = 306 values per write-out.
- Indexing: x = 3, y = 102; the first active peat column is x2,y2.
- Data ordering: x1,y1; x1,y2; x1,y3; …; x2,y1; x2,y2; x2,y3; …; x2,y n, etc.
- Frequency and volume: data written every year; each file contains 1,560,600 values (306 values × 5,100 years).

## Boundary conditions and special values
- Boundary condition columns are written with a value of -999.0.
- When a ditch is added, the affected column becomes a boundary condition and is written as -999.0 thereafter.

## Data sources and references
- See the linked paper for an overview of the model setup: https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1002/2016WR019898
- Units: centimetres (cm) for all measurements in both output files.

## Relevance for environmental monitoring
- Demonstrates standardized data structure and long-term hydrological outputs suitable for verification, quality assurance, and integration with other environmental datasets.
- Provides clear handling of boundary conditions and restoration scenarios to support reproducibility and comparative analyses.