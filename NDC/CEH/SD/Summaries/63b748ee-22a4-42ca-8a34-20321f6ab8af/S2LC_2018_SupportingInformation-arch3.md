# S2LC_2018 Supporting Information

- Overview
  - Describes the study area, classification methodology, technical details, and accuracy information for S2LC_2018, a fine-resolution land cover map of the Upper Welland catchment (UK) for 2018.
  - Part of a PhD project on Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment, supported by CENTA.

## Study Area
- Upper Welland Catchment area: about 340 km² (52.6°N, 0.6°W).
- Located in Leicestershire, Rutland and Northamptonshire; predominantly agricultural land use.

## Classification Methodology
- Approach: Random forest classification of Sentinel-2 imagery in Google Earth Engine (GEE); post-classification processing in QGIS v3.6.1.
- Image preprocessing:
  - Cloud-free mosaic created from eight Sentinel-2 images (1 May 2018 to 30 September 2018) with per-pixel values equal to the 50th percentile across images.
  - Eight input bands used (see Band details below).
- Training data:
  - 1,581 training polygons for 10 land cover classes.
  - Reference datasets: LCM2018 (UK Centre for Ecology and Hydrology), Crop Map of England (CROME, Rural Payments Agency), GWCT Allerton Project crop maps.
  - Training polygons uploaded to GEE for random forest classification.
- Post-processing:
  - Sieve function to remove polygons <20 pixels.
  - Manual correction of remaining classification errors using Thematic Raster Editor (ThRasE v. 20.3.23) in QGIS.
- Outputs:
  - Classified raster exported to QGIS for post-processing; final product is a GeoTiff with 10 m pixel size.

## Technical Details
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Extent and resolution:
  - Extent coordinates: approx. x 462,783 to 512,033; y 282,044 to 339,924 (British National Grid).
  - Pixel size: 10 m; raster dimensions: 4925 x 5788.
- Thematic resolution: 10 classes.
- Data type: 32-bit signed integer (Int32).
- File type: GeoTiff.

## Sentinel-2 Bands Used (Inputs for Random Forest)
- Band 2 (Blue): 0.490 μm, 10 m
- Band 3 (Green): 0.560 μm, 10 m
- Band 4 (Red): 0.665 μm, 10 m
- Band 5 (Vegetation Red Edge): 0.705 μm, 20 m
- Band 6 (Vegetation Red Edge): 0.740 μm, 20 m
- Band 7 (Vegetation Red Edge): 0.783 μm, 20 m
- Band 8 (NIR): 0.842 μm, 10 m
- Band 12 (SWIR): 2.190 μm, 20 m

## Land Cover Classes
1) Woodland — Broad-leaved and coniferous woodland, woody vegetation, hedgerows, tree boundaries  
2) Grassland — Grazing, amenity, or permanent grassland  
3) Water — Inland water bodies  
4) Built Environment — Urban/suburban areas, paved areas, roads  
5) Cereal Crops — Winter/spring sown wheat, barley, oats  
6) Oilseed Rape — Winter/spring sown oilseed rape  
7) Legumes — Field beans or spring peas  
8) Potato / Beet — Cropped areas of potato or sugar beet  
9) Bare Earth / Inland Rock — Fallow fields, bare soil, quarried areas  
10) Maize — Cropped areas of maize  

## Accuracy Assessment
- Validation approach: 700 randomly selected points across the map.
- Key accuracy metrics (class-level):
  - Woodland: Producer 89.4%, User 93.3%
  - Grassland: Producer 95.5%, User 88.2%
  - Water: Producer 100.0%, User 100.0%
  - Built Environment: Producer 85.0%, User 89.5%
  - Cereal Crops: Producer 94.9%, User 92.9%
  - Oilseed Rape: Producer 96.9%, User 91.3%
  - Legumes: Producer 84.2%, User 94.1%
  - Potato/Beet: Producer 92.9%, User 89.7%
  - Bare Earth/Rock: Producer 83.0%, User 97.5%
  - Maize: Producer 80.8%, User 100.0%
- Overall metrics:
  - Overall accuracy: 92.1%
  - Kappa: 0.91
- Appendix: Confusion matrix supporting the accuracy calculations.

## References and Data Sources
- Google Earth Engine: Gorelick et al. 2017
- Land Cover Map 2018 (GB): Morton et al. 2020
- Additional data sources for training: LCM2018, CROME 2018, GWCT Allerton Project crop maps

## Notes for Monitoring Framework Authors
- Demonstrates a reproducible workflow combining GEE-based classification with post-processing in GIS tools.
- Uses publicly available reference datasets for training and validation, with explicit metadata on bands, dates, and processing steps.
- Produces a high-accuracy, fine-resolution land cover product suitable for informing ecosystem service assessments and policy monitoring.
- Highlights practical data governance considerations: data provenance, transformation steps, and quality assurance through accuracy assessment.