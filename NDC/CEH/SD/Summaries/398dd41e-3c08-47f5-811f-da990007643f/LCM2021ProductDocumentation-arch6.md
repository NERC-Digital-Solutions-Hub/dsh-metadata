# The UKCEH Land Cover Map for 2021

- LCM2021 is the ninth UK land cover map produced by UKCEH, designed to support monitoring of the UK countryside and related environmental objectives.
- Product suite consists of six geospatial datasets (three for Great Britain and Northern Ireland each): 10 m Classified Pixel dataset, Land Parcel dataset, and 25 m Rasterised Land Parcel dataset. In addition, 1 km-derived products summarize these data at a coarser scale.
- Annual production aims to improve temporal consistency and change detection, with formal validation indicating overall accuracy of 82.6%.

## Data structure and datasets

- 10 m Classified Pixel datasets (GB and NI)
  - Generated from classified Classification Scenes; each pixel has:
    - Band 1: most likely UKCEH Land Cover Class
    - Band 2: probability/confidence for that classification
  - Not generalized with the UKCEH Land Parcel Spatial Framework to preserve fine landscape features; intended for specialist users.
- Land Parcel datasets (GB and NI)
  - Result from intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework
  - Land Parcel attributes (Table 3): gid, _hist, _mode, _purity, _conf, _stdev, _agg, _n
  - Parcels have a minimum area of ~0.5 ha (MMU)
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterized version of parcels with 3 bands:
    - Band 1: per-parcel dominant land cover (_mode)
    - Band 2: per-parcel mean confidence (_conf)
    - Band 3: per-parcel pixel purity (_purity)
- 1 km raster products
  - Summary products derived from 25 m data:
    - Dominant cover (1-band) for classes and aggregates
    - Percentage cover (21-band for classes; 10-band for aggregates)
  - Rounding means some totals may not sum exactly to 100; coastal areas may be under 100 due to mapping resolution
- Seasonal Composite Images
  - Sentinel-2 based seasonal composites (four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at ~10 m resolution
  - Context bands (see Context Rasters) used to improve classification
  - Gaps due to cloud are handled; classifier tolerates partial spectral information
- Context Rasters
  - 10 m context layers used to resolve spectral confusion (GB and NI have different lists)
  - Examples: height, aspect, slope, distance to buildings/roads/coast/freshwater, foreshore mask, tidal water, woodland mask (GB); plus urban mask and other distance layers (NI)
- Classification Scenes and tile approach
  - GB: 32 Classification Scenes covering the GB land surface
  - NI: a single Classification Scene (~49-band) using a 40-band Sentinel-2 Seasonal Composite plus NI context rasters
- UKCEH Land Parcel Spatial Framework
  - Framework for discretizing land into ~0.5 ha parcels
  - Used to organize pixels into parcels and support change detection
  - Identifiers (gid) do not exactly match LCM2015 parcel IDs for cross-year comparison

## Production methods

- Bootstrap Training
  - Automated training data generated from historic LCMs (LCM2018, LCM2019, LCM2020)
  - Training parcels filtered to >80% purity and consistent class across years
  - Enables near-wall-to-wall training data without new field collection
- Random Forest classification
  - RF classifier trained on Bootstrap Training data
  - For each Classification Scene, 10,000 samples per bag with replacement to balance class representation
  - Classifier output: 10 m Classified Pixel product (class ID + confidence)
  - Software stack: bespoke UKCEH tooling integrating Weka, PostGIS, and GDAL (open source)

## Validation and accuracy

- Validation dataset: 35,182 points spanning all 21 UKCEH Land Cover Classes
- Overall accuracy: 82.6% (95% CI: 82.19%–82.99%)
- Appendix 4 (confusion matrices) provides per-class producer’s and user’s accuracies and detailed misclassifications

## Outputs: interpretation and use

- 10 m Classified Pixel dataset
  - High-detail, pixel-level classifications with a confidence metric
  - Suitable for specialist analyses where fine spatial detail matters
- 25 m Rasterised Land Parcel dataset
  - Parcel-based aggregation with per-parcel mode (dominant class), conf, and purity
  - Facilitates change detection and cross-year comparison using fixed spatial units
- Land Parcel Dataset attributes
  - gid, _hist (history of class occurrences within parcel), _mode, _purity, _conf, _stdev, _agg (aggregate class), _n (pixel count)
- 1 km products
  - Simplified, large-scale overview of dominant classes and their percentage cover
  - Useful for broad-scale assessments and integration with other 1 km–scale data
- Display and interpretation
  - Appendix 5 and Appendix 6 provide recommended color recipes (including color-blind friendly options) for displaying UKCEH Land Cover Classes
  - Appendices also clarify relationships to BAP Broad Habitats and note areas of potential spectral confusion

## Data quality, limitations, and considerations

- Patchy data and spectral confusion
  - Some land cover types exhibit spectral similarity (e.g., Saltwater vs Freshwater in tidal areas)
  - Context rasters and seasonal signals help mitigate confusion but misclassifications can persist in complex mosaics
- Temporal and spatial specifics
  - Annual maps help differentiate real change from random noise; changes should persist year-to-year if real
  - Some sections fall below the minimum mapping unit (MMU) and may be generalized or underrepresented
- Cross-year comparability
  - Land Parcel identifiers (gid) may not align with LCM2015 identifiers; cross-year analyses should rely on spatial overlap rather than parcel ID
- BAP Broad Habitat mappings
  - 21 UKCEH Land Cover Classes map to BAP Broad Habitats with some intentional differences; Appendix 1–2 provide guidance on interpretation and potential ambiguities
- Coastal and rural edge effects
  - Near-coast areas can show lower precision in certain classes; coastal classes rely heavily on Context Rasters and classification logic
- Data evolution
  - The team plans continuous improvements; if new methods yield significant gains, methods may be re-applied to improve consistency and accuracy

## Appendices and display guidance

- Appendices cover detailed class descriptions, relationships between UKCEH classes and BAP Broad Habitats, full dataset naming, and comprehensive validation matrices
- Color palettes and color-blind friendly options are provided to support effective visualization and communication of results

- References and methodological notes outline foundational sources for bootstrap training, RF classification, and seasonal/sensor integration approaches