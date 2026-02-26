# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

## Overview
- Pipeline to convert GEE binary images into per-pixel locational probabilities for Abulug.
- Uses a MATLAB script to clean data and generate an unmasked probability image, followed by GIS steps to mask, reformat, and finalize with the correct projection.

## Inputs
- GEE binary images
- Shapefile for masking (e.g., river mask)
- MATLAB script: Process_Abulug_Locational_Probabilities.m

## Processing steps
- 00–03: Run MATLAB code to clean binary images and create a per-pixel locational probability image: Abulug_locational_probability_unmasked.tif
- 04: Apply the provided shapefile mask to remove non-river pixels (via GIS like QGIS)
- 05: Use Abulug_Locational_Probability_zeros.tif; in GIS, convert 0 values to NoData and set projection to EPSG:32651 (WGS 84 / UTM zone 51N)
- 06: Generate final per-pixel locational probability raster: Abulug_Locational_Probability.tif with 0s as NoData and correct projection

## Outputs
- Abulug_locational_probability_unmasked.tif (intermediate)
- Abulug_Locational_Probability_zeros.tif (intermediate)
- Abulug_Locational_Probability.tif (final)

## Considerations and best practices
- Ensure consistent projection (EPSG:32651) and appropriate NoData handling
- Accurate river mask is crucial for correct masking of non-relevant pixels
- Workflow combines MATLAB processing with GIS steps (e.g., QGIS) for masking and projection adjustments
- Final data quality depends on the initial binary images and mask accuracy