# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

- Purpose
  - Convert GEE binary images into per-pixel locational probability images, suitable for GIS analysis and sharing.
  - Ensure outputs are properly masked, projected, and prepared for dissemination.

- Workflow and steps
  - 00–03: Run MATLAB script Process_Abulug_Locational_Probabilities.m
    - Cleans the binary images and creates a single per-pixel locational probability image.
    - Produces Abulug_locational_probability_unmasked.tif.
  - 04: Apply river-mask using a provided shapefile (e.g., in QGIS) to remove non-river pixels.
  - 05: Post-process with the provided raster Abulug_Locational_Probability_zeros.tif
    - Convert image values from 0 to NoData.
    - Set projection to EPSG:32651 – WGS 84 / UTM zone 51N.
  - 06: Generate the final processed per-pixel locational probability raster
    - Abulug_Locational_Probability.tif
    - Ensure 0 values are NoData and the projection remains correct.

- Outputs and formats
  - Intermediate: Abulug_locational_probability_unmasked.tif
  - Masked/adjusted: Abulug_Locational_Probability_zeros.tif (preparation for final step)
  - Final: Abulug_Locational_Probability.tif

- Data governance and quality considerations
  - Ensure masking accurately reflects river features to avoid false positives.
  - Standardize handling of NoData (0s converted to NoData) and maintain consistent CRS (EPSG:32651).
  - Document processing steps and software used (MATLAB script and GIS tools) for reproducibility.
  - Capture provenance: original GEE inputs, scripts, and versioned outputs for traceability.

- Tools and accessibility for data stewards
  - MATLAB for initial cleaning and probability calculation.
  - GIS (e.g., QGIS) for masking and projection adjustments.
  - File formats: TIFF rasters and shapefiles, suitable for cataloging and sharing.