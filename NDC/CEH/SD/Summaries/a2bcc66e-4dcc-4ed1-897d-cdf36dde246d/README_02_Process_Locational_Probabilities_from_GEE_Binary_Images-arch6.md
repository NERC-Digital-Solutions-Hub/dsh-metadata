# 02_Process_Locational_Probabilities_from_GEE_Binary_Images

- Objective
  - Convert GEE binary images into per-pixel locational probabilities and produce a final, usable raster.

- Workflow overview
  - Steps 00–03: Run MATLAB script Process_Abulug_Locational_Probabilities.m to clean binary images and generate a single per-pixel locational probability image (Abulug_locational_probability_unmasked.tif). This step is performed in GIS context.
  - Step 04: Apply a provided shapefile mask (e.g., in QGIS) to remove non-river pixels.
  - Step 05: Use Abulug_Locational_Probability_zeros.tif; convert 0 values to NoData and set projection to EPSG:32651 (WGS 84 / UTM zone 51N). Requires GIS software.
  - Step 06: Produce the final processed per-pixel locational probability raster (Abulug_Locational_Probability.tif) with 0s as NoData and correct projection.

- Outputs and artifacts
  - Abulug_locational_probability_unmasked.tif (intermediate per-pixel probability)
  - Masked output via shapefile (04)
  - Abulug_Locational_Probability_zeros.tif (0s converted to NoData placeholder)
  - Abulug_Locational_Probability.tif (final locational probability raster)

- Data handling and formats
  - TIFF rasters for probability surfaces
  - Shapefile for geographic masking
  - MATLAB for initial data cleaning/combination
  - GIS steps (e.g., QGIS) for masking and projection enforcement

- Key considerations for data quality
  - Ensure correct GIS masking to retain only relevant features (e.g., rivers)
  - Verify NoData treatment and that 0 is properly converted to NoData
  - Confirm projection consistency (EPSG:32651) throughout processing

- Relevance for data products
  - Produces a self-serve, per-pixel probability map suitable for downstream analyses or visualization
  - Documented workflow supports reproducibility and potential reuse with updated inputs

- Potential challenges and mitigations
  - MATLAB environment setup and script assumptions; verify input formats
  - Accurate alignment between raster and shapefile masks; reproject if needed
  - Clear handling of NoData vs zero values to avoid misinterpretation in analyses

- Recommendations for end users
  - Validate final raster against source data and mask to ensure fidelity
  - Maintain metadata: original binaries, dates, projection, and processing steps for traceability