# The UKCEH Land Cover Map for 2020

- A user guide for LCM2020, the eighth UKCEH land cover map, produced annually using automated methods. It covers six datasets across Great Britain (GB) and Northern Ireland (NI), enabling annual monitoring of land cover change.
- Core aim: support informed decision-making in environmental policy and monitoring frameworks by providing transparent data production, validation, and data quality information.

## What LCM2020 includes

- Six datasets in total (GB and NI):
  - GB: 10m Classified Pixel dataset; Land Parcel dataset; 25m Rasterised Land Parcel dataset.
  - NI: 10m Classified Pixel dataset; Land Parcel dataset; 25m Rasterised Land Parcel dataset.
  - Note: Appendix 5 lists the six official dataset names and extents; GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (EPSG: 29903).
- Three main data products per region, with a total of six datasets across GB and NI:
  - 10m classified pixels (Classification Scenes output)
  - Land Parcel datasets (attributes intersected with 10m pixels)
  - 25m rasterised land parcels (per-parcel raster product)

## Land Cover classes and relationships

- Enables 21 UKCEH Land Cover Classes, aligned historically with Biodiversity Action Plan (BAP) Broad Habitats definitions (not a one-to-one mapping; some nuance retained for comparability with earlier maps).
- Classes can be linked to broad habitat types (e.g., Broadleaved woodland, Coniferous woodland, Arable, Improved Grassland, etc.) with notes on where spectral distinguishability is challenging.
- UKCEH Land Cover Classes are generally mapped against BAP Broad Habitats, with some regions requiring more generalized UKCEH Aggregate Classes in Land Parcel products.

## How the data are produced

- Sentinel-2 Seasonal Composite Images plus Context Rasters:
  - Seasonal Composite Images represent spectral information across winter, spring, summer, and autumn.
  - 10 Context Rasters (GB) resolve spectral confusions (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, woodland). NI uses an urban mask and distance to coast/freshwater/roads.
  - Bands from Sentinel-2 and context rasters are combined into Classification Scenes.
- Classification Scenes:
  - GB: 74 overlapping 100x100 km tiles; NI: a single 36-band scene per year for NI.
  - Each Classification Scene is trained and classified independently; overlaps are resolved by visual precedence in final cut.
  - 46-band GB Scenes; 43-band NI Scene per year.
- Bootstrap Training:
  - Fully automatic training using historic LCMs (2017–2019) to avoid new field data collection.
  - Training data filtered to high-purity parcels (>99% across 2017–2019); GB training objects ≈ 941k; NI ≈ 214k.
- Random Forest classification:
  - Pixels sampled in labeled bags; 10,000 samples per class with replacement to balance training.
  - Implemented with a bespoke pipeline that combines Weka, PostGIS, and GDAL; designed to maximize accuracy and reproducibility.
- Validation approach:
  - Validated against GB countryside survey data (2019, 2020), open data sources (National Forest Inventory, IACS), and bespoke validation points (n ≈ 34,715).
  - Overall accuracy reported at 79.2% (Appendix 4), with detailed producer’s and user’s accuracy across classes.

## Data specifics and formats

- Pixel and parcel datasets:
  - 10m Classified Pixel dataset: two-band raster; band 1 = most likely UKCEH Land Cover Class; band 2 = class membership probability (confidence). No generalisation with Land Parcel Spatial Framework to preserve detailed features.
  - 25m Rasterised Land Parcel dataset: three-band raster per parcel; band 1 = dominant class (_mode); band 2 = mean class confidence (_conf); band 3 = parcel purity (_purity).
  - 8-bit raster products; extents defined separately for GB and NI.
- Land Parcel Spatial Framework:
  - Derived from pre-2015 generalised cartography; parcels have a minimum area of ~0.5 ha (MMU).
  - GID identifiers differ from LCM2015; spatial overlap comparisons are not straightforward year-on-year.
- Seasonal and contextual data:
  - Seasonal Composite Images derived from Google Earth Engine (Sentinel-2 surface reflectance; bands listed in Table 4).
  - Context rasters and seasonal data designed to mitigate spectral confusion and support robust classification.

## Validation and accuracy considerations

- Validation methodology:
  - 34,715 validation points cross-referenced with Land Parcel datasets to determine correspondence.
  - Overall accuracy: 79.2% (Appendix 4).
- Validation nuances:
  - Validation is anchored to parcel-level mappings rather than directly to the 10m Classified Pixel dataset.
  - Appendix 4 provides detailed confusion matrices, producer’s accuracy, and user’s accuracy by class, illustrating where misclassifications occur and the relative reliability of each class.

## Data use, governance, and data sharing

- The guide emphasizes transparency and openness:
  - Data are intended for public dissemination; metadata and underlying data are shared where appropriate.
  - Acknowledges challenges in metadata completeness and the need to verify data provenance, especially when reusing older datasets.
- Governance and stewardship:
  - Clear documentation of data sources, methods, and validation supports reproducibility and governance for monitoring frameworks.
  - Annual production aims to differentiate random classification errors from real land-cover change, aiding change detection and trend monitoring.

## Relationship to monitoring and policy objectives

- The annual LCM2020 series supports:
  - Monitoring state and change of the UK countryside to inform environmental objectives.
  - Change detection and time-series analysis through consistent, repeatable mapping.
  - Stakeholder engagement through transparent methodology, data origins, and validation results.
- The use of Bootstrap Training and automated methods reduces reliance on costly field data while maintaining robust classification performance for policy-relevant monitoring.

## Limitations and caveats to consider

- Spectral confusion and edge cases:
  - Some classes (e.g., certain grassland types, bracken, upland peatland vegetation) exhibit spectral similarities that can cause misclassification.
  - Saltwater vs. Freshwater distinctions near coasts and tidal rivers can be problematic; coastal context layers help but are not perfect.
  - Upland habitats and peatland vegetation pose challenges due to small patch sizes and spectral ambiguity; ongoing work aims to improve this in future LCMs.
- Granularity and scale:
  - 10m pixels preserve detailed landscape features but are not generalised to the Land Parcel Framework; users should be aware of this when aggregating or comparing with parcel-based products.
- Historical identifiers:
  - Parcel identifiers (gids) differ from earlier datasets, limiting direct parcel-based year-to-year comparisons without spatial overlap analysis.

## Appendix highlights (for reference)

- Appendix 1 and 2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats; guidance on class definitions and potential field-sensing ambiguities.
- Appendix 4: Comprehensive validation matrices, including user’s and producer’s accuracy by class.
- Appendix 5: Full list of LCM2020 datasets and official metadata identifiers.

- Overall takeaway for monitoring framework authors:
  - LCM2020 provides a transparent, repeatable, scientifically validated land cover product with clearly documented methods, data provenance, and accuracy metrics.
  - The combination of 10m classified pixels, land parcel attributes, and 25m rasterised parcels, along with robust contextual and seasonal data, supports fine-grained monitoring and change detection while acknowledging limitations in certain habitat categories.
  - The Bootstrap Training and fully automated workflow facilitate annual updates, improving temporal consistency and enabling timely policy-relevant insights.