# Burnt area product for the boreal forest zone derived from MODIS imagery

## Overview
- Daily burn date at 500m resolution for the circumpolar boreal forest zone, provided as annual rasters for 2001–2011 (11 TIFF files).
- Pixel values represent the Julian day of the first burn in that year.
- Validated against Landsat ETM reference data; Kappa of 0.60 indicating moderate agreement.

## Study area and data sources
- Circumpolar boreal forest area defined by FAO Global Ecological Zones: boreal tundra woodland, boreal coniferous forest, boreal mountain systems; about 47 million km2, latitudinal range 40°N to 70°N.
- Countries: Russia, Canada, USA (Alaska), Norway, Sweden, Finland, and parts of China.
- Forested/woody areas identified using MODIS Land Cover Type (MOD12Q1) IGBP classes 1–8.
- Data used:
  - 16-day MODIS Nadir BRDF-Adjusted Reflectance (N-BAR) product (MCD43A4) for spectral bands, enabling stable vegetation monitoring.
  - Daily MODIS Thermal Anomalies product (MOD14A1) to locate burn events and date burning.
  - Snow mask and quality filtering from MODIS products (e.g., MCD43A2 BRDF_Albedo_Quality).
- Pixel size in outputs: ~500m (2400 × 2400 per granule).

## Burnt area detection algorithm
- Core index: Normalised Difference SWIR (NDSWIR) using NIR (MODIS band 2) and SWIR (MODIS band 6; 1.6 µm) to proxy canopy water content.
  - NDSWIR = (NIR − SWIR) / (NIR + SWIR)
  - 1.6 µm SWIR improves discrimination between burnt and non-burnt forest.
- Pre-processing: exclude snow-affected pixels and any fill values via quality datasets.
- Temporal focus: operate on the snow-free period (early June to late August; from Julian Day 161 to 241), consistent across latitudes.
- Inter-annual differencing: for each pixel, compute year-to-year changes by subtracting the previous year’s 16-day NDSWIR value from the current year’s for each 16-day period; average these differences to obtain a single annual difference value (Eq. 2).
- Disturbance detection:
  - Divide the study area into 16 windows of 600 × 600 pixels to reduce latitudinal/topographic variability.
  - In each window, use TA locations to identify known burnt pixels and compute a threshold: 60% of the difference between the window mean and the mean of known burnt pixels.
  - Apply threshold to produce a binary burnt/undisturbed map; remove clusters smaller than four pixels to reduce false positives.
- Burn dating:
  - Use thermal anomalies to assign burn dates to pixel clusters that correspond to TA-confirmed burns.
  - Pixels without a TA date are dated by bilinear interpolation from nearby dated pixels.
- Output: a 500m-resolution raster per year with pixel values equal to the Julian day of first burn.

## Burnt area product and data format
- Output product: 11 TIFF files (one per year, 2001–2011).
- Each file contains a raster where 1) burnt areas are identified, and 2) pixel values encode the Julian day of first burn for that year.

## Validation
- Reference data: manual interpretation of annual Landsat ETM timeseries (approx. 30 m) at 10 randomly selected locations, stratified by continent.
- Area and time: 2001–2007; for each location, eight images (one per year); baseline from 2000 to identify pre-2001 burns.
- Process: geo-location corrections, reprojected to equal-area projection, resampled to match 500m grid; pixel-by-pixel comparison excluding unclassified areas.
- Validation scope: from 34.8 million km2 (excluding water), 12.2 million km2 non-forest discarded, leaving 22.6 million km2 forest area evaluated.

## Results
- Identified 504 burnt areas in ETM imagery; 316 (62%) were at least partly detected by the CEH-BA product.
- Pixel-scale: 65,120 ETM-burnt pixels; 45,807 (70%) overlapped with CEH-BA burnt pixels.
- Commission errors: 41,719 (47%) of CEH-BA burnt pixels within the validation area had no corresponding ETM burnt pixel; about half of these (20,856) lay within CEH-BA burnt areas that overlapped with ETM-burnt areas.
- Overall agreement: Kappa = 0.60.
- Figure reference: boreal forest area with validation scene locations.

## Limitations and notes
- Some burnt areas identified by CEH-BA do not correspond to ETM-identified burns, indicating possible commission errors or detection of pre-cloud/late-burn biomass changes.
- Temporal gaps due to cloud cover can leave undated pixels; interpolation used to assign dates where TA data are missing.
- Validation limited to 2001–2007 periods due to Landsat availability; longer-term validation not shown.

## References
- C. George, C. Rowland, F. Gerard, and H. Balzter, "Retrospective mapping of burnt areas in Central Siberia using a modification of the normalised difference water index," Remote Sensing of Environment, 2006.