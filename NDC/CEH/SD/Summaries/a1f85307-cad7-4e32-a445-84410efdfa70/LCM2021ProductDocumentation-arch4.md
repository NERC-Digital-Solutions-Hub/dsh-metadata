# The UKCEH Land Cover Map for 2021

- Purpose and scope
  - User guide describing LCM2021 data production, validation and accuracy to help users apply UKCEH LCM data in current and future work.
  - Presents the data structure, methods, quality, and guidance for interpretation and use.

- Data product suite (LCM2021)
  - Six datasets in total, across Great Britain and Northern Ireland (GB and NI):
    - Three geospatial datasets per region:
      - 10 m Classified Pixel dataset (GB and NI)
      - Land Parcel dataset (GB and NI)
      - 25 m Rasterised Land Parcel dataset (GB and NI)
    - Additionally, 1 km raster products summarise the 25 m data (dominant class and percentage cover by class/aggregate class)
  - Coordinate systems:
    - GB: British National Grid, EPSG 27700
    - NI: Irish Grid (TM75), EPSG 29903
  - Pixel resolutions:
    - 10 m (classified pixels)
    - 25 m (rasterised land parcels)
    - 1 km (summary products)

- How the data are produced (methodology)
  - Bootstrap Training and Random Forest (RF) classification
    - Bootstrap Training samples land parcels from historic UKCEH LCM maps (2018–2020) to train the RF classifier.
    - Training samples are balanced across classes to improve learning for rarer classes.
  - Sentinel-2 Seasonal Composite Images and Context Raster layers
    - Seasonal Composites for four seasons derived from Sentinel-2 data (spectral bands listed in Table 4).
    - Ten Context Rasters (GB) and nine contextual masks (NI) added to reduce spectral confusion (e.g., terrain, proximity to features, water masks).
  - Classification Scenes and tiling
    - GB: 32 Classification Scenes using a modified OS 100 x 100 km tile grid; each tile trained and classified independently.
    - NI: single 49-band Classification Scene (40-band Sentinel-2 data plus NI context rasters).
  - Land Parcel Spatial Framework
    - Land parcels derived from generalising national cartography with a minimum area of ~0.5 ha (MMU).
    - 10 m pixels are organised into land parcels to reduce noise and aid change detection; unique parcel identifiers (gid) are not directly compatible with LCM2015.
  - Data processing tools
    - Custom UKCEH pipeline integrating Weka, PostGIS, and GDAL (open source).

- The UKCEH Land Parcel Spatial Framework
  - Land parcels are fixed real-world units (fields, parks, urban areas, etc.), designed to facilitate change detection and analysis over time.
  - MMU and generalisation help minimise fragmentation; parcels typically dominated by a single land cover type.

- Validation and data quality
  - Validation dataset: 35,182 points across all 21 LCM classes, using multiple sources (countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points).
  - Overall accuracy: 82.6% with a 95% confidence interval of 82.19%–82.99%.
  - Class-level notes
    - Some confusion remains between spectrally similar classes (e.g., Saltwater vs Freshwater, various grassland types).
    - The BAP Broad Habitat relationships are provided for interpretive consistency but are not one-to-one with UKCEH Land Cover Classes; notes and caveats are included in Appendices 1 and 2.
  - Validation details and matrices are provided in Appendix 4 (producer’s and user’s accuracies, per-class confusion).

- Datasets in detail
  - 10 m Classified Pixel dataset
    - Output: per-pixel class identifier (UKCEH Land Cover Class) and associated class probability/confidence.
    - Not generalised by the Land Parcel Spatial Framework to preserve fine-scale features (e.g., small patches under MMU).
  - Land Parcel dataset
    - Attributes derived from intersecting 10 m pixels with the Land Parcel Spatial Framework (per parcel).
    - Key fields include: gid, _hist (distribution of class frequencies within parcel), _mode (dominant class), _conf (mean class membership probability), _stdev, _purity, _agg (aggregate class), _n (number of 10 m pixels in parcel).
  - 25 m Rasterised Land Parcel dataset
    - 3-band raster: band 1 = dominant class (_mode), band 2 = mean confidence (_conf), band 3 = purity (_purity).
  - 1 km raster products
    - Dominant class and percentage cover for both UKCEH Land Cover Classes and aggregated classes.
    - Percentage values are integers and may not sum exactly to 100 due to rounding, especially near coastlines.

- Seasonal and contextual data
  - Seasonal Composite Images
    - 4 seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with Sentinel-2 bands and temporal information used for improved discrimination of vegetation types.
    - Occasional cloud gaps are handled by the classifier; gaps do not prevent nationwide coverage.
  - Context rasters
    - GB: 10 context rasters (height, aspect, slope, distance to buildings/roads/coast, distance to freshwater, foreshore and tidal masks, woodland mask).
    - NI: 9 context rasters (height, aspect, slope, urban mask, distances to coast/road/freshwater, foreshore and tidal masks).

- Practical guidance and caveats for use
  - Annual production and change detection
    - LCM2021 is part of an annual series intended to track real change; random, non-persistent errors are expected to flicker over time, aiding differentiation of real change versus noise.
  - Relationship to BAP Broad Habitats
    - UKCEH Land Cover Classes map motor alignments with BAP Broad Habitats, but not perfectly synonymous; Appendices 1–2 provide the detailed mapping and caveats.
  - Cross-version comparability
    - GID changes between LCM2015 and LCM2021 may limit direct parcel-by-parcel temporal comparisons; spatial overlap is still workable, but explicit id-based comparability is not guaranteed.
  - Display and interpretation
    - Color recipes for display are provided (Appendix 5) and include accessibility-friendly versions (Appendix 6) to support data presentation and communication.

- Appendices and additional resources
  - Appendix 1: Notes on UKCEH Land Cover Classes (class-specific interpretation guidance)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (descriptive summaries and relationships)
  - Appendix 3: Full list of datasets for UKCEH LCM2021
  - Appendix 4: Correspondence matrices (class-to-class confusions and accuracies)
  - Appendix 5–6: Recommended color recipes for displaying Land Cover Classes (standard and color-blind friendly)
  - Glossary: Key terms such as Bootstrap Training, Context Raster, Classification Scene, Seasonal Composite Image, UKCEH Land Cover Classes, and UKCEH Land Parcel Spatial Framework

- Relevance for data leadership and strategy
  - End-to-end data lifecycle: from data collection and automated classification to parcel-level attributes and 1 km summaries, enabling scalable monitoring of land cover state and change.
  - Governance and standards: clear documentation of methods, validation, and metadata, with explicit caveats and links to broader habitat classifications.
  - Usability and impact: provisions for user needs through detailed classification explanations, change detection capabilities, and display-ready color schemes to support decision-making and reporting.
  - Continuous improvement: annual production cycle with validated accuracy enabling ongoing assessment of method improvements and comparability over time.