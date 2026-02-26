# Supporting documentation for Kampala Flood Extents

## Overview
- Flood extents are produced by simulating rainfall events over a 5m Digital Elevation Model (DEM) using a 2D finite-volume hydrodynamic model (Glenis et al., 2018).
- DEM supplied by Makerere University; rainfall events sampled across a range of depths and durations.
- Infiltration effects incorporated within green areas based on Makerere University spatial data.

## Data Products
- GeoPackage containing polygons describing flood extents above a threshold for each rainfall depth and duration.
- Field units and descriptions: 
  - Threshold: meters (m) – the threshold used to define flooded areas from a grid of maximum water depth.
  - Rainfall: millimeters (mm) – total depth of rainfall during the event.
  - Duration: seconds (s) – duration of the rainfall event.

## Data Processing and Transformation
- Max depths converted into extents using multiple thresholds.
- Extents simplified using the Douglas-Peucker algorithm with a tolerance of 5m to reduce file size.

## Accessibility and Reuse
- Web interface for viewing extents: http://shear.ncl.ac.uk/flood
- Source code available for download: https://doi.org/10.5281/zenodo.3949902
- The GeoPackage provides polygons describing flood extents; metadata and field descriptions are documented (Table 1).

## Data Structure and Metadata
- Data product: GeoPackage with polygons representing flood extents above thresholds for various rainfall depths and durations.
- Metadata highlights: Units and descriptions for each field (Threshold, Rainfall, Duration) as detailed in Table 1.
- Principal reference for methods: Glenis, V., Kutija, V. & Kilsby, C.G. (2018) “A fully hydrodynamic urban flood modelling system representing buildings, green space and interventions.” Environmental Modelling and Software, 109, 272-292.

## Provenance and Citation
- Modelling workflow and data generation are documented in the cited 2018 publication.
- Reproducible access through web viewer and downloadable source code on Zenodo.

## Data Stewardship Considerations
- Governance and provenance: ensure proper credit to data sources (Makerere University DEM and spatial data) and the modelling methodology.
- Metadata quality: maintain clear definitions for units, thresholds, and descriptions (as per Table 1) to support discovery and reuse.
- Accessibility and discoverability: sustain the web viewer and code repository; ensure the GeoPackage remains accessible and well-documented.
- Interoperability and scalability: note potential challenges with large datasets and varied formats; document threshold choices, rainfall depths, and durations to support interoperability.
- Update and maintenance: provide processes for updating with new rainfall scenarios or improved DEMs, and versioning of data products.