# Cd File Naming Convention EIDCHELP-15389

## Overview
- Defines standardized file naming conventions for environmental monitoring products.
- Covers Average Amplitude, Vegetation Indices Mean, and Quality Layer outputs.
- Aims to support consistent data management, comparability over time, and easier access to underlying data.

## File Naming Conventions

### Average Amplitude
- Template: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
- Example: aveAmp_SAm_div_EVI_01_500_F1_annual_cl0.tif
- Key components:
  - location codes (e.g., SAm = South America)
  - div: normalised by mean vegetation index
  - Veg_index: NDVI or EVI
  - ndvi_thresh: mask out if mean VI over all years < 0.1 (no veg)
  - resolution: 500m, 1km, or 0.5 degree cells (05x05)
  - input data: code such as F1
  - cl0: classification/processing level suffix
  - weighted note: when upscaled to 0.5 degree, output is weighted by latitude
- aveAmp definition: average peak-to-trough, computed as amplitude * 2.0 / SQRT(0.5)

### Vegetation Indices Mean
- Template: <location>_<Veg_index>_mean_<resolution>_cl0.tif
- Example: SAm_EVI_mean_1km_cl0.tif
- Key components:
  - location and Veg_index (NDVI or EVI)
  - mean over the specified resolution
  - cl0 suffix indicating processing level

### Quality Layer
- Purpose: percent of good quality observations used in the spectral analysis per pixel
- Template: <location>_<Veg_index>_percent_<resolution>_cl0.tif
- Example: SAm_NDVI_percent_1km_cl0.tif
- Note: All TIFF files have a corresponding world file (.tfw) for georeferencing

## Data Formats and Georeferencing
- All outputs are TIFF (.tif) files
- Each TIFF has an accompanying world file (.tfw) to ensure proper georeferencing

## Relevance for Analysts Monitoring the Environment
- Enables consistent, comparable data products across time and regions.
- Supports transparent data provenance through encoded metadata in filenames (location, index, threshold, resolution, input data, processing level).
- Facilitates data discovery and integration with other datasets, addressing the need to increase data value and access to underlying data.