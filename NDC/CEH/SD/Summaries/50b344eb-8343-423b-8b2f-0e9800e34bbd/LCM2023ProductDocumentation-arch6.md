# The UKCEH Land Cover Map 2023

- UKCEH LCM2023 is the annual land cover map for the UK, produced from Sentinel-2 seasonal composites and Context rasters, classified with Bootstrap Training and Random Forest.
- 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats) are mapped across Great Britain and Northern Ireland.
- Aim: provide timely, detailed land cover data to support environmental monitoring, change detection, and policy/research needs, while enabling end users to understand data provenance and accuracy.

## Data products and structure

- Seven datasets in total:
  - 10 m Classified Pixel datasets for Great Britain and Northern Ireland (two-band rasters: most likely UKCEH Land Cover Class; second band = class membership probability/confidence).
  - 25 m Rasterised Land Parcel datasets (GB and NI) derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework.
  - Land Parcel Product datasets (GB and NI) with parcel-level attributes.
  - A 1 km summary raster product (GB and NI) covering dominant class and percentage cover for all classes and aggregates.
- Dataset specifics:
  - 10 m Classified Pixels: preserves fine landscape features; not generalized to parcel framework; includes confidence values.
  - 25 m Rasterised Land Parcels: built by rasterising parcel boundaries; three attributes per parcel (mode, conf, purity).
  - 1 km rasters: summarize 25 m data to 1 km cells; includes dominant class (and aggregates) and class percentages (rounded).
- Geographic scope and coordinate systems:
  - Great Britain: British National Grid (EPSG 27700); NI: Irish Grid (TM75, EPSG 29903).
- Official data access and citations are provided via DOIs per dataset.

## How the data are produced

- Seasonal Composite Images:
  - Derived from Google Earth Engine; Sentinel-2 bands are resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) are summarized with median reflectance.
  - Some gaps due to clouds are tolerated; classification handles partially complete spectral information.
- Context Rasters:
  - 10 m resolution rasters used to reduce spectral confusion; GB context rasters include terrain (height, aspect, slope), proximity to buildings/roads/water, foreshore and land-cover masks.
  - NI context rasters include urban mask, distance to coast/roads, and coastal masks.
- Classification Scenes and Bootstrap Training:
  - GB: 32 Classification Scenes (tiles ~100 x 100 km); NI: single Classification Scene covering NI.
  - Bootstrap Training uses historic UKCEH maps (LCM2020–LCM2022) to automatically sample training pixels with >80% probability and consistent class across years.
  - Random Forest classifier trained on balanced samples (10,000 per bag) to produce the 10 m Classified Pixels.
- Land Parcel framework:
  - UKCEH Land Parcel Spatial Framework provides fixed land parcel units (~0.5 ha MMU) to reduce noise and enable change detection; parcel IDs may not align perfectly with LCM2015 identifiers.
- Product validation:
  - 33,107 validation points across all 21 classes; overall accuracy 83% for LCM2023 (validated against 25 m rasterised parcel data).

## Data products: content and attributes

- 10 m Classified Pixels (GB and NI):
  - Band 1: dominant UKCEH Land Cover Class.
  - Band 2 (and additional metadata): class membership probability/confidence.
  - Not generalized by the Land Parcel Spatial Framework to preserve detail (e.g., narrow features, small patches).
- 25 m Rasterised Land Parcels (GB and NI):
  - Three bands: dominant parcel land cover (mode), confidence (conf), and purity (purity).
- Land Parcel Product attributes (GB/NI):
  - Example fields include gid, hist, mode, conf, purity, and aggregated overlap information.
- 1 km Summary Rasters (GB and NI):
  - Dominant cover (1 band) for both classes and aggregates.
  - Percentage cover (21 bands for classes; 10 bands for aggregates); values rounded and may not sum to 100 exactly due to rounding and coastal effects.
  
## Vision, validation, and reliability

- Accuracy:
  - Formal validation reports an overall accuracy of 83% at full thematic detail.
  - Validation dataset comprises GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke points.
- Known issues:
  - Some polygons missing from vector land parcel products; negligible impact on 1 km products; 10 m classified pixels are unaffected.
  - Classification method and training data evolve over time; changes can reflect methodological updates as well as real land cover change.
- Documentation and references:
  - DOIs provided for each data product; key methodological references include Bootstrap Training, Random Forest, and prior LCM series publications.

## Methodological notes and interpretation guidance

- UKCEH Land Parcel Spatial Framework:
  - Parcels are designed to represent discrete real-world units (min ~0.5 ha MMU); parcels often dominated by a single land cover class.
  - Historical parcel identifiers may not align with LCM2015 for direct parcel-based comparisons.
- Land cover class definitions and mapping considerations:
  - The 21 UKCEH Land Cover Classes are linked to BAP Broad Habitats; Appendix 1 and 2 provide mapping notes and potential spectral confusions (e.g., between grassland types, bog, heather, fen, etc.).
  - In some cases, BAP broad habitats and UKCEH classes diverge; detailed notes are provided to aid interpretation.
- Seasonal and contextual support:
  - Seasonal spectra and context rasters help reduce spectral confusion and improve classification robustness, particularly in heterogeneous landscapes (urban, coastal, wetland).

## Visualization and use of the data

- Color recipes and symbology:
  - Appendix 5 and Appendix 6 provide recommended color ramps for displaying UKCEH Land Cover Classes (including color-blind friendly options).
  - QGIS symbology files are provided to ease visualization of both standard and color-blind friendly palettes.
- Practical usage tips:
  - Use 10 m classified pixels when you need detailed, high-resolution mapping of features such as narrow corridors or small patches.
  - Use 25 m rasterised land parcels for stable, parcel-based change detection and for analyses that rely on fixed spatial units.
  - 1 km summary rasters are useful for broad-scale monitoring, trend analysis, and integration with coarser-scale datasets.

## Citations and further information

- Each LCM2023 dataset has a DOI for formal citation.
- Key references include Marston et al. (2024a–g) for 2023 datasets, and earlier LCM methodological works (e.g., Bootstrap Training, RF classification).
- Appendix 4 provides correspondence matrices and class-level validation metrics by land cover type (producer’s and user’s accuracy).

- Overall, LCM2023 provides a robust, annually produced UK land cover dataset suite with detailed high-resolution products, validated accuracy, and clear guidance on data provenance, usage, and visualization.