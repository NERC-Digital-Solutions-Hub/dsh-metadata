# climatologies of the tropical Andes 2

- A dataset of mean monthly and annual climatological rainfall maps at 5 km resolution for the tropical Andes, derived from TRMM Precipitation Radar (TPR) and gauge data using seven satellite-gauge merging methods.
- Time coverage:
  - TPR-based products: 1998-2014 (monthly and annual)
  - Gauge-based products: 1981-2010 (monthly and annual)
- Purpose: provide standardised rainfall climatologies to support environmental health monitoring, policy performance assessment, and cross-time comparisons.

## Data and merging methods

- TPR (satellite-based rainfall totals)
  - Uses TRMM Precipitation Radar data reprojected to 1 km, then averaged to 5 km.
- OK (ordinary kriging)
  - Interpolates mean monthly/annual gauge values (1981-2010) using a Gaussian process with normal-score transformation.
- ROK (residual ordinary kriging)
  - Interpolates residuals between TPR estimates and gauge values, then adds residuals back to TPR fields.
- KED (kriging with external drift)
  - Uses monthly TPR climatologies as external drift to predict gauge values; gauge data transformed to normal states.
- KED_TN
  - Extends KED by including MODIS NDVI as a secondary external drift term (lagged by two months to reflect vegetation response).
- RIDW (residual inverse distance weighting)
  - Interpolates residuals using IDW (power = 2) and adds back to TPR fields.
- LM (linear model)
  - Simple scaling relationship between TPR and gauge rainfall (Zg = a Zs,g), effectively a multiplicative bias correction.

- Outputs
  - Total monthly precipitation (mm month-1) and total annual precipitation (mm yr-1) for each method (OK, KED, KED_TN, ROK, RIDW, LM) and for TPR (monthly 1998-2014; annual 1998-2014).
  - Kriging estimation variance for monthly and annual maps (uncertainty).

## Data structure, format and projection

- File format and resolution
  - GeoTIFF (.tif) at 5 km resolution.
  - Spatial coverage approximately -19.2°S to 13.1°N and -81.7°W to -66.7°W.
- Projection
  - Data stored in Universal Transverse Mercator (UTM) zone 18; lat/lon conversion provided for non-gridded outputs.
- File collection
  - A ZIP archive contains 130 files named by merging method and calendar month (e.g., KED_apr.tif); annual maps end with _yr.tif.
  - Each method has corresponding kriging variance files for monthly and annual maps (e.g., KED_Var_apr.tif).
- Ocean masking
  - Except for TPR, ocean grid pixels are set to NA for all merging methods.
  - OK estimates beyond the largest semi-variogram range (~185 km) from gauges are NA.
- Metadata and example workflow
  - Includes example R code to read and reproject data to lat/lon, demonstrating data access and basic inspection.

## Variables mapped

- Monthly precipitation totals (mm month-1)
- Annual precipitation totals (mm yr-1)
- Kriging estimation variance (uncertainty, mm^2 month-1 or mm^2 yr-1)

## Access, usage and reference

- Data organization
  - 130 total files across seven methods and monthly/annual resolutions; accompanying variance files for kriging-based methods.
- Practical use for analysts
  - Standardised, comparable rainfall climatologies across methods support monitoring of environmental conditions and policy performance over time.
  - Multiple merging approaches enable cross-validation and assessment of uncertainty.
- Reference
  - Manz, B. et al. (2016). High-resolution satellite-gauge merged precipitation climatologies of the tropical Andes, Journal of Geophysical Research: Atmospheres.
- Accessibility note
  - Datasets are stored as georeferenced rasters suitable for integration into environmental monitoring portals and analyses.