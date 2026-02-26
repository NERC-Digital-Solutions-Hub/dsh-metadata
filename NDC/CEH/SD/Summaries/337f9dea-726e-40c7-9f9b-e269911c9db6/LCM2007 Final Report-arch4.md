# Final Report for LCM2007 - the new UK land cover map

## Executive summary
- LCM2007 delivers the first continuous parcel-based (vector) dataset for the UK with accompanying 25m and 1km raster products, covering GB and Northern Ireland, and aligned with Broad Habitats for policy relevance.
- Outputs include: vector parcels with 10 processing attributes and knowledge-based enhancements (KBEs), a 25m UK raster with 23 classes, and 1km summaries (percent cover or dominant class) for 23 LCM2007 classes and 10 aggregates.
- The project relies on a reusable spatial framework derived from national cartography (OS MasterMap, LPS) and integrates multiple external data sources (soil, elevation, urban boundaries) to improve classification accuracy and change detection.
- Validation shows overall LCM2007 accuracy around 83% with variability by class; substantial challenges remain in grassland, upland, fen/marsh/swamp and boundary feature delineation, influencing comparisons with Countryside Survey (CS).

## Data products and access
- Vector product: parcel-level polygons with attributes including area, source images, Broad Habitat (BH), KBEs history, FieldCode, and ProbList; supports traceability and validation.
- Raster products:
  - 25m resolution: 23 LCM2007 classes (UK-wide).
  - 1km resolution: two formats per location—percentage cover per class and dominant class.
- Access and licensing:
  - 1km rasters: freely available via the CEH Information Gateway.
  - Full vector and 25m rasters: available on request under licence from CEH (fees may apply).

## Data quality, validation, and comparability
- Accuracy and validation:
  - Overall LCM2007 validation accuracy around 83%, with class-level accuracy varying; KBEs applied to resolve about 20% of parcels.
  - Validation notes emphasize the need for user-led, location-specific validation due to spectral variability and data sources.
- Comparisons with Countryside Survey (CS) 2007:
  - Similar area estimates exist for some classes (e.g., Broadleaved woodland, Acid Grassland, Inland Rock) within CS 95% limits.
  - Dissimilar area estimates occur for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Differences explanations include: classification definitions, spectral confusion, inclusion of boundaries in LCM, and temporal range of imagery affecting field changes (e.g., temporary grass vs arable).
  - Grassland comparisons improve when using aggregated grassland categories, highlighting issues with one-to-many mappings between observed land cover and Broad Habitats.
- 4.3.3 Discussion highlights:
  - CS estimates are CS National Estimates scaled via ITE land classes; scaling impact on agreements is under study.
  - Fen, Marsh and Swamp show large UK-level differences due to mosaic and small patch sizes; many CS-recorded Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - The need for a common spatial framework to enable robust change detection across LCM generations is emphasized.

## Practical implications for data leaders
- Data strategy and governance:
  - LCM2007 demonstrates the value of a consistent, reusable nationwide spatial framework for multi-temporal land monitoring and policy support.
  - Integration of diverse external datasets (soil, elevation, urban boundaries) improves classification via knowledge-based enhancements.
- Data quality, metadata, and access:
  - Rich metadata and explicit processing provenance enable traceability and reproducibility; KBEs provide transparency on adjustments.
  - Access model: freely available 1km products; licenced access for full vector and 25m products—organizations should plan for licensing costs.
- Data use and collaboration:
  - Supports biodiversity policy, habitat monitoring, and ecosystem service assessments; cross-validation with CS offers added confidence.
  - Broad Habitat Association rules help resolve spectral confusions and improve thematic resolution, particularly for grassland and upland classes.
- Limitations and future directions:
  - Persistent spectral confusion in grassland types and some upland habitats; potential improvements from enhanced KBEs, more spectral information, or newer sensors.
  - Change detection remains complex due to differing spatial structures and class definitions across LCM generations; future work could harmonize spatial frameworks for robust change analysis.

## Key findings and knowledge outputs
- UK land cover distribution (LCM2007) shows over 50% in intensive use (Arable/Horticulture + Improved Grassland) or Built-up Areas; ~12% coniferous woodland and ~12% broadleaved woodland; remaining areas semi-natural, coastal, or aquatic.
- The UK-wide and country-level variations reflect different land-use patterns (e.g., England highest intensive use; Scotland higher conifer woodland and upland semi-natural areas).
- The Broad Habitat Association (BHA) framework and related validation approaches help address cross-class correspondences, especially for grassland and mosaic habitats.
- The report discusses substantial challenges in change detection between LCM1990, LCM2000, and LCM2007 due to spatial and thematic differences, advocating reorganization of older maps into a common spatial structure.

## Data governance and lifecycle
- The project covers end-to-end data lifecycle: acquisition (multi-temporal imagery), segmentation and classification, KBEs, validation, and dissemination with metadata-rich outputs.
- The 25m and vector products are designed for compatibility with national cartography and for reuse in future change monitoring and policy support.
- The appendix materials outline validation approaches, cross-walks between habitat classifications, and recommendations for users on assessing applicability to their needs.

## Practical recommendations for data leaders
- Leverage the UK-wide, reusable spatial framework (OS MasterMap / LPS-based) as a foundation for future land cover monitoring and cross-country comparability.
- Use KBEs and detailed parcel-level metadata to gauge data quality in specific locales; apply external validation (e.g., high-resolution imagery) for site-specific analyses.
- Plan for licensing costs when requesting full vector and 25m products; exploit freely available 1km rasters for broad-scale analyses and modelling.
- Consider aggregating grassland and other complex classes when comparing with field surveys to improve interpretability and agreement.
- Recognize and address change-detection limitations by aligning future maps to a common spatial structure to separate genuine land-cover change from methodological differences.

## Conclusion
- LCM2007 provides a high-resolution, UK-wide, vector-based land cover framework aligned with Broad Habitats, enabling policy-relevant environmental monitoring and planning.
- The project emphasizes data governance, provenance, and cross-validation with independent surveys, while acknowledging ongoing challenges in grassland, fen, and boundary feature classifications and in robust change detection across time.
- For data leaders, LCM2007 demonstrates a scalable, collaborative approach to national land-cover mapping, with clear pathways for governance, reuse, and policy-informed applications.