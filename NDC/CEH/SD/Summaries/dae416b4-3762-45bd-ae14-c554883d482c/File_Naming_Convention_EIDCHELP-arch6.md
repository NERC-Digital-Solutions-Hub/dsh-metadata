# Cd File Naming Convention EIDCHELP-15389

- This document defines the file naming conventions for data products related to average amplitude, vegetation indices, and quality layers, to support consistent data discovery and usage.

## Average Amplitude

- Pattern: <geographical projection>_aveAmp_<location>_[<div>]_<Veg_index>_<ndvi thresh>_<resolution>_<input data>_cl0.tif
- aveAmp definition: average peak-to-trough, computed as amplitude * 2.0 / √0.5
- Location codes: e.g., SAm = South America
- div: normalised by mean vegetation index
- Veg_index: NDVI, EVI
- ndvi_thresh: if the mean VI over all years is < 0.1, the area is masked as no vegetation
- resolution options: 500 m, 1 km, 05x05 = 0.5 degree cells
- weighted: when upscaled to 0.5 degree resolution, output is weighted by latitude

## Vegetation Indices Mean

- Pattern: <location>_<Veg_index>_mean_<resolution>_cl0.tif
- Example: SAm_EVI_mean_1km_cl0.tif
- Location, Veg_index, mean indicator, resolution, and cl0 in the filename

## Quality Layer

- Pattern: <location>_<Veg_index>_percent_<resolution>_cl0.tif
- Example: SAm_NDVI_percent_1km.tif
- Indicates the percentage of good quality observations used in the spectral analysis
- cl0 qualifier included in the filename

## Additional notes

- All TIFF files have a corresponding world file (.tfw) that should be used with the TIFF for georeferencing.