# climatologies of the tropical Andes 2

## Overview
- Dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes in South America.
- Derived from TRMM Precipitation Radar (TPR) and 723 monthly rainfall gauges using seven satellite-gauge merging methods.
- Document describes file structure, spatial projections, mapped variables, and provides an example R script for opening the files.
- For detailed methodology and scientific interpretation, see Manz et al. (2016).

## Data products and merging methods
- TPR: Mean monthly and annual totals from TRMM Precipitation Radar; re-projected to a 1 km grid and averaged to 5 km; time frames: monthly (1998-2014) and annual.
- OK (ordinary kriging): Interpolates gauge values (1981-2010) to the grid using a Gaussian process with a normal-score transform and chosen semi-variogram models.
- ROK (residual ordinary kriging): Interpolates residuals (TPR minus gauge values) with OK, then adds residuals back to TPR fields.
- KED (kriging with external drift): Uses monthly TPR climatologies as external drift predictors; gauge values are transformed to normal states before semivariogram fitting.
- KED_TN: Like KED but adds NDVI (MODIS) as secondary external drift with a two-month lag; NDVI monthly climatologies correlate with rainfall (ρ = 0.37–0.73).
- RIDW (residual inverse distance weighting): Interpolates residuals via inverse-distance weighting (power = 2) and adds back to the TPR field.
- LM (linear model): Zg = a Zs,g; uses a scaling coefficient to relate gauge to satellite estimates; effectively a multiplicative bias correction.
- Note: Ocean grid pixels are set to NA for all methods except TPR; OK-based estimates beyond the largest semi-variogram range are NA due to reliance on gauge data only.

## Mapped variables
- Total monthly precipitation (mm month-1): averages for 1981-2010 (OK, KED, KED_TN, ROK, RIDW, LM) and 1998-2014 (TPR).
- Total annual precipitation (mm yr-1): same time-framing distinctions as monthly, with TPR using 1998-2014.
- Monthly and annual kriging estimation variance (mm^2 month-1 and mm^2 yr-1), representing uncertainty for kriging estimates.

## Data file structure and spatial projection
- Files are GeoTIFF (.tif) at 5 km resolution in UTM zone 18 (EPSG appropriate for zone 18N/S) with extents roughly:
  - Latitude: -19.2°S to 13.1°N
  - Longitude: -81.7°W to -66.7°W
- The zip archive contains 130 files named by merging method and calendar month (e.g., KED_apr.tif); annual files end with _yr.tif.
- KED and KED_TN include accompanying kriging variance files named with Var (e.g., KED_Var_apr.tif).
- Ocean grid cells are omitted (NA) for non-TPR methods; OK estimates are NA beyond the maximum gauge-range distance (~185 km).
- Example R code shows how to read and reproject the data to lat/lon; data are stored as SpatialGridDataFrame objects with metadata.

## Data access and reuse notes
- The dataset is distributed as a zipped collection of 130 GeoTIFF files, enabling flexible use across methods and time scales.
- Documentation includes an example workflow in R for loading, inspecting, and reprojecting the rasters to a geographic coordinate system.
- Clear conventions for file naming (method, month, _yr for annual, Var for variance) support traceability and reproducibility.
- The material cites the primary scientific source for methodology and interpretation.

## Governance, provenance, and metadata considerations
- Detailed description of each merging method supports data provenance and methodological transparency.
- Metadata conveys spatial projection, resolution, temporal coverage, and the relationship between satellite and gauge data (including transformations and external drift variables like NDVI).
- Users should note the land-only constraint and the various uncertainties captured by kriging variance files.
- Useful for data stewards to ensure consistent storage, discoverability, and clear guidance on choosing the appropriate merging method for analysis.