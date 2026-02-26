# climatologies of the tropical Andes 2

## Overview
- Dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes, derived from TRMM Precipitation Radar (TPR) and 723 monthly rainfall gauges using seven satellite-gauge merging methods.
- Time periods: TPR products (1998-2014) and gauge-based climatologies (1981-2010); monthly and annual totals are provided for multiple merging approaches.
- Contents include 130 GeoTIFF files (5 km, UTM zone 18) and accompanying kriging estimation variance files for monthly and annual maps.
- Maps include total monthly precipitation (mm month-1) and total annual precipitation (mm yr-1); TPR maps use their respective time ranges.
- An example R-script to open and reproject the data is provided; background references describe data processing and interpretation.

## Data content and merging methods
- Mapped variables
  - Monthly precipitation totals (mm month-1) for OK, KED, KED_TN, ROK, RIDW, LM (1981-2010) and TPR (1998-2014).
  - Annual precipitation totals (mm yr-1) for the same methods and periods.
  - Kriging estimation variance for monthly and annual maps (uncertainty measure).
- Merging methods described
  - TPR: Satellite-derived climatologies reprojected to 5 km; used as baseline.
  - OK (ordinary kriging): interpolates gauge data to a grid using Gaussian process covariance.
  - ROK (residual ordinary kriging): interpolates residuals (TPR minus gauges) and adds back to TPR.
  - KED (kriging with external drift): uses monthly TPR fields as external drift; gauges transformed to normal states.
  - KED_TN: same as KED but adds NDVI (MODIS) as a secondary external drift with a two-month lag.
  - RIDW (residual inverse distance weighting): kriging residuals then IDW interpolation.
  - LM (linear model): simple scaling relationship between TPR and gauge values.

## Data file structure and projection
- File organization
  - 130 GeoTIFF files named by merging method and month (e.g., KED_apr.tif); annual maps end with _yr.tif.
  - Accompanying kriging variance files for monthly and annual maps (e.g., KED_Var_apr.tif).
- Spatial specifics
  - 5 km grid, UTM zone 18 projection; coverage roughly -19.2°S to 13.1°N and -81.7°W to -66.7°W.
  - Ocean grid pixels set to NA for all merging methods except TPR; OK estimates beyond the largest semivariogram range are NA.
- Data packaging
  - The zip contains 130 files with the naming convention described.

## Using the data
- Example workflow provided in R
  - Load necessary libraries (sp, rgdal).
  - Unzip and read files (e.g., KED_apr.tif, KED_Var_apr.tif) using readGDAL.
  - Inspect data structure, projection, and convert to lat/lon for mapping and analysis.
- Data interpretation notes
  - Variance files provide uncertainty alongside the corresponding precipitation maps.
  - NDVI-based external drift (KED_TN) includes a two-month lag to reflect vegetation response.

## References and guidance
- For detailed methodology, data processing steps, and interpretation, see Manz et al. (2016) High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.
- The document also provides a brief explanation of the mapped variables and the rationale behind different merging approaches.

## Practical considerations for data support
- Patchy gauge coverage and multiple merging methods require careful data integration and validation when creating end-user data products.
- Handling NA values is necessary for ocean areas and distant grid points outside gauge influence.
- When combining monthly and annual products, align temporal coverage and consider method-specific characteristics (e.g., TPR baseline vs gauge-based adjustments).
- Potential to link these rainfall climatologies with ancillary data (e.g., NDVI) for advanced analyses and dashboards.