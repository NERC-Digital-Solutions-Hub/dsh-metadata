# Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 delivers a continuous UK-wide land cover map at parcel/vector level with 25 m and 1 km raster products, aligned to Broad Habitats and supporting biodiversity policy and landscape monitoring.
- Comparisons are made with Countryside Survey (CS) 2007 to assess agreement and identify differences in extent and classification.
- Key outputs include 23 LCM2007 classes mapped to Broad Habitats, plus bespoke knowledge-based enhancements and documentation for traceability.

## Data provenance, spatial framework, and classification workflow
- Uses a UK-wide spatial framework built from national cartography and satellite imagery to delineate real-world land units, enabling consistent spatial structure for monitoring.
- Classification chain combines multi-temporal imagery with knowledge-based enhancements (KBEs) to improve thematic resolution and reduce spectral confusion.
- Differences in spatial framework and minimum mapping unit (MMU) between CS and LCM2007 influence area estimates and comparisons.
- Documentation includes parcel-level metadata, processing history, and KBE changes to support reproducibility and user-driven QA.

## Similar and dissimilar area estimates between LCM2007 and Countryside Survey 2007
- Similar area estimates occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Reasons for differences include:
  - Differences in what each method classifies as Arable and Horticulture, including boundaries/linear features and persistence of temporary grass vs arable across multi-year imagery.
  - Spectral confusion due to diverse crop types and growth stages, leading to misclassifications in arable areas.
  - Boundary and Linear Features being treated differently (_CS maps boundaries that may be below MMU; LCM integrates them into field polygons, affecting area calculations).
  - Grassland classifications: Improved vs Neutral grassland split is sensitive to spectral signatures and soil context, with soil data offering limited discrimination.
  - Dwarf Shrub Heath vs Acid Grassland and Montane interactions in upland areas; Montane classifications can subsume other upland types.
  - Fen, Marsh and Swamp is highly mosaic and patchy; CS and LCM2007 differ in how these areas are detected and allocated, with many Fen areas mapped as Rough Grassland or Acid Grassland by LCM2007.
- Implications: differences reflect distinct data sources, temporal windows, scales, and classification philosophies; cross-dataset validation requires nuanced interpretation.

## Change mapping and temporal considerations
- Change detection is challenging due to non-identical class definitions and spatial/temporal frameworks across years.
- Aggregated-class change analyses may be more robust than direct class-to-class comparisons; reprocessing older maps into a common spatial framework can aid comparison.

## Data products, provenance, and access
- Data products include:
  - Vector product: parcel polygons with 10+ attributes (area, source images, Broad Habitat, KBE history, etc.).
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: UK-wide summaries either as percentage cover or dominant class per pixel.
- Metadata emphasizes data lineage, KBEs applied, and processing history to enable traceability.
- Access:
  - 1 km raster data via the CEH Information Gateway.
  - Full vector and 25 m products available on request under licence; licensing fees may apply for some uses.

## Data quality, validation, and caveats
- Validation against CS 2007 ground data shows varying producer’s and user’s accuracies by class; overall accuracy for certain broad habitats is constrained by class complexity and spatial scale.
- Fen, Marsh and Swamp and other mosaic habitats present notable QA challenges due to patchiness and mixed land-cover signatures.
- Users should consider uncertainties, especially for grassland and montane classes, and refer to the Broad Habitat Association rules for cross-dataset comparability.

## Implications for Data Stewards (governance and management)
- Provenance and governance:
  - Maintain detailed data source documentation (CS 2007, LCM2007), processing chains, and MMU/spatial framework choices.
  - Preserve parcel-level metadata, KBE history, and probability lists to support reproducibility and targeted QA.
- Interoperability and reuse:
  - Use standardized Broad Habitat mappings to enable cross-dataset comparisons and policy-relevant reporting.
  - Provide both vector and raster formats to accommodate diverse applications, balancing detail with data volume.
- Access, licensing, and licensing terms:
  - Clearly communicate licensing requirements and any fees for vector and 25 m products; provide contact points for licensing inquiries.
- Change detection and time-series use:
  - Acknowledge methodological differences when comparing across years; prefer aggregated or harmonized class schemes for long-term monitoring.
- Data volume and storage:
  - Plan for large polygon counts and rich metadata; implement robust versioning and change-tracking mechanisms to manage updates.

## Challenges and considerations
- Incomplete alignment of user needs with outputs; high thematic resolution increases data volume and complexity.
- Timely access to and integration of multiple national datasets; harmonization is essential for UK-wide monitoring.
- Rich metadata is vital for reproducibility but adds to data size and processing requirements.
- Spectral confusion in grasslands and uplands necessitates ongoing refinement of KBEs and incorporation of ancillary data.

## Conclusion
- LCM2007 provides the first continuous UK-wide land cover map with detailed vector boundaries and accompanying raster products, enabling broad habitat monitoring and cross-country analyses.
- While offering substantial improvements and a reusable spatial framework, comparisons with CS 2007 reveal substantial differences driven by classification schemes, MMU, and mosaic/narrow feature mapping, underscoring the need for careful interpretation and robust metadata for governance and reuse.