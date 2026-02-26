# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope: User guide accompanying the release of three UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019). Describes content, production decisions, validation, terminology, and future plans to help users apply UKCEH LCM data in current and future work.
- Classification framework: 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; designed to support land-cover change detection and monitoring over time.

## Data products and structure

- Multi-year product suite (one year per map) with parallel GB and Northern Ireland versions.
- Core datasets (one year per product):
  - 20m Classified Pixels (new in this release): RF class membership per 20m pixel with per-pixel confidence.
  - Land Parcels: vector-based parcels summarising 20m pixels within a defined spatial framework.
  - 25m Rasterised Land Parcels: 3-band raster (dominant class, confidence, and purity) derived from Land Parcels.
  - 1km Dominant Cover: single-band raster of dominant class per 1km grid.
  - 1km Percent Cover: 21-band raster giving percentage cover per class per 1km.
  - 1km Percent Aggregate Cover: 10-band raster for aggregate classes per 1km.
  - 1km Dominant Aggregate Cover: 1-band raster for dominant aggregate class per 1km.
- Geographic coverage and formats:
  - Great Britain (GB) products in British National Grid (EPSG:27700).
  - Northern Ireland (NI) products in Irish Grid (EPSG:29903).
  - 42 total datasets across years and regions.
- Ancestry and data flow:
  - All products build on the 20m Classified Pixels foundation, interlinked with the UKCEH Land Parcel Spatial Framework.

## Production workflow and methodology

- Bootstrap Training: Automatic, self-starting training using historical maps (primarily LCM2015 to bootstrap LCM2017–2019) to derive training data without fresh field campaigns. Majoritiy signal across time leveraged to create training samples.
- Random Forest classification: Supervised RF classifier trained on bootstrapped samples; balanced sampling ensures rare classes are well represented.
- Seasonal and spectral inputs:
  - Seasonal Composite Images: Sentinel-2 TOA reflectance mosaics by season (winter, spring, summer, autumn) produced via Google Earth Engine.
  - Context Rasters (20m): Include terrain (height, aspect, slope) and proximity masks (distance to buildings, roads, sea, freshwater, etc.) to reduce spectral confusion.
  - No manual corrections were applied in this release to enable annual production; visual checks and formal validation were still conducted.
- Classification Scenes and tiling:
  - GB: 100x100 km tiles used to generate 36-band Seasonal Composite Images; 46-band Classification Scenes created from 36 spectral plus 10 context layers; 74 overlapping scenes classified independently and reconciled by visual inspection.
  - NI: Single 43-band (36 spectral + 7 context) Classification Scene per year, tailored to its geography.
- UKCEH Land Parcel Spatial Framework:
  - Maintains 0.5 ha minimum parcel size (MMU); parcels generalised from national cartography to represent discrete real-world units.
  - gid identifiers are year-to-year non-matching with LCM2015, enabling trunk-level change tracking via spatial overlap (gid-based comparisons supported for 2017–2019).
- Dataset lineage and metadata:
  - 20m Classified Pixels contain class and per-pixel confidence; 25m Land Parcels retain parcel-level hist, mode, purity, conf, stdev, etc.
  - 1km rasters aggregate 25m parcels into yearly grid summaries.

## Input data, context, and interpretation

- Seasonal inputs and spectral bands:
  - Sentinel-2 bands and resolutions listed; TOA reflectance used (not surface reflectance) due to availability and marginal improvements observed in this context.
  - Context rasters aid disambiguation for spectrally similar classes (e.g., coastal, urban, terrain-related features).
- Data governance and metadata:
  - 21 classes are tied to UKCEH/Land Cover Class definitions and each year’s outputs are designed for consistent change detection.
  - Appended material describes the relationship to UK BAP Broad Habitats and notes mapping nuances and detection limitations for some upland and coastal habitats.
- Validation approach:
  - UK-scale validation against multiple sources (GB countryside survey 2019, National Forest Inventory, IACS, bespoke validation points).
  - Reported accuracies (approximate):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data were the same across products and not a perfect ground-truth match to class definitions; results should be interpreted as relative indicators of performance.

## Outputs, interpretation, and usage notes

- 20m Classified Pixels:
  - Provides the most detailed representation, preserving fine features (e.g., narrow patches) that are not present in parcel-based products.
  - Band 1: most likely UKCEH Land Cover Class; Band 2: membership probability (0–100).
- Land Parcels:
  - Parcel-level attributes include histogram of class counts, modal class, parcel purity, and confidence metrics.
  - Some attribute names differ from LCM2015 to align with production software conventions.
- 25m Rasterised Land Parcels:
  - 3-band raster: Band 1 = modal class; Band 2 = mean confidence; Band 3 = parcel purity (as a percentage).
- 1km rasters (all year products):
  - 1km Percent Cover (21 bands): class-wise percentage cover per 1km.
  - 1km Percent Aggregate Cover (10 bands): broader category covers per 1km.
  - 1km Dominant Cover: dominant class per 1km.
  - 1km Dominant Aggregate Cover: dominant aggregate class per 1km.
- Visual and analytical guidance:
  - Appendix 3 provides recommended RGB color mappings for display of UKCEH Land Cover Classes.
  - Figures and tables illustrate how 20m, 25m, and 1km products relate and generalisation effects when moving to coarser grids.

## Validation, limitations, and future plans

- Validation caveats:
  - Validation uses a single, currency-limited set of points; some classes show higher confusion (e.g., certain upland, wetland, and coastal classes).
  - Class definitions are historical (BAP-based) but adapted for satellite detection; perfect spectral separation is not always possible.
- Limitations and challenges:
  - Data gaps and cloud cover gaps are mitigated with multi-season data and robust RF training, but some seasons may have gaps at specific locations.
  - The Land Parcel Spatial Framework is fixed to LCM2015’s geometry; gid changes mean direct parcel-to-parcel comparison with older maps may be limited.
- Future directions:
  - Annual LCM2020 planned (2021 release) with bootstrap from majority signal across 2017–2019; similar approach planned for 2021 (2018–2020 majority).
  - Exploration of filling seasonal gaps with alternative optical sources and multitemporal Sentinel-1 SAR data.
  - Ongoing evaluation of higher spatial resolution or alternative parcel frameworks to improve change detection and cross-map comparability.
  - Continuation of automated production to enable regular, coast-to-coast UK-wide updates.

## Practical takeaways for monitoring and policy use

- The LCM2017–2019 suite provides a comprehensive, automated, multi-resolution set of land-cover products suitable for monitoring change, reporting, and decision-making at national to local scales.
- For detailed habitat and land-cover analyses, use the 20m Classified Pixels and 25m Land Parcels; for broad-scale trend analyses or dashboard-style reporting, the 1km rasters (Percent Cover and Dominant/Aggregate layers) are efficient.
- Be mindful of data governance considerations when integrating with other datasets (e.g., changes in gid identifiers and class definitions over time) and the metadata quality of inputs.
- Expect ongoing improvements in accuracy and data richness as methods mature and additional data sources are integrated.