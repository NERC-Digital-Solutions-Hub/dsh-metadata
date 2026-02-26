# Final Report for LCM2007 - the new UK land cover map

- Focus: compare LCM2007 with Countryside Survey (CS) 2007, outline area estimates, data strengths/limitations, and describe data products and access.
- Context: LCM2007 provides a continuous parcel-based UK land cover map with vector (parcels) and raster products (25 m and 1 km), designed to support habitat monitoring, policy, and landscape planning.

## Similar area estimates (4.3.2)

- Similar results are defined as classes whose areas fall within Countryside Survey (CS) UK 95% confidence limits.
- Similar area estimates were found for:
  - Broadleaved woodland
  - Acid grassland
  - Inland rock

## Dissimilar area estimates (4.3.2)

- Dissimilar results fall outside CS 95% confidence limits.
- Dissimilar areas occurred for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key factors driving differences:
  - Differences in what CS vs. LCM2007 classify as “Arable and Horticulture” (e.g., inclusion of Boundary/Linear Features in LCM2007).
  - Spectral confusion in the Arable/Horticulture class due to wide crop diversity and multi-year imagery, leading to overestimation in some regions.
  - Boundary/linear features in CS maps often below LCM MMU; LCM2007 tends to incorporate those into adjacent field polygons, inflating certain arable/grassland areas.
  - Grassland-related discrepancies: LCM2007’s Improved vs. Neutral Grassland differ from CS classifications, influenced by soil data and spectral signatures.
  - Dwarf Shrub Heath vs. Bog differences largely due to allocation between habitats.
  - Montane habitats are poorly represented in CS, thus larger discrepancies for Montane vs. CS estimates.
  - Fen, Marsh and Swamp (CS vs. LCM2007) show large differences due to the mosaic nature of Fen and small patch sizes; LCM2007 may reclassify many Fen portions as Rough Grassland or Acid Grassland.

- Illustrative notes:
  - Arable and Horticulture: CS UK 2007 estimate (~46,574 km2) is within CS 2007 bounds; LCM2007 (~63,005 km2) exceeds CS upper bound (~51,276 km2). Differences partly due to what CS counts as arable vs. horticulture vs. temporary grass and uncropped land in LCM2007; multi-year imagery increases fields changing between temporary grass and arable, affecting spectral signatures.
  - Boundary features: CS maps boundaries/linear features not always mapped by MMU, whereas LCM2007 integrates many boundaries into adjacent field polygons, enlarging field areas in LCM2007.
  - Grassland: LCM2007’s Rough Grassland includes mixes of several grassland types; this contributes to differences in how Grassland classes map to CS categories.

## Change mapping and temporal considerations (4.3.3)

- Change mapping is complex due to:
  - Shifts in class definitions across 1990, 2000, 2007 maps.
  - Differences in spatial frameworks and map boundaries.
  - Classification error rates (~20%) complicating true change detection.
- No robust, established method to reliably separate real change from mapping error at Broad Habitat level yet.
- Recommendation: consider reorganising earlier CEH maps into a common spatial structure based on real-world land-use units; use aggregated class changes, or focus on consistently mapped classes; apply statistical trajectory approaches to identify implausible changes.

## UK Land Cover distribution (4.4)

- Summary: UK land cover shows over 50% in intensive land use (Arable + Improved Grassland) or Built-up Areas; remaining area is semi-natural.
- Forests/woodlands: about 12% (split roughly equally between Broadleaved and Coniferous woodland).
- Semi-natural: 30% (including Coastal, Semi-natural Grassland, Mountain, Heath, and Bog).
- Country-specific patterns:
  - England: highest intensive land use (~76%; ~40% Arable, ~27% Improved Grassland, ~9% Built-up Areas/Gardens).
  - Northern Ireland and Wales: about 64% intensive land use (Improved Grassland + Arable + Built-up Areas/Gardens).
  - Scotland: lowest intensive land use (~36%), but largest share of Coniferous Woodland; substantial semi-natural land (36% Mountain/Heath/Bog; 20% semi-natural grassland).
  - Freshwater distribution varies (England/Wales ~1%, Scotland ~2%, NI ~4%) due to features like Lough Neagh.
- Comparative note: LCM2007 vs LCM2000 differences show shifts in Arable and Grassland proportions; spatial framework changes contribute to interpretation challenges.

## Data products and access (5.x)

- Data products:
  - Vector product: parcel polygons with 10 attributes detailing processing history (Construct, ProbList, KBE) and final class, plus Broad Habitat sub-classes and field codes.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: 
    - A) Percent cover per 1 km pixel for each LCM2007 class.
    - B) Dominant class per 1 km pixel.
  - 1 km outputs also include aggregate class summaries.
- Metadata and quality:
  - Vector includes extensive processing history; KBEs and ProbList aid evaluation.
  - KBEs allow reverting to pre-KBE classifications via attributes, enabling interpretability and revalidation.
- Access:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster data available on request under licence from CEH; licence fees may apply.
- Validation and QA:
  - Ground reference validation used 9,127 CEH polygons; overall LCM2007 accuracy reported around 83%.
  - Class-specific accuracies vary; some classes (e.g., Fen, Marsh, Swamp) show QA improvements when validated against spatially matched polygons.

## Validation with Countryside Survey (CS) and Broad Habitat Association (4.5; Summary)

- Two CS-LCM2007 comparison approaches:
  - Comparison at the 1 km square level using CS 2007 Broad Habitats.
  - Comparison of national CS estimates with LCM2007 Broad Habitats.
- Key takeaways:
  - Agreement between LCM2007 and CS varies widely by Broad Habitats.
  - Grassland is particularly challenging due to one-to-many relationships between observed grass and Broad Habitats; leading to the development of Broad Habitat Association (BHA) rules to improve thematic accuracy beyond the Broad Habitat level.
  - LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture at the 1 km level, but overall Broad Habitat extent estimates differ, with Arable showing notable overestimation in LCM2007.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude due to mosaic nature, small patch sizes, and differing treatment of Fen across products.
- Conclusions:
  - Agreement with CS depends on the habitat type and the level of aggregation.
  - BHA rules help reconcile some cross-habitat correspondences and improve cross-product comparability.

## Methodological and governance notes (Appendices)

- Broad Habitat Association (BHA) Appendix explains rationale and rules for cross-walking LCM2007 classes to CS Broad Habitats, addressing edge-case mosaics and upland transitions (Bog, Dwarf Shrub Heath, Montane Habitats, Water classes, etc.).
- Bespoke validation approach (Appendix 4) emphasizes “fit for purpose” validation, using parcel-level metadata and a Bayesian-like informal method to assess plausibility of classifications against high-resolution imagery.
- Data provenance and metadata: LCM2007 vector includes CorePixels, ProbList, KBE, and Construct fields; multiple KBEs applied to improve classification in context (terrain, soils, urban proximity, coastal proximity, etc.).
- Appendix 1–3 demonstrate the detailed satellite imagery, processing steps, and example datasets used to derive products, highlighting the scale, segmentation, and asset-level attributes.

## Overall takeaway for data support and use

- LCM2007 provides the first UK-wide, continuous parcel-based land cover map with robust cross-boundary consistency and a set of derived raster products suitable for national to sub-national analyses.
- The dataset improves integration with other national products and supports change detection, policy analysis, habitat connectivity, and ecosystem assessment, but users should be cautious of habitat-specific discrepancies with CS data, especially for grassland, fen, montane, and boundary features.
- The combination of high-resolution vector data, comprehensive metadata, and Broad Habitat associations offers a flexible, transparent framework for validation and for tailoring analyses to specific policy or planning needs.
- Access: 1 km rasters publicly accessible; full vector/25 m rasters available under licence; ongoing opportunities to refine classifications and validation through integrated data sources and methodological advances.