# climatologies of the tropical Andes 2

## Overview
- A dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes, derived from TRMM Precipitation Radar (TPR) and 723 monthly rainfall gauges using seven satellite-gauge merging methods.
- Describes file structure, spatial projections, and a brief explanation of the mapped variables; includes an example R script to open the files.
- For detailed background on TPR processing and merging methods, refer to Manz et al. (2016) High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.

## Merging methods (overview)
- TPR: Mean monthly and annual totals from TRMM Precipitation Radar, re-projected to a fine grid and averaged to the target time scales, then averaged back to 5 km.
- OK: Ordinary kriging using gauge data (1981-2010) with normal-score transformation, selecting variogram models by visual inspection and SSE.
- ROK: Residual ordinary kriging; interpolate residuals (TPR − gauge) with OK and add back to TPR fields.
- KED: Kriging with external drift; monthly TPR fields act as predictors (external drift) for gauge rainfall.
- KED_TN: Like KED but adds MODIS NDVI as an external drift with a two-month lag to reflect vegetation response; NDVI and rainfall show ρ = 0.37–0.73.
- RIDW: Residual inverse distance weighting; interpolate residuals with IDW (power = 2) and add to original TPR fields.
- LM: Linear model using TPR rainfall to estimate gauge rainfall at ungauged locations (Zg = a Zs,g + b, with b dropped to compare to multiplicative bias correction).

- Ocean grid pixels are NA for all methods except OK; OK estimates farther than ~185 km from the nearest gauge are also NA.

## Mapped variables
- Total monthly precipitation (mm month^-1) for 1981-2010 (OK, KED, KED_TN, ROK, RIDW, LM) and for 1998-2014 (TPR).
- Total annual precipitation (mm yr^-1) for the same methods and periods as monthly totals.
- Monthly and annual kriging estimation variance (uncertainty) in mm^2 month^-1 and mm^2 yr^-1, respectively.

## Data file structure and spatial projection
- Files are GeoTIFF (.tif) at 5 km resolution, in a Universal Transverse Mercator projection (UTM zone 18).
- Spatial coverage approximately -19.2°S to 13.1°N latitude and -81.7°W to -66.7°W longitude.
- File naming: each merging method and calendar month (e.g., KED_apr.tif); annual files end with _yr.tif. Kriging variance files include “Var” in the name (e.g., KED_Var_apr.tif) for monthly and annual maps.
- The zip archive contains 130 files in total.
- The document provides guidance on reprojecting from UTM to lat/lon (non-gridded) and includes example metadata/details in the R workflow.

## Example R code for data extraction
- The documentation includes example R code to:
  - Load necessary libraries (sp, rgdal).
  - Unzip and read a specific file (e.g., KED_apr.tif) and its corresponding variance file (e.g., KED_Var_apr.tif).
  - Inspect the SpatialGridDataFrame structure and reproject to latitude/longitude using spTransform.
  - Illustrative steps show converting data and projecting coordinates for use in analyses or visualization.

## Usage and reference
- The dataset is grounded in satellite-gauge merging methodology with explicit uncertainty (kriging variance) accompanying the rainfall fields.
- Primary reference: Manz, B. et al. (2016) High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.