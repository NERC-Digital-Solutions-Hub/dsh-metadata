# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview and Purpose
- Release accompanying three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Map 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) using automated methods to enable rapid, annual updates.
- Classification based on Bootstrap Training plus Random Forest; no manual corrections this cycle to maintain speed and consistency with annual updates.
- Validation indicates UK-scale accuracy around 78–80% across the three products, with ongoing plans to improve methods and validation resources.

## Data Products and Structure
- Dataset suite for each year includes:
  - 20m Classified Pixels (GB and NI versions)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Percent Cover (GB and NI)
  - 1km Percent Aggregate Cover (GB and NI)
  - 1km Dominant Cover (GB and NI)
  - 1km Dominant Aggregate Cover (GB and NI)
- Total of 42 datasets (three years × multiple products) with a consistent 21 UKCEH Land Cover Classes across years.
- Outputs designed to enable self-serve data exploration and time-series comparisons, with fixed parcel structures to support change detection.

## Data Inputs and Temporal Context
- Seasonal information derived from Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) generated in Google Earth Engine.
- Seasonal data combined with Context Rasters to form Classification Scenes for robust spectral discrimination.
- Four seasons used: winter, spring, summer, autumn; some cloud gaps are tolerated and do not halt production.
- 20m Classified Pixels preserve detailed features; Land Parcels summarise these into fixed real-world units; 25m Rasterised Parcels provide a generalized view for broader analysis.

## Classification Framework and Methodology
- Automated pipeline uses Bootstrap Training to derive training data from historic maps, enabling rapid map production without new field data collection.
- Bootstrap Training is based on past LCMs (primarily LCM2015) and uses majority signals over time to train the classifier.
- Random Forest classifier trained on 10,000 samples per class per Classification Scene to balance classes and improve robustness.
- Production software integrates Weka, PostGIS, and GDAL (open-source stack).

## The UKCEH Land Parcel Spatial Framework
- Parcels have a minimum area of ~0.5 hectares (Minimum Mapping Unit, MMU) and are designed to represent discrete land units (fields, parks, urban areas, etc.).
- gid remains a unique parcel identifier, but new LCM2017–2019 parcels have different gid values than LCM2015 due to framework changes.
- The framework is not the only possible parcel structure; 20m Classified Pixels can be summarised by user-defined parcels (e.g., catchments, administrative boundaries).

## Datasets and Attributes
- 20m Classified Pixels (GB and NI): two-band rasters; band 1 = most likely class, band 2 = class membership probability (0–100) for per-pixel confidence.
- Land Parcels: attributes include gid, hist (list of class frequencies per parcel), _mode (dominant class), _purity (parcel-wide modal proportion), _conf (mean class membership probability), _stdev (uncertainty), _n (number of pixels). Note: some attribute names were updated to align with production tooling.
- 25m Rasterised Land Parcels: three bands per parcel raster — band 1 = _mode, band 2 = _conf, band 3 = _purity.
- 1km Raster Datasets:
  - 1km Percent Cover: 21-band raster (percent cover per class)
  - 1km Percent Aggregate Cover: 10-band raster (aggregate class cover)
  - 1km Dominant Cover: single-band raster (dominant class)
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class)

## Classification Scenes and Spatial Coverage
- Great Britain: 100x100 km tiles; 36-band Seasonal Composite Images combined with 10 Context Layers to produce 46-band GB Classification Scenes; 74 overlapping scenes classified independently, with visual precedence used to resolve overlaps.
- Northern Ireland: single 43-band Classification Scene per year (36 spectral bands + 7 context layers) determined by the minimum bounding rectangle of NI land mass.
- Outputs are designed to support UK-wide change detection and regional analysis.

## Bootstrap Training and Validation
- Bootstrap Training uses historic land cover signals to automatically create training data for the RF classifier, reducing need for fresh field data.
- Training samples are drawn with replacement to balance class representation (10,000 samples per class per scene).
- Validation conducted against GB countryside survey data (2019), National Forest Inventory, IACS, and bespoke validation points (22,325 total).
- UK-scale accuracy results:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes: a single validation set used across three products; some class label mappings are converted from other schemes, which can affect absolute truth interpretation; results reflect best available indicators and are expected to improve with method maturation.

## Class Definitions and Mapping (Appendix Highlights)
- 21 UKCEH Land Cover Classes defined, linked to BAP Broad Habitats with careful attention to naming conventions to avoid ambiguity (e.g., italicising BAP Broad Habitats when referenced; capitalising defined class names).
- Appendix includes detailed class descriptions, crosswalks to BAP Broad Habitats, and notes on detection limitations and potential spectral confusions.
- Color scheme guidance provided for displaying classes in maps.

## Practical Considerations and Notes
- The production approach deliberately avoids manual accuracy corrections to enable annual updates; visual checks and formal validation still performed.
- The move to 20m Classified Pixels preserves landscape features below the MMU seen in higher-level summaries, enabling finer-scale analyses.
- GID changes mean direct parcel-by-parcel comparisons with LCM2015 require spatial overlap rather than id-based matching.
- Future plans include expanding to additional data sources and higher-temporal-frequency input (e.g., Sentinel-1, alternative optical sources) to fill seasonal gaps and improve thematic detail.

## Appendix and Dataset Catalog (Appendix 5)
- Full dataset listings and metadata for LCM2017, LCM2018, and LCM2019, including the GB and NI variants of each product and their corresponding dataset names and storage arrangements.