# S2LC_2018 Supporting Information

- Study Area
  - Upper Welland Catchment, 340 km², located at 52.6°N, 0.6°W; spans Leicestershire, Rutland, and Northamptonshire in England.
  - Predominantly agricultural land use.

- Classification Methodology
  - Produced a fine-resolution land cover map (S2LC_2018) using a random forest classifier in Google Earth Engine (GEE).
  - Data inputs:
    - Cloud-free Sentinel-2 mosaic created from eight images captured between 1 May 2018 and 30 September 2018.
    - Per-pixel value representation as the 50th percentile across the eight images.
    - Eight input bands: Blue (B2, 10 m), Green (B3, 10 m), Red (B4, 10 m), Vegetation Red Edge (B5, 20 m; B6, 20 m; B7, 20 m), NIR (B8, 10 m), SWIR (B12, 20 m).
  - Training data:
    - 1,581 training polygons across 10 land cover classes.
    - Reference datasets: LCM2018 (UK Centre for Ecology and Hydrology), Crop Map of England (CROME, 2018), GWCT Allerton Project crop maps.
  - Processing workflow:
    - Training polygons uploaded to GEE for RF classification.
    - Post-classification processing in QGIS v3.6.1.
    - Sieve filtering to remove polygons < 20 pixels, followed by manual correction with Thematic Raster Editor (ThRasE v20.3.23).

- Technical Details
  - Coordinate Reference System: OSGB 1936 / British National Grid (EPSG:27700).
  - Extent and output: S2LC_2018 extent ~ [462,783.34, 282,044.35] to [512,032.90, 339,924.35]; pixel size 10 m; GeoTIFF format; 4,925 × 5,788 pixels.
  - Data type: 32-bit signed integer (Int32).
  - Thematic resolution: 10 land cover classes.

- Land Cover Classes
  - 1) Woodland: Broad-leaved and coniferous woodland, woody vegetation, or mature hedgerow/tree boundaries.
  - 2) Grassland: Grazing, amenity, or permanent grassland.
  - 3) Water: Inland water bodies.
  - 4) Built Environment: Urban/suburban areas, paved areas, roads.
  - 5) Cereal Crops: Winter/spring sown wheat, barley, oats.
  - 6) Oilseed Rape: Winter/spring sown oilseed rape.
  - 7) Legumes: Field beans or spring peas.
  - 8) Potato / Beet: Cropped areas of potato or sugar beet.
  - 9) Bare Earth / Inland Rock: Fallow fields, bare soil, quarry areas.
  - 10) Maize: Cropped areas of maize.

- Accuracy Assessment
  - Validation: 700 randomly selected points across the map.
  - Reported metrics (per class) include producer accuracy and user accuracy; overall accuracy 92.1% and Kappa 0.91.
  - Appendix 1 provides the confusion matrix underpinning these accuracy calculations.
  - Overall results indicate strong performance across most classes (e.g., Water 100% producer and user; Maize producer 80.8%, user 100%).

- Outputs and Purpose
  - S2LC_2018 serves as a high-resolution baseline for monitoring land cover change and assessing ecosystem services within the Upper Welland Catchment.
  - Aligns with the broader PhD project focused on Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment.

- Data, Sources, and Project Context
  - Part of the PhD project “Earth Observation and Modelling of Ecosystem Services in the Welland River Catchment,” supported by CENTA (Grant NE/L002493/1).
  - Related literature: Google Earth Engine (Gorelick et al., 2017); Land Cover Map 2018 (Morton et al., 2020).
  - Reference and training data summaries, including class totals, are provided in Appendix 1 of the document.