# Burnt area product for the boreal forest zone derived from MODIS imagery

## Purpose and scope
- A daily-burn date dataset at 500 m resolution for the circumpolar boreal forest zone, covering 2001–2011 (11 TIFF files, one per year).
- Pixel values represent the Julian day of first burn for each year.
- Focuses on the circumpolar boreal forest area defined by FAO ecological zones; latitudinal range 40°N to 70°N.

## Data sources and area description
- Forested areas identified using MODIS Land Cover Type (MOD12Q1) classes 1–8 (forest and woody vegetation).
- Spectral data from:
  - Nadir BRDF-adjusted reflectance (N-BAR) 16-day product MCD43A4 (NIR band 2 and SWIR band 6) for stable reflectance data.
  - 500 m thermal anomalies product MOD14A1 (active fire) to help separate burnt areas and date burns.
  - Snow and fill information via MCD43A2 BRDF-Albedo Quality dataset to exclude snow and invalid pixels.
- Validation reference data from Landsat ETM imagery (approx. 30 m) for annual pixel-level burn interpretation.

## Burnt area detection algorithm
- Key index: Normalised Difference SWIR (NDSWIR) = (NIR - SWIR) / (NIR + SWIR) using MODIS band 2 (NIR) and band 6 (SWIR 1.6 µm); more discriminatory for burnt vs. non-burnt forest than standard NDWI.
- Snow and fill pixels excluded to reduce error.
- Inter-annual change approach due to delay between fire and visible biomass loss in Siberian boreal zones:
  - Compute year-to-year 16-day NDSWIR differences for each pixel.
  - Average differences across all 16-day periods within the snow-free window to obtain a single annual difference value.
- Regional thresholding to separate disturbed from undisturbed:
  - Divide the scene into 16 windows of 600 × 600 pixels to reduce latitudinal/topographic variability.
  - In each window, set threshold at 60% of the difference between the mean of TA-identified burnt pixels and the window mean.
  - Apply threshold to produce a binary burnt/unburnt map; remove small clusters (< four pixels).
- Burn dating:
  - Use Thermal Anomalies (TA) locations to identify pixels that correspond to known burns.
  - Retain burnt pixels that align with a TA and assign those pixels the TA’s Julian Day.
  - Pixels without an associated TA (e.g., cloud-covered) are dated by bilinear interpolation from nearby dated pixels.
- Output: a 500 m resolution raster per year, with values = Julian Day of first burn.

## Temporal and spatial considerations
- Analysis focused on the snow-free period (approximately early June to late August) across the boreal zone to maintain consistency (Julian Days ~161–241), though lower latitudes have longer snow-free periods.
- Each granule covers 2400 × 2400 pixels, with each pixel ~500 m × 500 m.

## Validation procedures and results
- Validation dataset: manual interpretation of Landsat ETM time series at 10 randomly selected sites (stratified by continent), covering ~1.5% of the area; 34.8 million km² total area considered, with 22.6 million km² forest after discarding non-forest.
- For each site, eight ETM images (one per year 2001–2007) were checked and corrected for geolocation errors; images were reprojected to equal-area projection and resampled to match the burnt area map.
- Burnt area references: 504 burnt areas identified in ETM data; 316 (~62%) also detected by the CEH-BA product.
- Pixel-level validation: 65,120 ETM-burnt pixels; 45,807 (70%) also detected by CEH-BA; 47% of CEH-BA burnt pixels within validation area lacked corresponding ETM burnt pixels (commission errors), with about half of these overlapping partially with ETM burnt areas.
- Overall accuracy metric: Kappa coefficient = 0.60, indicating moderate agreement between CEH-BA product and ETM reference data.

## Outputs and interpretation for data use
- The dataset provides a longitudinal series of burnt area maps with explicit burn dates, enabling temporal analyses of boreal fire dynamics.
- Outputs are suitable for integration with other MODIS-derived products (land cover, thermal anomalies) for broader data-driven analyses and policy/research use.
- Users should be aware of validation results indicating moderate agreement and potential commission errors, especially in areas with partial overlap between product detections and ETM references.

## References
- C. George, C. Rowland, F. Gerard, and H. Balzter, "Retrospective mapping of burnt areas in Central Siberia using a modification of the normalised difference water index," Remote Sensing of Environment, 2006.