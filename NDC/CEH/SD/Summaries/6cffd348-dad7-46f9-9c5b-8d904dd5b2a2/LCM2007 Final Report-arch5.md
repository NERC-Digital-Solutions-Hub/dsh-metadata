# Final Report for LCM2007 - the new UK land cover map

## Key overview for Data Stewards
- LCM2007 provides the first UK-wide, parcel-based land cover map with coast-to-coast coverage, spanning vector (parcels) and raster products at 25 m and 1 km resolutions.
- It supports habitat monitoring, biodiversity policy, landscape planning, ecosystem services, catchment management, and related policy development with up-to-date, framework-aligned land cover data.

## Data products and access
- Vector product: 23 Broad Habitat classes with 10 processing attributes per parcel (e.g., Construct, ProbList, KBE history).
- Raster products: 25 m resolution (23 classes) and 1 km resolution (percent cover and dominant class), enabling both detailed and broad-scale analyses.
- Access and licensing: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request with potential licensing fees.
- Metadata: Rich provenance and processing history embedded in parcel attributes (KBE history, ProbList, etc.) to support traceability and reproducibility.

## Spatial framework and data provenance
- Spatial framework derived from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector), integrated with image segments and agricultural boundaries.
- MMU and generalisation: Minimum Mappable Unit of 0.5 ha; generalisation reduces polygon density while preserving spectral context.
- Knowledge-Based Enhancements (KBEs): Automated rules applied post-classification to improve thematic resolution (e.g., grassland sub-types, montane adjustments); KBEs affect about 20% of parcels and are auditable via the KBE history in the vector attributes.
- Data lineage: Parcel-level metadata enables users to trace processing steps and assess applicability to their site-specific analyses.

## Classification approach and knowledge-based enhancements
- Parcel-based supervised classification using multi-temporal imagery (40+ composites across Landsat SPOT IRS) with ground truth references.
- Seven automated KBEs applied in sequence to resolve spectral confusion and improve thematic resolution (e.g., grassland sub-types, montane delineation, urban-adjacency considerations).
- Broad Habitat sub-classes (BHSub) and FieldCodes provide additional detail, though not all sub-classes are validated with the same certainty; users are advised to perform their own validation at the sub-class level if used.

## Quality assurance, validation, and accuracy
- Validation dataset: 9,127 CEH ground reference points; overall vector product accuracy of 83% (class-level accuracy varies by habitat).
- Producer’s vs User’s accuracy: Reported per class; notable contrasts in bog, neutral grassland, and montane habitats due to spectral ambiguity and boundary effects.
- CS (Countryside Survey) 2007 comparison: 591 CS 1 km squares used for GB-wide validation and broad-habitat analyses.
  - Key challenges: grassland misclassification due to one-to-many relationships with Broad Habitats; spectral variability causes arable/horticulture overestimation in some areas; boundary features often mapped differently due to MMU constraints.
  - Fen, Marsh and Swamp areas show large discrepancies (spectral/mosaic complexity and MMU effects).
- Implications: Agreement with CS varies by Broad Habitat; grassland typologies drive most differences; a Broad Habitat Association (BHA) framework was developed to improve cross-level correspondence.
- Change mapping: LCM2007 and CS differ in spatial structure and temporal basis; separating real change from classification or framework differences remains challenging.

## UK-wide and country-level findings (4.4)
- UK distribution: Over half the UK is intensive land use (Arable and Horticulture plus Improved Grassland) with about 12% Broadleaved woodland and Coniferous woodland; coastal, semi-natural grasslands, and uplands make up the remainder.
- Country differences:
  - England: highest intensive land use (about 64%–76% depending on class), notable built-up areas.
  - Scotland: large share of Coniferous Woodland and substantial semi-natural areas; montane and upland habitats are more prominent.
  - Northern Ireland and Wales: intermediate levels of intensive land use; distinct regional patterns in grassland and woodland.
- Comparison with LCM2000: LCM2007 shows shifts in Arable and Horticulture and semi-natural grassland percentages; some differences may relate to spatial framework changes and MMU effects.
- Detailed table/figures (CS 2007 vs LCM2007) illustrate where estimates fall inside or outside CS confidence limits, highlighting areas of agreement and discrepancy across Broad Habitats.

## Similar and dissimilar area estimates (4.3.2)
- Similar area estimates occur for: Broadleaved woodland, Acid Grassland, Inland Rock.
- Dissimilar area estimates occur for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Key drivers of differences:
  - Differences in what is classified as certain habitats (classification schemes and MMU effects).
  - Spectral confusion and temporal range issues (images from multiple years affecting spectral variability, especially for arable crops).
  - Differences in mapping of Boundaries and Linear Features and how they are incorporated into field polygons.
  - Grassland classification ambiguity: Improved, Neutral, Calcareous, and Acid grasslands can be spectrally similar; this drives misclassification and broader category allocation.
  - Fen, Marsh and Swamp areas are particularly challenging due to mosaic nature and small patch sizes; CS patches below MMU can influence comparisons.

## Change mapping and temporal considerations
- LCM datasets are temporally distinct (LCM1990, LCM2000, LCM2007) with differing spatial structures; change detection requires careful methodological alignment to separate real habitat change from product differences.
- Typical image-classification errors can be around 20%; real habitat changes are often smaller, necessitating robust change-detection methods and potential reorganization of older maps into a common spatial framework.

## Practical guidance for Data Stewards
- Use the Broad Habitat Association (BHA) framework to interpret correspondences across taxonomic levels when direct class-to-class matches are not reliable, especially for grassland-related habitats.
- When comparing with field surveys (CS), account for MMU differences, spatial granularity, and thematic resolution; simplifying grassland classes can improve comparability.
- Leverage the 1 km raster products for broad analyses and the 25 m vector product for detailed spatial applications, while respecting licensing terms where applicable.
- Leverage parcel-level KBE history and ProbList metadata to assess classification robustness and to support audit trails and reproducibility.
- Recognize limitations in discriminating certain grassland types and upland montane habitats; consider integrating additional data sources or KBEs to refine allocations (e.g., dedicated KBEs for Fen, Marsh and Swamp).

## Governance implications and data stewardship considerations
- Mature spatial framework integration requires rigorous provenance and version control; the shared spatial structure supports consistent future monitoring and change detection but demands careful tracking of boundary sources and generalisation steps.
- KBEs introduce processing steps that must be versioned and auditable (via ProbList and KBE history) to ensure reproducibility and defendability of classifications.
- Rich metadata supports data lineage, enabling users to validate and adapt the data to their specific use cases, while acknowledging uncertainties in sub-class level accuracy.
- Limitations must be communicated clearly to users, particularly regarding grassland classification, fen-related habitats, and change detection challenges.

## Appendices and supporting context (for governance and validation)
- Appendix 4 Bespoke validation: emphasizes fit-for-purpose assessment, parcel-level metadata, and informal Bayesian-style validation approaches using high-resolution imagery to gauge consistency with LCM2007 classifications.
- Appendix 5 Broad Habitat Association (BHA): outlines rules for cross-walking LCM2007 classes to Countryside Survey categories, addressing known ambiguities in Bog, Dwarf Shrub Heath, Montane Habitats, Fen, Marsh and Swamp, Rough Grassland, Water classes, and tidal areas.
- Additional habitat definitions (Appendix 1) and data descriptors (Appendix 2–3) provide contextual taxonomy, satellite imagery details, and data provenance essential for data governance and reuse.