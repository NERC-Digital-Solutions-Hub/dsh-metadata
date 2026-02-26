# Cd File Naming Convention EIDCHELP-15389 nameing convention

## Purpose
- Defines standardized file naming conventions for three raster products used in environmental monitoring: Average Amplitude, Vegetation Indices Mean, and Quality Layer.
- Aims to improve data discovery, provenance, interoperability, and governance across monitoring outputs.
- All TIFF files have a corresponding world file (.tfw) for georeferencing.

## Naming conventions by product

- Average Amplitude
  - Filename pattern: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
  - Key components:
    - aveAmp: average peak-to-trough metric (defined as amplitude * 2.0 / SQRT(0.5))
    - location: example SAm = South America
    - div: normalised by mean vegetation index
    - Veg_index: NDVI or EVI
    - ndvi_thresh: if mean VI over all years < 0.1, masked as no veg
    - resolution: 500 m, 1 km, or 0.5 degree cells (noted as 05x05 for 0.5°)
    - input data: source dataset code (e.g., F1)
    - cl0: quality/processing level indicator
    - weighted: when upscaled to 0.5° resolution, output is latitude-weighted

- Vegetation Indices Mean
  - Filename pattern: <location>_<Veg_index>_mean_<resolution>_cl0.tif
  - Key components:
    - location, Veg_index (NDVI or EVI)
    - mean: indicates mean value across years
    - resolution: e.g., 1 km
    - cl0: quality/processing level indicator

- Quality Layer
  - Filename pattern: <location>_<Veg_index>_percent_<resolution>_cl0.tif
  - Key components:
    - location, Veg_index
    - percent: percentage of good quality observations used in spectral analysis
    - resolution: e.g., 1 km
    - cl0: quality/processing level indicator

## Examples
- aveAmp_SAm_div_EVI_01_500_F1_annual_cl0.tif
- SAm_EVI_mean_1km_cl0.tif
- SAm_NDVI_percent_1km.tif

## Notes
- All TIFF files should be used with their corresponding .tfw world files.