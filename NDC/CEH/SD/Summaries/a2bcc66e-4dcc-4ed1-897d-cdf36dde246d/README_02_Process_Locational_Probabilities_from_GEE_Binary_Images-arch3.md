# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

## Overview
- Describes a reproducible workflow to convert GEE binary images into per-pixel locational probabilities.
- Uses MATLAB for data cleaning and generation of a single probability image, followed by GIS steps to mask and finalize the dataset.
- Produces a geographically aligned raster suitable for integration into monitoring outputs.

## Workflow Steps
- 00–03: Run MATLAB script Process_Abulug_Locational_Probabilities.m to clean the binary images and create a single per-pixel locational probability image (Abulug_locational_probability_unmasked.tif).
- 04: Use a shapefile to mask the output, removing pixels not related to the river (e.g., in QGIS).
- 05: In GIS, process Abulug_Locational_Probability_zeros.tif to convert 0 values to NoData and set the projection to EPSG:32651 (WGS 84 / UTM zone 51N).
- 06: Produce the final processed per-pixel locational probability raster (Abulug_Locational_Probability.tif) with NoData in place of zeros and the correct projection.