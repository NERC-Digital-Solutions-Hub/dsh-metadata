# DigiBog model outputs. Description of data structure for column heights and water-table depths.

## Overview
- Two DigiBog model output files from the VNP Peatland Tipping Points project (see Linking ecosystem changes to their social outcomes: lost in translation, 2021, Ecosystem Services).
- Outputs cover a long-term peatland simulation run (5,100 years) including column heights and water-table depths.

## Simulation information
- Runtime: 5,100 years.
- Mineral layer thickness: 5.0 cm (peat builds on this layer; included in column height output).
- Ditching event: after 4,900 years, six ditches created with water-table depth of 60.0 cm.
- Restoration event: after 5,000 years, water-table in ditched columns set to 10.0 cm below the surface of the adjoining downslope column to simulate restoration.
- Continuation: simulation proceeds to 5,100 years.
- Units: centimetres (cm) for both files.
- Depth convention: negative water-table depths indicate surface ponding.

## Data structure and content
- Spatial layout: transect of 100 x 2 m x 2 m columns with boundary conditions at ends and along sides (total defined structure).
- Data layout note: x = 3, y = 102; x2,y2 is the first active peat column of the simulation.
- Data ordering: sequence — x1,y1; x1,y2; x1,y3; …; x2,y1; x2,y2; x2,y3; ….
- Temporal sampling: data written out every year; each file contains 1,560,600 values (306 values per write-out × 5,100 years).

## Boundary conditions and special values
- Boundary condition values: written as -999.0.
- Ditch events change a column to a boundary condition; after this, the column data are written as -999.0.

## Data encoding and interpretation
- Data represent column heights and water-table depths in centimetres.
- Negative water-table depths indicate surface ponding.
- Two output files provide the time series across the full simulation period.

## Provenance and references
- See the linked paper for an overview of model setup: https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1002/2016WR019898

## Data stewardship considerations
- Metadata needs: clear mapping from index positions (x, y) to physical locations, and explanation of boundary condition and ditch-rule conventions.
- Data volume handling: large time-series files (1.56 million values per file); plan for storage, transfer, and access.
- Interoperability: consistent unit usage (cm) and explicit sentinel value (-999.0) for boundaries to aid automation.
- Data freshness and provenance: note the simulation context and restoration scenario to support correct interpretation and reuse.