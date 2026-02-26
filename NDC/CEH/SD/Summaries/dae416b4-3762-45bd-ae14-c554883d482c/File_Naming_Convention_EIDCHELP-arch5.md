# Cd File Naming Convention EIDCHELP-15389

## Purpose and Scope
- Defines standardized file naming conventions for three data products used in vegetation analyses: Average Amplitude, Vegetation Indices Mean, and Quality Layer.
- Aims to improve interoperability, discovery, and reuse across large datasets.
- All TIFF files come with a corresponding world file (.tfw) to ensure georeferencing and spatial alignment.

## File Name Structures

- Average Amplitude
  - Pattern: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
  - Key components:
    - aveAmp: average peak-to-trough amplitude (calculated as amplitude * 2.0 / sqrt(0.5))
    - location: e.g., SAm = South America
    - div: normalised by mean vegetation index
    - Veg_index: NDVI or EVI
    - ndvi thresh: mask out as no veg if mean VI over all years < 0.1
    - resolution: 500m, 1km, or 0.5 degree cells (05x05)
    - input data: internal designation (e.g., F1, annual)
    - cl0: quality/processing flag
    - weighted note: when upscaled to 0.5 degree resolution, output is latitude-weighted

- Vegetation Indices Mean
  - Pattern: <location>_<Veg_index>_mean_<resolution>_cl0.tif
  - Key components:
    - location and Veg_index (NDVI or EVI)
    - mean: indicates mean value across years
    - resolution: 500m, 1km, or 0.5 degree
    - cl0: quality/processing flag

- Quality Layer
  - Pattern: <location>_<Veg_index>_percent_<resolution>_cl0.tif
  - Key components:
    - location and Veg_index
    - percent: percentage of good quality observations used in spectral analysis
    - resolution: as above
    - cl0: quality/processing flag

## Examples
- aveAmp_SAm_div_EVI_01_500_F1_annual_cl0.tif
- SAm_EVI_mean_1km_cl0.tif
- SAm_NDVI_percent_1km.tif

## Notes
- All TIFF files have a corresponding world file (.tfw) to accompany georeferencing data.