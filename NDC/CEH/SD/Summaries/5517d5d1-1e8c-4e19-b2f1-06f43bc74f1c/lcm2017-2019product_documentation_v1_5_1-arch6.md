# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Maps use 21 UKCEH Land Cover Classes (based on UK BAP Broad Habitats) and aim for rapid, annual updates via automatic methods.
  - Emphasises informed use: data production decisions, limitations, validation, and plans for future releases.

- Key outputs (datasets)
  - 20m Classified Pixels (GB and NI, per year): RF classification results with per-pixel class and a second band showing membership probability (0–100).
  - Land Parcels: attributes derived from intersecting 20m pixels with the UKCEH Land Parcel Spatial Framework (GB and NI).
  - 25m Rasterised Land Parcels: three-band raster (mode, conf, purity) summarising parcel-level information.
  - 1km Raster datasets (GB and NI):
    - 1km Percent Cover (21 bands) per 1km grid.
    - 1km Percent Aggregate Cover (10 bands) per 1km grid.
    - 1km Dominant Cover (single band) per 1km grid.
    - 1km Dominant Aggregate Cover (1 band) is also produced.
  - Each year has GB and NI versions, totaling 42 primary datasets; additional metadata and cross-year comparability considerations apply.

- Production methodology
  - Bootstrap Training: automatic, self-starting sampling of training data from historic maps (primarily LCM2015) to train the RF classifier; aims to leverage majority signal across time.
    - For LCM2017–2019, training samples drawn from UKCEH LCM2015 parcels with purity ≥ 99%.
  - Random Forest classification: bespoke UKCEH software integrates WEKA with PostGIS and GDAL; balanced training (10,000 samples per class) to improve rarer class accuracy.
  - Seasonal Composite Images: Sentinel-2 seasonal TOA reflectance (winter, spring, summer, autumn) used to create 36-band GB scenes; nine Sentinel-2 bands (2,3,4,5,6,7,8,11,12) per season; cloud gaps handled automatically; gaps may be filled with future data sources (e.g., SAR).
  - Context Rasters: 20m context layers to reduce spectral confusion (e.g., height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, urban mask, etc.).
  - Classification Scenes and spatial framework: GB classified with overlapping 100x100 km tiles (36-band scenes plus context, total 46 bands); NI uses a single tile per year (43 bands).
  - UK Land Parcel Spatial Framework: same parcel framework as LCM2015, with minor updates to indices; gid identifiers change between years, limiting direct parcel-ID comparisons across years (use gid for cross-year comparisons from 2017–2019).

- Data structure and geography
  - 21 UKCEH Land Cover Classes tied to BAP Broad Habitats; generalised to UKCEH Aggregate Classes where needed.
  - GB and NI data exist separately; coordinate systems:
    - GB: British National Grid (EPSG: 27700).
    - NI: Irish Grid (TM 75, EPSG: 29903).
  - Pixel resolutions and extents:
    - 20m Classified Pixels (highest detail).
    - 25m Rasterised Land Parcels (summary/aggregation).
    - 1km rasters (coarser aggregations) across GB and NI.

- Data quality, validation, and accuracy
  - Visual checks and formal validation performed; real-world validation resources used include GB countryside survey 2019, National Forest Inventory, IACS, and bespoke validation points (22,325 points).
  - Reported overall accuracy (UK scale):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Important caveats:
    - Validation points are not absolute truth; conversions between BAP and UKCEH classes can introduce subjectivity.
    - No manual corrections were applied to LCM2017–2019; classification is fully automatic with post-hoc checks.
    - Classification errors are expected to be randomly distributed over space and time; real land-cover change should persist against background noise as the time series grows.
  - Output formats and metadata designed to support data use, with notes on class naming conventions and potential confusion between BAP Broad Habitats and UKCEH Land Cover Classes (capitalisation and italics guidelines).

- Data access, formats, and display
  - Datasets include accompanying metadata and descriptive tables (Tables 2–5 in Appendix; Appendix 3 provides RGB color recipes for display).
  - 20m Classified Pixels preserve fine-scale features; 25m and 1km products provide progressively generalized outputs suitable for larger-scale analyses.
  - Land Parcel attributes (Table 5) include:
    - gid: parcel identifier
    - _hist: distribution of class counts within parcel
    - _mode: most frequent class
    - _purity: percentage of modal class
    - _conf: mean class membership probability (0–100)
    - _stdev: standard deviation of confidence
    - _n: number of pixels intersecting parcel
  - Differences from LCM2015 highlighted (e.g., removal of Composite field; changes in attribute naming; improvements to histogram representation).
  - Appendix 3 provides recommended RGB values for each of the 21 classes to enable consistent visualization.

- Practical considerations for data support and reuse
  - Outputs are designed to enable self-service analysis and time-series comparison, with clear guidance on using 20m, 25m, and 1km products together.
  - Users should be aware of gid changes and the need to use stable cross-year identifiers where possible; comparisons between LCM2017–2019 parcels should rely on gid rather than historical parcel IDs.
  - The data production approach emphasizes automation and annual updates; future versions (LCM2020, LCM2021) plan to refine bootstrap methods (e.g., moving toward multi-year majority signals) and potentially expand input data types.
  - Appendix 5 provides a full list of datasets for LCM2017, LCM2018, and LCM2019, including GB and NI products and their storage names.

- Summary of intended use and future plans
  - Goal: deliver timely, policy-relevant land cover information across the UK with a clear understanding of production choices, data structure, and validation status.
  - Future directions include exploring data gaps (e.g., full annual 4-season fill, potential use of Sentinel-1 SAR, broadened input sources) and enhancing cross-year comparability and utility for change detection.