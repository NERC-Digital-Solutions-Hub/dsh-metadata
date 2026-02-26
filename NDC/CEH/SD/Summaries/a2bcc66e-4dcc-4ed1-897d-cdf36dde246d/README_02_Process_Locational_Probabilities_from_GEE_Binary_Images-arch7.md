# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

- Objective
  - Convert GEE binary images into a single per-pixel locational probability raster for the Abulug study area, with river-area masking and proper projection.

- Processing steps
  - Steps 00–03: Run MATLAB script Process_Abulug_Locational_Probabilities.m
    - Cleans the binary images
    - Creates a single per-pixel locational probability image
    - Output: Abulug_locational_probability_unmasked.tif
  - Step 04: GIS-based masking
    - Includes a shapefile to mask out non-river pixels (applied in GIS tools like QGIS)
  - Step 05: GIS-based preparation of nodata and projection
    - Raster: Abulug_Locational_Probability_zeros.tif
    - Convert 0 values to NoData
    - Ensure projection: EPSG:32651 (WGS 84 / UTM zone 51N)
  - Step 06: Final raster
    - Final processed per-pixel locational probability raster: Abulug_Locational_Probability.tif
    - 0s remain as NoData
    - Projection remains correctly set

- GIS-specific considerations
  - Masking and nodata handling are performed in GIS (e.g., QGIS)
  - Consistent coordinate reference system (EPSG:32651) is required for downstream analyses and visualization
  - The workflow emphasizes preparing a clean, masked, and projection-consistent probability raster suitable for map-based visualization and analysis

- Outputs and formats
  - Abulug_locational_probability_unmasked.tif
  - Masking shapefile (for river-area masking)
  - Abulug_Locational_Probability_zeros.tif
  - Abulug_Locational_Probability.tif