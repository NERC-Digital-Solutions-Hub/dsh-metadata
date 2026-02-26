# The UKCEH Land Cover Map for 2022

- Purpose and scope
  - UKCEH LCM2022 is the tenth UK land cover map, produced annually to support monitoring of state and change in the UK countryside.
  - Provides 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) derived from Sentinel-2 seasonal composites plus context rasters.
  - Built to enable detection of real change over time and to support environmental objectives; includes formal validation and documentation to help users assess accuracy and limitations.

- Data products (seven datasets in total)
  - 10 m Classified Pixel datasets (Great Britain and Northern Ireland): high-detail pixel classifications with a confidence probability per pixel; not generalised by the Land Parcel Spatial Framework.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised versions of land parcels, carrying per-parcel attributes; used for consistent change detection and area statistics.
  - Land Parcel (vector) datasets (GB and NI): land parcel geometries generalised to ~0.5 ha MMU, aligned with UKCEH Land Parcel Spatial Framework for consistent parcel-based analysis.
  - 1 km Summary rasters (GB and NI): summarised products showing dominant class, aggregate dominance, and percentage cover per 1 km pixel.
  - Coordinate systems: GB = British National Grid (EPSG: 27700); Northern Ireland = TM75 Irish Grid (EPSG: 29903).
  - Band structure:
    - 10 m Classified Pixels: band 1 = most likely UKCEH Land Cover Class; band 2 = class membership probability (confidence).
    - 25 m Rasterised Land Parcels: three bands per parcel — band 1 = modal land cover class (mode), band 2 = mean confidence (conf), band 3 = purity.
  - Official dataset names and DOIs are provided for each product (Table 5 in the document).

- How the data were produced (production workflow)
  - Classification scene construction
    - Classification Scenes composed from Sentinel-2 Seasonal Composite Images (10 m) plus Context Rasters to reduce spectral confusion.
    - For Great Britain: 32 Classification Scenes (tiles ~100 x 100 km); for Northern Ireland: a single Scene covering the NI land area.
  - Bootstrap Training and Random Forest
    - Bootstrap Training uses historic LCM data (LCM2019–LCM2021) to automatically sample training observations, selecting pixels with >80% probability and consistent class across years.
    - Random Forest classifier trained on 10,000 samples per class; sampling balance ensures rare classes are sufficiently learned.
    - Training data limitations noted for arable and improved grassland classes due to crop rotations.
  - Context rasters and seasonal information
    - 10 m Context Rasters include terrain (height, aspect, slope), distance to roads/buildings/water, foreshore and land cover masks, etc.
    - Seasonal Composite Images created from four seasonal windows (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using Sentinel-2 bands; gaps due to clouds are tolerated by the classifier.
  - UKCEH Land Parcel Spatial Framework
    - Parcel geometries derived from generalised national cartography; MMU ≈ 0.5 ha.
    - Framework provides fixed parcels to reduce noise and support change detection over time.
  - Classification and output
    - 10 m pixel classifications produced and published as classified pixels (GB/NI) with an associated confidence band.
    - Parcels intersected with the Spatial Framework to generate land parcel attributes for vector and 25 m rasterised products.
  - Validation
    - Validation using 33,107 points across all 21 classes; overall accuracy 86.1%.
    - Validation data compiled from countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points.

- Data quality, validation, and known issues
  - Overall accuracy: 86.1% ( producer’s and user’s accuracy summaries across classes are provided in Appendix 4).
  - Known issues
    - Some vector land parcel polygons may be missing, causing nodata areas in derived 25 m raster parcels; effects are negligible for the 1 km summary rasters and the 10 m pixel datasets remain unaffected.
    - Differences between annual maps may reflect real change or methodological updates; users should consider potential method-related variability when comparing years.
  - Validation scope
    - Validation was performed against the 25 m rasterised land parcel dataset; the 10 m classified pixels retain higher detail but have not been independently validated at the pixel level to the same extent as the 25 m product.

- Data use and interpretation notes
  - The 21 UKCEH Land Cover Classes are aligned with UK BAP Broad Habitats but are not identical; some mappings are provided in Appendix 1 and 2 to reduce ambiguity.
  - The relationship between classes and BAP broad habitats is described, including cases where splits or combinations occur (e.g., urban vs suburban, bracken merging into acid grassland historically).
  - The 1 km summary rasters reflect a summary of 25 m data; percentage values are rounded to integers and may not sum exactly to 100 due to coastal and edge effects.
  - Seasonal and context data enable improved discrimination in spectral-confused areas (e.g., bare rocks, coastal zones, urban areas), but some misclassification with rare or spectrally similar classes remains possible.

- Accessibility, citation, and references
  - Each LCM2022 dataset has a DOI; user guidance includes recommended citations (Marston et al. 2023/2024 variants) with DOIs for each product.
  - The document provides further references on production methods and validation, including prior LCM products (LCM2021) and foundational methodology (Random Forest, Bootstrap Training).

- Appendices and supplementary material (highlights)
  - Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats, including guidance on interpretation and potential confusion between classes.
  - Appendix 3: Full list of LCM2022 datasets and DOI citations for GB and NI products, plus 1 km rasters.
  - Appendix 4: Correspondence matrices and accuracy metrics by class (user’s and producer’s accuracy).
  - Appendix 5–6: Color recipes for displaying land cover classes (standard and color-blind friendly), with accompanying QGIS symbology files.