# Final Report for LCM2007 - the new UK land cover map

## Overview
- Presents UK-wide land cover mapping (LCM2007) based on multi-temporal satellite imagery, integrated with national cartography, and designed for wide policy and environmental applications.
- Aims to provide a continuous UK, GB, and country-level view of Broad Habitats to support biodiversity monitoring, landscape planning, and policy reporting, while enabling change detection and integration with other data sources.

## Data Governance, Provenance, and Spatial Framework
- Spatial framework and data structure
  - UK-wide vector polygons derived from generalised national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) with multiple generalisation steps to align with remote-sensing resolution.
  - 0.5 ha minimum mapping unit; boundaries may differ from field-based surveys, affecting area estimates for some habitats.
- Provenance and metadata
  - Each polygon carries extensive provenance: source images, spectral classification history, processing steps, and knowledge-based enhancements (KBEs).
  - KBEs include automated rules that refine class assignments using contextual/ancillary data (urban boundaries, soils, proximity to coast/terrain).
- Knowledge-Based Enhancements (KBEs)
  - Seven automated rules addressing spectral confusion and increasing thematic resolution; applied sequentially with traceable polygon attributes.
  - Terrain/soil rules re-run after the initial pass to improve final classifications; full processing traceable via polygon attributes (Construct, KBE history, ProbList, etc.).
- Data management and interoperability
  - Continuous UK vector coverage with GB/NI split; emphasis on reproducibility, versioning of KBEs, and documentation to support audits and future updates.
  - MMU/MFW decisions (0.5 ha; 20 m) critical for user understanding of resolution and change-detection capabilities.
- Access and licensing
  - 1 km rasters available via CEH Information Gateway; full vector and 25 m products available on request (licensing and fees may apply).

## Data Products and Access
- Core data products
  - Vector: land parcels with attributes such as area, source images, Broad Habitat, and processing history (polygon construction, original spectral classification, KBE history).
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: UK-wide summaries per pixel (percentage cover and dominant class) for each LCM2007 class.
- Classification scheme and resolution
  - 23 LCM2007 classes mapped to Broad Habitat framework; 0.5 ha MMU; land cover mapped (not land use).
- Documentation and transparency
  - Rich metadata at parcel level supports validation and traceability; users encouraged to validate Broad Habitat sub-classes and ProbList outputs for their specific use cases.

## Data Production and Processing
- Image sources and processing
  - Multi-temporal composites created from Landsat, SPOT, LISS-III, and AWIFS imagery; atmospheric and topographic corrections applied; segmentation used to delineate land-cover objects.
- Classification and enhancements
  - Parcel-based supervised classification (maximum likelihood) with training areas from ground references.
  - KBEs applied to resolve spectral confusion and improve thematic resolution; knowledge about terrain, soils, urban areas used to adjust classifications.
- UK segmentation and assembly
  - Nine UK chunks defined to manage processing; merging and generalisation performed to maximise spectral similarity and reduce misclassification.
- Validation data and accuracy
  - Ground reference validation used to assess accuracy; CEH reported overall accuracy around 83% across LCM2007 classes in QA discussions (class- and habitat-specific accuracies vary).

## Quality Assurance, Validation, and Comparisons
- Ground-truth and CS cross-validation
  - Use of 9127 CEH ground reference points for validation; overall accuracy around 83% for LCM2007 classes; class-level accuracies vary by habitat type.
  - Comparisons with Countryside Survey (CS) 2007 at both 1 km square and national extent levels show mixed agreement across Broad Habitats.
- Key areas of divergence
  - Arable and Horticulture: CS UK total area lower than LCM2007; differences attributed to what is classified as Arable/Horticulture, spectral variability, and inclusion of boundary/linear features in LCM2007.
  - Grasslands: Improvements via Broad Habitat Association rules but remaining challenges due to one-to-many relationships between observed grass cover and multiple Broad Habitats.
  - Fen, Marsh and Swamp: Large disparities (CS 2007 vs. LCM2007) due to mosaic nature, small patch sizes, and differing mapping approaches; CS patches below MMU contribute to differences.
  - Montane, coastal, and aquatic/water classes: poorer CS representation and contrasting LCM2007 mappings lead to country- and habitat-specific discrepancies.
- Implications of comparisons
  - CS scaling-up methods and patch-size effects influence UK-wide estimates; results emphasize the need for careful interpretation when comparing products with different spatial/thematic structures.
  - The Broad Habitat Association rules provide improved interpretability but do not fully resolve all cross-product discrepancies.

## 4.5 Summary and Discussion (Key Insights for Data Stewards)
- Agreement between LCM2007 and CS varies widely by Broad Habitat; grassland classifications remain particularly challenging.
- KBEs and a common spatial framework enhance reproducibility and interpretability but require thorough documentation and version control for ongoing governance.
- LCM2007 aligns strongly with CS in certain areas (e.g., Arable and Horticulture on a 1 km CS basis) but generally reports higher Arable/Horticulture extents at the Broad Habitat level.
- Fen, Marsh and Swamp areas show order-of-magnitude differences due to classification complexity and patch sizes; potential for future KBEs to reallocate some areas to Fen, Marsh and Swamp.
- For data stewards, the emphasis is on robust provenance, clear documentation of KBEs, consistent metadata, and careful planning for updates and change detection within a unified spatial framework.

## Practical Guidance for Data Stewards
- Provenance and metadata
  - Maintain detailed records of KBEs applied, their versions, input datasets, and processing steps to enable auditability and reproducibility.
  - Use parcel-level ProbList and KBE history to inform quality assessments in location-specific contexts.
- Interoperability and standards
  - Ensure harmonised metadata schemas across GB/NI/Wales/England, with clear notes on MMU and MFW decisions.
  - Consider using Broad Habitat Associations when comparing with CS outputs to improve comparability.
- Access, licensing, and sustainability
  - Plan for licensing considerations and potential fees; document access pathways and data-use restrictions.
  - Establish processes for updates and future LCM iterations, ensuring that the generalised spatial framework remains a stable basis for change detection.
- Use and interpretation
  - Be aware of spectral confusion in complex habitats (notably arable, grassland, fen-related habitats) and communicate associated uncertainties.
  - Use aggregated classes or BHAs where appropriate to align with other monitoring programs and to reduce class-level confusion in stakeholder communications.
- Change detection and future work
  - Recognise the difficulties in direct change detection across different LCM generations; prioritise aggregated changes or trajectory-based methods.
  - Explore opportunities to reclassify or reallocate certain transitional habitats with KBEs to improve cross-product consistency in future updates.

## Key Takeaways
- LCM2007 delivers a comprehensive, governance-friendly UK land cover map with rich provenance, extensive metadata, and a robust approach to integrating national cartography with multi-temporal imagery.
- While overall accuracy is solid, specific habitat classes (notably various grasslands and fen-related habitats) exhibit notable variability and cross-product differences, necessitating careful interpretation and potential aggregation for comparability.
- Data stewards should leverage the detailed provenance and KBEs, maintain rigorous documentation and versioning, plan for licensing and updates, and apply appropriate aggregation or BH-Association frameworks to maximize governance and utility across sectors.