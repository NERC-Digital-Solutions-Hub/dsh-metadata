# S2LC_2018 Supporting Information

## Study Area
- Upper Welland Catchment (~340 km2) at 52.6°N, 0.6°W, spanning Leicestershire, Rutland and Northamptonshire.
- Land use is predominantly agricultural.

## Classification Methodology
- Purpose: produce a fine-resolution land cover map for 2018 (S2LC_2018) using a random forest classifier on Sentinel-2 imagery in Google Earth Engine (GEE), with post-classification processing in QGIS.
- Imagery and mosaic: cloud-free multiband Sentinel-2 mosaic created from eight images captured 1 May–30 September 2018; the per-pixel value is the 50th percentile across the eight images.
- Bands used (with resolutions): Band 2 (Blue, 10 m), Band 3 (Green, 10 m), Band 4 (Red, 10 m), Band 5–7 (Vegetation Red Edge, 20 m), Band 8 (NIR, 10 m), Band 12 (SWIR, 20 m).
- Training data: 1,581 polygons for 10 land cover classes, built from:
  - LCM2018 (CEH)
  - Crop map of England (CROME) 2018 (RPA)
  - GWCT Allerton Project crop maps
- Processing workflow: RF classification in GEE, export to QGIS v3.6.1; post-processing included sieve filtering of polygons <20 pixels and manual correction using Thematic Raster Editor (ThRasE v20.3.23).

## Technical Details
- CRS and extent: EPSG 27700 (OSGB 1936 / British National Grid); pixel size 10 m; overall raster size 4925 × 5788.
- Output: single 10-class GeoTIFF; data type Int32.
- Thematic classes (10): Woodland, Grassland, Water, Built Environment, Cereal Crops, Oilseed Rape, Legumes, Potato/Beet, Bare Earth / Inland Rock, Maize.
- Class descriptions are provided for each class.

## Accuracy Assessment
- Validation: 700 random points.
- Overall accuracy: 92.1%; Kappa: 0.91.
- Class-level accuracy (Producer / User):
  - Woodland: 89.4% / 93.3%
  - Grassland: 95.5% / 88.2%
  - Water: 100.0% / 100.0%
  - Built Environment: 85.0% / 89.5%
  - Cereal Crops: 94.9% / 92.9%
  - Oilseed Rape: 96.9% / 91.3%
  - Legumes: 84.2% / 94.1%
  - Potato/Beet: 92.9% / 89.7%
  - Bare Earth / Inland Rock: 83.0% / 97.5%
  - Maize: 80.8% / 100.0%
- The overall metrics and per-class accuracies are supported by Appendix 1 confusion matrix (n = 700).