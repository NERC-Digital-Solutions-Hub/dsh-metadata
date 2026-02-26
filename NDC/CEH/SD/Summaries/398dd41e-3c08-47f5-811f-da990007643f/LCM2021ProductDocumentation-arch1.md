# The UKCEH Land Cover Map for 2021

- Overview
  - UKCEH’s ninth land cover map (LCM2021), produced annually using automated methods to enable rapid updates.
  - Combines topic expertise with machine learning to identify land cover and monitor change.
  - Product suite includes six datasets (three for Great Britain and three for Northern Ireland): 10 m classified pixels, 25 m land parcels, and 25 m rasterised land parcels.
  - Formal validation reports an overall accuracy of 82.6% at full thematic detail.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Pixel-level classifications across 21 UKCEH Land Cover Classes.
    - Band 1: most likely class identifier; Band 2: class membership probability (confidence).
    - Not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine features (e.g., narrow patches).
  - Land Parcel datasets (GB and NI)
    - Created by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework.
    - Parcel attributes include: gid, _hist (class frequencies), _mode (dominant class), _purity, _conf (mean class membership confidence), _stdev, _agg (aggregated class), _n (number of 10 m pixels in parcel).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - 3-band rasters per parcel: dominant land cover (_mode), _conf, and _purity.
  - 1 km raster products
    - Dominant cover (1-band) for UKCEH classes and aggregates.
    - Percentage cover (21-band for classes; 10-band for aggregates) per 1 km pixel.
    - Rounding may cause sums to deviate from 100%; coastal pixels may be underrepresented due to mapping extents.
  - Seasonal Composite Images and Context Rasters
    - Seasonal Sentinel-2 composites (four seasons) used for classification.
    - 10 m GB Context Rasters (height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland mask).
    - 8 NI Context Rasters (height, aspect, slope, urban mask, distance to coast/roads/freshwater, foreshore and tidal masks).
  - Classification Scenes
    - GB: grid of 32 Classification Scenes (~100 x 100 km tiles) combining Seasonal Composite Images with 50-band Context Layers; each scene trained and classified independently.
    - NI: single 49-band Classification Scene (40 Sentinel-2 bands with context rasters).
  - Dataset naming and metadata (Appendix 3; Table 2)
    - Official dataset names and extents provided (GB/NI, GB/N I coordinates, EPSG codes, pixel resolutions, bands).

- Production workflow and methodologies
  - Bootstrap Training
    - Automatic training that uses historic wall-to-wall classifications (LCM2018–2020) filtered for >80% purity and consistent class across three years.
    - Enables a large, representative training set without new field data.
  - Random Forest classification
    - Pixels sampled into labeled bags; 10,000 samples per bag with replacement to balance classes.
    - RF classifier yields the 10 m Classified Pixel product.
  - Context and spectral differentiation
    - Context Rasters reduce spectral confusion among spectrally similar classes (e.g., bare rock vs. urban surfaces).
  - UKCEH Land Parcel Spatial Framework
    - Framework with ~0.5 ha minimum parcel size used to group pixels into land parcels for change detection and consistency across time.

- Spatial and temporal scope
  - Geography: Great Britain and Northern Ireland; coordinate systems GB (EPSG 27700) and NI (EPSG 29903).
  - Temporal context: annual map series intended to distinguish random errors from real changes; supports change detection over time.

- Validation and accuracy
  - Validation dataset: 35,182 reference points from GB-NI coverage, spanning all 21 classes.
  - Reported overall accuracy: 82.6% (95% CI: 82.19–82.99%).
  - Validation details and confusion matrices are provided (Appendix 4); some inter-class confusion remains due to spectral similarity among habitats.

- Relationship to Biodiversity Action Plan (BAP) Broad Habitats
  - UKCEH 21 Land Cover Classes are closely related to BAP Broad Habitats but not identical.
  - BAP definitions are italicised when referenced to avoid ambiguity; a detailed mapping is provided in Appendices 1 and 2.
  - Some BAP classes are split or aggregated into UKCEH classes (e.g., Urban vs Suburban; Heather vs Heather Grassland; Bracken merged with Acid Grassland in some cases).
  - Appendices describe how to interpret and relate UKCEH classes to BAP Broad Habitats for consistency across datasets and historical comparisons.

- Practical guidance and considerations
  - The 10 m Classified Pixels are not generalised by the Land Parcel Spatial Framework; best for specialist users who can accommodate higher noise in fine detail.
  - 25 m Rasterised Parcel data provide a more stable basis for comparison and change detection; primary validation targeted at these parcels.
  - Users should be aware of potential label mismatches with LCM2015 due to changes in parcel identifiers (gid) from the UKCEH Land Parcel Spatial Framework updates.
  - Seasonal and context data help disambiguate land-cover types in challenging areas (coastal, urban, flat terrain).

- Visualization and accessibility
  - Appendices include color recipes for displaying UKCEH Land Cover Classes (Appendix 5) and color-blind friendly variants (Appendix 6) to aid interpretation and visualization.

- Appendices at a glance
  - Appendix 1: Notes on UKCEH Land Cover Classes with interpretation guidance for several major classes.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and relationships to UKCEH classes.
  - Appendix 3: Full list of UKCEH LCM2021 datasets and naming conventions.
  - Appendix 4: Comprehensive correspondence (confusion) matrices between UKCEH classes and validation outcomes; producer and user accuracies.
  - Appendix 5 & 6: Color recipes for standard and color-blind friendly displays of the classes.