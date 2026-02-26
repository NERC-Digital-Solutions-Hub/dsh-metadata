# Final Report for LCM2007 - the new UK land cover map

## Overview
- CEH-produced UK Land Cover Map 2007 (LCM2007), the third national map, delivering a continuous parcel-based (vector) dataset plus raster products.
- Maps 23 Broad Habitat classes (LCM2007 classes) with aggregates to 10 groups; supported by extensive metadata and provenance.
- Provides coast-to-coast UK coverage and supports habitat monitoring, landscape planning, biodiversity policy, and related analyses.
- Products include: 25 m raster (23 classes), 1 km summary rasters, and a vector parcel data product with rich attributes.

## Data structure, provenance and governance
- Vector product: land parcels (polygons) with attributes such as area, training and source images, Broad Habitat (BH), Broad Habitat sub-classes, FieldCode, KBE history, ProbList, CorePixels, Construct, and other processing details.
- Raster products: 25 m (23 classes) and 1 km (dominant class and/or percent cover per 1 km pixel), derived from the vector dataset.
- Provenance: complete processing lineage, including segmentation, spectral classification (maximum likelihood), KBEs, and knowledge-based history; extensive metadata ensure traceability and reproducibility.
- Spatial framework: built on high-resolution national cartography (Ordnance Survey MasterMap and Large-Scale Vector) for robust integration with other national data.
- Data governance and access: data licensed via CEH with a mix of sources; 1 km rasters openly accessible via CEH Information Gateway; full vector and 25 m products available on request (licence may apply).

## Methodology and data processing
- Pre-processing and segmentation: cloud masking, atmospheric correction, geo-registration; multi-date image composites assembled for robust classification.
- Classification: parcel-based with a maximum-likelihood approach; 0.5 ha minimum mapping unit (MMU); core pixels used to train and derive segment statistics.
- Knowledge-Based Enhancements (KBEs): seven automated rules (terrain, soils, urban context, coastal/terrestrial context, vegetation/water cues, etc.) applied post-classification to resolve spectral ambiguities and to reassign ~20% of parcels to more probable classes; preserves traceability via ProbList and KBE history.
- Change and update: designed to support updates and explainability; documentation of processing steps aids future change detection and governance.

## Knowledge-based enhancements (KBEs)
- Resolve spectral confusion and improve thematic resolution by incorporating contextual data (terrain, soils, urban context, coastal/terrestrial cues, water, etc.).
- Sequenced application converges toward “truth” while preserving original spectral signatures for traceability and potential reversion.
- Enable refined mappings (e.g., Montane Habitats, various grassland types) with maintained linkages to original data.

## Quality assurance, validation and accuracy
- Ground reference data: 9,127 points collected 2006–2008 for training and validation.
- Overall accuracy: ~83% across LCM2007 classes, with substantial variation by class.
- Class-specific notes:
  - High producer accuracy: Bog (~93%), Improved Grassland (~89%), some grassland categories.
  - Notable issues: Neutral Grassland relatively low producer accuracy; Calcareous/Acid grassland distinctions; Montane and some coastal/montane classes challenging.
  - Fen, Marsh and Swamp: large discrepancies with Countryside Survey (CS) 2007 due to spectral complexity and mosaic nature; CS often records these areas as Rough Grassland or Acid Grassland in CS data.
- Comparisons with Countryside Survey (CS) 2007:
  - Similar-to-CS and dissimilar areas identified (e.g., Arable and Horticulture, Acid/Calcareous/Neutral Grasslands, Dwarf Shrub Heath, Montane, Fen/Marsh/Swamp, etc.).
  - Key causes of differences include: classification definitions, spectral variability, boundary/linear feature inclusion in LCM vs CS, patch size and MMU effects, and how grassland subtypes are represented spectrally.
  - Grassland category comparisons are particularly problematic due to one-to-many relationships between observed grass and Broad Habitat categories; KBEs and Broad Habitat Association rules were developed to address these.
- Practical implication: use class-specific accuracy when applying LCM2007 for policy or management decisions; be cautious with grassland and fen-related classes and when comparing with CS or other datasets.

## UK-wide and national distribution (LCM2007 vs Countryside Survey)
- UK distribution: over 50% of land in intensive use (Arable and Horticulture plus Improved Grassland); ~12% woodlands; about 30% semi-natural; remaining fractions include coastal, semi-natural grassland, and montane/bog areas.
- Country-level differences: England shows the highest share of intensive land use; Scotland has the largest proportion of Coniferous Woodland and the highest share of montane/semi-natural habitats; NI and Wales show distinct patterns in grasslands and built-up areas.
- Compared with LCM2000: LCM2007 shows higher Arable and Horticulture and lower unrecorded or coastal features in some aggregates; differences may be driven by temporal composites, spatial framework changes, and updated KBEs.

## Practical implications for data stewards and governance
- Provenance and metadata: LCM2007 provides an auditable processing chain, including image dates, sensors, segmentation steps, KBEs, and class mappings; essential for reproducibility and auditing.
- Change mapping: edition-to-edition change is difficult to robustly map due to changes in class definitions and spatial structure; aggregation or reclassification strategies are recommended for robust change detection.
- Spatial integration: continuous UK vector with strategy to produce nationwide, coherent boundaries; nine-chunk production with priority rules reduces boundary inconsistencies.
- Licensing and rights management: data are sourced from multiple licensing streams; users must observe attribution and rights for each component; access levels differ by product (vector/25 m vs 1 km rasters).
- Usage guidance: LCM2007 excels for habitat monitoring, landscape planning, and policy support; users should consult class-specific accuracy and consider activity-specific knowledge-based improvements when aggregating or linking to CS or other datasets.

## Key takeaways for data management and governance
- LCM2007 delivers an auditable, multi-product land-cover framework with strong provenance, knowledge-based enhancements, and integration of diverse national data sources.
- KBEs and contextual data improve classification while preserving traceability of decisions; the product is designed for reproducibility and future reuse.
- Accuracy is strong for several classes but varies notably by habitat, with grassland and fen-related classes presenting the largest challenges; this should guide use in policy and management.
- Access is governed via CEH with clear licensing channels; dissemination options include open 1 km rasters and licensed vector/25 m data; users should plan for attribution and rights management when integrating with other datasets.
- The dataset is intended to support national-scale habitat monitoring, policy evaluation, and cross-country comparisons, including European products like Corine, while acknowledging differences in spatial structure and classification schemes.