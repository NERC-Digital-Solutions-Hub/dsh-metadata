# Supporting documentation for Kampala Flood Extents

## Purpose and Scope
- Flood extents for Kampala district produced by simulating rainfall events over a 5m DEM using a 2D finite-volume hydrodynamic model (Glenis et al., 2018).
- Data are intended as standardized outputs to support monitoring environmental health and policy performance over time; datasets formatted for scrutiny, reuse, and integration with other monitoring data.

## Data and Modelling Approach
- DEM provided by Makerere University; rainfall events sampled across a range of depths and durations.
- Infiltration included within green areas based on Makerere spatial data.
- Maximum depths converted to extents using multiple thresholds; extents simplified with Douglas-Peucker algorithm (tolerance 5m) to reduce file size.
- Model framework described as a fully hydrodynamic urban flood modelling system that accounts for buildings, green space, and interventions (Glenis et al., 2018).

## Data Product and Metadata
- GeoPackage contains polygons describing flood extents above a specified threshold for each rainfall depth and duration.
- Field units and descriptions (Table 1):
  - Threshold: meters; description — the threshold used to define flooded areas from a grid of maximum water depth.
  - Rainfall: millimeters; description — total depth of rainfall during the event.
  - Duration: seconds; description — duration of the rainfall event.

## Accessibility and Reproducibility
- Web interface to view extents: http://shear.ncl.ac.uk/flood
- Source code available to download: https://doi.org/10.5281/zenodo.3949902

## Reference
- Glenis, V., Kutija, V. & Kilsby, C.G. (2018) A fully hydrodynamic urban flood modelling system representing buildings, green space and interventions. Environmental Modelling and Software, 109, 272-292.