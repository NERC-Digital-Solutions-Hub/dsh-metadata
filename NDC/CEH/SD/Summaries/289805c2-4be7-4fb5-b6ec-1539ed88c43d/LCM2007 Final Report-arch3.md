# Final Report for LCM2007 - the new UK land cover map

## Executive overview
- LCM2007 is the first continuous parcel-based UK land cover map, produced to support policy monitoring, habitat assessment, landscape planning, and ecosystem services evaluation.
- It provides UK-wide, coast-to-coast coverage with 23 land cover classes mapped to Broad Habitats (BH), using a 0.5 ha minimum mapping unit and rich polygon-level metadata.
- Outputs include a vector parcel product, a 25 m raster, and 1 km raster products (percent cover and dominant class), designed for broad policy use and integration with other datasets.
- The approach combines high-quality spatial framework from national cartography (MasterMap/LPS) with multi-temporal satellite imagery and knowledge-based enhancements (KBEs) to improve thematic resolution.

## Data sources, framework and methodology
- Spatial framework: GB-based OS MasterMap and LPS data, generalised to align with mapping units; nine UK spatial chunks enable a continuous UK vector product.
- Imagery and composites: multi-date imagery (summer and winter) from Landsat-5, Landsat ETM+, SPOT-4/5, and LISS-3; automated cloud/cloud-shadow masking; atmospheric and topographic corrections.
- Classification: parcel-based supervised maximum likelihood classification using 37 composite and 21 single-date images.
- Knowledge-Based Enhancements (KBEs): seven automated KBEs (terrain, soil, coastal/urban context, water, etc.) applied to resolve spectral ambiguities and refine habitat types; a ProbList (top five spectral classes) is retained to allow reversion if needed.
- Outputs and metadata: 23 LCM2007 classes, 10 polygon-level processing attributes (including KBE history), 25 m rasters, and 1 km rasters with percentage or dominant class summaries.
- Data access: 1 km rasters via CEH Information Gateway; vector and 25 m rasters available on request under licence.

## Validation and quality assurance
- Overall accuracy: 83% across GB for LCM2007 classes (based on 9,127 ground reference polygons).
- Producer/User accuracies vary by class; detailed matrices provided in the full report.
- Comparisons with Countryside Survey (CS) 2007:
  - CS provides field-based habitat mapping for 591 1 km squares; LCM2007 offers coast-to-coast satellite-derived extents.
  - Substantial agreement for dominant broad habitats in some areas, but notable differences in others due to methodological differences and spatial structure.
- Key interpretive framework: Broad Habitat Association (BHA) rules were developed to interpret correspondences when a single LCM2007 class could map to multiple CS habitat types.
- Why discrepancies occur:
  - Spectral ambiguity and one-to-many mappings between land cover and Broad Habitats, even with KBEs.
  - Mosaic and small patches (e.g., fen, montane, upland types) challenge spectral separation and validation.
  - Differences in how boundaries and features are represented (LCM MMU vs CS parcel delineations) and the need to combine multiple years of imagery.
  - Boundary and linear features are treated differently between CS and LCM2007 (CS includes some features below MMU; LCM2007 often aggregates them into surrounding polygons).

## Similar and dissimilar area estimates (CS vs LCM2007)
- Similar area estimates (within CS 95% confidence limits for the UK) observed for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (outside CS 95% limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Specific discussion points:
  - Arable and Horticulture: CS UK total ~46,574 km2; LCM2007 ~63,005 km2. Differences likely due to how “Arable and Horticulture” is defined (and inclusion of boundaries/linear features), spectral variability across multi-year imagery, and temporary grassland being mapped as arable in some years.
  - Boundary/Linear Features: CS maps many boundaries/lines; LCM2007 often includes these within field polygons, inflating arable/grassland areas.
  - Improved/Neutral Grassland: LCM2007 tends to show larger Improved Grassland and smaller Neutral Grassland areas than CS; spectral similarity and soil context play a role.
  - Dwarf Shrub Heath, Bog, Fen/Marsh/Swamp: CS shows larger, mosaic fen areas; LCM2007 often maps many fen elements as Rough Grassland or acid grassland. Montane habitats and coastal habitats show notable differences due to CS’s under-representation or differing data structures.
  - Fen/Marsh/Swamp: CS indicates relatively large extents; LCM2007 detects mosaic fen patterns less consistently due to patch size and spectral mixing.
- Overall takeaway: CS and LCM2007 provide complementary perspectives; CS offers ground-truth validation and fine spatial detail in some habitats, while LCM2007 provides nationwide, repeatable, policy-relevant baselines with consistent spatial structure.

## UK land cover distribution and country variation
- Across the UK, more than 50% of land is intensive or built-up (Arable + Improved Grassland + Built-up Areas and Gardens).
- Woodlands cover about 12% (split roughly equally between Broadleaved and Coniferous).
- The distribution varies by country:
  - England shows the highest share of intensive land use.
  - Scotland has the largest proportion of Coniferous Woodland and the most semi-natural and montane habitats.
  - Northern Ireland and Wales show distinct patterns in grassland and boundary features.
- LCM2000 vs LCM2007 comparison highlights changes in reported percentages for arable land, semi-natural grassland, coniferous woodland, and urban areas; spatial framework changes contribute to these differences and require careful interpretation.

## Change detection and monitoring implications
- LCM2007 provides a consistent, repeatable UK-wide framework suitable for habitat extent estimation and change detection when used with caution.
- Direct year-to-year change mapping is challenging due to differences in spatial structure, class definitions, and boundary representation across LCM generations.
- Recommendations for monitoring practice:
  - Use aggregated or harmonized classes to reduce misinterpretation due to classification changes.
  - Reorganise earlier CEH maps into a common, real-world spatial framework to enable coherent national change analyses.
  - Leverage the BH Association rules to improve cross-dataset comparability at multiple thematic levels.
- The LCM2007 framework is well-positioned to support policy areas including biodiversity surveillance, ecosystem services, catchment management, woodland planning, and Natura targets, provided users account for methodological differences when linking to CS or other datasets.

## Applications for monitoring, policy and environmental health
- Provides a robust, UK-wide land cover map to inform biodiversity assessment, habitat connectivity, and landscape planning.
- Acts as a contextual base map for higher-resolution habitat mapping and for monitoring habitat networks and change over time.
- Supports cross-country comparisons and standardized reporting across England, Scotland, Wales, and Northern Ireland.
- Enables integration with other data types (e.g., climate, hydrology, carbon accounting, urban studies) for multi-criteria environmental health indicators.

## Access, licensing and user guidance
- CEH Information Gateway hosts the 1 km raster data.
- Full vector and 25 m raster data are available on request under licence from CEH (fees may apply).
- Users should exploit polygon-level provenance and KBEs to understand reclassifications; KBEs can be revisited or removed to suit specific analyses.
- Bespoke validation approaches (e.g., informal Bayesian-like checks using high-resolution imagery) can help assess the consistency of LCM2007 at locations of interest.

## Limitations and considerations for users
- Spectral ambiguity and one-to-many mappings remain a fundamental challenge; KBEs mitigate but do not fully resolve all ambiguities.
- Mosaic and upland/seasonal habitats (e.g., fen, montane, dwarf shrub heath) pose ongoing validation and classification challenges.
- Comparison and change detection between LCM versions require careful alignment of spatial frameworks and class definitions.
- Topographic and winter imagery issues may affect some classifications; alternative composites or manual edits may be necessary for complex terrains.
- Ground-truth data alignment with polygon extents is critical; CS and field timing may differ from imagery acquisition.

## Key figures and outputs
- 23 land cover classes, 17 Broad Habitats; vector and raster products; 0.5 ha MMU; 10 polygon attributes; 1 km aggregate products.
- Overall accuracy around 83% with variable class-level performance.
- Nine production chunks enable UK-wide vector coverage; KBEs and ProbList support traceability of classification decisions.
- Broad Habitat Association framework enables interpretation of cross-dataset correspondences and supports cross-country policy analyses.

## Practical guidance for monitoring framework authors
- Use LCM2007 as a baseline UK-wide reference for habitat extent and change, while accounting for differences in spatial structure when coupling with CS or other inventories.
- Leverage the KBEs and polygon-level metadata to audit and adjust classification decisions in location-specific monitoring plans.
- Apply Broad Habitat Association rules to translate between LCM2007 and CS (or European datasets) at BH and aggregate levels to improve comparability.
- Plan for data governance and reuse by recognizing the importance of a stable spatial framework for repeatable nationwide monitoring.
- Consider licensing and data access needs early in project design and build collaborative workflows with CEH for validation and integration.