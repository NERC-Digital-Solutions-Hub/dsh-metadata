# Cd File Naming Convention EIDCHELP-15389

## Purpose
- Define standardized file naming for remote sensing vegetation data products to improve discoverability, interpretation, and interoperability.
- Cover amplitude-based metrics, vegetation indices means, and quality layers, with consistent metadata cues.

## File name templates

- Average Amplitude
  - Template: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
  - Notes:
    - aveAmp represents amplitude (calculated as 2.0 * amplitude / sqrt(0.5)).
    - location codes such as SAm = South America.
    - div is normalization by mean vegetation index.
    - Veg_index options include NDVI, EVI.
    - ndvi_thresh masks out data if mean VI over all years is < 0.1.
    - resolution options include 500m, 1km, 05x05 = 0.5 degree cells.
    - weighted applies when upscaling to 0.5 degree resolution.

- Vegetation Indices Mean
  - Template: <location>_<Veg_index>_mean_<resolution>_cl0.tif
  - Example: SAm_EVI_mean_1km_cl0.tif
  - Notes:
    - Simple, location- and index-specific mean imagery with a standard resolution tag.
    - All files have a corresponding world file (.tfw).

- Quality Layer
  - Template: <location>_<Veg_index>_percent_<resolution>_cl0.tif
  - Notes:
    - Indicates the percent of good quality observations used in the spectral analysis.
    - All files have a corresponding world file (.tfw).

## Key fields and codes

- geospatial projection: defines the coordinate system in the filename.
- location: regional code (e.g., SAm = South America).
- div: normalization by mean vegetation index.
- Veg_index: NDVI or EVI.
- ndvi thresh: threshold rule; mask if mean VI < 0.1 across years.
- resolution: data grid size (e.g., 500m, 1km, 0.5 degree).
- input data: references the underlying data source (e.g., annual).
- cl0: fixed suffix indicating a particular class or processing stage.
- weighted: flag used when upscaling to 0.5 degree res (applies latitude weighting).

## Calculation details

- Average Amplitude (aveAmp): amplitude multiplied by 2.0 and divided by the square root of 0.5.

## Examples

- aveAmp_SAm_div_EVI_01_500_F1_annual_cl0.tif
- SAm_EVI_mean_1km_cl0.tif
- SAm_NDVI_percent_1km.tif

## Additional notes

- All TIFF files include a corresponding world file (.tfw) for georeferencing.