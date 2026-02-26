# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

## Overview
- Document describes converting Google Earth Engine (GEE) binary images into per-pixel locational probabilities.
- Produces a final georeferenced raster suitable for analysis and reporting.

## Step-by-step workflow
- Step 00–03: Run MATLAB script Process_Abulug_Locational_Probabilities.m to clean binary images and create a single per-pixel locational probability image (Abulug_locational_probability_unmasked.tif).
- Step 04: Apply a mask using a shapefile (e.g., in QGIS) to retain only river-related pixels.
- Step 05: Prepare a raster (Abulug_Locational_Probability_zeros.tif) by converting 0 values to NoData and setting the projection to EPSG:32651 (WGS 84 / UTM zone 51N).
- Step 06: Produce the final processed per-pixel locational probability raster (Abulug_Locational_Probability.tif) with 0 values as NoData and correct projection.

## Data management and standards
- End-to-end pipeline from binary images to a final probability raster.
- Explicit handling of NoData values to ensure meaningful analysis outputs.
- CRS consistency (EPSG:32651) to standardize spatial analysis across datasets.
- Clear file naming conventions for traceability of intermediate and final products.

## Considerations for Data Leaders
- Emphasis on reproducibility: sequence of steps and tool usage (MATLAB, GIS) should be documented for auditability.
- Data quality and relevance: masking ensures outputs are focused on river-related areas.
- Metadata and discoverability: intermediate and final outputs should be well-documented (names, projections, purpose).
- Potential for automation: streamline steps 00–06 to reduce manual intervention and improve consistency.