# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview and purpose
- User guide accompanying the release of three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Describes content, production workflow, validation, decisions, and future plans to help users apply the data appropriately.
- Aims to enable informed use of UK-wide land cover information and to outline how data were produced and validated.

## Key data products and structure
- 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats; aligned with LCM2015; not a strict BAP map, but closely related).
- Data products per year include:
  - 20m Classified Pixels: new 20-meter RF classification results with per-pixel class probability; two-band rasters (dominant class and probability).
  - Land Parcels: 20m pixel classifications summarized within the UKCEH Land Parcel Spatial Framework; parcel-level attributes such as hist, mode, purity, conf, stdev, n.
  - 25m Rasterised Land Parcels: rasterized parcel outputs (3 bands: mode, conf, purity).
  - 1km Percent Cover: 21-band raster showing percentage cover by each UKCEH Land Cover Class per 1km grid.
  - 1km Percent Aggregate Cover: 10-band raster showing percentage cover for UKCEH Aggregate Classes per 1km.
  - 1km Dominant Cover: single-band raster of the dominant class per 1km grid.
  - 1km Dominant Aggregate Cover: single-band raster of dominant aggregate class per 1km.
- Datasets provided in two regional editions:
  - Great Britain (GB) using British National Grid (EPSG:27700).
  - Northern Ireland (NI) using Irish Grid (EPSG:29903).

## Data structure and extent
- GB: 74 overlapping 100x100 km Classification Scenes used to train/classify 36-band Seasonal Composite Images plus 20m Context Rasters; GB area significantly larger than a single scene.
- NI: A single 43-band Classification Scene per year for the island.
- Total datasets: 42 products (GB and NI across three years).
- Pixel and dataset specifics:
  - 20m Classified Pixels: 20m resolution, two bands (dominant class, confidence 0–100).
  - Land Parcels: parcel-level attributes aligned to a fixed spatial framework; some attribute field name changes from LCM2015 for production consistency.
  - 25m Rasterised Land Parcels: three bands (mode, conf, purity).
  - 1km rasters: 1km grid summaries (percent cover, percent aggregate cover, dominant, and dominant aggregate).

## Production workflow and data lineage
- Bootstrap Training: automatic training using historic LCM2015 observations to bootstrap classifier training for 2017–2019; future plans to bootstrap from majority signals across multiple years (e.g., 2017–2019).
- Training data: created from UKCEH LCM2015 parcels with high purity (≥99%), derived from stable training signals.
- Classifier: Random Forest (RF) using balanced sampling (10,000 pixels per class per training set) to counter class imbalance.
- Data inputs:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance) per season (winter, spring, summer, autumn) at 20m resolution.
  - Context Rasters (20m) including terrain and proximity features (height, aspect, slope, distance to buildings/roads/seawater/freshwater, foreshore, tidal water, woodland masks).
- Seasonal composites and context rasters are combined into Classification Scenes (GB uses 100x100 km tiles; NI uses a single tile per year).
- Software and tools: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL.

## Data quality, validation, and limitations
- Validation: UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (22,325 points total).
- Reported overall accuracy (producer’s or user’s accuracy summaries vary by class): 
  - LCM2017: ~78.6% overall agreement with validation data.
  - LCM2018: ~79.6% overall agreement.
  - LCM2019: ~79.4% overall.
- Validation caveats:
  - Validation points originate from sources with different class definitions; some conversions are subjective.
  - Validation sample currency relative to each product varies.
  - No manual corrections were applied in this release to enable annual generation; visual checks and formal validation were still performed.
- Classification bias and errors:
  - Some inter-class confusion remains (e.g., spectral similarity across land cover types).
  - The 20m Classified Pixels preserve finer landscape details compared with 25m parcel-based outputs, but parcel-averaged products simplify comparisons over time.
- Gaps and future enhancements:
  - Occasional seasonal gaps in Sentinel-2 data; future exploration of alternative optical sources and Sentinel-1 SAR to fill gaps.
  - TOA data used for this release; SR (surface reflectance) did not improve classification for current classes but may for future enhancements.
  - Potential development of narrower features and improved training data for upland peatland vegetation and other challenging classes.

## Class relationships and documentation
- Table 1 and Appendix 1/2 explain how UKCEH Land Cover Classes relate to UK BAP Broad Habitats, with notes on detection challenges and how some BAP classes are approximated by remote sensing.
- Appendix 3 provides a recommended RGB color mapping for display of the 21 UKCEH Land Cover Classes.
- Appendix 4 includes detailed confusion matrices and accuracy metrics by year/class (full tables for LCM2017, LCM2018, LCM2019).
- Appendix 5 lists the full set of datasets released for each year and region.

## Land Parcel Spatial Framework and temporal comparability
- UKCEH Land Parcel Spatial Framework remains the same geometry as LCM2015, but with re-ordered storage and indices for faster processing.
- gid (parcel identifier) values do not match LCM2015; comparisons should use spatial overlap or the gid-based linkage when possible.
- Minimum mapping unit (MMU) for land parcels is approximately 0.5 hectares; parcels are designed to represent discrete real-world units like fields, parks, and urban areas.
- The framework supports comparison via spatial overlap, though direct gid-to-gid matching across years is not possible.

## Future plans and governance considerations for data leaders
- Annual release cadence is intended (planning for LCM2020 in 2021 and beyond).
- Ongoing evaluation of additional data sources (e.g., Sentinel-1 SAR) to improve coverage during cloudy periods or to enhance classification for difficult habitats.
- Bootstrap Training and RF-based methods are expected to evolve; future maps will likely bootstrap from broader multi-year signals (e.g., majority signals across 2017–2019 or 2018–2020).
- The data ecosystem is designed to enable co-ownership and collaboration through standardized class structures and robust metadata, while acknowledging ongoing changes to class definitions and parcel identifiers.

## Practical notes for data leaders
- Use case readiness: outputs suitable for national-scale land cover monitoring, change detection, and integration with policy or planning workflows; 20m Classified Pixels offer detailed local representation, while parcel-based products provide structured summaries for time-series analysis.
- Data integration: align with LCM2015 history via spatial overlap or gid-based lookups where applicable; be prepared for non-matching parcel identifiers when cross-referencing with older products.
- Metadata and interpretation: consult Appendices 1–4 for class definitions, mapping to BAP habitats, and detailed validation results to inform interpretation and uncertainty assessment.
- Accessibility and planning: plan for annual updates; consider how annual changes influence long-term trend analyses and baseline alignment.