# Supporting documentation for Kampala Flood Extents

## Data Product Overview
- Flood extents for Kampala district produced by simulating rainfall events over a 5 m Digital Elevation Model (DEM) with a 2D finite-volume hydrodynamic model.
- DEM provided by Makerere University; rainfall events sampled across various depths and durations.
- Infiltration modeled within green areas using spatial data from Makerere University.
- Maximum water depths converted to flood extents using specified thresholds.
- Extents simplified with the Douglas-Peucker algorithm (tolerance 5 m) to reduce file size.
- A web interface for viewing extents is available, and the source code is downloadable.

## Data Product and Structure
- GeoPackage contains polygons describing flooding extents above a threshold for each rainfall depth and duration.
- Key fields (per Table 1):
  - Threshold: Units = meters; description = threshold used to define flooded areas from grid of maximum water depth.
  - Rainfall: Units = millimeters; description = total depth of rainfall during the event.
  - Duration: Units = seconds; description = duration of the rainfall event.
- The dataset supports multiple combinations of rainfall depth and duration mapped to extents.

## Data Provenance and Modeling Details
- Model: Fully hydrodynamic urban flood modeling system representing buildings, green space, and interventions.
- Data inputs:
  - 5 m DEM (from Makerere University)
  - Rainfall events across different depths and durations
  - Infiltration effects based on green-space data
- Reference: Glenis, V., Kutija, V., & Kilsby, C.G. (2018) Environmental Modelling and Software.

## Access, Reuse, and Licensing
- Web viewer: http://shear.ncl.ac.uk/flood
- Source code download: https://doi.org/10.5281/zenodo.3949902
- Data users should reference the cited modeling work and the repository when reusing.

## Data Processing and Quality Assurance
- Extents created by transforming maximum depths to flood extents using defined thresholds.
- Data size optimized through Douglas-Peucker simplification (5 m tolerance).
- Provenance documented via citation and available source code for reproducibility.

## How to Use the Data
- Interpret polygons as flood extents above a given threshold for a specific rainfall depth and duration.
- Use the accompanying field descriptions to select appropriate threshold, rainfall, and duration combinations for analysis or visualization.
- Access the GeoPackage and view results via the web interface; consult the metadata for unit definitions.

## Limitations and Considerations
- Extents depend on modeled scenarios (predefined rainfall events) and assumptions about infiltration and urban features.
- Users should consider model scope and the 5 m DEM resolution when applying results to decision-making or planning.