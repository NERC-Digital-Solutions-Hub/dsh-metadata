# Final Report for LCM2007 - the new UK land cover map

- A UK-wide, parcel-based land cover map (LCM2007) with accompanying 25 m raster and 1 km raster products, aligned to Broad Habitats to support environmental monitoring, habitat assessment, and policy evaluation over time.
- Outputs include:
  - Vector parcels with detailed metadata (processing history, training, KBEs).
  - 25 m raster with 23 LCM2007 classes.
  - 1 km raster products (percentage cover and dominant class) for 23 classes and 10 aggregates.
  - 0.5 ha minimum mappable unit; GB and NI stored as separate databases.
- Scale and framework:
  - Based on detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) to improve spatial consistency and integration with other data.
  - Object-based parcels enhanced with knowledge-based rules (KBEs) to improve thematic resolution, particularly for grasslands and montane/bog transitions.

## Key issues: dissimilar area estimates vs Countryside Survey (CS)

- Dissimilar area estimates (UK CS 95% confidence bounds) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Likely causes:
  - Differences in what is classified as Arable and Horticulture (e.g., temporary grass and uncropped land included in LCM’s Arable/Horticulture).
  - Spectral confusion due to varied crop types and growth stages; temporal range of imagery affects spectral signatures.
  - Inclusion of Boundary and Linear Features in LCM areas versus CS boundary mapping, inflating field-area estimates in LCM.
  - Grassland misclassifications: one-to-many mappings to Broad Habitats; Improved/Neutral/Calcareous/Acid grasslands variability.
  - KBEs and terrain/soil data reclassifications influence grassland and montane classifications.
  - Fen, Marsh and Swamp is highly mosaic and small-scale; CS vs LCM structural differences explain large discrepancies.
- Result: CS and LCM2007 provide different pictures of UK land cover depending on class, scale, and method; both offer complementary views.

## UK-wide comparisons and totals (LCM2007 vs CS 2007)

- LCM2007 shows over 50% of the UK in intensive land uses (Arable + Improved Grassland) or Built-up Areas/Gardens; main semi-natural areas are woodlands and montane/grassland types.
- England tends to have the highest percentage of intensive land use; Scotland has the highest share of semi-natural/woodland and montane types.
- Fen/Marsh/Swamp and some upland classes show large discrepancies due to their spectral ambiguity and small patch sizes relative to the mapping unit.

## Change detection and interpretation

- LCM2007 introduces a common UK spatial framework, enabling better comparison over time and with other data sources, but direct change detection with earlier CEH maps is complex due to:
  - Different spatial structures (parcel-based vs prior segment/pixel approaches).
  - Thematic shifts (Broad Habitats and KBEs) and differences in boundary definitions.
- Recommended approaches for monitoring change:
  - Use aggregated or cross-wound classes to reduce misinterpretation from framework differences.
  - Consider trajectory analyses that focus on consistent, reliably mapped classes.
  - Reconcile earlier maps by re-organising into a common spatial structure based on real-world land-use units.

## Data access and formats

- 1 km raster data (aggregates and percentages) available via CEH Information Gateway.
- Full 25 m vector and 25 m raster data available under licence on request from CEH.
- Licences may apply; some datasets require permissions.

## Implications for environmental monitoring and policy

- Provides a consistent, UK-wide frame for habitat monitoring, biodiversity assessment, ecosystem services, landscape planning, and catchment management.
- Enables multi-source data integration and change detection with explicit documentation of processing steps and KBEs.
- Supports linking land cover to Broad Habitats and policy frameworks, while allowing user-driven adjustments to KBEs or class definitions when needed.
- Facilitates cross-country comparisons and assessments of naturalness in river catchments and other policy-relevant areas.

## Relationship to European and national data and policy

- UK component of Corine Land Cover 2006 derived from LCM2007 vector with generalisation and thematic transformations.
- Aligns with European data programs (Corine, LUCAS) and EU-scale monitoring efforts, providing a robust national base for broader assessments.

## Data quality, validation, and interpretation guidance

- LCM2007 includes rich parcel-level metadata and probability distributions for top spectral variants, enabling targeted validation at the location of interest.
- Bespoke validation acknowledges that “fit for purpose” depends on use; cross-validation with field surveys (Countryside Survey) provides context for interpretation.
- The 1:1 accuracy varies by habitat type; grassland, fen, montane and boundary features present particular challenges.

## Notable features and future directions

- KBEs improve the resolution of grassland sub-types and montane habitats using contextual and ancillary data (soil, terrain, urban context).
- The generalised spatial framework improves efficiency for future national land cover mapping and monitoring, supporting robust change detection with a common structure.
- Opportunities exist to integrate additional data (e.g., sub-surface soil data, climate, LiDAR) to further refine specific habitat delineations and improve change-tracking capabilities.

Appendices and related material (summary)

- Broad Habitat Association (BHA): rules for aligning LCM2007 classes with Countryside Survey broad habitats, including caveats for tricky mosaics (bog, fen, grassland, montane, water, and built-up areas).
- Bespoke validation: methodology for user-driven, location-specific quality checks and probabilistic assessments using high-resolution imagery and KBEs.
- Example datasets and metadata: descriptions of vector and raster products, class codes, KBEs, and processing history to support reproducibility and QA.