# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three UKCEH land cover maps: LCM2017, LCM2018 and LCM2019.
  - Each map comprises a suite of datasets mapping 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) across Great Britain and Northern Ireland.
  - Maps are produced automatically using Bootstrap Training with a Random Forest classifier; annual update aims to reduce lag between observation and map.
  - Visual checks and formal validation were performed; no manual corrections were applied this time. Validation suggests maps are of similar quality to the latest predecessor (LCM2015), with overall accuracy around 78–80% across years.

- Key concepts and terminology
  - Classification Scenes: multi-layer rasters combining seasonal spectral data with Context Rasters to classify land cover.
  - Seasonal Composite Images: Sentinel-2 based medians per season (TOA reflectance used in production).
  - Context Rasters: 20 m rasters of terrain and proximity features (height, slope, distance to road/sea/buildings, etc.) to reduce spectral confusion.
  - Bootstrap Training: automatic, historical-data-derived training approach that seeds the classifier for the next map using majority signals from prior maps.
  - UKCEH Land Parcel Spatial Framework: fixed 0.5 ha minimum mapping unit used to summarize 20 m classified pixels into land parcels, with attributes for each parcel.

- What is included in the data products
  - 20 m Classified Pixels: new feature in LCM2017–2019; RF classification results per pixel with two bands: class label and confidence (0–100).
  - Land Parcels: parcels derived by intersecting 20 m Classified Pixels with the Spatial Framework; parcel-level attributes including histograms of class counts, mode, purity, and confidence.
  - 25 m Rasterised Land Parcels: rasterized version (25 m) of Land Parcels with three bands: modal class (_mode), parcel-averaged confidence (_conf), and parcel purity (_purity).
  - 1 km Raster Products:
    - 1 km Percent Cover: 21-band raster giving per-class percent cover per 1 km.
    - 1 km Percent Aggregate Cover: 10-band raster giving per-aggregate-class percent cover per 1 km.
    - 1 km Dominant Cover: single-band raster of dominant class per 1 km.
    - 1 km Dominant Aggregate Cover: dominant aggregate-class per 1 km.
  - Dataset extents and coordinate systems
    - GB: British National Grid (EPSG: 27700); NI: Irish Grid (EPSG: 29903).
    - Datasets are provided in GB and NI variants with corresponding pixel/parcel grids.

- How the data were produced (production workflow)
  - Classification inputs
    - Seasonal Sentinel-2 data (TOA reflectance) processed into four-season Seasonal Composite Images (winter, spring, summer, autumn).
    - Nine Sentinel-2 bands used for classification (spectral data), with 20 m resolution for seasonal composites.
  - Context information
    - 20 m Context Rasters (terrain, urban proximity, roads, coast, freshwater, etc.) to help disambiguate spectrally similar classes.
  - Classification Scenes and tile strategy
    - Great Britain: 100 x 100 km GB Classification Scenes; 74 overlapping tiles used to ensure balanced training and coverage.
    - Northern Ireland: a single 43-band (36 spectral + 7 context) classification scene per year covering NI.
  - Bootstrap Training and Random Forest
    - Bootstrap Training draws from UKCEH LCM2015 with high-purity parcels (≥99%) to form training data for RF classification of 2017–2019 scenes.
    - RF classifier trained with balanced sampling (10,000 samples per class per bag) to prevent dominance by common classes.
  - Software and validation
    - Custom UKCEH software integrating WEKA, PostGIS and GDAL.
    - Validation performed against multiple datasets (GB countryside survey 2019, National Forest Inventory, IACS, expert validation points).

- Land Parcel Spatial Framework details
  - Framework unchanged in geometry from LCM2015, but with re-ordered storage and new indices for faster processing.
  - gid numbers do not match LCM2015 parcels; comparisons should use gid for cross-year matching.
  - MMU (minimum mapped unit) is ~0.5 ha; parcels aim to represent discrete real-world units (fields, parks, woodlands, etc.).
  - Framework remains a convenient structure for temporal comparison, while acknowledging potential need for future refinement as data and methods evolve.

- Validation and accuracy
  - Validation dataset: 22,325 points across years against Land Parcel mappings.
  - Reported overall accuracies (UK scale)
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Notes on validation
    - Validation data come from sources with different purposes and class definitions; conversions to UKCEH classes are inherently subjective.
    - Currency of validation points varies by product year; results are indicators of performance rather than absolute truth.
    - Full correspondence tables and appendix materials available in the document.

- Class structure and interpretation
  - 21 UKCEH Land Cover Classes, aligned with BAP Broad Habitats (though not identical to BAP definitions).
  - Appendix notes describe how each class is defined spectrally and contextually, including potential confusion (e.g., between arable and improved grassland, or between upland peat and related habitats).
  - General guidance on interpreting complex or spectrally similar classes and how context rasters improve discrimination.

- Outputs, usage, and future directions
  - Outputs emphasize self-serve access to per-pixel classification confidence (20 m) and parcel-level summaries (land parcels) plus multi-scale 1 km rasters.
  - Authors note potential to incorporate additional data types in future releases (e.g., alternative optical sources, SAR data, or refined atmospheric/processing inputs).
  - Annual update plan intends to maintain a consistent backbone (Bootstrap Training + RF) while evolving training data and input layers to improve accuracy and detail.

- Appendix highlights (for data interpretation)
  - Appendix 1 & 2 provide detailed notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats, including detection considerations and common classification challenges.
  - Appendix 3 provides an RGB color recipe for displaying the 21 classes.
  - Appendix 5 lists the full datasets per year (LCM2017, LCM2018, LCM2019), including 20 m Classified Pixels, Land Parcels, 25 m Rasterised Parcels, 1 km products, and related metadata.

- Practical notes for data users (archetype aligned)
  - Expect 21-class outputs with a robust but imperfect accuracy around 78–80% at national scale; use parcel-level attributes for change detection and aggregation to higher scales.
  - Be aware gid changes between LCM2015 and later maps; cross-year parcel comparisons should rely on the Land Parcel Spatial Framework identifiers rather than parcel IDs alone.
  - The 20 m Classified Pixels dataset is now provided with a per-pixel confidence score, enabling uncertainty-aware analyses.
  - For cross-year change analysis, Bootstrap Training leverages majority signals from prior maps, which supports temporal consistency but may still reflect training data biases.
  - If detailed upland or coastal vegetation types are needed, consult Appendix notes on class definitions and consider potential improvements with future data additions.