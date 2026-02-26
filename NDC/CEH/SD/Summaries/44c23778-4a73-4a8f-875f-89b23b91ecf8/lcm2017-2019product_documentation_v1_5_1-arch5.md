# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- Release and user guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map contains 21 UKCEH Land Cover Classes (aligned with earlier LCMs) derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Data produced automatically via Bootstrap Training with a Random Forest classifier; aims to deliver annual UK-wide maps without manual corrections.
- Validation shows maps are of similar quality to the preceding LCM2015; ~80% correspondence with validation points, acknowledging limitations in validation data alignment and class definitions.
- Data philosophy emphasizes traceability, reproducibility, and suitability for change detection across years.

## Production and data structure

### Datasets per year
- 20m Classified Pixels (GB and NI)
- Land Parcels (GB and NI)
- 25m Rasterised Land Parcels (GB and NI)
- 1km Dominant Cover (GB and NI)
- 1km Dominant Aggregate Cover (GB and NI)
- 1km Percent Cover (GB and NI)
- 1km Percent Aggregate Cover (GB and NI)
- Each year yields a total of 42 datasets (two regional variants × multiple products).

### 20m Classified Pixels
- New addition in LCM2017–2019: 2-band, 8-bit rasters.
- Band 1: nominated land cover class; Band 2: class membership probability (0–100) for per-pixel confidence.
- Retains detailed features (not generalised by the parcel framework) to preserve landscape granularity.

### Land Parcels
- Intersects 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
- Attributes include:
  - gid: unique parcel identifier (updated from LCM2015; notmatch for year-to-year parcel comparisons).
  - _hist: pixel-frequency histogram per class as tuples.
  - _mode: most frequent class within parcel.
  - _purity: percentage of modal class across pixels.
  - _conf: mean class membership probability (0–100) per parcel.
  - _stdev: standard deviation of _conf.
  - _n: number of 20m pixels intersecting parcel.
- Note: some attribute names differ from LCM2015 to align with production software; functionality preserved.

### 25m Rasterised Land Parcels
- Rasterised from Land Parcels to 25m pixels; three bands carry from Land Parcels:
  - Band 1: _mode (dominant class)
  - Band 2: _conf (parcel-averaged confidence)
  - Band 3: _purity (parcel purity)

### 1km Raster Products
- 1km Percent Cover: 21-band raster per 1km grid (percent cover by each class).
- 1km Percent Aggregate Cover: 10-band raster for aggregate classes (percent cover per 1km).
- 1km Dominant Cover: single-band raster with dominant class per 1km grid.
- 1km Dominant Aggregate Cover: single-band raster with dominant aggregate class per 1km grid.

### Seasonal Composite Images and Context Rasters
- Seasonal Composite Images created from Sentinel-2 TOA reflectance (TOA used; not all SR data available across years during production).
- Four seasons per year (winter, spring, summer, autumn) from 9 Sentinel-2 bands; seasonal gaps represented as nulls.
- 20m Context Rasters (GB) include terrain (Height, Aspect, Slope), distances to buildings, roads, sea, freshwater, foreshore, tidal water, and woodland.
- NI Context Rasters include terrain plus urban mask and distance-to-coast/freshwater/road layers.

### Classification Scenes and UKCEH Land Parcel Spatial Framework
- GB: 100x100 km tiling; 36-band Seasonal Composite Images combined with 20m Context Rasters to create 46-band GB Classification Scenes; 74 overlapping Scenes classified independently; visual inspection determines precedence where overlaps occur.
- NI: single 43-band Classification Scene per year (36 spectral bands + 7 context layers) covering the minimum bounding rectangle of NI land mass.
- The UK Land Parcel Spatial Framework defines ~0.5 ha MMU; parcels are fixed units used to stabilise time-series analysis and reduce classification noise.

### Bootstrap Training
- Bootstrap Training creates automatic training data from historic maps to train RF classifier without fresh field data.
- For LCM2017–2019, bootstrap samples from LCM2015 parcels with ≥99% purity were used.
- Future plans: bootstrap from majority signal across multiple years (e.g., 2017–2019 for LCM2020; 2018–2020 for 2021).

### Random Forest classification
- RF classifier trained with balanced sampling: 10,000 samples per class, drawn with replacement.
- Software stack: bespoke UKCEH tools integrating WEKA, PostGIS, and GDAL (open source).

## Data quality, validation, and limitations

- Validation: UK-scale comparison with GB countryside survey data (2019), National Forest Inventory data, IACS data, and bespoke LCM validation points (22,325 total).
- Reported overall accuracy at the national scale:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Validation points are not absolute truth; some misclassification is expected.
  - Validation datasets differ from product class definitions; conversions introduce subjectivity.
  - Currency and class-mapping differences can affect comparability; approximately 80% correspondence is considered robust for automatic LCMs.
- Visual checks and formal validation were performed; no manual regional corrections were applied in these years to maintain automation.

## Data governance, lineage, and notes for users

- Versioning and identifiers:
  - Land Parcel gid values differ from LCM2015; cross-year parcel-based comparisons require using gid, not spatial overlap.
- Spatial and data extents:
  - Great Britain: GB British National Grid (EPSG: 27700)
  - Northern Ireland: NI Irish Grid (EPSG: 29903)
  - Extents defined per dataset (GB and NI versions) with 20m, 25m, and 1km products.
- Class definitions and mapping:
  - 21 UKCEH Land Cover Classes aligned with UKCEH LCM2015/2007/2000 lineage; no direct UK BAP “standalone” mapping due to remote-sensing limitations.
  - Appendix materials provide detailed relationships between UKCEH classes and BAP Broad Habitats; some refinements exist for upland and coastal categories.
- Dataset packaging and accessibility:
  - Each year includes a consistent dataset suite; Appendix 5 lists full dataset names and holdings.
  - Data are structured to support both direct usage (20m Pixels) and summary/parcel-based analyses (Land Parcels, 1km rasters).

## Appendices and additional guidance

- Appendix 1 and 2: UKCEH Land Cover Classes descriptions and their relationship to BAP Broad Habitats; nuances for specific classes (e.g., Heather, Bog, Saltmarsh, etc.).
- Appendix 3: RGB color recipes for displaying classes (for visualization consistency).
- Appendix 4: Validation details and confusion matrices across LCM2017–LCM2019; producer’s and user’s accuracies per class; notes on cross-class confusion and data limitations.
- Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019, including GB/NI scope and dataset names.

## References and sources

- Core methodological references for RF classification, bootstrap training, and related satellite data sources.
- Documentation and prior reports on UKCEH LCM2007, LCM2015, and related validation frameworks.