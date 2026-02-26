# The UKCEH Land Cover Map for 2020

## Purpose and Scope
- User guide for the UKCEH Land Cover Map 2020 (LCM2020), the eighth UK land cover map.
- LCM2020 comprises six geospatial datasets (three for Great Britain and Northern Ireland): 10m Classified Pixels, Land Parcel Dataset, and 25m Rasterised Land Parcels (GB); plus 10m Classified Pixels, Land Parcel Dataset, 20m Classified Raster Product (NI), and 25m Rasterised Land Parcels (NI).
- Outputs include 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats), derived from Sentinel-2 Seasonal Composite Images plus 10 Context Layers.
- Emphasises data production method, validation, and data accuracy to help users make informed decisions.
- Annual production introduced; methods continually improved; minimal manual correction to maintain consistency and enable change detection.

## Data Holdings and Structure
- Six datasets in total:
  - Great Britain: 10m Classified Pixels, Land Parcel Product, 25m Rasterised Land Parcel Product.
  - Northern Ireland: 10m Classified Pixels, Land Parcel Product, 20m Classified Raster Product, plus 25m Rasterised Land Parcel Product.
- Coordinate reference:
  - GB: EPSG: 27700 (British National Grid).
  - NI: EPSG: 29903 (Irish Grid).
- Spatial framework and units:
  - UKCEH Land Parcel Spatial Framework used to generalise land parcels; parcels have a minimum area of ~0.5 ha (Minimum Mappable Unit, MMU).
  - 10m Classified Pixels are not generalised by the Land Parcel framework to preserve small features; intended for specialist users.
- Band structure:
  - 10m Classified Pixels: 2 bands (class ID, confidence/probability).
  - 25m Rasterised Land Parcels: 3 bands per parcel (dominant class _mode, confidence _conf, and purity _purity).
  - 20m Classified Raster Product (NI): details not specified in the summary, but presented as a raster classification product.
  - Land Parcel Dataset: contains per-parcel attributes (e.g., _hist, _mode, _purity, _conf, _stdev, _agg, _n) and parcel identifiers (gid).

## Data Production Methods
- Sentinel-2 Seasonal Composite Images:
  - Seasons: winter, spring, summer, autumn; 9 Sentinel-2 bands used (spectral), resampled to target resolution.
  - Seasonal composites combined with Context Rasters to create Classification Scenes.
- Context Rasters:
  - 10m GB context rasters include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, and wooden/vegetation masks.
  - 7 context rasters for Northern Ireland (including urban mask and distance to coast/freshwater/roads).
- Classification Scenes:
  - GB uses 100x100 km tiles to select 36-band Seasonal Composite Images; results in 46-band GB Classification Scenes.
  - NI uses a single 36-band Seasonal Composite Image with 7 NI context rasters, forming a 43-band NI Classification Scene.
- Bootstrap Training:
  - Fully automatic training using historical LCMs (2017–2019) filtered to >99% purity across three years.
  - Training sets: GB ~941,027 objects; NI ~214,833 objects.
  - Bootstrap Training samples recent observations to train classifiers for the new map.
- Random Forest Classification:
  - Supervised learning; balanced training by sampling 10,000 pixels per class with replacement.
  - Produces the 10m Classified Pixels product; RF learning relies on majority signal from large training sets.
  - Classification software is bespoke, integrating Weka with PostGIS and GDAL (open source tools).

## Validation and Accuracy
- Product validation:
  - Compared against GB countryside survey data (2019–2020), open-source National Forest Inventory data, IACS data, and bespoke validation points.
  - Total validation points: 34,715.
  - Overall accuracy: 79.2% (full thematic detail) as reported in Appendix 4.
- Validation detail:
  - Confusion matrices and class-wise producer’s and user’s accuracies provided in Appendix 4.
  - Validation performed against Land Parcel datasets rather than the 10m pixel dataset (noting differences in validation basis).

## The UKCEH Land Parcel Spatial Framework
- Based on LCM2007 development, with minor updates since LCM2015.
- Changes include re-ordered storage and new indices for faster processing; gid identifiers may not match LCM2015 when comparing time series.
- MMU of ~0.5 ha; land parcels generalised from national cartography to represent discrete real-world units (fields, parks, woodlands, etc.).
- Parcel-based organization reduces classification noise and supports change detection over time.

## Relationship to BAP Broad Habitats
- 21 UKCEH Land Cover Classes relate to UK Biodiversity Action Plan (BAP) Broad Habitats but are not exact equivalents.
- BAP Broad Habitats are italicised when referred to; UKCEH Land Cover Classes are capitalised when defined.
- Appendix 1 and Appendices 2 provide mapping notes and nuances, including cases where a single BAP habitat maps to multiple UKCEH classes (e.g., Freshwater, Saltwater distinctions).

## Data Access, Display, and Use
- The 10m Classified Pixels preserve fine landscape features (not generalised), suitable for specialists who understand the implications for accuracy and MMU.
- The dataset validation is performed against Land Parcel data; users should interpret pixel-level accuracy with this context in mind.
- The document includes recommended color mappings for display (Appendix 3) and detailed correspondence matrices (Appendix 4) for class relationships.

## Governance, Updates, and Limitations
- Annual production aims to maximize temporal consistency and support change detection; improvements to methods may lead to re-application across the entire catalogue.
- Manual corrections are not performed to maintain automation; errors are treated as random and used to inform future method development.
- If new methods yield significant accuracy improvements, there is consideration to re-apply across the catalogue to maximize comparability.
- The document notes current limitations, including challenges in harmonizing across different systems/formats and the continued need for better upland vegetation mapping and peatland characterization.

## Appendix and Datasets (Appendix 5)
- Full list of datasets for UKCEH LCM2020:
  - GB: 10m Classified Pixels; Land Parcel Product; 25m Rasterised Land Parcel Product.
  - NI: 10m Classified Pixels; Land Parcel Product; 20m Classified Raster Product; 25m Rasterised Land Parcel Product.
- Datasets are documented with names, extents, coordinate systems, and product descriptions to support data governance and metadata requirements.

## References
- Key methodological references for Random Forests, bootstrap training, Sentinel-2 processing, and historical LCM studies cited to support reproducibility and governance.