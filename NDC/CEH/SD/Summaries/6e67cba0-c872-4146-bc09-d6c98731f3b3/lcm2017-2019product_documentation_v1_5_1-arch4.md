# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - Release of three national land cover maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a range of geospatial datasets, describing 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Production is automated (Bootstrap Training + Random Forest) to enable rapid, annual updates; no manual corrections were performed this cycle.
  - Visual checks and formal validation indicate maps are of comparable quality to the last major release (LCM2015).

- Data assets and structure
  - Datasets per year (GB and Northern Ireland): 42 datasets in total.
  - Core dataset families:
    - 20m Classified Pixels (GB and NI): per-pixel classification with an associated confidence band.
    - Land Parcels: attributes describing parcel-level composition and confidence metrics.
    - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity).
    - 1km raster products:
      - 1km Percent Cover (21-band)
      - 1km Percent Aggregate Cover (10-band)
      - 1km Dominant Cover (1-band)
      - 1km Dominant Aggregate Cover (1-band)
  - Spatial framework: UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha); gid is the stable parcel identifier across 2017–2019, but gid values do not match those from LCM2015.

- Production methodology
  - Bootstrap Training: uses historic LCM observations (primarily 2015) to automatically generate training data for new maps, enabling repeated production without new field data.
  - Random Forest classification: trained with balanced sampling (10,000 samples per class per Classification Scene) using a bespoke production tool (integrating WEKA, PostGIS, and GDAL).
  - Classification Scenes and tiling: GB uses overlapping 100x100 km tiles to generate 36-band Seasonal Composite Images (TOA Sentinel-2) plus 20m Context Rasters, forming 46-band Classification Scenes; NI uses a single 43-band scene.
  - Seasonality and data sources: Seasonal Composite Images built from Sentinel-2 bands across four seasons; Google Earth Engine used for data processing; TOA reflectance used (SR data not yet adopted due to marginal improvements in this context).

- Context and classification aids
  - Context Rasters (20m) used to reduce spectral confusion, including terrain (Height, Aspect, Slope), distance to buildings/roads/coast/freshwater, foreshore, tidal water, and woodland.
  - Seasonal information and 9 Sentinel-2 bands (plus additional bands) feed the classifier to differentiate vegetation types.

- Validation, accuracy, and interpretation
  - Validation dataset: GB countryside survey 2019 data, National Forest Inventory data, IACS data, and bespoke LCM validation points (n ≈ 22,325).
  - Reported overall accuracy (UK scale) for each year:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation cautions: same validation points used across all three products; accuracy figures reflect mapping alignment with UKCEH classes and conversions from other schemes;仍 not absolute truth.

- Data governance, metadata, and usability
  - Coordinate systems:
    - Great Britain: British National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid (TM75, EPSG: 29903)
  - Dataset attributes and nomenclature were updated to align with production software; some attribute names differ from LCM2015 (designed for consistency within the production workflow).
  - Parcel-level data attributes (Land Parcels) include: gid, hist, mode, purity, conf, stdev, n; 25m parcels carry mode, conf, purity.
  - Product descriptions emphasize the intended use: consistent cross-year comparison via the new Land Parcel Spatial Framework; direct parcel-id matching with previous products (LCM2015) is not possible.

- Practical implications for data leadership
  - A robust, annual, scalable pipeline now exists for national land cover mapping, enabling near-real-time monitoring of land cover change with a consistent 21-class schema.
  - The framework supports time-series analysis, change detection, and integration with parcel-based analyses using the fixed Land Parcel Spatial Framework.
  - The mix of 20m pixel data and 1km summary products offers both high-detail visualization and wide-area statistics suitable for policy, planning, and natural capital accounting.

- Limitations, caveats, and future direction
  - No manual corrections were applied; classification errors remain and are spatially variable.
  - Some spectral confusion persists among certain classes (e.g., upland vegetation, bracken vs. acid grassland; saltwater vs. freshwater in coastal zones).
  - Data gaps due to cloud cover: classification scenes tolerate incomplete spectral information; ongoing exploration of supplementary sources (e.g., Sentinel-1) to fill gaps.
  - GID stability across 2017–2019 supports year-to-year comparisons within the current framework; cross-walks to LCM2015 are limited.
  - Plans to release an LCM2020 in 2021 with expected bootstrap from 2017–2019 majority signals; potential enhancements include finer spatial frameworks and expanded data inputs.

- Access and references
  - The document provides detailed appendices on UKCEH Land Cover Classes, BAP Broad Habitats, colour schemes, and full validation results (Appendix 4 and Appendix 5 outline dataset lists and lineage).
  - Core references include Breiman (Random Forest), Carrasco et al. (Sentinel-1/2 comparisons), Jackson (BAP definitions), Morton et al. (LCM2007 methodology).