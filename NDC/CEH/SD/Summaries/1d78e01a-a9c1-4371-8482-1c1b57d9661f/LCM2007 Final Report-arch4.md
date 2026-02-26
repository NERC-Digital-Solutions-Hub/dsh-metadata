# Final Report for LCM2007 - the new UK land cover map

- Overview
  - First continuous parcel-based UK land cover map (LCM2007) derived from national cartography, combined with multi-temporal satellite imagery.
  - Covers Great Britain and Northern Ireland; 25 m raster and continuous vector parcels; minimum mappable unit of 0.5 ha.
  - Classifies 23 land cover classes ( Broad Habitats aligned), plus 10 aggregate/broad classes for 1 km products.
  - Intended to support biodiversity monitoring, ecosystem services, landscape planning, and catchment management; enables policy-relevant analyses.

- Data framework and production
  - Spatial framework built from detailed national cartography (OS MasterMap for GB; LPS for NI) and integrated with image segmentation to align with a 0.5 ha MMU.
  - Multi-temporal imagery used: Landsat, SPOT, IRS AWIFS, LISS-III; image composites created to enhance class separation; seasonal timing chosen to reflect phenology.
  - Ground reference data from CEH and Countryside Survey (CS) used for training/validation; additional data include soils, elevation, boundaries, and other ancillary layers.
  - Image pre-processing includes cloud masking, atmospheric and topographic corrections; segmentation and integration with cartographic frameworks to form a unified workflow.

- Classification and knowledge-based enhancements
  - Parcel-based supervised maximum likelihood classification using ~37 composites and 21 single-date images.
  - Knowledge-based enhancements (KBEs): regionally adaptive rules (about 20% of parcels) to improve thematic resolution using context such as urban boundaries, coastal proximity, soils, and terrain.
  - Seven automated KBE algorithms applied in a defined sequence; provide an ability to revert to spectral classifications if needed.
  - Output includes class probabilities and top five spectral class results per parcel.

- Products, metadata, and access
  - Vector product: 23 LCM2007 classes with 10 attributes documenting processing stages, KBE history, and provenance for full traceability.
  - Raster products:
    - 25 m raster: 23 classes.
    - 1 km raster: two formats—percent cover per 1 km square for each class, and dominant class per 1 km square.
  - Access:
    - 1 km raster via CEH Information Gateway.
    - Full vector and 25 m raster available on request under licence (fees may apply).

- Quality assurance, validation, and comparability
  - Ground validation: 9,127 points; overall accuracy ~83% across LCM2007 classes.
  - Class-specific performance: high accuracy for Coniferous Woodland, Arable/Horticulture, Littoral Rock; lower for Neutral/Calcareous Grasslands and Montane Habitats.
  - Countryside Survey (CS) 2007 comparison:
    - Broad Habitat correspondence: ~62% at GB level; higher (76%) when using Broad Habitat Association (BHA) framework.
    - Grassland-related mismatches common; aggregation of grassland types increases agreement.
    - Fen, Marsh and Swamp estimates differ by order of magnitude due to mosaic nature and mapping challenges; many CS Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Differences in data structure, classification, and MMU between LCM2007 and CS complicate direct change detection; a joint interpretation with BH associations improves comparability.

- UK-wide and country-level insights
  - LCM2007 UK summary: more than half of UK land in intensive use (Arable and Horticulture + Improved Grassland); woodlands ~12% (Broadleaved and Coniferous); remaining area semi-natural and coastal.
  - Country differences: England and Northern Ireland show higher intensive land use; Scotland hosts more Coniferous Woodland and upland semi-natural habitats; Wales shows substantial coastal and urban features.
  - Comparison with LCM2000 indicates shifts in arable and semi-natural grassland proportions, but attribution is complex due to spatial framework changes and classification updates.

- Implications for data strategy for Data Leaders
  - Demonstrates the value of a parcel-based, cartography-derived spatial framework for scalable, policy-relevant land cover products.
  - Emphasizes the importance of robust metadata and traceable processing (KBE histories, probabilities) to support governance, reuse, and licensing.
  - Highlights cross-region data integration challenges (GB vs NI) and the need for standardized cross-border classifications to support policy and reporting.
  - Suggests leveraging multiple data sources (CS, field surveys, LiDAR, other national datasets) to improve thematic accuracy and support change detection.
  - Provides a model for data collaboration with national bodies and external validation with national surveys.

- Limitations, challenges, and future directions
  - Spectral confusion remains for certain habitats (notably grasslands and montane mosaics); KBEs mitigate but do not eliminate all misclassifications.
  - Differences in spatial structure across CEH maps (LCM1990, LCM2000, LCM2007) complicate change detection; future work may re-align older maps to a common spatial framework.
  - Fen, Marsh and Swamp remain difficult to map accurately; potential to develop additional KBEs to allocate parts of these areas to related classes.
  - LCM2007 serves as a foundation for ongoing UK land surface mapping; future refinement should focus on standards alignment, policy-relevant outputs, and enhanced cross-border consistency.

- Example datasets and visualization
  - Vector and 25 m raster formats offer comparable detail; 1 km rasters suitable for UK-wide modelling and integration with other datasets (e.g., meteorological, species distributions).
  - An array of example datasets demonstrates the distribution of Broad Habitats (and their aggregation) across the UK.

- Conclusion
  - LCM2007 delivers the first continental-scale, parcel-based UK land cover map with rich metadata and a reusable spatial framework anchored in national cartography.
  - The product supports policy-relevant analyses across biodiversity, ecosystem services, and landscape planning, while acknowledging challenges in grassland and fen classifications.
  - The integrated approach (cartography-based framework, multi-temporal imagery, KBEs, and robust QA) provides a robust foundation for ongoing monitoring, change detection, and cross-sector data strategy.

- Data governance and licensing notes
  - 1 km raster data accessible via CEH gateway; full vector and 25 m raster available on request under licence (fees may apply).
  - Documentation and provenance included to enable traceability and reproducibility; users encouraged to validate Broad Habitat sub-classes where needed.