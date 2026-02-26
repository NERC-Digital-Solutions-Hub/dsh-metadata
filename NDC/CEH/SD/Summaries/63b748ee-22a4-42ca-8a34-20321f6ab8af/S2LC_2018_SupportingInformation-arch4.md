# S2LC_2018 Supporting Information

- Purpose: Document the study area, classification methodology, technical details, and accuracy information for S2LC_2018, a fine-resolution land cover map of the Upper Welland catchment (UK) for 2018, produced as part of a PhD project on Earth Observation and ecosystem services.

## Study Area
- Upper Welland Catchment (52.6°N, 0.6°W), about 340 km².
- Located in Leicestershire, Rutland and Northamptonshire, predominantly agricultural land use.

## Classification Methodology
- Approach: Random forest classification implemented in Google Earth Engine (GEE) with post-classification processing in QGIS v3.6.1.
- Data inputs:
  - Cloud-free Sentinel-2 multi-band mosaic created from eight images (May 1 – Sept 30, 2018) to maximise differentiation of agricultural land covers.
  - Eight Sentinel-2 bands used as inputs (with specified spatial resolutions): Blue (B2, 10 m), Green (B3, 10 m), Red (B4, 10 m), Vegetation Red Edge (B5, 20 m; B6, 20 m; B7, 20 m), NIR (B8, 10 m), SWIR (B12, 20 m).
  - Pixel values represent the 50th percentile across the eight images.
- Training data:
  - 1,581 training polygons across 10 land cover classes.
  - Reference datasets: LCM2018 (CEH), Crop map of England (CROME) 2018 (RPA), GWCT Allerton Project crop maps.
- Processing steps:
  - Random forest classification in GEE.
  - Post-classification: sieve filter to remove polygons < 20 pixels, manual correction with Thematic Raster Editor plugin for QGIS (ThRasE v. 20.3.23).
- Output:
  - Classified raster exported to QGIS for further processing.
  - Thematic resolution: 10 classes; Data type: Int32; File Type: GeoTiff.
- Documentation and reproducibility:
  - Tools and versions referenced (GEE, QGIS v3.6.1) to support reproducibility.
  - CRS: OSGB 1936 / British National Grid (EPSG:27700).
  - Dataset extent: specific geographic bounds provided; Pixel size: 10 m.
- Technical details:
  - Width: 4925 px, Height: 5788 px.
  - Pixel origin and extent values listed; raster dimensions and band count confirm a single-band classification.

## Land Cover Classes
- 1. Woodland: Broad-leaved and coniferous woodland, woody vegetation, or mature hedgerow/tree field boundaries.
- 2. Grassland: Grazing, amenity, or permanent grassland.
- 3. Water: Inland water bodies.
- 4. Built Environment: Urban/suburban areas, paved areas, roads.
- 5. Cereal Crops: Winter or spring sown wheat, barley, oats.
- 6. Oilseed Rape: Winter or spring sown oilseed rape.
- 7. Legumes: Field beans or spring peas.
- 8. Potato / Beet: Cropped areas of potato or sugar beet.
- 9. Bare Earth / Inland Rock: Fallow fields, bare soil, quarried areas.
- 10. Maize: Cropped areas of maize.

## Accuracy Assessment
- Validation: 700 randomly selected points across the map.
- Overall metrics:
  - Overall Accuracy: 92.1%
  - Kappa Coefficient: 0.91
- Class-level producer and user accuracies (examples):
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
- Note: Some classes show lower producer accuracy (e.g., Maize, Bare Earth) indicating potential confusion with other classes; overall accuracy remains high.
- Confusion matrix: Appendix 1 contains the detailed matrix used for calculations.

## Reference Data and Data Provenance
- Training polygons rely on three reference datasets:
  - LCM2018 (UK Centre for Ecology and Hydrology)
  - Crop map of England (CROME) 2018 (Rural Payments Agency)
  - GWCT Allerton Project crop maps
- Appendix data provide the class-by-class cross-tabulations used for accuracy calculations.

## Endnotes and Context
- The dataset supports ecosystem services modelling and land cover analysis within the Welland catchment.
- It demonstrates an integrated workflow from multi-temporal Sentinel-2 imagery to a 10-class land cover map with documented accuracy and metadata suitable for reuse and comparison with other UK land cover products.