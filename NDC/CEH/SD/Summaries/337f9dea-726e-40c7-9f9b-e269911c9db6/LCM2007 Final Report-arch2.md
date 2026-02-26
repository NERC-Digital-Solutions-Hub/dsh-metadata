Final Report for LCM2007 - the new UK land cover map

- Overview
  - LCM2007 is the UK-wide, parcel-based Land Cover Map (vector) with accompanying 25 m and 1 km raster products.
  - Built from generalised national cartography (Ordnance Survey) and multi-temporal satellite data; designed to enable repeatable UK-wide monitoring of Broad Habitats and land cover change.
  - Outputs include: 23 Broad Habitat classes (vector; min unit ~0.5 ha), 25 m raster (23 classes), 1 km raster (percent cover and dominant class), plus extensive metadata and provenance for traceability.
  - Accuracy: ground-reference validation reported overall accuracy around 83% for LCM2007 classes; class-specific accuracy varies by habitat type.

- Dissimilar area estimates versus Countryside Survey (CS) 2007 (Chapter 4.3.2)
  - Arable and Horticulture
    - CS UK estimate: 46,574 km2; LCM2007: 63,005 km2 (CS upper limit ~51,276 km2).
    - Main reasons: differences in what is classified as Arable/Horticulture; spectral confusion; inclusion of Boundary/Linear Features in LCM2007’s Arable/Horticulture area.
    - Temporal mixing: LCM2007 uses multi-year imagery; fields changing between temporary grass and arable across years inflate Arable/Horticulture area in some places.
  - Improved Grassland and Neutral Grassland
    - LCM2007 shows ~10,000 km2 more in Improved Grassland and ~10,000 km2 less in Neutral Grassland than CS.
    - Likely due to how Neutral vs Improved grassland is spectrally distinguished and, in some cases, field composition on soils; difficulty in discriminating these classes spectrally.
  - Dwarf Shrub Heath and Bog
    - Differences largely reflect allocation between these habitats; LCM2007 and CS show substantial overlap but not exact parity.
  - Montane Habitats and Fen, Marsh and Swamp
    - Montane representation linked to thresholds and extensions; Fen/Marsh/Swamp areas differ markedly due to mosaic nature of Fen and the small size of many patches.
    - Fen areas in CS often map to Rough Grassland or Acid Grassland in LCM2007, reflecting spectral ambiguity and patch size issues.
  - Boundaries and Linear Features
    - CS maps many boundaries/linear features explicitly; LCM2007 often incorporates these into adjacent field polygons, inflating arable/improved grassland extents.
  - Overall interpretation
    - Large discrepancies stem from: different spatial structures (parcel vs CS mapping), different class definitions, spectral variability, and the need to reconcile single-year CS maps with multi-year LCM imagery.
    - CS patch size and spatial structure (below MMU) can strongly influence area estimates, particularly for Fen, Marsh and Swamp and small woodland patches.

- Discussion on comparison and methodological issues (Chapter 4.3.3)
  - Agreement between LCM2007 and CS varies by Broad Habitat; grasslands are particularly challenging due to one-to-many relationships with habitat types.
  - KBEs (knowledge-based enhancements) improve thematic resolution but do not fully resolve discrepancies for all habitats.
  - LCM2007 shows high correspondence with CS 1 km squares for Arable and Horticulture, yet country-wide Broad Habitat extents differ substantially.
  - Grassland and upland mappings reflect spectral similarity and context; using a single grassland class can substantially improve correspondence (up to ~87–90%).

- UK-wide land cover distribution and cross-country patterns (Chapter 4.4)
  - UK distribution: more than 50% of land in intensive use (Arable + Improved Grassland) or Built-up areas; about 12% coniferous woodland; a large share of semi-natural areas elsewhere.
  - Country variation:
    - England: highest intensive land use (~40% Arable, ~27% Improved Grassland, ~9% Built-up).
    - Scotland: lower overall intensive use; higher Coniferous Woodland presence; largest share of semi-natural habitats (notably montane and upland types).
    - Northern Ireland and Wales: intermediate intensive use; mosaic of habitats with significant grassland and woodland components.
  - Comparison with LCM2000 indicates shifts in Arable and Semi-natural grassland proportions; spatial framework changes complicate direct year-to-year comparability.

- Products, access, and provenance (Chapter 5)
  - Data formats:
    - Vector: land parcels with attributes (area, source images, Broad Habitat, KBE history, ProbList, etc.).
    - Raster: 25 m (23 LCM2007 classes) and 1 km (percent cover and dominant class per square).
  - Provisional access:
    - 1 km raster data: CEH Information Gateway.
    - Full vector and 25 m rasters: available on request under licence from CEH (fees may apply).
  - Metadata and traceability: extensive provenance (KBE history, construct details, image sources) to support reproducibility and validation.
  - Knowledge-based enhancements (KBE): a suite of post-classification rules (terrain, soil, urban context, coastal proximity, etc.) applied to parcels to refine class assignments; applied to a subset of parcels.

- Change detection and methodological implications (Chapter 6)
  - Change mapping across LCM1990, LCM2000, and LCM2007 is not straightforward due to non-commensurate class definitions and differing spatial structures.
  - Robust separation of real habitat change from classification error remains challenging; suggested approaches include focusing on aggregated classes, consistently mapped classes, or trajectory-based analyses.
  - Recommend re-structuring earlier CEH maps into a common spatial framework based on real-world land-use units to enable clearer change detection; LCM2007’s spatial framework supports this goal.

- Implications for environmental monitoring and policy
  - LCM2007 provides a consistent, UK-wide frame for monitoring Broad Habitat extents and landscape change, supporting biodiversity assessment, habitat connectivity analyses, and policy evaluation.
  - The vector-based parcel structure with rich provenance supports integration with other data (climate, soils, hydrology, urban planning) and multi-scale analyses.
  - European and policy linkages: data contribute to Corine Land Cover mapping and other pan-European monitoring efforts; supports habitat-based policy contexts (Natura, biodiversity targets, catchment management).

- Appendices and related context
  - Broad Habitat Associations (BHA): rules linking classes across Broad Habitat categories to CS classifications, addressing edge cases and mosaics (e.g., Fen vs. Grassland, Bog vs. Dwarf Shrub Heath).
  - Appendix materials provide definitions for Broad Habitats, satellite data sources, and validation approaches; useful for understanding classification decisions and uncertainties.

- Bottom line
  - LCM2007 delivers a high-quality, parcel-based UK land cover map with robust raster counterparts, designed for standardized monitoring and change detection.
  - Real-world monitoring requires careful interpretation of dissimilarities with Countryside Survey, especially for grasslands, fen-related habitats, and boundary features, as well as an appreciation of the impacts of using multi-year imagery and differing spatial structures.
  - The product suite enables nationwide analyses, supports policy-relevant habitat assessments, and provides a solid foundation for future land cover monitoring and integration with other environmental data.