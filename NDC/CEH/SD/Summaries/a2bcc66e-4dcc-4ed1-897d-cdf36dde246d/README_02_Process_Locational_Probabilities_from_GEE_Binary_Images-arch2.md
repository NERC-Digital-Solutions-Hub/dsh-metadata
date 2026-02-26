# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

## Purpose
- Document the workflow to convert Google Earth Engine binary images into per-pixel locational probability rasters for a defined area (Abulug).
- Produce a standardized output suitable for environmental monitoring analyses and policy performance assessments.

## Step-by-step workflow
- Step 00–03: Run MATLAB code Process_Abulug_Locational_Probabilities.m
  - Cleans the binary images and creates a single per-pixel locational probability image.
  - Produces Abulug_locational_probability_unmasked.tif.
- Step 04: Masking in GIS (e.g., QGIS)
  - Use a provided shapefile to mask out non-river pixels, yielding river-focused outputs.
- Step 05: Prepare zeros raster in GIS
  - Work with Abulug_Locational_Probability_zeros.tif.
  - Convert image values from 0 to NoData and set projection to EPSG:32651 - WGS 84 / UTM zone 51N.
- Step 06: Finalize locational probability raster
  - Produce Abulug_Locational_Probability.tif with 0 values converted to NoData and correct projection.

## Outputs
- Abulug_locational_probability_unmasked.tif (temporary, before masking)
- Abulug_Locational_Probability_zeros.tif (zero-to-NoData and projection-adjusted)
- Abulug_Locational_Probability.tif (final per-pixel locational probability raster)

## GIS and projection details
- Masking performed using a shapefile (e.g., in QGIS) to exclude non-river pixels.
- Final projection set to EPSG:32651 (WGS 84 / UTM zone 51N).

## Relevance to environmental monitoring
- Produces a standardized, per-pixel probability raster to quantify river-related presence/likelihood, suitable for integration into monitoring datasets and policy performance analyses.

## Data management and quality considerations
- Aligns with standard monitoring practices: verify, quality assure, clean, and transform data; store final datasets in appropriate portals.
- Ensures outputs are masked to relevant features (river) and consistently projected for comparability over time.