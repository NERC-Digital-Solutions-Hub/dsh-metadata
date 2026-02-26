# S2LC_2018 Supporting Information

- A fine-resolution land cover map of the Upper Welland catchment (UK) for 2018, produced as part of a PhD project on Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment.
- Output: S2LC_2018 raster with 10 land cover classes at 10 m resolution, plus methodology and accuracy details.

## Study Area
- Upper Welland Catchment: 340 km², centered at roughly 52.6°N, 0.6°W.
- Location spans parts of Leicestershire, Rutland and Northamptonshire; predominantly agricultural land use.

## Classification Methodology and Data Sources
- Approach: Random forest classification implemented in Google Earth Engine (GEE), with post-classification processing in QGIS 3.6.1.
- Input data: Cloud-free Sentinel-2 mosaic created from eight images (May 1 – Sept 30, 2018); per-pixel value = 50th percentile across the eight images.
- Sentinel-2 bands used (input features):
  - Band 2 Blue (0.490 μm, 10 m)
  - Band 3 Green (0.560 μm, 10 m)
  - Band 4 Red (0.665 μm, 10 m)
  - Band 5 Vegetation Red Edge (0.705 μm, 20 m)
  - Band 6 Vegetation Red Edge (0.740 μm, 20 m)
  - Band 7 Vegetation Red Edge (0.783 μm, 20 m)
  - Band 8 NIR (0.842 μm, 10 m)
  - Band 12 SWIR (2.190 μm, 20 m)
- Training data:
  - 1,581 polygons across 10 land cover classes.
  - Reference datasets: LCM2018 (UKCEH), Crop map of England (CROME) 2018, GWCT Allerton Project crop maps (Eye Brook and Stonton sub-catchments).
- Processing steps:
  - Train random forest classifier in GEE.
  - Post-classification processing in QGIS: sieve to remove polygons <20 px, manual correction with Thematic Raster Editor (ThRasE v. 20.3.23).

## Output and Technical Details
- Output format: GeoTIFF (S2LC_2018) with 10-class thematic resolution.
- Coordinate Reference System: OSGB 1936 / British National Grid (EPSG:27700).
- Map extent and size: 4925 × 5788 pixels; pixel size 10 m.
- Extent coordinates (approx): X 462,783 to 512,033; Y 282,044 to 339,924.
- Data type: 32-bit signed integer (Int32).
- Class definitions (10 classes):
  1) Woodland — Broad-leaved and coniferous woodland, hedgerows/tree boundaries
  2) Grassland — Grazing/amenity/permanent grassland
  3) Water — Inland water bodies
  4) Built Environment — Urban/suburban areas, paved areas, roads
  5) Cereal Crops — Winter/spring sown wheat, barley, oats
  6) Oilseed Rape — Winter/spring sown oilseed rape
  7) Legumes — Field beans or spring peas
  8) Potato / Beet — Cropped areas of potato or sugar beet
  9) Bare Earth / Inland Rock — Fallow, bare soil, quarries
  10) Maize — Cropped areas of maize

## Accuracy Assessment
- Validation: 700 randomly selected points across the map.
- Overall accuracy: 92.1%
- Kappa coefficient: 0.91
- Class-level performance (producer and user accuracies, where available):
  - Woodland: Producer 89.4%, User 93.3%
  - Grassland: Producer 95.5%, User 88.2%
  - Water: Producer 100.0%, User 100.0%
  - Built Environment: Producer 85.0%, User 89.5%
  - Cereal Crops: Producer 94.9%, User 92.9%
  - Oilseed Rape: Producer 96.9%, User 91.3%
  - Legumes: Producer 84.2%, User 94.1%
  - Potato/Beet: Producer 92.9%, User 89.7%
  - Bare Earth / Inland Rock: Producer 83.0%, User 97.5%
  - Maize: Producer 80.8%, User 100.0%

## Reproducibility and References
- Methodology aligns with established remote sensing workflows: Google Earth Engine for classification (Gorelick et al., 2017) and QGIS for post-processing.
- Related data sources and accuracy framework referenced (Morton et al., 2020; Gorelick et al., 2017).