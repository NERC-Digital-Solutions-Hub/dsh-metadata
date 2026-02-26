The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Purpose and scope
  - Release and user guide for three UKCEH national land cover maps: LCM2017, LCM2018, LCM2019.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed for broad-scale monitoring and change detection.
  - Maps produced automatically using Bootstrap Training with a Random Forest classifier; aims for annual updates to monitor land cover change.
  - Validation indicates maps are of similar quality to LCM2015; around 79% overall accuracy, with ongoing improvements and caveats about validation data.

- Production approach and data lineage
  - Bootstrap Training: automatic training dataset derived from historic UKCEH LCMs (primarily LCM2015) to bootstrap new maps; targets majority signal over time.
  - Random Forest classification: training data balanced to ensure representation of all classes; pixel-level classification for 20m Classified Pixels.
  - Data products in the release (GB and NI) include:
    - 20m Classified Pixels (new; per-pixel class and confidence)
    - Land Parcels (attributes derived by intersecting 20m pixels with the UKCEH Land Parcel Spatial Framework)
    - 25m Rasterised Land Parcels (3-band rasters: mode, conf, purity)
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Datasets are duplicated for GB and NI, yielding 42 datasets in total; year-to-year comparisons rely on gid-based parcel identifiers due to changes in the underlying spatial framework.
  - The 20m Classified Pixels preserve finer landscape features compared with parcel-based summaries; 25m and 1km products generalise to broader scales.

- Spatial framework and data structure
  - UK Land Parcel Spatial Framework defines land parcels (~0.5 ha MMU) to reduce noise and support change detection.
  - Parcel identifiers (gid) are consistent within a given year but do not match LCM2015 identifiers; cross-year comparisons use gid-based matching rather than exact parcel IDs.
  - GB uses a 100x100 km tiling approach to select Sentinel-2 Seasonal Composite Images; NI uses a single tile for the entire land mass.

- Inputs and imagery
  - Seasonally aggregated Sentinel-2 imagery (TOA reflectance, median per season) at 20m resolution; four seasons (winter, spring, summer, autumn).
  - Seasonal images combined with 20m Context Rasters to form Classification Scenes.
  - Context Rasters (20m) include terrain (height, aspect, slope) and proximity metrics (distance to buildings, roads, sea, freshwater) plus land-use masks (urban, woodland) and coastal/foreshore indicators.
  - TOA data preferred over surface reflectance (SR) in this release; Google Earth Engine provides the Sentinel-2 data.

- Classification scenes and geographic scope
  - Great Britain: 74 overlapping 100x100 km Classification Scenes; each year mapped separately with overlaps allowed to maximize training variation; final outputs integrate the best results.
  - Northern Ireland: a single 43-band Classification Scene per year (36 spectral bands + 7 context layers).
  - The production process includes a minimal amount of manual judgment (only for visual precedence when overlaps occur).

- Data governance, metadata and accessibility
  - Datasets come with detailed metadata (coordinate systems, extents, class definitions, and attribute schemas); GB uses EPSG:27700 (British National Grid), NI uses EPSG:29903 (Irish Grid).
  - Attribute naming differences relative to LCM2015: keys like _hist, _mode, _purity, _conf, and _n; some attributes reorganised to align with production software conventions.
  - Users are advised of potential non-recoverable cross-year parcel identifiers and to rely on gid for cross-year comparisons.
  - Outputs are designed for open dissemination and interoperability (uses open-source tools like Weka, PostGIS, GDAL).

- Validation and accuracy
  - Validation framework for UK scale uses countryside survey data (2019), National Forest Inventory, IACS, and bespoke interpretation points (about 22,325 points).
  - Reported overall accuracy at the UK scale:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data are not absolute truth; they are best-available indicators with caveats on class conversions and representativeness.
  - Appendix 5 provides confusion matrices and class-level producer’s and user’s accuracies to inform class-specific monitoring decisions.

- Dataset specifics and usage notes
  - 20m Classified Pixels: new in 2017–2019 release; class membership probabilities for 21 classes; highest probability determines class; second band encodes confidence (0–100).
  - Land Parcels: include parcel-level attributes describing pixel composition, modal class, confidence, purity, and overlap counts; changes since LCM2015 include renamed attributes and simplified descriptions.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) derived from Land Parcels; provide parcel-averaged summaries at 25m resolution.
  - 1km Datasets: aggregation from 25m pixels; include 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band) and 1km Dominant Aggregate Cover (1 band). Percent values are rounded; sums may not exactly equal 100 due to rounding and coastal partial coverage.
  - The UKCEH Land Parcel Spatial Framework remains fixed for the release period; future updates may refine to accommodate higher-resolution data and different MMUs.
  - Appendix 2 and related material provide detailed Biodiversity Action Plan (BAP) Broad Habitats definitions and detection notes; Appendix 3–4 offer color schemes for mapping and accessibility considerations.

- Future directions and ongoing improvements
  - UKCEH plans to continue annual LCM releases (LCM2020 planned for 2021) with bootstrap updates using multi-year majority signals and enhancements to training data.
  - Ongoing assessment of input data (e.g., incorporating alternative optical sources, synthetic aperture radar) to address potential gaps (e.g., cloud cover gaps) and improve classification robustness.
  - Exploration of higher-resolution or alternative parcel structures to improve detection of narrow features and fine-scale changes while balancing processing demands.

- References and further resources
  - Methodological notes on bootstrap training, Random Forest classification, and related biodiversity habitat classifications (Appendices 1–2).
  - Full dataset lists and structures provided in Appendix 6; data product metadata summarized in Table 2.
  - Validation and accuracy details, including confusion matrices, provided in Appendix 5.