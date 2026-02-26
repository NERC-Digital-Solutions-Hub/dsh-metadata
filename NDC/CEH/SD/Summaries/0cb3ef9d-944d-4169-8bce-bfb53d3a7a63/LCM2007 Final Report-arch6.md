# Final Report for LCM2007 - the new UK land cover map

- Presents the UK’s first continuous parcel-based land cover map (LCM2007) with a suite of raster and vector products for UK, GB, England, Scotland, Wales and Northern Ireland.
- Built from multiple data sources (national cartography, satellite imagery, soils, DEMs, urban boundaries) and aligned to a common spatial framework to enable robust change detection and cross-country comparisons.
- Uses a parcel-based classification approach with knowledge-based enhancements (KBE) to improve thematic accuracy, particularly where spectral data alone are insufficient.

## Data sources and methodological framework

- Data integration
  - National cartography as the spatial framework (OS MasterMap, LPS Large-scale Vector), plus agricultural and boundary layers.
  - Satellite imagery across multiple sensors (Landsat, SPOT, LISS-III, AWIFS) with pre-processing (cloud masking, atmospheric and topographic corrections).
  - Ancillary data (ground references, soil/terrain data) to support classification and KBE.
- Spatial framework and mapping units
  - MMU of 0.5 ha; parcel-based segmentation using the MasterMap-based framework to improve stability and applicability for change detection.
- Classification and enhancements
  - Parcel-based supervised classification with maximum likelihood, using multi-date composites.
  - Knowledge-based enhancements (KBE) applied post-classification to reduce spectral confusions and refine land-cover types using context (urban, soils, terrain).
  - Production chunks defined to ensure UK-wide, continuous coverage; manual hole-filling used sparingly.
- Output and metadata
  - Vector parcels with rich metadata (processing history, KBE history, ProbList, etc.).
  - Raster products at 25 m and 1 km resolutions; 23 LCM2007 classes plus 10 aggregates; multi-scale outputs for diverse analyses.
- Validation and quality assurance
  - 9127 CEH ground-reference points used for validation; overall accuracy around 83% across LCM2007 classes.
  - Class- and country-level validation metrics reported; transparency on caveats and limitations.

## Key findings from the Countryside Survey (CS) comparison

- Similar area estimates (within CS 95% confidence limits) for some Broad Habitats (e.g., Broadleaved woodland, Acid Grassland, Inland Rock).
- Dissimilar area estimates for several classes (e.g., Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, coastal habitats).
- Major drivers of discrepancies
  - Differences in class definitions and how temporary grassland and agricultural boundaries are mapped.
  - Spectral variability and confusion, especially for Arable and Horticulture due to diverse crops and phenology across years.
  - Boundary and linear features often treated differently (boundary lines vs field polygons) and MMU-driven differences.
  - Grassland classifications (Improved vs Neutral vs Calcareous/Acid) and the treatment of mosaic or transitional areas (Fen/Marsh/Swamp) differ between CS and LCM2007.
  - Fen, Marsh and Swamp is highly mosaic and often under-represented in spectral-only classifications; CS captures some small-scale features CS could detect but LCM2007 may classify as Rough Grassland or Acid Grassland.
- Implications
  - Direct one-to-one comparisons are challenging; LCM2007’s parcel framework and KBEs provide improved spatial consistency but may diverge from CS field-based delineations in certain habitats.
  - The comparison supports development of further KBEs to allocate grassland and mosaic areas (e.g., Fen) more consistently.

## UK-wide land cover patterns and country differences (LCM2007)

- Overall distribution
  - A substantial portion of the UK is intensive land use (Arable and Horticulture plus Improved Grassland) with notable built-up areas.
  - Woodlands and semi-natural areas constitute a smaller, but significant, share; coastal and montane habitats occupy smaller shares with regional variation.
- Country-level variations
  - England and Northern Ireland show higher proportions of intensive land use; Scotland shows more semi-natural and montane/woody habitats (e.g., Coniferous Woodland) and different coastal/montane patterns.
  - Spatial distribution reflects climate, topography, land management, and urban expansion patterns across England, Scotland, Wales, and Northern Ireland.
- Temporal and methodological notes
  - LCM2007 uses a consistent spatial structure to enable cross-country comparability and change detection, contrasting with earlier maps that used different spatial schemes.

## Data products, access, and usage

- Product suite
  - Vector parcel data with detailed attributes and KBE history.
  - 25 m raster and 1 km raster products, with both dominant-class and percentage-cover summaries for 1 km grids.
- Accessibility and licensing
  - 1 km raster data accessible via the CEH Information Gateway.
  - Full vector and 25 m raster data available on request under licence from CEH; fees may apply for some users/applications.
- Documentation and QA
  - Comprehensive metadata and appendices documenting methods, QA procedures, and usage guidance.
  - Bespoke validation described to help users assess fit-for-purpose for their specific applications.

## Change detection, challenges, and future directions

- Change detection context
  - LCM2007 provides coast-to-coast UK-wide coverage with a robust spatial framework, enabling national-scale change analyses when combined with other data sources.
  - Differences in spatial/thematic structures between CEH maps (LCM1990/2000 vs LCM2007) complicate direct change detection; sophisticated approaches are required to separate true change from methodological differences.
- Recommendations for future work
  - Reorganize earlier CEH maps into a common, real-world spatial framework to facilitate consistent change analyses.
  - Use aggregated or harmonized classes to enhance comparability and track trajectories of broad habitat change.
  - Leverage the parcel-level metadata and KBEs to reallocate mosaic/persistent transitional areas (e.g., Fen vs Rough Grassland, Neutral vs Improved Grassland).
- Implications for data support
  - The wealth of metadata and KBEs enables users to perform site-specific validation against high-resolution imagery and to generate uncertainty bounds (e.g., using fuzzy category assessments).
  - Cross-domain data integration (eo, field surveys, climate, soils) remains essential for richer, policy-relevant interpretations.

## Validation, caveats, and data support considerations

- Validation approach
  - Bespoke validation framework with parcel-level metadata to assess class plausibility locally.
  - Encourages user-driven validation using high-resolution imagery to quantify plausibility (fit-for-purpose focus).
- Caveats for users
  - Recognize spectral variability and mosaic nature of some habitats; expect differences with field surveys and historic maps.
  - Use KBEs and probability lists to assess uncertainty and consider aggregating to higher-level classes when appropriate.
- Data support implications
  - LCM2007 provides a robust, repeatable UK-wide reference for habitat monitoring, biodiversity assessments, and ecosystem-service analyses, with a transparent QA framework and clearly documented limitations.
  - The parcel-based structure and multi-scale outputs support diverse analytical needs, from national policy to local planning.

Note: This summary emphasizes data integration, classification methodology, validation, comparison with Countryside Survey, product availability, and change-detection considerations relevant for data support and governance.