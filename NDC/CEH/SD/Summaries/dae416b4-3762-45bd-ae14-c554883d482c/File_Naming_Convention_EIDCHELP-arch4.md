# Cd File Naming Convention EIDCHELP-15389

## Overview
- Defines consistent file naming conventions for three data product types: Average Amplitude, Vegetation Indices Mean, and Quality Layer.
- Filenames encode key attributes to aid discovery, interoperability, and governance of vegetation-related rasters.

## Filename structure and component meanings

- Average Amplitude (aveAmp)
  - Pattern: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
  - What each component conveys:
    - geographical projection at the start
    - location code (e.g., SAm = South America)
    - div: normalised by mean vegetation index
    - Veg_index: NDVI or EVI
    - ndvi_thresh: if mean VI over all years < 0.1, then masked as no vegetation
    - resolution: 500 m, 1 km, or 0.5 degree cells (noted as 05x05)
    - input data: source data label
    - cl0: class/quality flag indicator
  - Calculation note: aveAmp = average peak-to-trough, i.e., amplitude * 2.0 / SQRT(0.5)
  - Upscaling consideration: when upscaled to 0.5 degree resolution, output is weighted by latitude

- Vegetation Indices Mean
  - Pattern: <location>_<Veg_index>_mean_<resolution>_cl0.tif
  - What each component conveys:
    - location code
    - Veg_index: NDVI or EVI
    - mean: average value across years
    - resolution: 1 km or other supported scales
    - cl0: class/quality flag indicator

- Quality Layer
  - Pattern: <location>_<Veg_index>_percent_<resolution>_cl0.tif
  - What each component conveys:
    - location code
    - Veg_index: NDVI or EVI
    - percent: percentage of good quality observations used in the spectral analysis
    - resolution: 1 km or other supported scales
    - cl0: class/quality flag indicator

## Additional notes for data management

- All TIFF files have a corresponding world file (.tfw) to support georeferencing.
- The cl0 suffix appears consistently across examples, indicating a standard class/quality labeling convention.

## Examples (from the document)

- Average Amplitude
  - aveAmp_SAm_div_EVI_01_500_F1_annual_cl0.tif
- Vegetation Indices Mean
  - SAm_EVI_mean_1km_cl0.tif
- Quality Layer
  - SAm_NDVI_percent_1km.tif

## Relevance for Data Leaders

- Promotes consistent metadata-rich file naming, facilitating data discovery, governance, and cross-team collaboration.
- Enables quick interpretation of key attributes (location, index, resolution, data quality) directly from the filename.
- Supports alignment across multiple data products by using uniform patterns and suffixes (cl0, world file presence).