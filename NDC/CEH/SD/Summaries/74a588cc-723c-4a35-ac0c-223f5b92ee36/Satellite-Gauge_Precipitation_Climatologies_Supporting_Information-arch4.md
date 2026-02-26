# climatologies of the tropical Andes 2

## Overview
- A dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes in South America.
- Derived from the TRMM Precipitation Radar (TPR) and 723 rainfall gauges using seven satellite-gauge merging methods.
- Includes file structure, spatial projections, and a brief explanation of mapped variables; provides an example R-script to open the files.
- Primary scientific background is Manz et al. (2016) on high-resolution satellite-gauge merged precipitation climatologies of the tropical Andes.

## Data products and merging methods
- TPR: Mean monthly/annual rainfall from TRMM Precipitation Radar; re-projected to a 1 km grid and averaged to 5 km.
- OK (ordinary kriging): Spatial interpolation of gauge data (1981-2010) with Gaussian covariance; normal-score transform and back-transform.
- ROK (residual ordinary kriging): Interpolates residuals (TPR minus gauge) and adds back to TPR field.
- KED (kriging with external drift): Uses monthly TPR climatologies as external drift in universal kriging.
- KED_TN: Like KED, plus MODIS NDVI as an external drift variable with a two-month lag (ρ between 0.37-0.73).
- RIDW (residual inverse distance weighting): Interpolates residuals via inverse-distance weighting and adds to TPR field.
- LM (linear model): Simple regression Zg = a Zs,g to estimate ungauged rainfall from satellite estimates.
- Note: Ocean grid pixels are NA for all methods except TPR; OK estimates beyond the largest variogram range from gauges are NA.

## Variables and coverage
- Total monthly precipitation (mm month-1) for OK, KED, KED_TN, ROK, RIDW, LM; TPR provides mean monthly totals (1998-2014).
- Total annual precipitation (mm yr-1) for OK, KED, KED_TN, ROK, RIDW, LM; TPR provides mean annual totals (1998-2014).
- Kriging estimation variance (monthly and annual) expressed in mm^2 month-1 and mm^2 yr-1, respectively, representing uncertainty of the estimates.

## Data file structure and spatial projection
- All files are GeoTIFF (.tif) at 5 km resolution in a UTM zone 18 projection.
- Spatial extent roughly -19.2°S to 13.1°N (lat) and -81.7°W to -66.7°W (lon); conversion to lat/lon shown in example code.
- The zip archive contains 130 files named by merging method and calendar month (e.g., KED_apr.tif); annual files end with _yr.tif.
- Accompanying variance files exist for monthly and annual maps (e.g., KED_Var_apr.tif) containing kriging variance values.
- Example data access and transformation to latitude/longitude are provided via R (sp and rgdal).

## Access and example workflow
- The document includes example R code to:
  - unzip and read a specific file (e.g., KED_apr.tif) and its corresponding variance file.
  - inspect class, structure, and projection details.
  - re-project from UTM to latitude/longitude for non-gridded coordinates.

## Practical considerations for data leaders
- Data stewardship: multiple merging methods offer alternative representations of rainfall; choose method based on data gaps, ocean exclusion, and uncertainty (variance maps available).
- Data quality and gaps: sparse gauge coverage can affect accuracy; KED_TN leverages NDVI as a proxy for vegetation response to rainfall (lagged), potentially improving estimates in data-poor areas.
- Discoverability and metadata: 130 files with clear naming conventions; accompanying variance files aid uncertainty assessment.
- Collaboration and reuse: dataset aligns with broader satellite-gauge merging approaches; supports cross-network data practice by providing standardized, well-documented rainfall climatologies for the tropical Andes.

## References
- Manz, B., W. Buytaert, Z. Zulkafli, W. Lavado, B. Willems, L.-A. Robles, and J.-P. Rodriguez-Sanchez (2016). High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.