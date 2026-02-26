# Final Report for LCM2007 - the new UK land cover map

- Provides the first continuous parcel-based UK land cover map (LCM2007) with 23 land cover classes mapped to 17 Broad Habitats.
- Outputs include a vector parcel product, a 25 m raster, and 1 km raster products, plus UK-wide summaries.
- Data are designed to support biodiversity monitoring, policy development, landscape planning, and policy-relevant analyses.

## Key data, scope and outputs

- Spatial units and classifications
  - 23 LCM2007 classes linked to 17 Broad Habitats.
  - Minimum mapped unit (MMU) of 0.5 ha; vector delivers land parcels; 25 m raster and 1 km summary rasters accompany.
- Coverage and validation
  - Ground reference validation: 9,127 points.
  - Overall accuracy: 83%; class-level accuracy varies; higher accuracy when considered as Broad Habitat Associations for some classes.
- Outputs and accessibility
  - Vector product with extensive metadata (processing steps, KBEs history, ProbList).
  - 25 m raster for the 23 classes.
  - 1 km raster products (percent cover and dominant class per pixel) for all 23 classes and 10 aggregates.
  - Access via CEH Information Gateway; full vector/25 m data on request (licence may apply).

## Data sources and production workflow

- Satellite and ancillary data
  - Primary imagery: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m pixels); AWIFS as backup.
  - 2-date summer–winter composites used to improve class separation; ~91% UK mapped from composites.
- Ground-truth and external data
  - Ground reference training/validation data (9,127 points).
  - External datasets integrated to support spatial framework (OS MasterMap GB; LPS NI; boundaries, urban extents, soils, DEMs).
- Framework and processing
  - GB framework built from OS MasterMap; NI framework from LPS; integrated with image segmentation and boundaries.
  - Image pre-processing includes cloud masking, atmospheric correction, precise geo-registration (RMSE < 0.3 pixel), topographic correction.
  - Parcel-based segmentation forms a contiguous UK-wide vector; processing done in nine chunks to ensure seamless pan-UK coverage.

## Classification and knowledge-based enhancements

- Methodology
  - Parcel-based supervised maximum likelihood classification applied to 37 composites and 21 single-date images.
  - Training areas drawn from ground reference data; iterative refinement to improve accuracy.
- Knowledge-based enhancements (KBEs)
  - Post-classification KBEs address spectral confusions using contextual data (urban context, proximity to coasts, terrain, soils).
  - Approximately 20% of parcels are revised by KBEs; improve thematic resolution (e.g., distinguishing semi-natural grassland types with soil/altitude data).
- Thematic detail
  - KBEs support separation of grassland sub-types (acid, calcareous, neutral) and montane habitat adjustments.
  - Some spectral ambiguity remains for certain classes, influencing final accuracy for a subset of parcels.

## Data products in detail

- Vector product
  - Parcel-level polygons with attributes: area, source images, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, KBE history, ProbList, CorePixels, Construct.
- Raster products
  - 25 m: 23 LCM2007 classes.
  - 1 km: two summarize modes per pixel — (A) percentage cover by class; (B) dominant class.
- Metadata and documentation
  - Comprehensive metadata enabling traceability of processing history and decisions.
  - Guidance on interpreting KBEs and their relation to Broad Habitats.

## Validation, uncertainty and interpretation

- Validation approach
  - Field validation (2006–2008) with 9,127 ground reference points.
  - Overall accuracy 83%; class-level accuracy varies; higher accuracy when aggregated to Broad Habitat associations.
  - KBEs and external data can cause lower accuracy for some classes due to spectral ambiguity.
- Bespoke validation and outputs
  - Appendix describes a flexible, user-focused validation approach (e.g., using high-resolution imagery for plausibility checks and providing upper/lower accuracy estimates by class).

## Comparison with Countryside Survey (CS)

- Two CS–LCM2007 comparison approaches
  - 1 km CS squares vs. LCM2007 BH mapping.
  - National CS estimates vs. LCM2007.
- Key findings
  - Agreement varies widely by Broad Habitat; grassland shows notable discordance due to one-to-many relationships with BHs and the need for Broad Habitat Association (BHA) rules.
  - LCM2007 correlates strongly with CS 2007 for Arable and Horticulture on a square basis but tends to overestimate Arable and Horticulture at the Broad Habitat level (differences partly due to temporal range, spectral variability, and inclusion of boundary/linear features in LCM2007).
  - Fen, Marsh and Swamp estimates differ by an order of magnitude; CS often records mosaic compositions that LCM2007 assigns to Rough Grassland or other BHs.
  - Montane, coastal habitats and boundary features contribute to regional differences; CS may underrepresent small patches that LCM2007 can map.
- Implications for users
  - High correspondence for some classes at the 1 km CS level; use Grassland consolidation or BH Association rules to improve CS alignment.
  - Recognize differences in spatial structure and MMU when comparing CS and LCM2007 outputs.

## UK land cover distribution and historical context

- UK-wide distribution highlights
  - Over 50% of the UK is Arable and Horticulture or Improved Grassland.
  - Woodland accounts for about 12% (split roughly evenly between Broadleaved and Coniferous).
  - Remaining areas occupied by semi-natural habitats, coastal areas, and urban/other classes.
- Country-level patterns
  - England: highest proportion of intensive land use (Arable + Improved Grassland + Built-up Areas).
  - Scotland: largest share of Coniferous Woodland and the highest proportion of Mountain/Heath/Bog in semi-natural areas.
  - NI and Wales show different distributions due to landscape and management practices.
- Temporal and methodological context
  - LCM2007 continues the CEH land cover series, bridging LCM1990 and LCM2000 with a new spatial framework based on detailed cartography (OS MasterMap and Large-Scale Vector).
  - CS field data provide complementary ground truth to satellite-derived outputs; LCM2007 also supports Corine Land Cover 2006 derivation for Europe.

## Change detection and spatial framework

- Change detection
  - LCM2007 provides a robust framework for monitoring habitat change and informing biodiversity targets, though direct one-to-one change detection with earlier CEH maps is complex due to differing spatial and thematic structures.
  - Reorganizing older maps into a common, world-real land-use framework is recommended to improve change detection consistency.
- Spatial framework
  - The generalised UK cartography-based framework enhances integration with other national datasets, enabling better cross-dataset analyses and policy-relevant outputs.
  - Boundary and linear features (not mapped at MMU scale) are treated contextually in CS vs LCM2007 comparisons.

## Access, usage and policy relevance

- Access
  - 1 km rasters publicly accessible via the CEH Information Gateway.
  - Full vector and 25 m raster datasets available on request (licensing may apply).
- Policy and applications
  - Supports biodiversity monitoring, habitat connectivity analyses, ecosystem services assessments, and landscape planning.
  - Enables habitat network analyses, Natura targets, and assessments of “naturalness” in river catchments when integrated with other data.
  - Serves as a consistent UK reference frame for country comparisons and policy evaluation.

## Practical guidance for data supporters and end users

- Data integration and QA
  - Leverage the parcel-level metadata and KBEs to understand and validate classification decisions in local areas.
  - Consider bespoke validation for local applications, given class-level variability in accuracy.
- Use and interpretation
  - For cross-dataset comparisons (e.g., with CS), be mindful of MMU differences, spectral variability in Arable/Grassland, and the impact of boundary feature incorporation in LCM2007.
  - When aligning with CS or other datasets, use Grassland consolidation to improve comparability and apply Broad Habitat Association rules for more robust correspondences.
- Change monitoring
  - Treat LCM2007 as a common spatial framework that facilitates future national-scale monitoring and change detection, while recognizing the need for methodological alignment when comparing with earlier CEH maps.