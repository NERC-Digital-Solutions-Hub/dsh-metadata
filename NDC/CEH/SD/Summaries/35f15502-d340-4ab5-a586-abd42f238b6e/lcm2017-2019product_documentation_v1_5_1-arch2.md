# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Aim and Scope
- Presents three UKCEH land cover maps (LCM2017, LCM2018, LCM2019) and their accompanying user guide.
- Produces 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with a structure that supports land cover change detection over time.
- Uses automated production (Bootstrap Training with Random Forest) to enable annual map release; includes validation and guidance for informed application.

## Data Production and Validation

- Bootstrap Training
  - Uses historic UKCEH LCM2015 data (from 1990–2007) to generate spectral training observations for the current classification.
  - Selection criterion: parcels with ≥99% purity from LCM2015 to bootstrap training; supports automatic learning for new maps.
  - Sampling: for each year, 10,000 samples per class to balance learning.

- Random Forest Classification
  - Custom UKCEH pipeline integrating Weka, PostGIS, and GDAL.
  - Produces the 20m Classified Pixels product; classification scene outputs used to create all other products.
  - No manual corrections (auto-classification only) to enable annual timesteps; visual checks and formal validation still performed.

- Seasonal Composite Images and Context
  - Sentinel-2 seasonal composites (winter, spring, summer, autumn) generated in Google Earth Engine using TOA reflectance; 20m resolution.
  - Context Rasters (20m) provide terrain, urban proximity, roads, coast, water, etc., to reduce spectral confusion.

- Classification Scenes and Parcel Framework
  - Great Britain: 100x100 km overlapping tiles yield 36-band Seasonal Composite Images plus 10 context layers; 46-band Classification Scenes classified independently and overlapped for quality, with visual precedence to select best results.
  - Northern Ireland: single 43-band Scene per year determined by the island’s extent.
  - UK Land Parcel Spatial Framework: maintains 0.5 ha MMU minimum; parcels are 21-class units (same framework as LCM2015 but with processing changes); unique parcel identifiers (gid) do not match LCM2015 for parcel data, though gid can be used for year-to-year comparisons.

- Datasets and Products
  - 20m Classified Pixels: new 2-band 8-bit rasters; band 1 = most likely class, band 2 = per-pixel confidence (0–100).
  - Land Parcels: attributes derived by intersecting 20m Classified Pixels with the Land Parcel Framework; includes hist, mode, purity, conf, stdev, n.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) summarising parcel data at 25m resolution.
  - 1km Raster Products: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).

- Dataset Extents and Formats
  - GB and NI bilingual versions; coordinates set to GB National Grid (EPSG:27700) and NI Irish Grid (EPSG:29903).
  - 42 datasets in total (three years × multiple products) across GB and NI.

- Validation and Accuracy
  - Validation against GB countryside survey (2019), National Forest Inventory, IACS, plus bespoke LCM validation points (22,325 total).
  - Overall accuracy: 2017 ≈ 78.6%, 2018 ≈ 79.6%, 2019 ≈ 79.4%.
  - Validation data are not perfect truth; differences in class definitions and currency considerations acknowledged.
  - Appendix 4 provides full validation tables and confusion matrices.

## Data Content and Class Mapping

- UKCEH Land Cover Classes
  - Maps 21 UKCEH Land Cover Classes (aligned with LCM2015 and earlier mappings) derived from UK BAP Broad Habitats; classes include Arable, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Heather/Hither, Fen/Marsh/Swamp, Bog, Inland Rock, Saltwater, Freshwater, Supralittoral/Littoral categories, Urban, Suburban, Saltmarsh, and others.
  - BAP Broad Habitats are provided to aid interpretation but are not interchangeable with UKCEH classes; terminology capitalized for defined classes and italicized for BAP references where appropriate.

- Relationship and Generalization
  - UKCEH Land Cover Classes (21) map closely to BAP Broad Habitats but are defined for satellite detection and national monitoring; UKCEH Aggregate Classes (10) offer generalized representations when detailed thematic mapping is unnecessary.

- Visualisation and Colour
  - Appendix 3 provides RGB colour recipes for displaying each UKCEH Land Cover Class.

## Temporal and Spatial Details

- Time Series and Change Detection
  - Annual production aims to enable near-future change detection and policy evaluation across decades.
  - Bootstrap Training uses majority signals across recent years to sustain classifier performance across 2017–2019 and planned future years.

- Spatial Framework and MMU
  - Land Parcels retain a ~0.5 ha MMU; summaries at 20m (pixels) and 25m (parcels) scale allow flexible analysis from fine detail to coarse regional patterns.
  - The framework supports comparing across years, though parcel identifiers may not match exactly between LCM2015 and the 2017–2019 products.

## Practical Considerations for Analysts

- Outputs suitable for monitoring and policy evaluation
  - Multi-resolution products enable scalable monitoring: 20m pixel detail, parcel-based summaries, and 1km grids for broad trend analysis.
  - Clear documentation of production methods, validation results, and class mappings support reproducibility and auditability.

- Data Access and Use
  - The release includes a full dataset catalog (Appendix 5) and detailed metadata for cross-year comparison; users should reference gid for year-to-year parcel comparisons, noting potential identifier changes.

- Limitations and Future Directions
  - No manual corrections were performed this release; classification errors are expected but are intended to be randomly distributed over time to reveal true land cover changes.
  - Some spectral confusion remains (e.g., Saltwater vs Freshwater; upland peatland vegetation complexities); future work may incorporate additional data sources (e.g., Sentinel-1, other optical or SAR inputs) and refined training data to improve separation of challenging classes.
  - Expect annual LCM updates; 2020 and beyond plan to leverage broader Bootstrap Training signals to further improve accuracy and change-detection capability.

## Appendices and Supporting Material

- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats.
- Appendix 3: Recommended RGB colour recipe for display of each class.
- Appendix 4: Full validation results (confusion matrices, producer’s and user’s accuracies) for LCM2017, LCM2018, and LCM2019.
- Appendix 5: Full list of datasets included for LCM2017, LCM2018, and LCM2019 (dataset names, extents, and formats).