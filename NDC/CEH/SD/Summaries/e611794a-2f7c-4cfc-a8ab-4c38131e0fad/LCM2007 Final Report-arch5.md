# Final Report for LCM2007 - the new UK land cover map

## Overview
- UK-wide, parcel-based land cover map (LCM2007) built from national cartography with coast-to-coast coverage.
- Maps Broad Habitats (BH) across 23 LCM2007 classes, plus 17 BH sub-classes and 10 aggregated classes.
- Derived products: full vector parcels with provenance metadata, a 25 m raster, and 1 km summary rasters.
- Aimed to support habitat monitoring, biodiversity policy, landscape planning, and ecosystem services assessment.

## Data sources, spatial framework, and structure
- Spatial framework derived from detailed cartography (OS MasterMap, LPS Large-Vector) to improve interoperability and change detection.
- MMU set to 0.5 ha; generalised cartography used to delineate real-world land units and enable reuse.
- Spatial framework integrates with external data (ag boundaries, soils, DEM, urban boundaries) to enhance delineation and consistency.
- Vector parcels carry extensive metadata and a “ProbList” of top spectral classes (for transparency and later reversion if needed).

## Production workflow and methods
- Image pre-processing: multi-sensor composites (summer–winter) with cloud masking, atmospheric correction, geo-registration, and topographic correction.
- Image segmentation and integration: segmentation on composites, integrated with cartographic parcels and agricultural boundaries.
- Image classification: parcel-based supervised maximum likelihood classification using numerous composites; iterative refinement with training data; ProbList captured for each parcel.
- Knowledge-based enhancements (KBEs): seven automated rules applied to resolve spectral confusion using context (urban, terrain, soils, proximity to coast) and applied sequentially.
- Post-processing and QA: manual edits, hole-filling with auxiliary data, and validation against ground-reference data and Countryside Survey (CS) data.
- Change mapping considerations: challenging due to differing class structures across LCM2000/1990/2007; spectral change detection limited by classification error and lack of robust separation methods.

## Knowledge-based enhancements (KBEs)
- Purpose: resolve spectral confusion and improve thematic resolution toward BH classifications.
- Inputs: contextual data such as urban/coastal boundaries, terrain, soil types, and coastal proximity.
- Output: KBEs modify a portion of parcels; original spectral classifications remain accessible via the ProbList to enable user-controlled adjustments.
- KBEs support differentiation among grassland types (Acid/Calcareous/Neutral) and help separate semi-natural grasslands from Improved Grassland.

## Validation, accuracy, and comparison with Countryside Survey
- Ground reference validation: 9,127 polygons (2006–2008); overall LCM2007 accuracy ~83%; class-level accuracies vary (e.g., Bog high producer accuracy but low user accuracy; Neutral Grassland often problematic).
- Countryside Survey (CS) comparison (2007): GB broad habitat correspondences at 62% (BH level) and 76% (BHA level); grassland classifications show substantial variability due to one-to-many relationships; aggregation of grassland types improves correspondence.
- Key differences explained: temporal mismatches and how “Arable and Horticulture” is mapped (including boundary/linear features and temporary grass considerations); boundary features in CS vs MMU-driven LCM mappings; spectral variability and misclassification of arable areas due to multi-year image stacking.
- Fen, Marsh and Swamp shows large discrepancies due to complexity and small patch sizes; many CS Fens map to rough grassland or acid grassland in LCM2007.
- Country- and region-level results vary due to habitat distributions and CS mapping approaches.

## UK Land Cover distribution (4.4)
- UK-wide: more than 50% intensive land use (Arable and Horticulture plus Improved Grassland) or built-up areas; woodlands ~12% (split between Broadleaved and Coniferous).
- Scotland holds a larger share of Montane and Coniferous Woodland; England shows higher intensive land use; Northern Ireland and Wales vary in semi-natural vs intensive land uses.
- LCM2007 versus LCM2000: notable differences in arable and semi-natural grasslands; conifer changes; urban area representation slightly reduced in LCM2007.
- CS vs LCM2007 comparisons reveal substantial differences in some broad habitats due to data structure and scale.

## Access, licensing, and reuse
- 1 km raster data accessible via the CEH Information Gateway (URL provided in the document).
- Full vector product and 25 m raster product available on request under license from CEH; licensing fees may apply.
- Data suitable for habitat monitoring, policy development, and environmental planning; rich metadata supports traceability and audit.

## Practical guidance for data stewards
- Data governance and provenance: LCM2007 emphasizes extensive provenance, with detailed metadata and documentation of processing steps and KBEs.
- Metadata and lineage: maintain and publish polygon-level lineage, including original spectral classifications (ProbList) and KBEs history.
- Access controls and licensing: follow CEH licensing; prefer 1 km rasters for broad analyses; manage 25 m and vector data via licensing terms.
- Update and maintenance: KBEs and the spatial framework provide flexibility for future updates with improved imagery and datasets; plan for change-detection enhancements.
- Validation and quality assurance: use ground-truth data where feasible; utilize CS or similar benchmarks to quantify uncertainty across habitat classes.
- Data governance implications: balance spectral information with contextual knowledge; document KBEs and decisions to enable reproducibility and auditability.

## End-to-end takeaways
- LCM2007 delivers a comprehensive, coast-to-coast UK land cover map aligned with Broad Habitats, leveraging a reusable spatial framework derived from national cartography and enhanced by segmentation and knowledge-based rules.
- Combines spectral data with contextual information (soil, terrain, urban proximity) to improve classification, though some habitats remain challenging due to spectral similarity and landscape complexity.
- Provides robust provenance, versioning, and clear pathways for access and licensing, supporting policy, planning, and environmental monitoring while highlighting areas requiring cautious interpretation (e.g., Arable, Fen, and Grassland classes).