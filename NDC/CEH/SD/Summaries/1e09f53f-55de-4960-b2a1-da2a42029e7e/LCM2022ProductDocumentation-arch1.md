# The UKCEH Land Cover Map for 2022

- Overview
  - UKCEH's tenth land cover map, LCM2022, comprises 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats and is delivered as seven geospatial datasets: three per region (Great Britain and Northern Ireland) plus a 1 km summary raster product covering both regions.
  - Datasets include: 10 m Classified Pixels, Land Parcel Datasets, 25 m Rasterised Land Parcels, and a 1 km Summary Raster. Appendix 3 lists official dataset names; DOIs and citations provided in Table 5.

- Data products and structure
  - 10 m Classified Pixels (GB and NI)
    - Created from classified Classification Scenes; each pixel has a class id (UKCEH Land Cover Class) and a class membership probability.
    - First band: most likely class; second band: associated probability/confidence.
    - Not generalised by Land Parcel Spatial Framework to preserve fine landscape details; validated against 25 m rasterised data.
  - Land Parcel Datasets
    - Created by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework to generate parcel attributes (e.g., gid, hist, mode, conf, purity).
    - Parcels have a minimum area (MMU) of about 0.5 ha; used for change detection and analysis across time.
  - 25 m Rasterised Land Parcels
    - Raster representation (25 m) of land parcels with three bands: dominant land cover (mode), mean confidence (conf), and parcel purity (purity).
  - 1 km Summary Rasters
    - Summary products across GB and NI: dominant cover at 1 km, percentage cover per class and per aggregate class.
    - Percentage values are rounded; coastal areas may not sum exactly to 100 due to pixel aggregation rules.
  - Seasonal Composite Images
    - Derived from Sentinel-2, resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
    - Uses 10 Sentinel-2 bands plus context rasters to form Classification Scenes (GB: 32 tiles; NI: single 49-band scene).
    - Occasional cloud gaps; the classifier tolerates partial spectral information.
  - Context Rasters
    - 10 m context layers used to reduce spectral confusion (GB: height, aspect, slope; distances to buildings/roads/tidal water/freshwater; foreshore, woodland, saltmarsh masks; NI: similar but includes urban mask and coastal/freshwater/road distances).
  - The UK Land Parcel Spatial Framework
    - Framework used to generalise national cartography into discrete land parcels (~0.5 ha MMU); identifiers may have changed since LCM2015, affecting direct parcel-id comparisons over time.
  - Production and Methods
    - Bootstrap Training and Random Forest (RF) classifier
      - Bootstrap Training automatically samples training observations from historic land maps (LCM2019–LCM2021) to train the RF classifier for LCM2022.
      - Training sets require Pixels with >80% probability and consistent class across three years.
      - RF classifier is trained with balanced sampling (10,000 samples per class per bag) to avoid dominance by common classes.
      - Software uses bespoke UKCEH tools integrating WEKA, PostGIS, and GDAL (open source).
  - Validation and Accuracy
    - Formal validation used 33,107 reference points across all 21 classes.
    - Overall accuracy: 86.1% (full thematic detail).
  - Known Issues
    - A small number of polygons are missing from the vector Land Parcel products, causing nodata areas in the 25 m rasterised parcel dataset; effect on 1 km products is negligible. 10 m classified pixels remain unaffected.
  - Citing and References
    - Each LCM2022 dataset has a DOI; citations provided (e.g., Marston et al. 2024a–g); see Table 5 for details.

- Methodology in more detail
  - Classification approach
    - Classification Scenes combine Sentinel-2 Seasonal Composite Images with Context Rasters to create spectral + contextual inputs for classification.
    - Bootstrap Training data are drawn from historical LCM maps to enable wall-to-wall training data, supporting rapid updates with short refresh intervals.
    - The RF classifier assigns each 10 m pixel to the most likely UKCEH Land Cover Class; confidence provided per pixel.
  - Seasonal and spectral details
    - Seasonal Composites built from four seasons of Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 8a, 11, 12); cloud gaps are represented as nulls.
    - Context rasters include terrain, proximity to infrastructure, and coastal features to disambiguate spectrally similar classes.
  - Spatial and coordinate details
    - GB data: British National Grid (EPSG 27700); NI data: Irish Grid TM75 (EPSG 29903).
    - Parcel counts: GB ≈ 6,741,294 parcels; NI ≈ 902,252 parcels.
  - Validation specifics
    - Validation dataset comprises GB countryside survey data, National Forest Inventory data, Rural Payments Agency data, and expert validation points.
    - Validation results summarized as overall accuracy; per-class producer’s and user’s accuracies are provided in the underlying appendix (Appendix 4).

- Relationship to BAP Broad Habitats
  - 21 UKCEH Land Cover Classes are related to BAP Broad Habitats but are not identical; BAP classes can be slightly different in spectrum-based mapping contexts.
  - Appendices provide detailed mappings and notes on how UKCEH classes relate to BAP Broad Habitats; italicised BAP terms indicate cross-references to habitat nomenclature.

- Practical considerations for analysts
  - Annual updates help distinguish real changes from classification noise; random errors are expected to flicker over time, while real changes persist.
  - Users should consider the 0.5 ha MMU of Land Parcels when interpreting parcel-level outputs; fine-scale features are retained in the 10 m classified pixels but may be generalised in parcel products.
  - The products are designed for monitoring state and change of the UK countryside and to support environmental objectives; changes in methods between years may yield small differences beyond actual land cover change.

- Appendices and display
  - Appendix 5 and 6 provide recommended color palettes for displaying the 21 classes, including color-blind-friendly options, with accompanying QGIS symbology files (lcm_raster.qml and lcm_raster_cb_friendly.qml).