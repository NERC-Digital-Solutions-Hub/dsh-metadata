# Topographic change dataset for Antamok River catchment during Typhoon Mangkhut (2018) generated with r.avaflow

- Overview
  - Data collection: numerical simulations using free software r.avaflow v2.4 to generate maps of topographic change.
  - Study area and event: Antamok River catchment, Itogon, Philippines, during Typhoon Mangkhut in 2018.
  - Purpose: provide measures of topographic change (deposition and erosion) to inform environmental monitoring, policy evaluation, and future decision-making.

- Data details
  - Nature and units: Change in topography expressed in metres; positive values indicate deposition, negative values indicate erosion.
  - Quality control: Data validated against observed channel widening limits via remote sensing before and after the Typhoon event.

- Data structure and contents
  - ASCII files:
    - Test1_N.asc — final topographic change for the Northern part of the catchment
    - Test1_S.asc — final topographic change for the Southern part of the catchment
  - GeoTIFF files (topographic change by time/part):
    - Northern part: N_3.tif, N_30.tif, N_60.tif, N_180.tif
    - Southern part: S_3.tif, S_30.tif, S_60.tif, S_180.tif

- Spatial reference
  - Coordinate Reference System (CRS): EPSG:3124 - PRS92 zone 4

- Relevance for monitoring frameworks
  - Provides a structured, time-resolved depiction of terrain response to extreme events, useful for evaluating policy-driven monitoring outputs and scenario analyses.
  - Demonstrates integration of simulation-derived data with quality control against remote-sensing observations, aiding governance of data provenance and trust.

- Considerations and caveats
  - Dataset is model-generated for a specific event/location; results depend on model parameters and input assumptions.
  - Metadata is partly conveyed through filenames; additional metadata may be needed for formal governance, data sharing, and interoperability.