# DigiBog model outputs. Description of data structure for column heights and water-table depths.

## Overview
- Two DigiBog model output files from the VNP Peatland Tipping Points project.
- Simulated peatland transect comprised of 100 main columns with 2 m × 2 m footprints, plus boundary conditions along ends and sides.

## Simulation details
- Runtime: 5,100 years.
- Mineral layer thickness: 5.0 cm.
- At year 4,900: six ditches created with a water-table depth of 60.0 cm.
- At year 5,000: restoration step sets water-table in ditched columns to 10.0 cm below the surface of the adjoining downslope column.
- Simulation continues to year 5,100.
- Units: centimetres (cm) for both column heights and water-table depths.
- Negative water-table depths indicate surface ponding.

## Data structure
- Grid layout: transect of 100 main columns plus boundary condition columns along ends and sides, totaling 306 values per write-out (conceptually three blocks of 102 values each).
- Coordinate framing: x = 3, y = 102; x2,y2 is the first active peat column.
- Data ordering within a year: x1,y1; x1,y2; x1,y3; x1,yN; x2,y1; x2,y2; x2,y3; x2,yN; etc.
- Boundary condition values: written as -999.0.
- Ditch treatment: when a ditch is added, the corresponding column becomes a boundary condition and is written as -999.0.

## Time, resolution and volume
- Data written every year; each file contains 1,560,600 values (306 values per year × 5,100 years).
- Both files use centimetre-depth values for column heights and water-table depths.

## Data content (variables)
- Column heights (peat column height) and water-table depths for each column across the transect.
- Negative water-table depths indicate ponding at the surface.

## Practical notes for GIS use
- Large, time-enabled dataset requiring parsing into a 3D array or time-series raster stack.
- -999.0 marks boundary/missing values; handle appropriately in GIS analyses.
- Coordinate alignment and unit consistency (cm) are essential for integration with other peatland datasets and temporal analyses over 5,100 years.