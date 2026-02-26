# The UKCEH Land Cover Map for 2022

- LCM2022 is the tenth UK land cover map produced by UKCEH, created from automatic classification of Sentinel-2 Seasonal Composite Images plus Context Rasters using Bootstrap Training and a Random Forest classifier.
- Purpose: to describe data production, validation, and accuracy to help users apply LCM data for current and future work, and to support monitoring of land cover state and change.

## Product suite and datasets

- Three geospatial datasets for each of Great Britain and Northern Ireland:
  - 10 m Classified Pixel dataset (classified pixels with a dominant land cover class and a confidence probability)
  - Land Parcel dataset (attributes derived from intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework)
  - 25 m Rasterised Land Parcel dataset (per-parcel raster of dominant class, confidence, and purity)
- A 1 km Summary Raster product for GB and NI (dominant class, aggregate, and percentage cover summaries)
- Appendix 3 lists official dataset names and DOIs for each product

## Land cover classes and framework

- LCM2022 defines 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats (with some nuanced mappings and notes in Appendices 1–2)
- Classes are used consistently across GB and NI products, with explicit classification considerations described in the guide

## Data production and methods

- Seasonal Composite Images: derived from Google Earth Engine; Sentinel-2 surface reflectance resampled to 10 m; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec)
- Context Rasters (10 m for GB; 9–10 rasters for GB; 9 rasters for NI): include terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, water, foreshore, woodland, etc.)
- Classification Scenes:
  - GB: a grid of 32 tiles (approx. 100 x 100 km each) to train and classify independently
  - NI: a single Classification Scene covering the region
  - NI uses a 49-band scene (40-band Sentinel-2 seasonal plus NI context rasters)
- Bootstrap Training: automatic, uses historic LCM observations (LCM2019–LCM2021) with >80% probability and consistent class across years to train the classifier, reducing reliance on new field data
- Random Forest classifier: 10,000 samples per bag, balanced across classes to avoid dominance by common classes
- Software: bespoke UKCEH pipeline integrating WEKA, PostGIS, and GDAL (all open source)

## Validation and accuracy

- Validation dataset: 33,107 points across all 21 classes, compiled from GB countryside survey data, National Forest Inventory, Rural Payments data, and targeted validation points
- Reported overall accuracy: 86.1% (with producer’s and user’s accuracy detail provided in Appendix 4)
- Validation is performed against the 25 m Rasterised Land Parcel product; 10 m Classified Pixels are not included in formal validation

## Data structure and attributes

- 10 m Classified Pixels: two-band output per pixel
  - Band 1: dominant UKCEH Land Cover Class
  - Band 2: class membership probability/confidence
- 25 m Rasterised Land Parcels: three-band raster (dominant class, conf, purity) at 25 m resolution
- Land Parcel dataset attributes include per-parcel statistics (_hist, _mode, _conf, _stdev, _agg, _n, ogc_fid) to support change detection and analysis
- 1 km summary rasters: dominant class, percentage cover across 21 classes (and 10 aggregate classes), with rounding leading to minor sums away from 100% in some cases

## Spatial framework and coordinates

- GB: British National Grid (EPSG: 27700)
- NI: Irish Grid (TM75, EPSG: 29903)
- Land Parcel Spatial Framework designed to represent discrete units (approx. 0.5 ha MMU) for stable, comparable units over time

## Known issues and caveats

- A small number of polygons are missing from vector land parcel products, causing nodata areas in the 25 m rasterised parcels; impact on 1 km products is negligible
- 10 m Classified Pixels are not part of the official validation against the 25 m parcel dataset
- Methodology changes year-to-year may introduce differences beyond real land cover change; annual production improves temporal consistency and change detection but requires careful interpretation when comparing across years

## Data access, citations, and governance

- Each LCM2022 dataset has a DOI and should be cited accordingly (DOIs provided in Table 5)
- The guide references Marston et al. (2023/2024) for overview and prior methods
- Data products are hosted and documented for reuse, with explicit guidance on how to attribute data and when to use each product (10 m pixels, 25 m parcels, 1 km summaries)

## Practical implications for monitoring frameworks

- Annual production and robust validation enable distinguishing real change from random classification error, supporting timely policy monitoring
- A hierarchical data structure (pixels, parcels, and summaries) supports multiple scales of analysis and integration with other monitoring datasets
- Bootstrap Training enables near-wall-to-wall training data, reducing field data needs while maintaining broad geographic coverage
- User-guidance on data interpretation, confidence bands, and class confusion (especially among habitat types) aids transparent reporting and decision-making
- Data governance: explicit metadata, DOIs, and clear usage notes facilitate traceability, reproducibility, and governance of monitoring outputs

## Visualisation and supplementary resources

- Appendix 5 and Appendix 6 provide recommended colour schemes (including color-blind friendly options) and accompanying QGIS symbol files for effective visualization
- Documentation includes comprehensive glossaries and relationships between UKCEH Land Cover Classes and UK BAP Broad Habitats to aid interpretation