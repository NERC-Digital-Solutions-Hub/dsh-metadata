# S2LC_2018 Supporting Information

- Describes the study area, classification methodology, technical details and accuracy information for S2LC_2018, a fine-resolution land cover map of the Upper Welland catchment (UK) for 2018.
- Part of the PhD project Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment, supported by CENTA.

## Study Area
- Upper Welland Catchment location: 52.6°N, 0.6°W; about 340 km2.
- Spans the English counties of Leicestershire, Rutland and Northamptonshire.
- Land use is predominantly agricultural.

## Classification Methodology
- Classification approach: Random forest applied to Sentinel-2 imagery in Google Earth Engine (GEE).
- Image preparation: Cloud-free mosaic created from eight Sentinel-2 images captured 1 May 2018 to 30 September 2018; mosaic value per pixel is the 50th percentile across images.
- Inputs (eight bands): 
  - Band 2 (Blue, 10 m)
  - Band 3 (Green, 10 m)
  - Band 4 (Red, 10 m)
  - Band 5 (Vegetation Red Edge, 20 m)
  - Band 6 (Vegetation Red Edge, 20 m)
  - Band 7 (Vegetation Red Edge, 20 m)
  - Band 8 (NIR, 10 m)
  - Band 12 (SWIR, 20 m)
- Training data: 1,581 polygons for 10 land cover classes, created in QGIS.
  - Reference datasets: LCM2018 (UK CEH), Crop Map of England (CROME) 2018 (RPA), GWCT Allerton Project crop maps.
- Processing workflow: Training polygons uploaded to GEE for random forest classification; output raster exported to QGIS 3.6.1 for post-processing.
- Post-classification processing: 
  - Sieve operation to remove polygons < 20 pixels.
  - Manual correction of remaining errors using Thematic Raster Editor plugin for QGIS (ThRasE v. 20.3.23).

## Technical Details
- Coordinate Reference System (CRS): EPSG:27700 – OSGB 1936 / British National Grid.
- Extent: S2LC_2018 geographic extent with coordinates provided; unit = meters.
- Thematic resolution: 10 land cover classes.
- Data type: Int32 (32-bit signed integer).
- File type: GeoTIFF.
- Dimensions: 4925 (width) x 5788 (height); Pixel size = 10 m.
- Origin and pixel-size specifics: documented in the technical details.

## Land Cover Classes
- 1. Woodland: Broad-leaved and coniferous woodland, woody vegetation, or mature hedgerow / tree field boundaries.
- 2. Grassland: Grazing, amenity, or permanent grassland.
- 3. Water: Inland water bodies.
- 4. Built Environment: Urban or suburban areas, paved areas, roads.
- 5. Cereal Crops: Winter or spring sown wheat, barley, oats.
- 6. Oilseed Rape: Winter or spring sown oilseed rape.
- 7. Legumes: Field beans or spring peas.
- 8. Potato / Beet: Cropped areas of potato or sugar beet.
- 9. Bare Earth / Inland Rock: Fallow fields, bare soil, quarried areas.
- 10. Maize: Cropped areas of maize.

## Accuracy Assessment
- Validation: 700 randomly selected points across the map.
- Metrics per class include producer accuracy and user accuracy; overall metrics:
  - Overall accuracy: 92.1%
  - Kappa coefficient: 0.91
- Notable per-class accuracies (sample):
  - Water: Producer 100.0%, User 100.0%
  - Maize: Producer 80.8%, User 100.0%
  - Bare Earth / Inland Rock: Producer 83.0%, User 97.5%
  - Woodland: Producer 89.4%, User 93.3%
  - Grassland: Producer 95.5%, User 88.2%
  - Urban/Suburban: Producer 85.0%, User 89.5%
  - Cereal Crops: Producer 94.9%, User 92.9%
  - Oilseed Rape: Producer 96.9%, User 91.3%
  - Legumes: Producer 84.2%, User 94.1%
  - Potato / Beet: Producer 92.9%, User 89.7%
- Appendix 1 contains the full confusion matrix underpinning these results.

## References and Appendix
- Key references:
  - Gorelick, N. et al. (2017). Google Earth Engine: Planetary-scale geospatial analysis for everyone. Remote Sensing of Environment.
  - Morton, R.D. et al. (2020). Land Cover Map 2018 (20 m classified pixels, GB). NERC EIDC.
- Data sources for training and validation: LCM2018, CROME 2018, GWCT Allerton Project crop maps.
- The document includes additional appendix with the full confusion matrix and dataset details.