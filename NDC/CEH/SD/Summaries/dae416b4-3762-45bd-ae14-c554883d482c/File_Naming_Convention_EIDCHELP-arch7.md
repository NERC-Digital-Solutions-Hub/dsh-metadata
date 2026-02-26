# Cd File Naming Convention EIDCHELP-15389

## Overview
- Defines naming conventions for GIS raster data products produced for EIDCHELP.
- Targets map-based data visuals (Average Amplitude, Vegetation Indices Mean, and Quality Layer).
- Ensures consistency across datasets and aids in interpretation by GIS analysts and end users.

## File naming patterns

### Average Amplitude
- Pattern: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
- Key components:
  - location: e.g., SAm = South America
  - div: normalization by mean vegetation index (optional)
  - Veg_index: NDVI or EVI
  - ndvi thresh: if mean VI over all years < 0.1, masked as no vegetation
  - resolution: 500m, 1km, or 0.5-degree cells labeled as 05x05
  - input data: source data identifier
  - cl0: accompanying quality/class indicator
- Calculation note:
  - aveAmp = average peak-to-trough, computed as amplitude * 2.0 / sqrt(0.5)

### Vegetation Indices Mean
- Pattern: <location>_<Veg_index>_mean_<resolution>_cl0.tif
- Key components:
  - location: geographic area code (e.g., SAm)
  - Veg_index: NDVI or EVI
  - mean: indicates mean value over time
  - resolution: 500m, 1km, or 0.5-degree cells (05x05)
  - cl0: accompanying quality/class indicator

### Quality Layer
- Pattern: <location>_<Veg_index>_percent_<resolution>_cl0.tif
- Key components:
  - location: geographic area code
  - Veg_index: NDVI or EVI
  - percent: percent of good quality observations used in spectral analysis
  - resolution: 500m, 1km, or 0.5-degree cells (05x05)
  - cl0: accompanying quality/class indicator
- Example: SAm_NDVI_percent_1km.tif

## Common notes and constraints
- All TIFF files have a corresponding world file (.tfw) for georeferencing.
- The naming conventions help quickly identify location, index, metric, masking, resolution, and data lineage.
- Cl0 suffix indicates an associated data quality or classification layer included in the naming convention.

## Practical guidance
- Use these patterns consistently when publishing or sharing raster products to support clear interpretation and comparability across datasets.
- Ensure masking thresholds (e.g., ndvi_thresh) are applied before naming to reflect data validity.
- When scaling to a common resolution (e.g., 0.5-degree), apply latitude-weighting as specified for aggregated outputs.