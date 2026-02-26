# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- Release and explanation of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Objective: produce UK-wide land cover maps automatically using Bootstrap Training and Random Forest (RF) classifiers, enabling annual updates.
- No manual corrections were applied for these products to maintain rapid production; visual checks and formal validation were still conducted.
- Validation indicates maps are of similar quality to the prior LCM2015; accuracy around 78–80% across 21 classes.

## Key concepts and terminology
- Bootstrap Training: automatic sampling of historical land cover data (from prior maps) to generate spectral training observations for RF classification.
- Classification Scene: 46-band GB scene composed of Seasonal Composite Image bands plus 20m Context Raster bands used for classification.
- Seasonal Composite Image: median TOA reflectance per season from Sentinel-2, across four seasons.
- Context Rasters: 20m layers providing terrain, proximity, and other contextual cues to reduce spectral confusion.
- UKCEH Land Cover Classes vs. UK BAP Broad Habitats: 21 classes used, aligned for continuity with past maps; not a perfect one-to-one with BAP habitats but designed to support change detection.

## Data and production workflow
- Sentinel-2 data: Seasonally aggregated TOA reflectance; TOA chosen over SR based on comparable classification performance in this project.
- Geographic scope and tiling:
  - Great Britain: classification performed on overlapping 100x100 km GB tiles (74 Classification Scenes).
  - Northern Ireland: a single 43-band Classification Scene per year.
- UKCEH Land Parcel Spatial Framework: fixed parcel-based structure (MMU ~0.5 ha); parcels used to summarize 20m classified pixels into higher-level products.
- Bootstrap Training data source: primarily LCM2015 observations; future maps planned to bootstrap from majority signals across 2017–2019, then across 2018–2020 for subsequent updates.
- Software and tools: bespoke production pipeline integrating Weka (machine learning), PostGIS, and GDAL.

## Datasets and products
- 20m Classified Pixels: new addition; RF outputs assign each pixel a primary class with a second band indicating confidence (0–100). Preserves fine details below 0.5 ha MMU; not generalised by the parcel framework.
- Land Parcels: parcel-level attributes derived by intersecting 20m pixels with the UKCEH Land Parcel Spatial Framework.
  - Key fields: gid (parcel ID), _hist (histogram of class counts per parcel), _mode (dominant class), _purity (percentage of modal class), _conf (mean class membership probability), _stdev (std dev of confidence), _n (number of 20m pixels in parcel).
  - Note: gid identifiers differ from LCM2015; comparisons between years should use gid across 2017–2019.
- 25m Rasterised Land Parcels: three-band raster with band 1 = _mode, band 2 = _conf, band 3 = _purity.
- 1km Raster Datasets (derived by aggregating 25m parcels within 1km squares):
  - 1km Percent Cover: 21-band raster (percent cover per class per 1km).
  - 1km Percent Aggregate Cover: 10-band raster (percent cover per UKCEH Aggregate Class per 1km).
  - 1km Dominant Cover: 1-band raster (dominant class per 1km).
  - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km).

## Classification details and data extents
- Geographic coordinate systems:
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: Irish Grid (TM75, EPSG 29903).
- Class depth and structure:
  - 21 UKCEH Land Cover Classes based on UKBAP Broad Habitats (as defined in Appendix notes).
  - 8-bit rasters; 20m classified pixels preserve fine landscape features; 1km products generalise to broader patterns.
- Extents and granularity:
  - GB datasets are partitioned into tiles; NI uses a single classification for year.
  - Pixel sizes: 20m (classified pixels), 25m (land parcels rasters), 1km (percent/dominant products).

## Validation and accuracy
- Validation data sources: GB Countryside Survey 2019, open-source National Forest Inventory, IACS data, and bespoke LCM validation points (22,325 points total).
- Reported overall accuracy (producers’/users’ accuracy context varies by class):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Caveats:
  - Validation data were mapped to UKCEH classes, which required conversions; accuracy figures are indicative, not absolute truth.
  - Some classes (e.g., upland peatland, bracken separation) remain challenging; results reflect ongoing refinement.
  - Validation points derive from data sources with different purposes and class definitions.

## Future directions and usage considerations
- Annual update plan: aim to release a new LCM each year; continue to refine Bootstrap Training and classifier performance.
- Data access and metadata: emphasis on making datasets discoverable and usable, with clear provenance and class mappings.
- Potential enhancements:
  - Exploration of additional input sources (e.g., Sentinel-1 SAR) to fill spectral gaps or cloud-related gaps.
  - Possible refinements to the Land Parcel Spatial Framework to align with finer-resolution data.
  - Ongoing assessment of improvements in training data to boost accuracy and reduce confusions between similar classes.

## Practical implications for analysts
- The product suite provides multi-scale land cover representations (20m pixels, 25m parcels, and 1km summaries) suitable for change detection and landscape analyses.
- The Bootstrap Training approach enables rapid annual updates with minimal new field data, while maintaining UK-wide coverage.
- Data can be used for time-series analyses, regulatory and biodiversity assessments, and integration with other spatial datasets, with attention to gid-based year-to-year comparisons for parcel-level analyses.
- Users should be aware of potential class ambiguities in coastal, upland, and spectrally similar areas, and consider cross-walking or local calibration where high thematic detail is required.