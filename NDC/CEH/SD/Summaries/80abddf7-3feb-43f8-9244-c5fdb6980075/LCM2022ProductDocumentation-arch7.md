# The UKCEH Land Cover Map for 2022

- Aims and scope
  - UKCEH LCM2022 provides annual, map-based land cover data across Great Britain (GB) and Northern Ireland (NI) using seven datasets: three GB and NI-specific datasets (10 m classified pixels, classified land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster for both GB and NI.
  - All datasets underpin 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, with formal validation and accuracy assessments described to support informed use.

- Data products and formats
  - 10 m Classified Pixel datasets (GB and NI)
    - Pixel-level classification with two bands: the most likely UKCEH Land Cover Class identifier and the associated class membership probability (confidence).
    - Not generalized by the Land Parcel Spatial Framework to preserve fine landscape details (e.g., narrow features).
  - Land Parcel Datasets (GB and NI)
    - Derived by intersecting the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to create parcel attributes.
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterized version of land parcels with 3-band output: dominant land cover (mode), confidence (conf), and purity (purity) per parcel.
  - Land Parcel Product (vector)
    - Parcel-level attributes designed for change detection and spatial analyses; includes per-parcel statistics and identifiers.
  - 1 km Summary Raster products (GB and NI)
    - Dominant class per 1 km pixel (two products: class and aggregate class) and percentage cover per class/aggregate (21 class bands and 10 aggregate bands). Rounding may cause minor total deviations from 100%.
  - Classification Scenes and Seasonal Imagery
    - GB: 32 Classification Scenes covering GB land surface; NI: a single Classification Scene determined by NI extent.
    - Seasonal Composite Images derived from Sentinel-2 (10 m res) across four seasons (Jan–Mar, Apr– Jun, Jul–Sep, Oct–Dec) with multiple spectral bands.
  - Context Rasters
    - 10 m context rasters used to reduce spectral confusion (GB and NI have different sets of contextual layers such as height, slope, distances to roads/coastal features, binary masks for urban, woodland, and coastal features).
  - Catalog and provenance
    - Datasets are individually DOId and cite Marston et al. (2024) for production details; Appendix 3 lists official dataset names and DOIs.

- Methodology highlights
  - Seasonal and contextual data fusion
    - Land cover mapping based on Classification Scenes that combine Sentinel-2 seasonal spectral information with Context Rasters to improve discriminative power.
  - Bootstrap Training and Random Forest
    - Training observations are automatically sampled from historical maps (Bootstrap Training) to train a Random Forest classifier, enabling wall-to-wall mapping without new field data.
  - Data processing framework
    - A bespoke software workflow integrates Weka, PostGIS, and GDAL tools to produce the 10 m pixels, 25 m parcels, and 1 km summaries.
  - Validation and accuracy
    - Overall accuracy of 86.1% across 21 LCM classes, validated against 33,107 reference points from GB/NL countryside surveys, National Forest Inventory data, Rural Payments Agency data, and bespoke validation points.
  - Temporal context
    - Annual production aims to improve temporal consistency and enable robust change detection; random errors are expected to flicker over time, while real changes persist.

- UKCEH Land Cover Classes and BAP crosswalk
  - 21 UKCEH Land Cover Classes are aligned with BAP Broad Habitats (with intentional differences to preserve consistency with earlier products).
  - Appendices provide detailed class descriptions, nuances, and cautions about spectral similarity and context-based distinctions (e.g., arable vs improved grassland, littoral vs supralittoral zones).

- Dataset specifications and spatial details
  - Coordinate systems
    - GB: British National Grid, EPSG 27700
    - NI: Irish Grid, EPSG 29903
  - Extents and granularity
    - GB: 10 m and 25 m products; NI: 10 m and 25 m products; 1 km summary covers both GB and NI.
  - Parcel framework and MMU
    - UKCEH Land Parcel Spatial Framework with a minimum mapping unit (MMU) of ~0.5 hectares; parcels represent discrete land units like fields, parks, water bodies, etc.
  - Parcel counts
    - GB parcels: 6,741,294
    - NI parcels: 902,252
  - Pixel and band structure
    - 10 m Classified Pixels: 2 bands (class, conf)
    - 25 m Rasterised Parcels: 3 bands (mode, conf, purity)
    - 1 km summary rasters: multiple bands (dominant class, percentage cover per class/aggregate)

- Practical guidance for GIS use
  - Detail and fidelity
    - 10 m classified pixels preserve fine landscape features; suitable for detailed mapping and fine-scale analyses but are not generalized to the parcel framework.
  - Change detection and interpretation
    - Annual maps help distinguish real land cover changes from method-driven variations; expect some inter-annual noise that diminishes as the time series matures.
  - Classification confidence and interpretation
    - First band provides the most likely land cover class; the second band provides a per-pixel confidence measure to support uncertainty-aware analysis.
  - 1 km products
    - Useful for broad-scale summaries; percentage values are rounded and may not sum exactly to 100% due to coastline effects and the 1 km pixel aggregation.
  - Color and visualization
    - Appendix 5 and Appendix 6 provide recommended color recipes for displaying the 21 classes and a color-blind-friendly version; accompanying QGIS symbology files (lcm_raster.qml and lcm_raster_cb_friendly.qml) are provided.

- Validation, issues, and caveats
  - Known issues
    - A small number of polygons are missing from vector land parcel products, causing nodata gaps in the 25 m rasterised parcel dataset; impact on 1 km products is negligible; 10 m classified pixels remain unaffected.
  - Method changes
    - The document notes that ongoing methodological refinements may introduce slight differences between consecutive annual maps; changes reflect real changes and/or method updates.

- Access, citation, and references
  - Dataset DOIs and citations are provided for each product (10 m classified pixels GB/NI; 25 m rasterised land parcels GB/NI; land parcels GB/NI; 1 km summary rasters GB/NI). See Table 5 for DOIs and Marston et al. (2023–2024) for production context.
  - Users are encouraged to cite the corresponding DOI for each dataset and May reference Marston et al. (2023) for background on previous LCM production.

- Appendices and supplemental material
  - Appendix 1–3: Class notes, BAP Broad Habitats, and full dataset lists.
  - Appendix 4: Correspondence matrices and accuracy details per class (producer and user’s accuracy).
  - Appendix 5–6: Color recipes for display, including color-blind friendly version; accompanying QGIS symbol files provided.