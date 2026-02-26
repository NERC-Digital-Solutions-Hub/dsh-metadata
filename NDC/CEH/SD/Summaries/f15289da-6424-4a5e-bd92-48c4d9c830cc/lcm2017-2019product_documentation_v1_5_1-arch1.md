# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and overview
- A user guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map suite provides a range of geospatial datasets describing land cover across the UK.
- Automatic production approach aims to enable annual UK-wide maps with validated quality similar to the latest predecessor (LCM2015).
- Visual checks and formal validation were performed; no manual corrections were applied in these releases.

## Data content and classification framework
- LCMs describe 21 UKCEH Land Cover Classes (based on BAP Broad Habitats, Jackson 2000) and include a near one-to-one mapping to UKCEH Aggregate Classes (10).
- Terminology bridges UKCEH Land Cover Classes, UK BAP Broad Habitats, and Aggregates; readers are cautioned about differences and consistent naming conventions.
- Tables outline the relationships among Broadleaved/Coniferous woodland, Arable, Various Grassland types, Wetlands (Fen, Marsh, Swamp, Bog), Freshwater, Saltwater, Coastal categories, Built-up areas (Urban and Suburban), and other coastal and upland habitats.
- Appendix 1 and 2 provide detailed notes on class definitions and detection considerations, including limitations for upland peatland and spectral detection challenges.

## Production methodology
- Bootstrap Training: automatic, history-based training using older UKCEH LCMs (not field-collected data) to generate spectral training observations for current classification.
- Training data for 2017–2019 derive from UKCEH LCM2015; majority signal sampling supports robust learning across time.
- Random Forest (RF) classifier applied to 20m Sentinel-2 Seasonal Composite Images (TOA reflectance) plus 20m Context Rasters to create Classification Scenes.
- Classification Scenes: GB produced as overlapping 100x100 km tiles (36-band seasonal composites + 10 context layers = 46 bands per scene), NI produced with a single 43-band scene per year.
- Training balance: 10,000 samples per class per bag, drawn with replacement to balance rare classes.
- Software: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL.

## Dataset structure and content
- Product suite includes multiple raster and vector products (per year and per region):
  - 20m Classified Pixels: new 2-band, 8-bit rasters (class label and confidence 0–100) derived from RF, preserving fine detail, not generalised by parcels.
  - Land Parcels: parcel-level attributes derived from intersecting 20m classified pixels with the UKCEH Land Parcel Spatial Framework; includes history, mode class, Purity, Confidence, Stdev, etc.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) derived by rasterising parcel data; supports a fixed 25m grid.
  - 1km Raster Datasets: 
    - 1km Percent Cover (21-band, 8-bit): percentage cover per class per 1km cell.
    - 1km Percent Aggregate Cover (10-band, 8-bit): percentage cover per Aggregate Class.
    - 1km Dominant Cover (single-band): dominant class per 1km cell.
    - 1km Dominant Aggregate Cover (1-band): dominant aggregate class per 1km cell.
- Dataset extents and coordinate systems:
  - GB: Great Britain – British National Grid (EPSG: 27700).
  - NI: Northern Ireland – Irish Grid (TM75, EPSG: 29903).
- For each year (2017, 2018, 2019), the full set includes GB and NI versions, totaling 42 datasets per year (20m, parcels, 25m, and 1km products across regions).

## Seasonal inputs and classification scenes
- Seasonal Composite Images (Sentinel-2) produced via Google Earth Engine:
  - Four seasons: winter, spring, summer, autumn.
  - Bands 2,3,4,5,6,7,8,11,12 used; TOA reflectance (SR data explored but TOA used due to similar performance during production).
  - Some seasonal data gaps due to cloud; RF classifier can tolerate partial seasonal information.
- Context rasters (20m) used to reduce spectral confusion (terrain, proximity to urban features, coast, roads, etc.).
- Seasonal Classification Scenes:
  - GB: 100x100 km tiles; 74 overlapping scenes classified independently with cross-scene overlap for training balance.
  - NI: a single 43-band classification scene per year.

## UKCEH Land Parcel Spatial Framework
- Fixed framework used to summarise 20m Classified Pixels into land parcels.
- Parcels are ≈0.5 ha minimum size; designed to reflect real-world discrete units (fields, parks, urban blocks, etc.).
- GID identifiers: gid are stable within the current framework but do not match LCM2015 parcel IDs; cross-map comparisons should use gid for 2017–2019 rather than LCM2015 IDs.
- The framework allows users to supply their own parcel structures; future refinement may adjust MMU and support finer resolutions.

## Validation and accuracy
- Validation datasets (GB countryside survey 2019, open National Forest Inventory, IACS, bespoke validation points) totaling 22,325 points.
- Overall accuracy at the national scale:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation points were converted to UKCEH Land Cover Classes; accuracy figures are indicative rather than absolute truths due to potential classification mismatches and data source differences.
- Validation tables (Appendix 4) provide full correspondence details and accuracy metrics by class.

## Practical considerations for analysts
- The data programmatically emphasizes annual updates with a consistent class framework intended for change detection and time-series analyses.
- No manual corrections were applied in these releases; errors are expected to be randomly distributed over space and time.
- Approximately 80% overall correspondence between automatic maps and validation data is considered strong given the automated production approach and harmonised class scheme.
- Users should be aware of gid mismatches when comparing to LCM2015 and plan to use the gid field for cross-year parcel comparisons (not parcel IDs from older products).

## Appendices and supporting information
- Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats, including detection caveats and class-specific considerations.
- Appendix 3: Recommended RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Full validation results and confusion matrices (LCM2017, LCM2018, LCM2019) with per-class producer and user accuracies.
- Appendix 5: Full list of datasets per LCM year (GB and NI products) and dataset naming conventions.

## Future directions and plans
- Ongoing evaluation of satellite inputs (TOA vs SR) and exploration of additional data sources (e.g., Sentinel-1) to improve classification under cloud and other conditions.
- Annual release plan to extend the time series beyond 2019, with evolving Bootstrap Training strategies and potential refinements to the Land Parcel Spatial Framework and MMU.