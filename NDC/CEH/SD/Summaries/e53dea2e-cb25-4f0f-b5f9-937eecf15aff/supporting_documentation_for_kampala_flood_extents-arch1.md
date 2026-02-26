# Supporting documentation for Kampala Flood Extents

## Overview
- Flood extents for Kampala district produced by simulating rainfall events over a 5 m Digital Elevation Model (DEM) using a 2D finite-volume hydrodynamic model.
- DEM supplied by Makerere University; rainfall scenarios cover a range of depths and durations.
- Infiltration effects included within green areas using spatial data from Makerere University.
- Maximum water depths converted to flood extents using multiple thresholds; extents simplified with the Douglas-Peucker algorithm (tolerance 5 m) to reduce file size.
- Web interface to view extents available at http://shear.ncl.ac.uk/flood; source code downloadable at the Zenodo link provided.

## Data and methods
- Modelling approach: Fully hydrodynamic urban flood modelling system representing buildings, green space, and interventions.
- Data inputs:
  - 5 m DEM (from Makerere University)
  - Rainfall events with varying depths and durations
  - Infiltration adjustments in green spaces (based on Makerere spatial data)
- Output processing:
  - Convert maximum depths to flood extents using selected depth thresholds
  - Simplify resulting extents with Douglas-Peucker (tolerance 5 m)
- Accessibility:
  - Web viewer for extents
  - GeoPackage containing the flood extent polygons for each rainfall-depth-duration combination
  - Source code available for download

## Data contents and formats
- GeoPackage: Polygons describing flood extents above a given threshold for each combination of rainfall depth and duration.
- Fields: Each record includes threshold (in meters), rainfall depth (in millimeters), and duration (in seconds). Units and descriptions are provided in Table 1 of the documentation.

## Access and usage
- Viewing: Web interface at http://shear.ncl.ac.uk/flood
- Reproducibility: Source code downloadable from the cited Zenodo DOI (https://doi.org/10.5281/zenodo.3949902)
- Data format: GeoPackage with flood extent polygons and associated metadata (threshold, rainfall, duration)

## Reference
- Glenis, V., Kutija, V., & Kilsby, C.G. (2018). A fully hydrodynamic urban flood modelling system representing buildings, green space and interventions. Environmental Modelling and Software, 109, 272-292.