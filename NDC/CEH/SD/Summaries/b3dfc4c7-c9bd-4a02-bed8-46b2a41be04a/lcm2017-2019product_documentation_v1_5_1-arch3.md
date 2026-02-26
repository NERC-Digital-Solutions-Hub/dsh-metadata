# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- Presents three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each map includes a suite of geospatial datasets mapping UK land cover using 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats; with accompanying guidance to support informed use, validation, and future planning.
- Aims to enable policy scrutiny, environmental health monitoring, change detection, and decision-making with an emphasis on data provenance, quality, and transparency.

## Data products and structure
- 20m Classified Pixels: new 20m RF-classified pixel data with two bands per pixel:
  - Band 1: nominated land cover class (21 classes).
  - Band 2: classification confidence (0–100).
- Land Parcels: parcel-level attributes derived from the 20m Classified Pixels using the UKCEH Land Parcel Spatial Framework; key attributes include:
  - gid: unique parcel identifier (stable within a product line but not identical to LCM2015).
  - _hist: histogram of class counts per parcel.
  - _mode: most frequent class in parcel.
  - _purity: percentage of modal class within parcel.
  - _conf: mean class membership probability (0–100).
  - _stdev: standard deviation of confidence.
  - _n: number of 20m pixels intersecting parcel.
- 25m Rasterised Land Parcels: rasterized parcel products (3 bands) summarizing parcel data at 25m resolution.
- 1km Raster Datasets (aggregations across parcels):
  - 1km Percent Cover: 21-band raster showing percent cover per class.
  - 1km Percent Aggregate Cover: 10-band raster for aggregate classes.
  - 1km Dominant Cover: single-band raster of dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band raster for dominant aggregate class.
- Dataset extents: GB (Great Britain) and NI (Northern Ireland) versions, each year, yielding 42 datasets across the three years.

## Production methodology
- Classification approach: automatic, data-driven, with no manual corrections (to enable annual updates) but with extensive validation.
- Bootstrap Training: automatic, self-starting training using historic maps to guide current classification; leverages majority signals across years.
  - Bootstrap training for LCM2017–2019 derived from LCM2015 with parcels having purity ≥ 99%.
  - Future bootstrap plans target majority signals across multiple years (e.g., 2017–2019 for LCM2020; 2018–2020 for 2021).
- Random Forest (RF) classification: supervised learning using balanced sampling (10,000 samples per class) to train the RF model; production software integrates WEKA, PostGIS, and GDAL.
- Data sources: Sentinel-2 Seasonal Composite Images (TOA reflectance, resampled to 20m) across four seasons; combined with 20m context rasters to form Classification Scenes.
- Seasonal composites: four-season TOA-based images (winter, spring, summer, autumn) with gaps due to cloud; RF classifier tolerates partial spectral information.
- Context rasters (20m): GB includes terrain (Height, Aspect, Slope), proximity to buildings/roads/seas/freshwater, foreshore, tidal water, and a woodland mask; NI includes terrain, urban mask, and proximity layers.
- Classification Scenes: GB uses 100x100 km tiles (74 overlapping scenes classified independently); NI uses a single 43-band scene per year for the entire territory.

## The UKCEH Land Parcel Spatial Framework
- Grounded in a framework used since LCM2007, with minor updates for 2017–2019; parcel geometries remain consistent with LCM2015, but parcel identifiers (gid) differ for cross-year comparability.
- Minimum Mapping Unit (MMU) ~0.5 ha; parcels represent discrete real-world units (fields, parks, urban areas, etc.) and help reduce classification noise and support change detection.
- Users can summarize 20m Classified Pixels using their own parcel structures beyond the provided framework.
- Future frameworks may evolve to finer resolutions and smaller MMU to reflect higher-resolution data.

## Validation and accuracy
- UK-scale validation used 22,325 points from GB Countryside Survey 2019, National Forest Inventory, IACS, and manual interpretation points.
- Reported overall accuracy (across three products with a common validation set, variable currency):
  - LCM2017: ~78.6%
  - LCM2018: ~79.6%
  - LCM2019: ~79.4%
- Validation is not an absolute truth: points vary in precision, and class definitions require conversion to UKCEH classes; results are best interpreted as indicators of performance and used with caution.
- Detailed confusion matrices and per-class producer’s and user’s accuracies are provided in appendices.

## Metadata, terminology, and governance
- Datasets categorized into 21 UKCEH Land Cover Classes linked to BAP Broad Habitats; generalised 21-class scheme provided alongside aggregated 10-class schemes where relevant.
- Clear notes on the relationship and potential ambiguities between UKCEH Land Cover Classes and UK BAP Broad Habitats; terminology is capitalized to denote defined classes.
- Tables and appendices provide class derivations, mapping notes, and reporting conventions (including color recipes for visualization).

## Practical considerations for monitoring frameworks
- Annual map production enables near-real-time tracking of land cover change across the UK, supporting policy evaluation and environmental health assessment.
- The 20m Classified Pixels dataset preserves high spatial detail (beneficial for small patches and narrow features), while 25m and 1km products provide generalized summaries suitable for regional or national policy reporting.
- The per-pixel class probability (confidence) and parcel-level histograms enable uncertainty assessment and confidence-aware decision-making.
- Data accessibility considerations:
  - Cross-year parcel identifiers (gid) are not guaranteed to be stable year-to-year; comparability relies on spatial overlap or the parcel framework rather than a direct gid match.
  - The framework provides a transparent lineage (Bootstrap Training → RF classification → parcel summarization) and detailed metadata to support governance and reproducibility.
- Limitations and future directions:
  - Some upland peatland and saltwater/freshwater distinctions remain challenging; ongoing work aims to improve training data and detection for specialist habitats.
  - Gaps in gap-filling for cloud-covered seasons; exploration of alternative data sources (e.g., Sentinel-1 SAR) for complete seasonal classification.

## Appendix highlights (for interpretive context)
- Appendix 1: Notes on UKCEH Land Cover Classes and practical detection considerations for each class; discusses typical confusions and how context rasters mitigate some misclassifications.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitat definitions and their relationship to UKCEH classes.
- Appendix 3: Recommended RGB color mappings for display of UKCEH Land Cover Classes.
- Appendix 4: Validation tables and confusion matrices for LCM2017, LCM2018, and LCM2019 (granular per-class performance and overall accuracy metrics).
- Appendix 5: Full dataset listing and structure across LCM2017, LCM2018, and LCM2019, including GB and NI datasets.