# Burnt area product for the boreal forest zone derived from MODIS imagery

## Overview
- Presents a burnt area product for the circumpolar boreal forest zone using MODIS imagery.
- Outputs: 11 TIFF files (one per year, 2001–2011); each pixel value is the Julian day of the first burn that year.
- Validation against Landsat ETM reference imagery yields a Kappa of 0.6.

## Study area and data sources
- Study area defined as the circumpolar boreal forest per FAO Global Ecological Zones: boreal tundra woodland, boreal coniferous forest, boreal mountain system; about 47 million km2, lat 40–70°N.
- Included countries: Russia, Canada, USA (Alaska), Norway, Sweden, Finland, and a small part of China.
- Forested and woody areas identified using MODIS Land Cover Type (MOD12Q1) classes 1–8.
- Data sources:
  - Nadir BRDF-Adjusted Reflectance (N-BAR) 16-day product MCD43A4 for spectral information (NIR and SWIR) to support vegetation phenology and burn assessment.
  - MODIS Thermal Anomalies product (TA) MOD14A1 to identify burn dates and separate burnt areas from other disturbances.
  - Snow masking via BRDF-Albedo Quality 16-day product MCD43A2; data granules ~2400×2400 pixels at ~500 m resolution.

## Burnt area detection algorithm
- Core index: Normalised Difference SWIR (NDSWIR) using NIR (MODIS band 2) and SWIR (MODIS band 6), with 1.6 µm band for improved discrimination between burnt and non-burnt forest.
  - NDSWIR = (NIR − SWIR) / (NIR + SWIR).
- Snow and invalid data are excluded using quality masks (BRDFAlbedo quality and fill values).
- Disturbance detection relies on inter-annual change:
  - For each pixel, compute the 16-day NDSWIR value differences between year y and year y−1.
  - Average these differences across the 16-day periods to obtain a single annual difference value.
- Spatial variability mitigation:
  - Divide the scene into 16 windows of 600×600 pixels.
  - In each window, set a threshold at 60% of the difference between the mean of known burnt pixels (from TA) and the window mean to classify burnt vs. unburnt.
  - Remove small clusters <4 pixels to reduce false positives.
- Burn dating:
  - Use TA locations to assign burn dates to burnt pixels.
  - Pixels within burnt areas without a TA are discarded unless dated by proximity to TA-dated pixels.
  - Undated pixels are dated via bilinear interpolation from nearby dated pixels.
- Output:
  - A 500 m burn map per year with pixel values equal to the Julian day of first burn in that year.

## Validation procedure
- Reference data: manual interpretation of annual Landsat ETM time-series (≈30 m) from random stratified sites across continents.
- Sampling:
  - 10 ETM locations, totaling about 1.5% of study area; 2001–2007 period; up to eight images per site per year.
  - Baseline year 2000 used to identify pre-2001 burns.
  - Preference for summer acquisitions (June–August) when available.
- Method:
  - Geolocation corrections, reprojection to equal-area sinusoidal projection, and pixel-by-pixel comparison after excluding unclassified areas.
- Results:
  - 504 burnt areas identified in ETM; 316 (62%) also detected by the CEH-BA product.
  - Per-pixel: 65,120 ETM burnt pixels; 45,807 (70%) overlap with CEH-BA.
  - Commission errors: 41,719 CEH-BA burnt pixels without ETM counterpart (47% of CEH-BA burnt pixels); about half of these overlap with ETM-burnt areas.
  - Overall agreement: Kappa = 0.60.

## Key findings and implications
- The inter-annual NDSWIR difference approach, combined with TA validation and windowed regional thresholds, enables detection of biomass loss and disturbance associated with burning in boreal forests.
- Integration of multiple MODIS products (N-BAR, TA, snow mask) supports robust burnt area identification and burning date assignment at 500 m resolution.
- Validation indicates moderate agreement with high-resolution Landsat references; the method reasonably detects major burnt areas but exhibits commission errors, highlighting regional variability and detection limits due to cloud, snow, and data gaps.
- The approach provides annual, date-specific burnt area maps suitable for monitoring and informing policy decisions within the boreal forest monitoring framework.

## Data and methodological notes for monitoring practice
- Data sources are publicly available MODIS products, enabling reproducibility and integration into monitoring workflows.
- The method explicitly accounts for spatial variability and data gaps, using windowed thresholds and interpolation for undated pixels.
- The requirement to align with high-resolution reference data and manage cloud/snow constraints is addressed through quality masks and validation design.
- Output products (annual 500 m burnt area maps with burn dates) support temporal trend analysis and policy-relevant reporting for boreal fire disturbance.