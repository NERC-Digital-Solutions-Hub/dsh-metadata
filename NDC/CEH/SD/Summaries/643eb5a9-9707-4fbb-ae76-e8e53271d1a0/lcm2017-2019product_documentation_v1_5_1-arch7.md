# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- UKCEH releases three new national land cover maps: LCM2017, LCM2018, and LCM2019.
- All maps use 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and match the style of LCM2015.
- Maps are produced automatically using Bootstrap Training plus a Random Forest classifier; no manual corrections are applied this cycle.
- Aims to enable rapid, annual updates to monitor land cover change.
- Validation indicates maps are of similar quality to the latest predecessor (LCM2015); observed accuracy around 78–79% at the UK scale for 2017–2019.

## Production approach and data structure
- Bootstrap Training: automatically samples training data from UKCEH LCM2015, selecting parcels with at least 99% purity to form the bootstrap training set. This fosters a large, majority-signal training base without new field data.
- Random Forest classification: balanced sampling (10,000 samples per class) from classification scenes to generate the 20m Classified Pixels product (pixel-level land cover with a per-pixel confidence).
- Seasonal Composite Images: classifier uses Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) for four seasons; 9 spectral bands used. Some cloud gaps may occur; future work may incorporate SAR, additional sources, or reflectance products.
- Context Rasters: 20m context layers (e.g., terrain, proximity to buildings/roads/coast, water) to reduce spectral confusion and improve classification.
- Classification Scenes:
  - Great Britain: 74 overlapping 100x100 km tiles, each producing a 46-band Classification Scene (36 spectral bands + 7 context layers).
  - Northern Ireland: a single 43-band Classification Scene per year.
- UKCEH Land Parcel Spatial Framework: fixed 0.5 ha minimum mappable unit; parcels summarise 20m Classified Pixels. gid identifiers are stable within the new framework but do not match LCM2015 parcels; comparison should use gid across 2017–2019.
- Data framework and extents: GB and NI datasets are provided in their respective national grids (GB: EPSG:27700; NI: EPSG:29903). The suite includes 42 datasets (year x region x dataset type).

## Datasets and their structure
- 20m Classified Pixels (new addition)
  - 2-band rasters per year per region.
  - Band 1: nominal UKCEH Land Cover Class (21 classes).
  - Band 2: class membership probability (0–100) indicating classification confidence.

- Land Parcels
  - Attributes per parcel (gid and derived fields):
    - _hist: list of class counts per parcel as tuples (class_id:count).
    - _mode: most frequent land cover class within parcel.
    - _purity: percentage of the modal class within the parcel.
    - _conf: mean class membership probability (0–100).
    - _stdev: standard deviation of _conf.
    - _n: number of 20m pixels intersecting the parcel.
  - Note: attribute names differ from LCM2015; wording aligned to production software.

- 25m Rasterised Land Parcels
  - 3-band rasters:
    - Band 1: _mode (dominant class within parcel).
    - Band 2: _conf (parcel-averaged class membership probability).
    - Band 3: _purity (parcel homogeneity).

- 1km Datasets (derived by aggregating 25m parcels within 1km grids)
  - 1km Percent Cover: 21-band raster (per 1km grid, percentage cover for each class).
  - 1km Percent Aggregate Cover: 10-band raster (percentage cover for each UKCEH Aggregate Class).
  - 1km Dominant Cover: 1-band raster (dominant UKCEH Land Cover Class per 1km).
  - 1km Dominant Aggregate Cover: 1-band raster (dominant UKCEH Aggregate Class per 1km).

- Dataset extents and pixel sizes
  - 20m Classified Pixels: high-detail 20m grid.
  - 25m Rasterised Land Parcels: 25m grid summarising parcels.
  - 1km rasters: 1km grid for broader-scale analyses.
  - GB extents: Roberts GB grid (EPSG:27700) for most products; NI extents: EPSG:29903.

## GB vs NI specifics
- Great Britain: classification uses overlapping 100x100 km tiles to generate 46-band Classification Scenes; 74 GB tiles selected to ensure training balance and seasonal coverage.
- Northern Ireland: uses a single 43-band Classification Scene per year; streamlined due to smaller area.
- Land Parcel Spatial Framework: unchanged geometry relative to LCM2015 but with reindexed storage; gid values are not directly comparable to LCM2015 parcels, though gid remains stable year-to-year within 2017–2019 for cross-year parcel comparisons.

## Validation and accuracy
- Validation dataset: 22,325 points drawn from GB countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points; points intersected with LCM Land Parcel datasets to assess correspondence.
- UK-scale accuracy (approximate and currency-adjusted):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Caveats: validation uses cross-compatible but not perfectly matched class mappings; observations are not absolute truth; the validation sample sources differ in purpose and may require class conversions.

## Use cases and guidance for GIS specialists
- When detailed land cover is needed with intact spatial detail, use the 20m Classified Pixels.
- For change detection or parcel-based analyses, use Land Parcels with their per-parcel _hist and _mode/_purity/_conf attributes.
- For wall-to-wall, coarser analyses, employ the 1km Percent Cover, 1km Percent Aggregate Cover, and 1km Dominant/ Dominant Aggregate rasters.
- The 20m Context Rasters improve classification of spectrally similar classes (e.g., wetlands, urban vs non-urban) and are important for robust RF learning.
- The Bootstrap Training approach leverages historic maps (LCM2015) to produce rapid updates; future maps plan to use multi-year majority bootstrap (e.g., 2017–2019) for the next release.
- Cross-year comparisons are facilitated via gid for 2017–2019 parcels, but parcel IDs do not align with LCM2015; use gid-based comparisons across 2017–2019.

## Appendices and additional resources
- Appendix 1 & 2: UKCEH Land Cover Classes and the Biodiversity Action Plan (BAP) Broad Habitats; detailed class definitions and detection considerations.
- Appendix 3: Recommended RGB color mapping for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation details and confusion matrices (per class) for LCM2017, LCM2018, and LCM2019.
- Appendix 5: Full dataset listing by year and dataset type (GB and NI variants).

## Future plans
- Continue annual releases with automated methods to enable yearly LCM updates; future work may expand input data sources (e.g., higher-resolution SAR, additional optical sensors) and refine training data or class delineations as needed.