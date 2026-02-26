# The UKCEH Land Cover Maps for 2017, 2018 and 2019
v1.5.1

- Overview
  - User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Provides content, structure, production workflow, validation, and guidance for informed use in current and future work.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; near-equivalent mapping across years to support change detection.
  - Annual release aim; automated production to enable rapid UK-wide mapping.

- Key Data Products (per year)
  - 20m Classified Pixels (GB and NI)
    - 2-band rasters: Class (band 1) and per-pixel class membership probability (band 2, scaled 0–100).
    - Preserves fine landscape detail; not generalized by Land Parcel Framework.
  - Land Parcels
    - Attributes for each parcel: gid, _hist (histogram of class counts), _mode (dominant class), _purity, _conf (mean class membership probability), _stdev, _n (pixel count).
    - Note: gid values differ from LCM2015; parcel framework retained for time-series flexibility.
  - 25m Rasterised Land Parcels
    - 3-band raster: band 1 _mode, band 2 _conf, band 3 _purity.
  - 1km Raster Datasets
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Dataset Extents
    - Great Britain (GB) and Northern Ireland (NI) versions for each year.
    - GB grid: British National Grid, EPSG:27700; NI grid: Irish TM75, EPSG:29903.

- Production Methodology
  - Bootstrap Training
    - Automatic, field-free training using historic maps (Bootstrap Training) to sample spectral training observations.
    - Bootstrap sources: UKCEH LCM2015 for 2017–2019; LCM2015 bootstrap derived from 1990–2007 observations with manual inputs.
    - For 2017–2019, land parcels with purity ≥ 99% in LCM2015 used to seed training data.
    - Planned evolution: future bootsrapping to reflect majority signal across multiple years.
  - Random Forest Classification
    - Training uses balanced sampling: 10,000 samples per class from each training bag.
    - Produces 20m Classified Pixels; subsequent products derived from parcel-based summarization.
  - Seasonal Composite Imagery and Classification Scenes
    - Sentinel-2 Seasonal Composite Images (TOA reflectance) per season (winter, spring, summer, autumn) used to create 36-band Seasonal Composite Images.
    - Context Layers (20m) added to create Classification Scenes.
    - Great Britain: 74 overlapping 100x100 km tiles used to generate 46-band GB Classification Scenes; NI uses a single 43-band scene per year.
    - Gaps due to cloud are handled; the classifier tolerates partial data; future work may incorporate SAR (Sentinel-1) or alternative sources to fill gaps.
  - Context Rasters
    - GB 20m context rasters include terrain (Height, Aspect, Slope), distances to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask.
    - NI context rasters include similar context plus urban mask and distances to coast/freshwater/roads.
  - UKCEH Land Parcel Spatial Framework
    - 0.5 ha minimum MMU; parcels designed to represent discrete land units (fields, parks, urban, etc.).
    - Framework is reused with minor updates; gid values differ from LCM2015; 2017–2019 parcel comparisons use gid-based matching.

- Validation and Accuracy
  - Validation dataset: GB countryside survey 2019, open forest inventory, IACS, and bespoke LCM validation points (22,325 points total).
  - Reported overall accuracy (UK scale):
    - 2017: 78.6%
    - 2018: 79.6%
    - 2019: 79.4%
  - Note: Validation uses the same points across products; class label mappings require careful interpretation; approximately 80% correspondence is considered strong for automatically produced, annual maps.
  - Appendices provide detailed confusion matrices and producer’s/user’s accuracies per class.

- Class Relationships and Documentation
  - 21 UKCEH Land Cover Classes are aligned with UK BAP Broad Habitats where possible; attention to potential ambiguities between UKCEH vs BAP nomenclature.
  - Appendix notes cover class definitions, detection considerations, and potential confusions (e.g., upland peatland vegetation, bracken, saltwater/freshwater distinctions, and linear features).
  - RGB color guidance provided for display; mapping between classes and colors is defined to aid visualization.

- Practical Considerations for Analysts
  - Time-series use: Gid-based parcel matching may limit direct comparison with LCM2015; parcel overlap can still support change detection via pixel-level data, but exact parcel IDs may differ year-to-year.
  - Data quality and gaps: Cloud gaps in Sentinel-2 seasonal composites; TOA used over SR owing to data availability during production.
  - Output formats and scales: Detailed metadata provided; multiple raster resolutions (20m, 25m, 1km) and multiple summary products enable flexible analysis and policy monitoring.
  - Future directions: Annual updates, expansion to higher resolutions, broader satellite inputs (including SAR), and exploration of alternative parcel frameworks for finer change detection.

- Appendix and Resource Availability
  - Full dataset descriptions and relationships between class schemes, along with metadata about geographic extents and pixel/parcel attributes.
  - Full list of datasets per year provided (20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, 1km products across GB/NI).