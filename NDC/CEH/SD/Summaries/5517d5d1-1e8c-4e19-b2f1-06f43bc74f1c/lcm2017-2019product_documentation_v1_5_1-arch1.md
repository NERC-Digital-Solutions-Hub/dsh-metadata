# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map set includes 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligned with earlier maps (LCM2015) to facilitate change detection.
- Maps produced automatically (Bootstrap Training + Random Forest) to enable near‑annual UK-wide coverage.
- Pan-UK products available for Great Britain (GB) and Northern Ireland (NI); annual releases planned going forward.

## Content and data structure
- Datasets included per year:
  - 20m Classified Pixels: RF classification results with per-pixel class probability (Band 1 = most likely class, Band 2 = confidence 0–100).
  - Land Parcels: attributes linked to UKCEH Land Parcel Spatial Framework; minor attribute changes since LCM2015.
  - 25m Rasterised Land Parcels: three-band rasters with dominant class, confidence, and purity.
  - 1km Raster products: 
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
- GB and NI versions produced; total of 42 datasets across the three years.
- GB uses 100x100 km Classification Scenes with 46-band data; NI uses a single 43-band Classification Scene per year.
- 20m Classified Pixels preserve fine features (not generalised by parcel framework) to retain narrow or small habitat features.

## Production approach and datasets
- Seasonal Composite Images: Sentinel-2, 4 seasons (winter, spring, summer, autumn); TOA reflectance used (Surface Reflectance not yet providing improvement in this workflow).
- Context Rasters (20m): provide ancillary spatial context to reduce spectral confusion (e.g., height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal water masks; woodland mask).
- Bootstrap Training: automatic training set generated from historic LCM2015 with >99% purity parcels; used to bootstrap training for 2017–2019 maps; future plans include bootstrapping from majority signal across multiple years.
- Random Forest classification: custom RF workflow; balanced sampling with 10,000 samples per class per Classification Scene; integrates Weka, PostGIS, and GDAL.
- UK Land Parcel Spatial Framework: fixed 0.5 ha minimum mappable unit; parcels used to summarise 20m pixel classifications; gid identifiers do not match LCM2015 due to framework changes; framework designed for rapid processing and time-series comparisons.

## Validation and quality
- Validation datasets: GB countryside survey 2019, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points in total).
- Reported overall accuracies at UK scale:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Validation points derived from sources with different purposes; some class translations required; accuracy around 80% is considered impressive for an automatic, annual production system.
  - Full correspondence tables and Appendix 4 provide detailed validation results.

## Key terminology and class mapping
- 21 UKCEH Land Cover Classes map to UK BAP Broad Habitats (HB) with some nuanced relationships and occasional refinements (see Appendix for detailed mappings).
- Generalised UKCEH Aggregate Classes offered for users who do not require thematic detail.
- Appendix 1–2 provide extended notes on individual Broad Habitats and their remote-sensing detectability, including caveats for upland peatland, bracken, and coastal habitats.

## Differences from prior products and notable changes
- No manual accuracy corrections applied in this cycle (fully automatic classification).
- Land Parcel Framework: gid values do not match LCM2015; parcel structure retained for consistency in time-series, but direct parcel-identifier comparisons with LCM2015 are not possible.
- Datasets updated to include 20m Classified Pixels (new in this release) with per-pixel probabilities and enhanced 25m Rasterised Parcel outputs.
- Minor dataset attribute changes (Table 5) to align with production software conventions; some historical descriptions superseded by more streamlined attributes.

## Practical usage and caveats for analysts
- 20m Classified Pixels provide richer detail; 25m and 1km products offer coarser summaries suitable for broad-scale analyses.
- Per-pixel probability (Band 2 in 20m) helps quantify classification confidence, supporting uncertainty-aware analyses.
- Automatic maps are intended for change detection and trend analysis; expect some inter-year variability due to random forest bootstrap and seasonality.
- Validation reflects UK-wide accuracy; local or regional accuracy may differ, particularly for spectrally similar or small patches.
- Users needing exact LCM2015 comparisons should rely on gid-based matching, noting gid differences; cross-year parcel comparisons should be done via spatial overlap rather than parcel IDs.

## Appendices and dataset details
- Appendix 1–2: UKCEH Land Cover Classes and BAP Broad Habitat definitions; detailed notes on class derivations and detection considerations.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Full validation results and confusion matrices for LCM2017, LCM2018, LCM2019 (including producer's and user's accuracies per class).
- Appendix 5: Full list of datasets and their GB/NI scope across LCM2017, LCM2018, and LCM2019 (including dataset names and storage metadata).