# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Overview
  - Release of three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Each map provides 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and mirrors the class structure used in LCM2015.
  - Aims to enable rapid, annual UK-wide land cover mapping with formal validation and documentation.
  - All outputs are produced automatically, with no manual corrections in this release; visual checks and validation are still performed.

- Data and outputs included
  - 20m Classified Pixels: per-pixel class with a confidence measure (two-band 8-bit rasters; probability 0–100 for the nominated class).
  - Land Parcels: vectors/attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; includes parcel-level histograms, modal class, purity, confidence, standard deviation, and number of constituent pixels.
  - 25m Rasterised Land Parcels: three-band rasters for band1 (modal class), band2 (confidence), band3 (purity).
  - 1km Raster Products:
    - 1km Percent Cover: 21-band raster with percentage cover per class.
    - 1km Percent Aggregate Cover: 10-band raster for aggregated classes.
    - 1km Dominant Cover: single-band raster of dominant class per 1km cell.
  - Extents and formats: Great Britain (GB) and Northern Ireland (NI) versions; coordinate systems GB National Grid (EPSG:27700) and NI Irish Grid (EPSG:29903); pixel origins align with national grids.

- Production approach and inputs
  - Bootstrap Training combined with Random Forest classifier to generate classifications automatically.
  - Sentinel-2 Seasonal Composite Images (median reflectance per season) used to form Classification Scenes; four seasons (winter, spring, summer, autumn).
  - Ten Context Rasters (e.g., height, slope, distance to features) added to reduce spectral confusion and improve classification.
  - Classification Scenes: GB production uses 100x100 km tiles; 74 overlapping scenes; NI uses a single 43-band scene per year.
  - Bootstrap Training: history-driven training derived from UKCEH LCM2015 data, enabling rapid updates without new field campaigns. Future plans indicate bootstrap using majority signals over the selected years.

- UKCEH Land Parcel Spatial Framework
  - Uses a fixed 0.5 ha minimum mapping unit; designed to represent discrete land units (fields, parks, urban, etc.).
  - gid identifiers are consistent across LCM2017–LCM2019 for cross-year comparisons; gid values differ from LCM2015.
  - Spatial framework supports changing analytics boundaries; users can summarize 20m pixels using alternative parcel structures if desired.

- Data structure and key details
  - 20m Classified Pixels: two bands (class, confidence); preserves fine landscape features compared with parcel-aggregated outputs.
  - Land Parcels: attributes include gid, _hist (class frequencies within parcel), _mode (dominant class), _purity (modal proportion), _conf (mean class membership probability), _stdev, _n (pixel count).
  - 25m Rasterised Parcels: 3-band output (mode, conf, purity).
  - 1km rasters: 21-band Percent Cover, 10-band Percent Aggregate Cover, and single-band Dominant Cover.

- Validation and accuracy
  - UK-scale validation using GB countryside survey 2019 data, open data sources (National Forest Inventory, IACS), and bespoke LCM validation points.
  - Validation sample: 22,325 points; overall accuracy:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation points reflect cross-year currency and class mapping; accuracy targets are approximate indicators rather than absolute truth.
  - Appendices provide full validation tables and confusion matrices (Appendix 4).

- Class definitions and relationships
  - 21 UKCEH Land Cover Classes are aligned with UK BAP Broad Habitats but are not exact BAP mappings; italics used to reference BAP terms where appropriate.
  - Appendix 1 and 2 provide detailed class definitions and the relationships between UKCEH classes, Aggregate Classes, and BAP Broad Habitats.

- Visualization and colour coding
  - Appendix 3 provides a recommended RGB color recipe for displaying UKCEH Land Cover Classes (per class).

- Practical considerations for analysts
  - Data are designed for monitoring environmental change and policy performance over time, with standardized formats for comparison.
  - The time-series design expects that classification errors are randomly distributed; persistent real changes should emerge as the series evolves.
  - There are potential spectral confusions between similar land cover types; context rasters and multi-scale outputs help mitigate this.
  - Gaps due to cloud cover in seasonal composites are addressed by algorithmic tolerance; future work may incorporate SAR (Sentinel-1) to fill gaps.

- Appendices and additional notes
  - Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats, including detection limitations and region-specific caveats.
  - Appendix 3: RGB color recipes for display.
  - Appendix 4: Full validation confusion matrices and accuracy metrics (LCM2017–LCM2019).
  - Appendix 5: Full list of datasets and their naming conventions, including GB and NI outputs for each year.

- Future directions and plans
  - Annual LCM releases are planned going forward.
  - Potential enhancements include broader satellite inputs, additional data sources (e.g., SAR), and refinements to training data and parcel frameworks to support finer resolution or different boundary alignments.