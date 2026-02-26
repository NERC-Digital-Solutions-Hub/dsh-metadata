# The UKCEH Land Cover Map for 2023

- Purpose: User guide for LCM2023, UKCEH’s annual land cover map. Describes data production, validation, and data accuracy to help users apply the data in current and future work.
- Product suite (seven datasets total):
  - Three datasets for Great Britain and Northern Ireland each: 
    - 10 m Classified Pixels (pixel-level land cover)
    - Land Parcels (vector parcel framework)
    - 25 m Rasterised Land Parcels
  - A 1 km summary raster product covering GB and Northern Ireland

- UKCEH Land Cover Classes and BAP relationship:
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats
  - Classes linked to BAP Broad Habitats but not identical; BAP terms italicised when used
  - Appendix 1–2 detail crosswalks and notes on mapping considerations
  - The typical one-to-one relationship is assumed, with a few exceptions (e.g., Freshwater vs Saltwater representation; Urban vs Suburban split)

- Datasets and product descriptions:
  - 10 m Classified Pixel datasets (GB and NI)
    - Derived from multiple Classification Scenes classified with a Random Forest
    - Band 1: most likely UKCEH Land Cover Class; Band 2: class probability (confidence)
    - Not generalised by the Land Parcel Spatial Framework to preserve fine features
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised version of Land Parcels with three bands: dominant land cover (mode), confidence (_conf), and purity (_purity)
  - Land Parcel products (GB and NI)
    - Include parcel-level attributes (gid, hist, mode, conf, purity, etc.)
  - 1 km Summary Raster products (GB and NI)
    - Dominant class per 1 km pixel (21-class and 10-class aggregates)
    - Percentage cover per class (and aggregates); values are integer-rounded
    - Coastal areas may sum to less than 100% due to mapping resolution; est. 1600x25 m pixels per 1 km pixel
  - Coordinate systems and extents:
    - GB: British National Grid (EPSG: 27700)
    - NI: Irish Grid TM75 (EPSG: 29903)
  - Dataset metadata and access: Each dataset has a DOI; citations provided (Table 5)

- Seasonal Composite Images and Context Rasters:
  - Seasonal Composite Images derived from Sentinel-2 via Google Earth Engine
    - Four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec)
    - 10 Sentinel-2 bands used; occasional gaps due to cloud cover
  - Context Rasters (10 m) to reduce spectral confusion
    - Great Britain: height, aspect, slope; distance to buildings, roads, tidal water, freshwater; foreshore mask; woodland mask; saltmarsh mask
    - Northern Ireland: height, aspect, slope; urban mask; distance to coast, freshwater, roads; foreshore; tidal water

- Classification Scenes and Bootstrap Training:
  - GB: 32 Classification Scenes (tiles ~100 x 100 km) for full GB coverage
  - NI: Single Classification Scene (~minimum bounding rectangle)
  - Bootstrap Training: automatic, uses historic land cover maps to train a Random Forest without new field data
    - Training pixels selected from LCM2020–2022 with >80% probability and same class across three years
    - RF classifier trained with balanced sampling (10,000 samples per bag per class)
  - Software: bespoke UKCEH tool integrating Weka, PostGIS, and GDAL (open-source stack)

- The UKCEH Land Parcel Spatial Framework and MMU:
  - Spatial framework built from generalized national cartography
  - Land parcels have minimum area ~0.5 ha (MMU)
  - Parcels designed to represent discrete real-world units; most parcels are dominated by a single land cover
  - Framework supports change detection and comparison over time
  - IDs (gid) may not match LCM2015 when comparing with older datasets due to framework changes

- Product validation and accuracy:
  - Validation set: 33,107 reference points across 21 classes
  - Overall accuracy: 83% for LCM2023
  - Validation data sources: GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points
  - Appendix 4 provides detailed confusion matrices and accuracies by class

- Known issues and caveats:
  - Some polygons missing from vector Land Parcel products; minor nodata areas in 25 m rasterised parcels
  - 10 m Classified Pixels remain unaffected by missing parcels
  - Methodological changes between annual maps mean some differences reflect production methods, not only real change

- How to cite and access datasets:
  - Each LCM2023 dataset has a DOI and recommended citation
  - References include Marston et al. (2023–2024) and Morton et al. (2011)
  - DOIs cover:
    - 10 m Classified Pixels (GB and NI)
    - 25 m Rasterised Land Parcels (GB and NI)
    - Land Parcels (GB and NI)
    - 1 km Summary Rasters

- Colour schemes and data presentation:
  - Appendix 5 and 6 provide recommended colour ramps for displaying UKCEH Land Cover Classes
  - QGIS symbol files lcm_raster.qml and color-blind-friendly versions are provided

- Practical implications for data use (summary for data support):
  - Rich, multi-resolution data enabling self-service exploration (pixels, parcels, and summaries)
  - High-resolution 10 m data preserve fine landscape features; 25 m parcels facilitate temporal comparison and aggregation
  - Seasonal composites and context rasters help resolve spectral confusion between similar land covers
  - Bootstrap Training and RF classification provide scalable annual updates with documented accuracy
  - Explicit mapping to BAP Broad Habitats aids compatibility with ecological and regulatory analyses
  - Validation and known issues documented to guide quality assessment and integration with other datasets

- Notable references and DOIs (selected):
  - LCM2023 data products (10 m classified pixels GB/NI; 25 m rasterised land parcels GB/NI; land parcels; 1 km rasters)
  - Marston et al. (2023, 2024) for production methods and dataset-specific details
  - Morton et al. (2011); Smith et al. (2007) for historical context of the land parcel framework

- Appendix highlights (quick reference):
  - Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats
  - Appendix 3: Full list of LCM2023 datasets and DOIs
  - Appendix 4: Correspondence/accuracy matrices for class crosswalks
  - Appendix 5–6: Colour recipes for standard and colour-blind-friendly displays with associated QGIS symbol files