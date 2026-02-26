# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Delivers the first continuous parcel-based UK land cover map (LCM2007) with a suite of raster products to support nationwide analysis, policy, and planning.
  - Integrates detailed national cartography with multi-temporal satellite imagery to produce coast-to-coast coverage across GB and Northern Ireland.

- Data products and formats
  - Vector product: land parcels (polygons) with extensive attributes, including Broad Habitat (BH), BHSub, FieldCode, KBE history, ProbList, and processing history.
  - Raster products:
    - 25 m resolution: 23 LCM2007 classes.
    - 1 km resolution: two formats per class—percentage cover per 1 km pixel and dominant class per 1 km pixel.
  - Metadata and provenance
    - Full processing history, class numbers, and knowledge-based enhancements (KBEs) are recorded to enable traceability and potential reversion of KBEs.
  - Access
    - 1 km rasters via CEH Information Gateway.
    - Full vector and 25 m rasters available on request; licensing may apply.

- Spatial framework and data sources
  - Spatial framework derived from high-detail national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector).
  - Multi-sensor satellite data (Landsat, SPOT, and LISS-3/AWIFS) plus ancillary data (soil, topography, urban outlines, boundaries).

- Image processing, segmentation, and enhancements
  - Multi-date, multi-sensor image composites processed with segmentation and maximum likelihood classification.
  - Knowledge-based enhancements (KBEs) applied post-classification to improve thematic resolution and reduce spectral confusion.
  - Contextual data (terrain, soils, proximity to urban areas, etc.) inform KBEs and reclassifications where spectral signals are ambiguous.

- Accuracy, validation, and interpretation
  - Overall validation against Countryside Survey (CS) 2007 shows about 83% accuracy for LCM2007 classes; class-level performance varies.
  - Comparisons between LCM2007 and CS reveal:
    - High correspondence for some broad habitats (e.g., certain woodland and grassland classes) within UK-wide CS confidence limits.
    - Notable dissimilarities for Arable and Horticulture, Improved Grassland, Neutral Grassland, Montane Habitats, Bog, and Fen, Marsh and Swamp due to spectral variability, boundary delineation, and temporal image range.
  - The report discusses how CS scales-up methods differ and how MMU and boundary features affect area estimates, especially for smaller or mosaic habitats.

- Countryside Survey vs LCM2007: key insights
  - Grassland classification is particularly challenging due to one-to-many relationships with Broad Habitats; Broad Habitat Association rules were developed to better align datasets.
  - Large differences in Fen, Marsh and Swamp estimates are explained by mosaic land-cover types and differing spatial representations between CS and LCM2007.
  - The comparison emphasizes the value of combining in situ (CS) and satellite-based (LCM2007) data for a fuller understanding of land cover dynamics and uncertainty.

- UK-wide and country-level land cover patterns (LCM2007 vs CS)
  - LCM2007 indicates substantial intensive land use (Arable and Horticulture + Improved Grassland) and built-up areas, with woodlands making up a smaller but significant share.
  - England, Scotland, Wales, and Northern Ireland show varying distributions of intensive vs semi-natural habitats, influenced by regional land-use patterns and habitat types.

- Practical implications for data support
  - Parcel-level metadata and the ProbList/KBE history enable users to assess credibility and tailor interpretations to local contexts.
  - The vector and raster products support self-serve data discovery, cross-comparison, and integration with other datasets (e.g., climate, hydrology, biodiversity indicators).
  - KBEs illustrate how contextual data improve classification; users are encouraged to validate and, if needed, reclassify using their own criteria.

- Limitations and caveats for users
  - Some habitat distinctions remain difficult to resolve spectrally (e.g., certain grasslands, fen mosaics) and depend on ancillary data quality.
  - Temporal differences in image acquisition can affect classifications where fields cycle between temporary grassland and arable crops.
  - Countryside Survey patch size and MMU differences can influence area estimates, particularly for small or fragmented habitats.

- Data interpretation and future directions
  - LCM2007 provides a robust UK-wide framework with a reusable spatial structure for future monitoring and change detection.
  - The Broad Habitat Association rules help harmonize CS and LCM classifications and guide future improvements in grassland and mosaic habitats.
  - The report suggests continued integration with additional data sources (soil, geology, LiDAR, climate) to further enhance classification accuracy and change detection across the UK.