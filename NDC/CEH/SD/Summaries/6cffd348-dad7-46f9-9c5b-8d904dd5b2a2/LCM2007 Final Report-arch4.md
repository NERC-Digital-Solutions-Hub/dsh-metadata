# Final Report for LCM2007 - the new UK land cover map

- The document presents UK-wide land cover mapping for 2007 (LCM2007), comparing it with the Countryside Survey (CS) 2007, and detailing data products, validation, and usage implications for policy and practice.
- LCM2007 is a parcel-based land cover map aligned with Broad Habitats (BH) and BH associations, integrating national cartography with multi-temporal satellite imagery, and supported by knowledge-based enhancements (KBEs).

## 4.3.2 Similar area estimates and 4.3.2 Dissimilar area estimates (CS vs LCM2007)

- Similar area estimates (within CS 95% confidence limits UK): 
  - Broadleaved woodland, Acid Grassland, and Inland Rock.
- Dissimilar area estimates (outside CS 95% limits UK): 
  - Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; coastal habitats.
- Specific discussion highlights:
  - Arable and Horticulture: CS UK estimate ~46,574 km2 vs LCM2007 ~63,005 km2 (or 46,090 for arable + 1,690 horticulture in LCM2007). Differences attributed to classification definitions, spectral confusion, inclusion of boundaries/linear features in LCM2007, and temporal multi-year imagery affecting land-change signals (temporary grass vs arable).
  - Spectral confusion in Arable; broad range of crops and growth stages cause misclassifications.
  - Boundary and Linear Features: CS maps many boundaries; LCM2007 MMU (0.5 ha) suppresses some boundaries, leading to field-size differences.
  - Improved/Neutral Grassland: LCM2007 shows about 10,000 km2 more Improved Grassland and 10,000 km2 less Neutral Grassland than CS—differences reflect field-level spectral signatures and field-level species composition not captured by KBEs.
  - Dwarf Shrub Heath vs Bog: differences largely due to allocation between these habitats; Montane and coastal habitats are poorly represented in CS, so differences are expected.
  - Fen, Marsh and Swamp: CS 2007 estimates are an order of magnitude higher than LCM2007; Fen areas are mosaics or small patches hard to identify spectrally; many CS Fen areas appear as Rough Grassland or Acid Grassland in LCM2007. QA discussions emphasize spatial structure and patch size effects.
- Overall interpretation: CS estimates are influenced by field-based delineation and scaling methods; LCM2007 emphasizes spectral-based mapping with a harmonised spatial structure, leading to systematic differences in several key classes.

## 4.4 UK Land Cover

- Summary of UK-wide land cover: more than 50% of the UK is intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas; about 12% Broadleaved/Mixed/Yew woodland; 12% Coniferous woodland; remaining areas semi-natural (coast, semi-natural grassland, mountain/heath/bog, etc.).
- Country breakdown:
  - England: highest intensive land use (76%: 40% Arable + 27% Improved Grassland + 9% Built-up).
  - Northern Ireland and Wales: around 64% intensive land use (Improved Grassland + Arable + Built-up).
  - Scotland: lowest intensive land use (36%), but highest Coniferous Woodland; major share of semi-natural habitats (36% Mountain/Heath/Bog; 20% semi-natural grassland).
- Comparisons with LCM2000:
  - LCM2007 shows higher Arable (26%) and lower Grassland (13% semi-natural) than LCM2000 (23% Arable; 17% semi-natural grassland); minor changes in woodland and urban areas.
- Table 4.8 (Broad Habitats vs CS 2007: UK totals and country-level comparisons) highlights where LCM2007 falls within CS confidence limits or exceeds them, illustrating varying levels of agreement across habitats and countries.

## 4.5 Summary and discussion

- Agreement between LCM2007 and CS varies widely by Broad Habitat; grassland categories are particularly challenging due to one-to-many relationships between observed grass and BH classifications.
- Broad Habitat Association (BHA) rules were developed to improve correspondence at BH Associations, in addition to BH and Aggregate class levels.
- Key findings:
  - High correspondence between LCM2007 and CS 2007 for Arable and Horticulture at the 1 km square level; however, UK-wide BH extent estimates for Arable and Horticulture tend to be higher in LCM2007.
  - Fen, Marsh and Swamp shows large UK differences due to complex mosaics and small patch sizes; many CS Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Montane, coastal habitats show CS data limitations; differences are expected.
- Implications for data strategy:
  - LCM2007 uses a robust framework that combines national cartography with multi-date imagery; KBEs help resolve spectral ambiguities.
  - Change detection is constrained by differences in spatial and thematic structure between LCM generations; cross-dataset reconciliation remains essential.
  - Future work could leverage KBEs to re-allocate some grassland areas to Fen, Marsh and Swamp using supplementary data.
- Overall guidance for application:
  - LCM2007 provides a consistent UK-wide base for habitat monitoring with strong policy relevance, but users should be aware of class-definition differences and apply BH/BHA mappings and validation as appropriate.
  - The project emphasizes the need for integrating high-resolution cartography with remote sensing for robust, reusable change detection and governance.

## 5.x Vector and Raster products (data structure and access)

- Vector product: land parcels (polygons) with attributes including area, source images, BH, FieldCode, KBE history, ProbList, CorePixels, Construct, etc. BHSub provides sub-classes for additional descriptive detail; provided metadata supports provenance and user-driven validation.
- Raster products:
  - 25 m raster: 23 LCM2007 classes (BH-aligned) with corresponding metadata.
  - 1 km raster: two formats per pixel:
    - Percentage cover per class (for each LCM2007 class).
    - Dominant class per pixel.
- Data access:
  - 1 km rasters are freely accessible via the CEH Information Gateway.
  - Full vector and 25 m raster require licensing/requests; license fees may apply.
- Practical considerations:
  - Vector format provides richer metadata per parcel but larger files; 25 m raster offers similar thematic detail with simpler processing.
  - The 1 km data are suitable for UK-wide modeling and integration with additional datasets (e.g., meteorological, species distribution).

## 6 Discussion (change detection context and policy relevance)

- LCM2007 represents the first continuous parcel-based UK dataset with associated raster products at multiple resolutions, enabling broad applications in biodiversity assessment, landscape planning, climate, hydrology, and policy.
- Change detection across generations (LCM1990, LCM2000, LCM2007) is not straightforward due to differing spatial structures, scales, and thematic mappings; sophisticated methods are needed to distinguish real change from methodological differences.
- LCM2007 is designed to be compatible with Countryside Survey outputs conceptually, while preserving UK-wide coverage and a reusable spatial framework for future monitoring.
- European links: LCM2007 outputs feed into Corine Land Cover mappings (via transformations), contributing to pan-European environmental assessment.
- Access and governance considerations for Data Leaders:
  - CEH provides 1 km rasters free of charge; 25 m and vector products require licensing.
  - Rich metadata and processing provenance support governance, reproducibility, and cross-organization collaboration.
- The document emphasizes integrating diverse data sources (cartography, EO, soil, climate, LiDAR, in situ surveys) to build robust, policy-relevant land information systems with clear pathways for change detection and habitat connectivity analysis.

## Practical takeaways for Data Leaders

- Build on a robust, segment-based spatial framework that combines national cartography with multi-date remote sensing to support scalable, repeatable nationwide mapping and change detection.
- Leverage knowledge-based enhancements to improve thematic resolution in heterogeneous landscapes; ensure KBEs are well-documented and auditable for governance and user adjustment.
- Maintain rich metadata and provenance, enabling auditability, reproducibility, and cross-department collaboration; ensure appropriate access controls and licensing for data sharing.
- Align product classifications with established habitat schemes (BH/BHA) to maximize policy relevance and cross-study comparability, while acknowledging limitations in spectral discrimination for complex habitats.
- Use 1 km raster products for coarse-scale national analyses and 25 m vector/raster products for detailed local work; integrate with external datasets for enhanced modeling and decision support.

## Appendices and validation context

- Bespoke validation: emphasizes “fit for purpose” assessment, parcel-level metadata, and an informal Bayesian-like approach to validate LCM2007 classifications against imagery; recommends fuzzy categories (plausible, probably, possibly) to bound accuracy estimates.
- Broad Habitat Association (BHA): outlines rationale for cross-walks between LCM2007 classes and CS/BH classifications; provides rules to improve correspondence when direct one-to-one mapping is ambiguous (e.g., Bog, Dwarf Shrub Heath, Montane Habitats, Fen, Marsh and Swamp, Rough Grassland, Water classes, tidal areas).

## Endnotes and references (context)

- The report situates LCM2007 within a historical CEH mapping lineage (LCM1990, LCM2000) and the Countryside Survey program, with connections to UK Biodiversity Action Plans and European datasets (Corine, LUCAS).
- The document acknowledges ongoing and future work to improve cross-dataset reconciliation, change detection, and integration with policy-relevant habitat networks and ecosystem services analyses.