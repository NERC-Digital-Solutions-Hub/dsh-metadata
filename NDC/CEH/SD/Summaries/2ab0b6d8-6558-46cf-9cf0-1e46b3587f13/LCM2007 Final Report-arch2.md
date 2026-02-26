# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presents UK Land Cover Map 2007 (LCM2007), the third CEH land cover map derived from satellite data, aimed at providing a consistent, policy-relevant evidence base for environmental monitoring, biodiversity habitat assessment, ecosystem services, and landscape planning.
  - Uses a continuous UK-wide vector land parcel framework with improved spatial and thematic accuracy, enabling policy-relevant monitoring and landscape-change analysis.
  - Outputs include vector parcels (10 million across GB and NI), 25 m raster, and 1 km summaries; includes extensive metadata and knowledge-based enhancements (KBEs).

- Data inputs and outputs
  - Spatial framework: national cartography (OS MasterMap for GB, LPS for NI) integrated with agricultural boundaries and segmentation to form a segment-based vector framework.
  - Imagery: multi-date, 20–30 m sensors (Landsat TM/ETM+, SPOT, IRS LISS/AWIFS) with 6-band composites; cloud masking and atmospheric/topographic corrections.
  - Classification and enhancements: parcel-based supervised classification to 23 LCM2007 classes, followed by seven automated KBEs to resolve spectral confusion; manual edits limited to small/rare areas.
  - Products: vector land parcels with detailed processing metadata; 25 m raster with 23 classes; 1 km rasters with percentage cover and dominant class; accompanying documentation and KBEs history.

- Dissimilar area estimates (CS 2007 vs LCM2007) and key habitats (4.3.2)
  - Dissimilar area estimates identified for:
    - Arable and Horticulture
    - Improved Grassland
    - Neutral Grassland
    - Dwarf Shrub Heath
    - Bog
    - Montane Habitats
    - Coastal habitats
  - Main causes of differences:
    - Differences in what is classified as each habitat between CS and LCM2007
    - Spectral confusion due to broad spectral variability within these classes
    - Inclusion of Boundary and Linear Features in LCM2007’s Arable/Horticulture category
    - MMU impacts: Countryside Survey maps finer features; LCM2007 uses a 0.5 ha MMU which can merge/split features differently
    - Temporal differences: LCM2007 uses multi-year imagery; vegetation changes across years affect classification of seasonal crops and temporary grassland
    - Grassland complexities: neutral vs improved grassland distinctions are spectrally subtle and soil data limited in resolving species composition
    - Fen/Marsh/Swamp: CS maps fen mosaics that are often split differently in LCM2007; small patch sizes and mosaic nature challenge consistent mapping
  - Specific examples:
    - Arable and Horticulture UK total around 63,005 km2 in LCM2007 vs CS 46,574 km2; part of difference due to temporary grass/uncropped land inclusion and field-boundary representations in LCM2007.
    - Spectral variability of arable impact: crops and growth stages produce signatures that can lead to overestimation of arable area in some regions.
    - Boundary/linear features: CS maps many boundaries below MMU; LCM2007 incorporates them into field polygons, increasing apparent arable/improved grassland areas.
    - Grassland classes: LCM2007 shows larger Improved Grassland area and smaller Neutral Grassland area, reflecting classification of fields that field surveys identify as neutral grassland but spectrally resemble improved grassland.
    - Dwarf Shrub Heath and Bog: allocation between these can shift based on soil and spectral context.
    - Fen/Marsh/Swamp: CS 2007 areas large relative to LCM2007; many Fen areas mapped as Rough Grassland or Acid Grassland by LCM2007 due to spectral/mosaic complexity.

- UK Land Cover: distribution and country differences (4.4)
  - UK-wide: over 50% of land is intensive (Arable and Horticulture + Improved Grassland) or Built-up; roughly 12% woodlands; about 30% semi-natural; 1–4% freshwater depending on country.
  - England: highest intensive land-use (~76%: ~40% Arable, ~27% Improved Grassland, ~9% Built-up).
  - Scotland: more Coniferous Woodland and upland semi-natural areas; largest proportion of Mountain/Heath/Bog in the semi-natural category; freshwater distribution varies by major water bodies.
  - Northern Ireland and Wales: mixed intensification patterns; NI includes montane and coastal variabilities; Wales shows different distributions in coastal/grassland/sheep-dominated landscapes.
  - Comparison to LCM2000: LCM2007 increases Arable share (26% vs 23%) and semi-natural grassland share (13% vs 17% in 2000); Coniferous Woodland slightly up (6.1% vs 5.4%).

- Comparison with Countryside Survey (4.5) and interpretation
  - Agreement between LCM2007 and CS varies widely across Broad Habitats (BH) and among national aggregates.
  - Grassland categories are particularly challenging due to one-to-many relationships with BH, leading to Broad Habitat Association (BHA) rules to improve cross-class correspondence.
  - LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture at the 1 km square level, but estimates a larger total Arable/Horticulture area than CS national estimates.
  - Fen/Marsh/Swamp differences are extreme (CS ~4392 km2 UK vs LCM2007 ~101 km2) due to the mosaic nature of fen and small patch sizes; many CS fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - National extent comparisons show some BH totals aligning with CS within CS 95% confidence limits (e.g., some woodland and freshwater categories), while others diverge due to methodological differences and data structure.
  - The analysis highlights the need for cross-dataset compatibility and suggests future work using KBEs to better allocate ambiguous areas (e.g., Fen, Marsh and Swamp) to the correct BH.

- Practical implications for environmental monitoring
  - LCM2007 provides a robust, repeatable UK-wide framework for land cover and Broad Habitat monitoring, useful for habitat assessment, ecosystem services analysis, landscape planning, and catchment management.
  - Change mapping remains challenging due to differing map structures, class definitions, and methodological differences across LCM generations; KBEs and BHA rules help improve interpretation.
  - Comparisons with field surveys (CS) are informative but require careful reconciliation of spatial structure, temporal windows, and ground-truth variations; integration with field data and other datasets enhances interpretation.

- Access, licensing, and data visibility
  - UK-wide 1 km rasters accessible via the CEH Information Gateway; full vector and 25 m rasters available on request under licence (licence fees may apply).
  - Data licensing details and CEH Information Gateway access are provided in the report.

- Validation, quality assurance, and bespoke validation (Appendix 4)
  - The concept of “fit for purpose” accuracy; acknowledges no absolute truth in geography and variability in data quality by location and use.
  - Parcel-level metadata enables validation of relevant classes in specific locations; recommends using high-resolution imagery to assess consistency between LCM2007 attributions and observed imagery (informal Bayesian-style validation).
  - A Python-based tool has been developed to facilitate this fuzzy/two-part validation approach (high vs moderate probability parcels).

- Broad Habitat Association (Appendix 5) – rationale for cross-walking LCM2007 vs Countryside Survey
  - Provides rules for aligning LCM2007 BH and CS classifications across several habitat types (Bog, Dwarf Shrub Heath, Montane Habitats, Built-up Areas, Fen/Marsh/Swamp, Rough Grassland, Water classes, etc.).
  - Addresses issues of ecological continua, mosaic habitats, and boundary cases; many rules are reciprocal with caveats about non-reciprocal mappings when one dataset characterizes a feature differently (e.g., Built-up Areas and Gardens vs grassland/water within urban boundaries).

- European and data context
  - LCM2007 supports integration with European products (e.g., Corine Land Cover) by providing vector-derived base that can be transformed thematically to pan-European schemes; linked to IMAGE2006 data and harmonized European monitoring efforts.

- Summary takeaway for analysts
  - LCM2007 delivers a first continuous parcel-based UK land cover framework with broad policy relevance and cross-country comparability, but users should be aware of persistent differences with field surveys and cross-map discrepancies, especially for grasslands and fen-related habitats.
  - Employ KBEs and Broad Habitat Associations to interpret classifications, and leverage parcel-level metadata for targeted validation.
  - Use the 1 km rasters for broad-scale modelling and the vector/25 m data for detailed spatial analyses, while recognising limitations in change detection due to methodological shifts across LCM generations.