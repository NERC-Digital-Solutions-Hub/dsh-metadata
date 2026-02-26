# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and Scope
- Presents three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each map delivers a suite of geospatial data describing land cover across the UK, aligned to 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
- Aims to enable rapid production, improved consistency over time, and informed decision-making in land cover monitoring and environmental policy.

## Production Overview and Rationale
- Maps produced automatically using Bootstrap Training combined with a Random Forest classifier to achieve annual outputs without manual corrections.
- Seasonal information derived from Sentinel-2 Seasonal Composite Images (TOA reflectance), aggregated with 20 m Context Rasters to form Classification Scenes.
- Visual checks and formal validation indicate product quality is comparable to the previous LCM2015, with an emphasis on minimizing human intervention to maintain annual timeliness.
- Visual and statistical validation performed to assess accuracy and reliability, with ongoing plans to refine methods.

## Data Structure and Classes
- 21 UKCEH Land Cover Classes, mapped to UK BAP Broad Habitats; relations and derivations documented in Appendix material.
- Product suite includes 42 datasets in total (GB and NI, for each year): 
  - 20 m Classified Pixels (new addition; per-pixel classification with confidence score)
  - Land Parcels (parcel-level attributes derived from 20 m data)
  - 25 m Rasterised Land Parcels (three-band raster: dominant class, confidence, and purity)
  - 1 km Raster Datasets:
    - 1 km Percent Cover (21 bands)
    - 1 km Percent Aggregate Cover (10 bands)
    - 1 km Dominant Cover (single band)
    - 1 km Dominant Aggregate Cover (single band)
- Classification Scenes: GB uses 100 x 100 km tiles to create 74 overlapping Scenes (46-band GB Scenes per tile, including spectral and context data); NI uses a single 43-band Scene per year for the landmass.
- Land Parcel Spatial Framework: preserved general structure from LCM2015 with minor reorganisations for speed; gid identifies parcels, but new maps use different gid values; parcels have a minimum area of ~0.5 ha (MMU) to represent discrete units (fields, parks, etc.).

## Data Production Details
- Bootstrap Training: leverages historic LCM observations (LCM2015) with high purity (>99%) to bootstrap training data; aims to capture majority signal across time and enable successive updates (plans for 2020–2021 to use multi-year majority signals).
- Random Forest Classification: balanced sampling (10,000 samples per class) from bootstrap data; software integrates Weka with PostGIS and GDAL; designed to avoid bias toward more common classes.
- Seasonal Composite Imagery: Sentinel-2 TOA reflectance from four seasons (winter, spring, summer, autumn); cloud gaps exist but spectral rehabilitation relies on multi-season data; future work may incorporate alternative optical sources or SAR (Sentinel-1) to fill gaps.
- Context Rasters: 20 m layers providing terrain, proximity to buildings/roads/coast/freshwater, foreshore and tidal masks, etc., to reduce spectral confusion.
- Classification Scenes: GB: 74 overlapping tiles produce extensive coverage; NI: single annual scene per year due to smaller extent.

## Data Products and Metadata
- 20 m Classified Pixels: 2-band, 8-bit rasters; band 1 = most likely class, band 2 = confidence (0–100) for the class; preserves fine-scale features below 0.5 ha MMU.
- Land Parcels: parcel-level attributes derived from 20 m data; key fields include gid, hist (histogram of class counts in parcel), mode (dominant class), purity (modal proportion), conf (mean class membership probability), stdev, and n (number of pixels intersecting parcel). Note: some attribute names differ from LCM2015 for production consistency.
- 25 m Rasterised Land Parcels: three bands (mode, conf, purity) derived from Land Parcels; designed to compress parcel data while preserving per-parcel confidence and dominance.
- 1 km Datasets:
  - 1 km Percent Cover: 21-band raster (per-class percent cover per 1 km grid)
  - 1 km Percent Aggregate Cover: 10-band raster (per-aggregate class)
  - 1 km Dominant Cover: single-band raster (dominant class per 1 km grid)
  - 1 km Dominant Aggregate Cover: single-band raster (dominant aggregate class)
- Geographic Extents: GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (EPSG: 29903).
- Dataset counts: total of 42 datasets (per year and per geography).

## Visuals and Examples
- Figures and tables illustrate:
  - Dataset ancestry (20 m classified pixels → land parcels → 25 m raster parcels → 1 km rasters)
  - GB classification scenes vs. NI single-scene approach
  - Generalisation effects from 20 m vs. 1 km products
  - RGB color specifications for displaying the 21 UKCEH Land Cover Classes

## Validation and Accuracy
- UK-scale validation uses countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points (n ≈ 22,325).
- Reported overall accuracy (producer's and user’s) by year:
  - LCM2017: ~78.6% overall accuracy
  - LCM2018: ~79.6% overall accuracy
  - LCM2019: ~79.4% overall accuracy
- Caveats: validation sample sources have differing class definitions; conversions to UKCEH classes introduce subjectivity; currency of validation data varies by product year. Nevertheless, ~80% correspondence for the 21-class automatic maps is considered robust and usable, with potential for improvement as methods mature.
- Appendix 4 provides detailed per-class confusion matrices and accuracy metrics.

## Accessibility, Governance, and Future plans
- Emphasis on openness and the ability to share underlying data with governance structures (as applicable to monitoring frameworks).
- Ongoing evolution of Bootstrap Training strategies and expansion of satellite data inputs; plans to increase the frequency and resolution of future LCM products (e.g., potential refinements to handle gaps, explore additional data sources, and refine training datasets).
- Appendix material (Appendix 1–5) documents class derivations, BAP relationships, colour mapping, validation tables, and a full dataset list for LCM2017–LCM2019.

## Appendices and Supplemental Resources
- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats (definitions, detections, and caveats).
- Appendix 3: RGB color recipes for displaying each UKCEH Land Cover Class.
- Appendix 4: Full validation statistics and confusion matrices by year and class.
- Appendix 5: Full list of datasets per year and geography (GB and NI) with dataset names and storage details.
- References: foundational sources for methods (Random Forest, bootstrap training, remote sensing classifications) and habitat frameworks.