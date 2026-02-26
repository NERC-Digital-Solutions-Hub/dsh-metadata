# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and Overview
- Presents three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map comprises 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) configured for remote-sensing detection.
- Maps produced automatically using Bootstrap Training and a Random Forest classifier; seasonal Sentinel-2 composites (TOA) plus 20m Context Rasters.
- No manual corrections applied this time; visual checks and formal validation conducted.
- Validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points; overall UK-scale accuracy around 78.6–79.6% across 2017–2019.
- Aim to enable annual releases, rapid production, and ongoing assessment of land cover change.

## Data Landscape and Structure
- 42 datasets per release (GB and Northern Ireland for each year), mirroring the 20m–1km data cascade.
- Core datasets:
  - 20m Classified Pixels: new 2-band rasters from RF classification of Sentinel-2 seasonal scenes; includes classification confidence.
  - Land Parcels: fixed spatial framework (gid, _hist, _mode, _purity, _conf, _stdev, _n); designed to summarise 20m pixels within parcels (~0.5 ha MMU).
  - 25m Rasterised Land Parcels: three-band rasters (band1=_mode, band2=_conf, band3=_purity).
  - 1km Raster Datasets:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Spatial framework and extents:
  - Great Britain: GB National Grid (EPSG:27700)
  - Northern Ireland: Irish Grid (EPSG:29903)
  - Minimum mapping unit around 0.5 ha; Land Parcels are designed for consistent temporal comparison.
- Dataset relationships:
  - 20m Classified Pixels feed into Land Parcels, which then underpin 25m Rasterised Land Parcels and 1km products.
  - UKCEH Land Cover Classes correspond to, but are not identical to, UK BAP Broad Habitats; general mapping and interpretation notes provided in appendices.

## How It Was Built (Methodology)
- Bootstrap Training:
  - Training data derived from UKCEH LCM2015 with >99% purity, enabling automatic bootstrap sampling for classifier training.
  - Bootstrap sets evolve; future maps planned to bootstrap from majority signals across multiple years.
- Random Forest Classification:
  - Balanced sampling: 10,000 samples per class from labelled training bags.
  - Production software integrates Weka, PostGIS, and GDAL (open source).
- Seasonal Composite Images:
  - Sentinel-2 TOA median reflectance for four seasons (winter, spring, summer, autumn) across nine bands; gaps due to cloud accounted for; classifier tolerant of partial data.
  - Context Rasters (20m) provide terrain, distance-to features, and proximity cues to reduce spectral confusion.
- Classification Scenes:
  - GB: 100x100 km tiles, overlapping to balance training data; NI: single 43-band scene per year.
  - Overlaps may yield minor regional differences; manual precedence used to select final results.
- UK Land Parcel Spatial Framework:
  - Unchanged in geometry from LCM2015, but with restructured storage and new indices; gid values do not match LCM2015 across years (use gid for cross-year comparisons 2017–2019).
- Validation:
  - 22,325 validation points across GB, mapped to UKCEH Land Parcels; accuracy indicators provided per class and overall.

## Data Products and Usage
- 20m Classified Pixels:
  - Primary, high-detail pixel-level product; per-pixel class (Band 1) and confidence (Band 2, 0–100).
  - Preserves fine landscape features that may be missed in parcel-based summaries.
- Land Parcels:
  - Attributes per parcel reflecting composition and confidence: gid, _hist (per-class counts), _mode (dominant class), _purity (percent of modal class), _conf (mean class membership confidence), _stdev, _n (number of pixels).
  - Some attribute names differ from LCM2015; improved histogram formatting and probability interpretation.
- 25m Rasterised Land Parcels:
  - 3-band rasters: band1=_mode, band2=_conf, band3=_purity.
- 1km Datasets:
  - 1km Percent Cover: 21 bands (per-class cover percentages).
  - 1km Percent Aggregate Cover: 10 bands (aggregate class percentages).
  - 1km Dominant Cover: single-band map of the dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band dominant aggregate class per 1km cell.
- Notes on use:
  - 20m pixels retain fine-scale features; Land Parcels provide a stable framework for change detection.
  - Cross-year comparisons require using gid, not parcel identifiers, due to frame reordering.

## Data Quality, Limitations, and Future Directions
- Validation:
  - UK-wide accuracy around 79%; class-level producer’s accuracy ranges show varying performance (e.g., Saltmarsh, Freshwater, Urban, etc.).
  - Validation data may differ in purpose and class mapping; results are indicative rather than absolute truth.
- Limitations and challenges:
  - Some upland, peatland, and spectral-confusion areas (e.g., Bog, Fen, Peatland vegetation) show inter-class confusion; coastal Saltwater/Freshwater delineation relies on context rasters.
  - No manual corrections this release due to automation constraints; future iterations may explore targeted refinements.
- Future directions:
  - Potential expansion to include additional satellite inputs (e.g., Sentinel-1 SAR) to fill seasonal gaps and improve spectral discrimination.
  - Review of training data and potential new bootstrap strategies for improved year-over-year consistency.
  - Continued annual release with streamlined production to monitor land cover change dynamics.

## Metadata, Access, and Governance
- Appendices provide in-depth notes on UKCEH Land Cover Classes and BAP Broad Habitats, including mappings, notes, and crosswalks between class schemes.
- RGB color recipes and validation tables are provided to support visualization and interpretation.
- Full dataset catalog and annual data listings are documented (Appendix 5); data assets are designed to support cross-year analyses and integration with partners.
- Notes on data identifiers:
  - gid remains stable for each land parcel across the LCM2017–LCM2019 family but does not match LCM2015 parcel IDs; comparisons should use gid for cross-version consistency.

## Appendices (Key Context)
- Appendix 1–2: UKCEH Land Cover Classes and UK BAP Broad Habitats definitions, with detailed notes on class derivation, detection challenges, and compatibility with remote sensing.
- Appendix 3: RGB color mappings for display of UKCEH Land Cover Classes.
- Appendix 4: Validation and confusion matrix considerations; per-class user and producer accuracies, and overall metrics.
- Appendix 5: Full listing of datasets released per year and data product naming conventions.