# climatologies of the tropical Andes 2

## Overview
- Dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes, derived from TRMM Precipitation Radar (TPR) and 723 monthly rainfall gauges using seven satellite-gauge merging methods.
- Describes file structure, spatial projections, and mapped variables; includes an example R script to open the files.
- For detailed background on TPR processing, merging methods, and interpretation, see Manz et al. (2016) High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.

## Rainfall products and merging methods
- TPR: Mean monthly and annual totals from TRMM Precipitation Radar (TPR). 1 km resampled to 5 km; time spans 1998–2014 (annual) and calendar months of those years (monthly).
- OK (ordinary kriging): Spatial interpolation of 1981–2010 gauge totals to 5 km using Gaussian processes; gauge data transformed to normal, then back-transformed after kriging.
- ROK (residual ordinary kriging): Interpolates residuals (TPR vs gauge) with OK and adds residuals to the TPR field.
- KED (kriging with external drift): External drift using monthly TPR climatologies as predictor variables; gauge values transformed to normal prior to semivariogram fitting.
- KED_TN: Like KED but uses MODIS NDVI as external drift with a two-month lag; NDVI climatologies derived from MODIS; correlation with gauge rainfall ρ = 0.37–0.73.
- RIDW (residual inverse distance weighting): Interpolates residuals with IDW (power = 2) and adds to the original TPR climatology.
- LM (linear model): Zg = a Zs,g using satellite estimates to predict gauge rainfall; intercept dropped (scalar multiplication only) for comparability to multiplicative bias correction.

Notes:
- Ocean grid pixels are set to NA; OK estimates beyond the largest variogram range (~185 km) from gauges are NA.

## Mapped variables
- Total monthly precipitation (mm/month) averaged over 1981–2010 for OK, KED, KED_TN, ROK, RIDW, and LM; TPR uses 1998–2014.
- Total annual precipitation (mm/yr) averaged over 1981–2010 for the same methods; TPR uses 1998–2014.
- Kriging estimation variance (mm^2/month or mm^2/yr) as a measure of uncertainty for the corresponding kriging estimates.

## Data file structure and spatial projection
- Files: 130 GeoTIFFs (.tif) at 5 km resolution in UTM zone 18; spatial coverage roughly -19.2°S to 13.1°N, -81.7°W to -66.7°W.
- Naming: files named by method and calendar month (e.g., KED_apr.tif); annual maps end with _yr.tif; accompanying KED_Var_apr.tif files provide kriging variance.
- The zip bundle includes all files and notes on re-projection and conversion to lat/lon.

## Example R code for data extraction
- Provides sample workflow to read and convert GeoTIFFs to latitude/longitude using sp and rgdal in R.
- Demonstrates:
  - Unzipping and loading KED_apr.tif and KED_Var_apr.tif
  - Inspecting the SpatialGridDataFrame structure and projection
  - Re-projecting to longlat WGS84
  - Accessing metadata such as grid coordinates, cell size, and number of points
- Useful for reproducibility and integration with other datasets.