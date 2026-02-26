# The UKCEH Land Cover Map for 2022

## Overview
- UKCEH Land Cover Map 2022 (LCM2022) is the tenth UK land cover map, produced annually to monitor state and change of the UK countryside.
- Built from classification Scenes combining Sentinel-2 Seasonal Composite Images with Context Rasters, using Bootstrap Training and a Random Forest classifier.
- Contains 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats), mapped across Great Britain and Northern Ireland.
- Emphasises temporal consistency, change detection, and facilitating monitoring for environmental objectives.

## Product Suite (datasets and outputs)
- Seven datasets total, plus a 1 km summary raster product (GB and NI):
  - 10 m Classified Pixel datasets (GB and NI): multi-band rasters with two bands per pixel — the most likely UKCEH Land Cover Class (integer) and the associated class probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised representation of land parcels with three bands capturing dominant class (mode), confidence, and purity.
  - Land Parcel Datasets (GB and NI): vector land parcel attributes linked to the 10 m pixels via the UKCEH Land Parcel Spatial Framework.
  - 1 km Summary Raster datasets (GB and NI): summary rasters giving dominant class and percentage cover per 1 km pixel (both 21-class and 10-class aggregations).
  - Seasonal Composite Images: four-season Sentinel-2 derived composites used for classification.
  - Context Rasters: 10 m layers added to reduce spectral confusion (GB and NI variants).
  - Classification Scenes: GB uses 32 tiles for full GB coverage; NI uses a single Scene for Northern Ireland.
- Dataset references and DOIs are provided for formal citation (see Citations).

## Data Production and Methodology
- Classification approach:
  - Bootstrap Training: automatic generation of training data from historic LCM maps (LCM2019–LCM2021) with >80% probability and consistent class across three years.
  - Random Forest classifier trained on bootstrap samples to assign land cover classes.
  - Training set balanced by sampling 10,000 pixels per class per bag to prevent dominance by common classes.
- Seasonal and spectral information:
  - Seasonal Composite Images built from Sentinel-2 bands across four seasons to provide temporal signals.
  - 10 m Context Rasters (GB) include topography (height, aspect, slope) and proximity masks (buildings, roads, tidal water, freshwater, foreshore, woodland, saltmarsh). NI context rasters include urban mask and proximity layers.
- Classification Scenes and tiling:
  - GB: 32 Classification Scenes (approx. 100 x 100 km tiles) to manage regional phenological variation; some overlaps and region-specific tiling adjustments.
  - NI: single Classification Scene sized to the minimum bounding rectangle of NI land mass.
- UK Land Parcel Spatial Framework:
  - Land parcels are generalized to ~0.5 ha MMU and aligned to a spatial framework; 10 m pixels are then aggregated into parcels for the 25 m products.
  - Note: gid identifiers in the new framework do not match LCM2015 identifiers, affecting exact cross-version parcel comparisons.
- Validation and accuracy:
  - Formal validation used 33,107 reference points across all 21 classes.
  - Overall thematic accuracy reported at 86.1%.

## Key Outputs and Data Structure Details
- 10 m Classified Pixels (GB and NI):
  - Two bands: class identifier (UKCEH Land Cover Class) and confidence/probability per pixel.
  - No generalisation by the Land Parcel Spatial Framework for the 10 m pixels to preserve fine landscape detail (e.g., small patches and narrow features).
- Land Parcel Datasets:
  - Land Parcel Product (vector) and associated 25 m Rasterised Land Parcel Product (GB and NI).
  - Raster products include per-parcel mode, conf, and purity attributes; parcel attributes (gid, hist, mode, conf, purity, etc.) documented in Table 3 of the source.
- 25 m Rasterised Land Parcel Datasets:
  - Three-band rasters: dominant land cover class (mode), mean confidence (conf), and pixel purity (purity) per parcel.
- 1 km Summary Rasters:
  - Dominant class per 1 km cell (21-class and 10-class aggregations) and percentage cover per class (21 and 10 classes, respectively).
  - Caution: percentage sums may not exactly equal 100 due to rounding; coastal areas may sum to less than 100 due to mapping extent.
- Seasonal Composite Images and Context Rasters:
  - Seasonal composites derived from Sentinel-2 data (4 seasons; 10 bands used).
  - Context rasters provide additional spatial context to improve discrimination among spectrally similar classes.
- Coordinate Systems:
  - Great Britain: British National Grid, EPSG 27700.
  - Northern Ireland: Irish Grid (TM75), EPSG 29903.
- Relationship to UK BAP Broad Habitats:
  - 21 UKCEH Land Cover Classes are related to UK BAP Broad Habitats; differences exist and are noted in Appendices.
  - Ambiguities between class definitions are documented with emphasis on context rasters and training data.

## Validation, Accuracy, and Known Issues
- Validation:
  - 33,107 validation points spanning all 21 classes; overall accuracy 86.1%.
- Known issues:
  - A small number of polygons missing from vector Land Parcel products; corresponding nodata areas in 25 m raster land parcels; negligible impact on 1 km summary rasters.
  - 10 m classified pixel datasets are unaffected by this issue.
  - Methodological changes year-on-year mean some differences can reflect updates in production techniques, not only real change.

## Practical Considerations for Analysts
- Monitoring and change detection:
  - Annual production supports distinguishing persistent change from random classification errors (random errors tend to flicker year to year).
  - The 1 km and parcel-based outputs enable aggregation, trend analysis, and integration with other environmental data.
- Data integration and reuse:
  - Bootstrap Training enables rapid production without fresh field training data; however, occasional limitations exist (e.g., crop rotations affecting arable and improved grassland training data).
  - Training data for some classes may rely on external datasets (e.g., UKCEH Land Cover plus: Crops for 2022) in certain rotations.
- Compatibility and comparisons:
  - GID changes between LCM2015 and LCM2022 mean cross-version comparison by parcel IDs may require spatial overlap methods rather than direct ID matching.
  - The product suite is designed to maximize temporal comparability and support comprehensive environmental monitoring over time.

## Access, Citations, and References
- Each LCM2022 dataset has a DOI and citation (Table 5 in the source). Key references include:
  - Marston et al. (2024a–g) for the individual dataset publications and production methods.
  - Marston et al. (2023) for overview of the LCM2021 methods.
- Disclaimer:
  - As methods continue to evolve, there may be slight differences in outputs between consecutive maps beyond real environmental change.
- Appendices provide:
  - Detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats (Appendices 1–2).
  - Full list of LCM2022 datasets and their metadata (Appendix 3).
  - Correspondence matrices for validation (Appendix 4).
  - Colour recipes for visualizing land cover classes (Appendices 5–6).