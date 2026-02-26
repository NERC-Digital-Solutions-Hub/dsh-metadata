# Burnt area product for the boreal forest zone derived from MODIS imagery

## Overview
- A daily-burn-date product for the circumpolar boreal forest zone at 500 m resolution.
- 11 TIFF files covering years 2001–2011; each pixel value is the Julian day of the first burn in that year.
- Validation against Landsat ETM reference images yielded a Kappa of 0.60.

## Data scope and area
- Boreal forest area defined by FAO Global Ecological Zones: Boreal tundra woodland, Boreal coniferous forest, Boreal mountain system.
- Latitudinal extent: 40°N to 70°N; includes Russia, Canada, USA (Alaska), Norway, Sweden, Finland, and part of China.
- Forested/woody areas identified using MODIS Land Cover Type (MOD12Q1) classes 1–8.

## Data sources and inputs
- Spectral inputs: 16-day MODIS Nadir BRDF-Adjusted Reflectance (N-BAR) product MCD43A4 (bands in NIR and SWIR) for stable reflectance.
- Active fire information: MODIS Thermal Anomalies product MOD14A1 to identify burnt pixels and dates.
- Snow/fill masking: MODIS BRDF-Albedo Quality MCD43A2 to exclude snow; pixels with fill values removed.
- Temporal window: analysis focused on snow-free period (approximately 161–241 Julian days) for consistency across latitudes.

## Burnt area detection algorithm
- Index used: Normalised Difference SWIR (NDSWIR) = (NIR − SWIR) / (NIR + SWIR) using MODIS band 2 (NIR) and band 6 (SWIR); 1.6 µm SWIR band improves discrimination of burnt vs. non-burnt forest.
- Inter-annual difference: compute year-over-year 16-day NDSWIR differences per pixel, then average across the 16-day periods to get a single annual difference value.
- Variability control: divide the study area into 16 windows of 600 × 600 pixels to reduce latitudinal/topographic variability.
- Thresholding: within each window, set a 60% threshold of the difference between the mean of known burnt pixels (from TA) and the window mean to produce a binary burnt/unburnt map.
- Small-patch filtering: remove burnt clusters smaller than four pixels.
- Burn area vs. date: use TA to confirm burnt pixels; assign Julian Day to pixels within burnt areas that correspond to a TA. Pixels lacking a TA date are dated by bi-linear interpolation from nearby dated pixels.

## Output, dating, and data management
- Output: 500 m resolution raster maps for each year (2001–2011) with pixel values equal to the Julian day of first burn.
- Data handling: method yields disturbed areas including some non-burn disturbances; dating yields a mix of dated and undated pixels, with undated ones interpolated from around-dated pixels.
- Data availability and updates: the product is designed for ongoing sharing and updating within data portals/catalogues (as per data steward practices), with explicit provenance from MODIS inputs and TA validation.

## Validation and accuracy
- Validation reference: manual interpretation of Landsat (ETM) time series (~30 m) at 10 sites (stratified by continent), across 2001–2007.
- Area and sampling: evaluated about 22.6 million km² of forested area; 504 burnt areas identified in Landsat; 316 (62%) were at least partially detected by the CEH-BA product.
- Pixel-level results: 65,120 Landsat-burnt pixels; 45,807 (70%) overlapped with CEH-BA; 41,719 (47%) CEH-BA burnt pixels had no Landsat counterpart (commission errors, with half of these overlapping with other CEH-BA burnt areas).
- Overall agreement: Kappa = 0.60.

## Data quality, limitations, and considerations for data stewards
- Temporal limitations: cloud cover and snow can leave portions undated; some pixels dated via interpolation.
- Spatial limitations: windowed thresholding mitigates, but does not eliminate, local variability; some misclassifications occur in heterogeneous landscapes or small burns.
- Validation limitations: Landsat-based reference data provide a benchmark but indicate notable commission and omission tendencies; interpretation and geo-location adjustments were needed prior to comparison.

## Reproducibility and references
- Key methodology references: George, Rowland, Gerard, and Balzter (2006) on retrospective burnt-area mapping using a modified Normalised Difference Water Index.
- Data lineage: derived from MODIS sources (N-BAR reflectance, active fire TA) and validated against high-resolution Landsat ETM data.