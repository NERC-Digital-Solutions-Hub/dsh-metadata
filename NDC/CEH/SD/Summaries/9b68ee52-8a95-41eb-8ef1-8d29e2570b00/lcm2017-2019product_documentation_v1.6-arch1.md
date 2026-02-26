# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

## Overview
- Release of three national UKCEH land cover maps: LCM2017, LCM2018 and LCM2019, each mapping 21 UKCEH Land Cover Classes based on Biodiversity Action Plan Broad Habitats.
- Maps produced automatically using Bootstrap Training plus a Random Forest classifier; seasonal Sentinel-2 composites and contextual raster layers form the Classification Scenes.
- Aims to enable rapid UK-wide mapping with annual updates; no manual accuracy corrections were applied this cycle, though visual checks and formal validation were performed.
- Validation at UK scale indicates high-but-improving quality compared with the predecessor (LCM2015), with around 78–80% overall accuracy.

## Data inputs and production approach
- Bootstrap Training: automatic generation of training data from historic maps (LCM2015) using parcels with purity ≥ 99%; creates balanced training samples across 21 classes.
- Random Forest classification: bespoke software (integrating Weka, PostGIS and GDAL) trained on 10,000 samples per class; outputs 20m Classified Pixels.
- Temporal and spectral inputs:
  - Seasonal Composite Images: Sentinel-2 median TOA reflectance per season (winter, spring, summer, autumn) at 20m, derived via Google Earth Engine.
  - Context Rasters: 20m context layers (terrain, urban proximity, roads, coast, freshwater, etc.) to reduce spectral confusion.
- Classification Scenes and tiles:
  - Great Britain: overlapping 100x100 km tiles producing 46-band Classification Scenes; 74 overlapping GB scenes classified; visual checks determine final precedence in overlaps.
  - Northern Ireland: single 43-band Classification Scene per year.

## Data products and dataset structure
- 20m Classified Pixels (new): 2-band, 8-bit rasters per year; band 1 = most likely UKCEH Land Cover Class; band 2 = membership probability (0–100) for confidence.
  - Preserves fine landscape details (no initial generalisation by parcels).
- Land Parcels: attributes derived from intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha). Key attributes include:
  - gid, _hist (pixel frequency per class), _mode (dominant class), _purity (percent modal class), _conf (mean class membership probability), _stdev, _n (npix).
  - Note: gid values differ from LCM2015; direct temporal parcel-ID matching across years is not possible; use gid for cross-year parcel comparisons.
- 25m Rasterised Land Parcels: rasterised 1-band to 3-band product (dominant class, confidence, purity) derived from Land Parcels.
- 1km Raster Datasets (summary and aggregation):
  - 1km Percent Cover: 21-band raster showing percent cover per UKCEH Land Cover Class per 1km cell.
  - 1km Percent Aggregate Cover: 10-band raster for 10 aggregate classes.
  - 1km Dominant Cover: single-band raster of the dominant Land Cover Class per 1km cell.
  - 1km Dominant Aggregate Cover: dominant aggregate class per 1km cell.
- Coordinate systems and extents:
  - Great Britain: British National Grid (EPSG:27700); Northern Ireland: Irish Grid (EPSG:29903).
  - Land Parcel data and rasters provided for GB and NI with accompanying extent details (meters).

## Classification workflow and data framework
- UK Land Parcel Spatial Framework: maintains parcel-based structure to represent discrete land units (~0.5 ha MMU); designed to reduce noise and support change detection.
- Bootstrap Training concept: uses historic map signal to bootstrap new classifications; the primary signal is preserved across years, enabling rapid updates.
- Describes relationship between 21 UKCEH Land Cover Classes and UK BAP Broad Habitats; explains limitations in mapping exact BAP Broad Habitats from space and the need to treat the classes as a consistent, repeatable proxy for change detection.
- Appendices provide mapping definitions, class relationships, and practical guidance for using the data (including color recipes and confusion matrices).

## Validation and accuracy
- Validation dataset: GB countryside survey 2019, National Forest Inventory, IACS data, and bespoke LCM validation points (22,325 points in total).
- Overall accuracy (UK-scale validation):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation results indicate substantial alignment with reference data, though authors caution that validation samples come from different purposes and class definitions, and conversions to UKCEH classes introduce some subjectivity.
- Confusion and accuracy vary by class (producer’s and user’s accuracy reported per class in Appendix 5); around 80% correspondence is achieved across the 21-class automatically produced maps.

## Key considerations, limitations and guidance
- BAP Broad Habitats vs UKCEH Land Cover Classes: 21-class products are designed for consistency and change detection rather than exact field-based habitat delineation; some ambiguity remains in translating BAP categories to remote-sensing classes.
- MMU and detectability: minimum mappable unit ~0.5 ha; many patchy or narrow features may be underestimated or not captured in some years.
- Spectral and contextual challenges: some land-cover types share spectral signals, requiring Context Rasters (e.g., slope and distance-to-features) to improve separation; salts, brackish water, and coastal mosaics may incur commission or confusion errors.
- Temporal and data limitations: class signals rely on seasonal spectral information; cloud gaps are handled, but future work may integrate alternative data sources (e.g., Sentinel-1 SAR) or surface reflectance (SR) in place of TOA where beneficial.
- Parcel identifiers: cross-year comparisons across LCM2017–2019 use gid, but gid values differ from LCM2015; direct 2015↔2019 parcel-ID matching is not supported.

## Future directions and plans
- Aims to release a new LCM annually; plans to refine Bootstrap Training in future editions (e.g., using multi-year majority signals and possibly expanding training data sources).
- Continued evaluation of input data choices (e.g., expanding spectral/temporal inputs, potential use of SAR, improved gap-filling strategies) to enhance classification stability and accuracy.

## References and further information
- Appendices include detailed class definitions (BAP Broad Habitats), dataset metadata, confusion matrices, and recommended display color schemes for the land cover classes.
- Key methodological references include work on Random Forests, Bootstrap Training concepts, and prior UKCEH LCM production reports.