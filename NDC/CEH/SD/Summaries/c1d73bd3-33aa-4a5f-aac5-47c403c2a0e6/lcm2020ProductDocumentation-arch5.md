The UKCEH Land Cover Map for 2020

## Purpose and scope
- User guide for the UKCEH Land Cover Map 2020 (LCM2020), the eighth UKCEH map, consisting of six geospatial datasets for Great Britain (GB) and Northern Ireland (NI).
- Outputs include three GB/NI datasets: 10m Classified Pixel dataset (pixel-level classification with a confidence band), 10m Land Parcel dataset (parcels with attributes), and 25m Rasterised Land Parcel dataset (per-parcel rasters with three bands).
- The product uses automatic classification of Classification Scenes (Sentinel-2 Seasonal Composite Images plus 10 Context Rasters) via Bootstrap Training and a Random Forest classifier.
- Annual production aims to maximize temporal consistency, enable change detection, and distinguish real change from random errors as time-series matures.
- Overall validation indicates just over 79% accuracy at full thematic detail (LCM2020).

## Data architecture and contents
- Land cover classes: 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats terminology, with careful cross-walk to BAP Broad Habitats and distinctions described in appendices.
- Datasets (Appendix 5 overview):
  - 10m Classified Raster Product – GB
  - Land Parcel Product – GB
  - 25m Rasterized Land Parcel Product – GB
  - 10m Classified Raster Product – NI
  - Land Parcel Product – NI
  - 25m Rasterized Land Parcel Product – NI
- Classification outputs:
  - 10m Classified Pixels: two bands per pixel — band 1 = most likely UKCEH Land Cover Class; band 2 = probability/confidence for that classification. These pixels are not generalized by the UKCEH Land Parcel Spatial Framework to preserve fine features.
  - Land Parcel datasets: derived by intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework; include parcel-level attributes (e.g., aggregated composition, confidence, purity, and other metadata fields).
  - 25m Rasterised Land Parcels: three-band rasters per parcel (dominant land cover class, mean class probability/confidence, parcel purity).
- Dataset metadata and attributes (illustrative examples from Table 2/3):
  - Parcel attributes include eigen variables such as _hist, _mode, _purity, _conf, _stdev, _agg, and _n; unique identifiers (ogc_fid, gid) and extent metadata.

## Production methods and workflow
- Seasonal information:
  - Seasonal Composite Images derived from Sentinel-2 (four seasons: winter, spring, summer, autumn) using nine bands; some seasonal gaps may exist due to cloud cover, but the classifier tolerates partial data.
- Context data:
  - 10m Context Rasters for GB include terrain (Height, Aspect, Slope) and proximity/mask layers (distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland mask).
  - NI context rasters include Height, Aspect, Slope, urban mask, and distance layers to coast, freshwater, and roads.
- Classification Scenes:
  - GB used 100x100 km tile classification scenes, overlapping 74 scenes, each trained/classified independently; a manual precedence rule resolves overlaps when necessary.
  - NI used a single 100x100 km tile (minimum bounding rectangle) due to smaller area.
- Bootstrap Training:
  - Fully automatic training using historical LCM data (LCM2017–2019) filtered to high-purity parcels (>99% across three years); results in large training sets (GB: ~941k, NI: ~214k objects).
  - The bootstrap approach leverages wall-to-wall historic maps to generate abundant training data, enabling classifier learning without fresh field data.
- Random Forest classification:
  - Balanced sampling: 10,000 pixels per class per training bag to train the RF classifier.
  - The process uses bespoke UKCEH software integrating Weka with PostGIS and GDAL.
- Validation:
  - Validation against GB countryside survey (2019–2020), National Forest Inventory, IACS data, and bespoke validation points (34,715 points total) aligned with Land Parcel datasets.
  - Reported overall accuracy: ~79.2% (the Appendix 4 validation summary provides detailed confusion matrices and class-wise producer/user accuracies).

## Land Parcel Spatial Framework and data governance
- UK Land Parcel Spatial Framework:
  - Designed to generalize national cartography into discrete land parcels (~0.5 ha MMU) for stable change detection; used to derive Land Parcel datasets from 10m Classified Pixels.
  - Some identifiers (gid) changed relative to LCM2015, which may affect direct parcel-based comparisons across editions.
- Data governance considerations:
  - The framework enables consistent change detection and a fixed structure for time-series analysis, while preserving detailed 10m spatial patterns for specialist use.
  - The 10m Classified Pixels are not integrated with the Land Parcel Spatial Framework in order to maintain high-detail features, with the trade-off that cross-edition parcel-based comparisons require parcel ID consistency.

## Descriptions of limitations and caveats
- Incomplete user-needs picture: the product targets specialist users who understand the implications of pixel-level detail and parcel-based aggregation.
- Data timing and standardization:
  - Annual production prioritizes timeliness over manual correction; significant manual corrections used in earlier maps are not performed to enable annual updates.
  Real change vs random error is more reliably distinguished over a time series as the dataset matures.
- Class confusion and limitations:
  - Notable interclass confusion in upland vegetation (peatlands, bogs, Heather/Heather Grassland, fen/marsh/swamp).
  - Saltwater vs Freshwater confusion near coasts, and occasional misclassification of coastal or tide-affected areas.
  - Some classes require careful interpretation due to spectral similarity (e.g., arable vs improved grassland, neutral grassland).
- Data structure caveat:
  - The Land Parcel identifiers may not be directly comparable to LCM2015 identifiers due to re-ordering and storage changes.

## Practical guidance for data stewards and users
- Use case alignment:
  - For high-detail landscape features and fine patches below 0.5 ha MMU, prefer the 10m Classified Pixels (specialist use) rather than parcel-aggregated outputs.
  - For stable time-series analysis and change detection, rely on the Land Parcel Spatial Framework outputs and parcel-based metrics.
- Interpretation and crosswalks:
  - Be aware of differences between UKCEH Land Cover Classes and UK BAP Broad Habitats; consult Appendices 1–2 for crosswalks and definitions.
  - Use provided color recipes and correspondence matrices to visualize and interpret class relationships accurately.
- Validation and quality control:
  - Refer to Appendix 4 for class-wise accuracy and confusion matrices when assessing suitability for specific analyses.
  - Consider the limitations noted in upland peat and coastal classes when interpreting results in those regions.

## Appendices and key references
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats; detailed class definitions and crosswalk guidance.
- Appendix 3: Recommended color recipes for display of UKCEH Land Cover Classes.
- Appendix 4: Full validation matrices, including producer’s and user’s accuracy per class.
- Appendix 5: Full list of LCM2020 datasets and their official names.
- References: Key methodological sources on Random Forests, Bootstrap Training, and prior LCM work.

## Summary of datasets (Appendix 5)
- UKCEH LCM2020, Dataset: 10m Classified Raster Product (GB)
- UKCEH LCM2020, Dataset: Land Parcel Product (GB)
- UKCEH LCM2020, Dataset: 25m Rasterized Land Parcel Product (GB)
- UKCEH LCM2020, Dataset: 10m Classified Raster Product (NI)
- UKCEH LCM2020, Dataset: Land Parcel Product (NI)
- UKCEH LCM2020, Dataset: 25m Rasterized Land Parcel Product (NI)