# S2LC_2018 Supporting Information

- Purpose and scope: Describes the study area, classification methodology, technical details and accuracy for S2LC_2018, a fine-resolution land cover map of the Upper Welland Catchment (UK) for 2018. Produced as part of the PhD project on Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment, funded by CENTA.

## Study Area
- Upper Welland Catchment (~340 km²) located at 52.6°N, 0.6°W; spans Leicestershire, Rutland and Northamptonshire.
- Predominantly agricultural land use.

## Data and Imagery Used
- Sentinel-2 data used to create a cloud-free mosaic from eight images captured between 1 May 2018 and 30 September 2018.
- Eight input bands (Bands 2, 3, 4, 5, 6, 7, 8, 12) with varying spatial resolutions; per-pixel value is the 50th percentile across the mosaic.

## Training Data and Reference Sources
- 1,581 training polygons for 10 land-cover classes.
- Reference datasets:
  - LCM2018 (CEH)
  - Crop Map of England (CROME) 2018 (RPA)
  - Paper crop maps from Eye Brook and Stonton sub-catchments (GWCT Allerton Project)
- Training polygons uploaded to Google Earth Engine (GEE) for Random Forest classification.

## Classification Methodology and Processing Pipeline
- Random Forest classifier implemented in Google Earth Engine; post-classification processing in QGIS v3.6.1.
- Post-processing steps:
  - Apply sieve to remove polygons <20 pixels.
  - Manual correction of remaining errors using Thematic Raster Editor plugin ThRasE v. 20.3.23.
- Output raster exported to QGIS for final processing.

## Technical Details and Data Specifications
- Coordinate Reference System (CRS): EPSG:27700 (OSGB 1936 / British National Grid).
- Extent and dimensions: Projected extent with dimensions 4925 × 5788 pixels.
- Pixel size: 10 m.
- Data type: Int32 (32-bit signed integer).
- File type: GeoTIFF.
- Thematic resolution: 10 land-cover classes.

## Land Cover Classes (S2LC_2018)
1. Woodland — Broad-leaved and coniferous woodland, woody vegetation, or mature hedgerow/tree boundaries.
2. Grassland — Grazing, amenity, or permanent grassland.
3. Water — Inland water bodies.
4. Built Environment — Urban/suburban areas, paved areas, roads.
5. Cereal Crops — Winter/spring sown wheat, barley, oats.
6. Oilseed Rape — Winter/spring sown oilseed rape.
7. Legumes — Field beans or spring peas.
8. Potato/Beet — Cropped areas of potato or sugar beet.
9. Bare Earth / Inland Rock — Fallow fields, bare soil, quarried areas.
10. Maize — Cropped areas of maize.

## Accuracy Assessment
- Validation approach: 700 randomly selected points across the map.
- Metrics: Producer accuracy, User accuracy, Overall accuracy, and Kappa coefficient.
- Overall accuracy: 92.1%
- Kappa: 0.91
- Class-level results (selected highlights):
  - Water: Producer 100.0%, User 100.0%
  - Maize: Producer 80.8%, User 100.0%
  - Woodland: Producer 89.4%, User 93.3%
  - Grassland: Producer 95.5%, User 88.2%
  - Built Environment: Producer 85.0%, User 89.5%
  - Bare Earth/Rock: Producer 83.0%, User 97.5%
- Appendix 1 documents the confusion matrix underlying these results.

## Access, Reuse and References
- Processing relied on open tools and platforms:
  - Google Earth Engine (GEE)
  - QGIS v3.6.1
  - Thematic Raster Editor (ThRasE v. 20.3.23)
- Cited literature:
  - Gorelick et al. (2017) on Google Earth Engine
  - Morton et al. (2020) Land Cover Map 2018 dataset
- The dataset details and methodology are documented to support reproducibility and future reuse within similar land-cover mapping efforts.