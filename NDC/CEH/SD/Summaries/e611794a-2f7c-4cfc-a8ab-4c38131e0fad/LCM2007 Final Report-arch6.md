# Final Report for LCM2007 - the new UK land cover map

- The UK’s first continuous parcel-based land cover map (LCM2007) delivering 23 land cover classes linked to 17 Broad Habitats, with a 0.5 ha minimum mapping unit, and outputs at vector (parcels), 25 m raster, and 1 km raster resolutions.
- Produces UK-wide cover estimates and distributions to support habitat monitoring, biodiversity, ecosystem services, landscape planning and catchment management, with coast-to-coast coverage across the UK.

## Key data products and structure

- Data products
  - Vector: land parcels with 10 detailed processing attributes (including Construct, ProbList, KBE history) and BH/Sub classifications.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summaries per class — percentage cover and dominant class; plus aggregates to 10 Broad Habitat Associations.
- Class structure and framework
  - 23 LCM2007 classes mapped to 17 Broad Habitats; MMU 0.5 ha.
  - 1 km rasters used for broad-scale modeling; 25 m rasters and vectors enable finer analyses.
- Accessibility
  - 1 km rasters via the CEH Information Gateway.
  - Full vector and 25 m rasters available under licence on request (licensing and IPR may apply).

## Production and data lineage

- Foundation and segmentation
  - Parcel-based framework derived from national cartography (OS MasterMap and LPS Large-scale Vector); image segmentation integrates administrative boundaries with spectral segments.
- Classification and enhancements
  - Parcel-based supervised maximum likelihood classification using multi-date composites.
  - Seven Knowledge-Based Enhancements (KBEs) applied to resolve spectral confusion and improve thematic resolution; KBEs are contextual/ancillary-data driven (urban, coastal, terrain, water, soils).
  - ProbList provides top-5 class probabilities per parcel; KBE results are recorded for auditability and reversibility.
- Outputs and validation
  - Outputs include detailed processing history (Construct, ProbList, KBE) and core pixel statistics.
  - Ground-reference validation reported; overall accuracy around 83%, with variable class-level performance.

## Knowledge-based enhancements (KBEs)

- Purpose and inputs
  - Seven automated KBEs applied after initial spectral classification to improve thematic resolution using contextual data (urban context, coastal proximity, terrain/soil data, water presence, etc.).
- Impact and audit trail
  - KBEs typically reclassify around 20% of parcels; results are fully documented in the parcel metadata, enabling users to inspect original spectral classifications via ProbList.
- Reversibility and user validation
  - KBEs are designed to be reversible so users can review the spectral basis behind a parcel’s final class.

## Relationship and comparison with Countryside Survey (CS)

- Agreement and variability
  - Variation in agreement between LCM2007 and CS across Broad Habitats; strongest correspondences seen in certain grassland and woodland categories, with more discrepancy in arable, improved grassland, neutral grassland, dwarf shrub heath, bog, montane and coastal habitats.
- Causes of dissimilarities
  - Differences in what CS and LCM2007 classify as “Arable and Horticulture” (including boundary and linear features), spectral variability for arable crops, and the inclusion of boundaries/lines in LCM2007.
  - Grassland ambiguity: one-to-many relationships between observed grass types and Broad Habitats; this prompted Broad Habitat Association (BHA) rules to improve cross-product comparability.
  - Fen, Marsh and Swamp variability is large due to mosaic nature and small patch sizes; differences in spatial structure and MMU affect comparisons.
  - Montane, bog, and upland classifications show notable divergence due to altitude, spectral thresholds, and mapping conventions.
- Change mapping challenges
  - Robust change detection is difficult due to differences in spatial structure, survey methods (CS field survey vs. spectral-classification-based maps), and evolving class definitions across LCM generations.

## Practical implications for data support and use

- Strengths
  - Provides a robust, reusable UK-wide spatial framework with a clear lineage (parcel-based, segmented framework, and KBEs) suitable for diverse data products and policy applications.
  - Combines high-resolution 25 m detail with broad 1 km summaries for multi-scale analyses; enables self-service exploration via the vector and 25 m products.
  - KBEs offer transparency and traceability, allowing users to understand and adjust classifications based on context (soil, terrain, urban features).
- Cautions and limitations
  - Class- and country-level accuracy varies; grassland and upland habitats (bog, montane, calcareous/acid grasslands) exhibit notable uncertainties.
  - Arable and horticulture areas may be over- or misclassified due to spectral variability and the inclusion of boundary features.
  - Change detection between LCM generations requires careful methodological alignment due to differing spatial structures and mapping logic.
- Guidance for data support
  - Use ProbList and KBE attributes to audit classifications and apply user validation against high-resolution imagery or local knowledge.
  - For national-scale analyses, rely on 1 km summaries; for detailed policy-relevant work, utilize the 25 m vector/raster products with accompanying metadata.
  - Consider supplementing with additional data sources (e.g., field surveys, LiDAR, Corine/LUCAS) for edge habitats or where CS and LCM comparisons are essential.

## Change mapping and cross-dataset considerations

- Complexities
  - Comparisons across LCM2007, CS, and earlier LCM versions reveal substantial structural and thematic differences, complicating change detection.
- Recommended approaches
  - Focus on aggregated/broader categories or re-organize older data into a common spatial structure based on real-world land-use units to enable meaningful change assessment.
  - Combine with independent data (ecological surveys, ground truth) and use trajectory-based analyses to filter implausible changes.

## Practical figures and takeaways

- Composition and coverage
  - 23 land cover classes mapped to 17 Broad Habitats; MMU 0.5 ha; 25 m raster; 10-class vector attributes; 1 km summaries.
  - Over 90% UK classified from multi-date composites; minimal manual filling required.
- Accuracy and validation
  - Overall accuracy around 83% from ground-reference validation; class-level performance varies by habitat type.
  - Grassland simplification (grouping into a single grassland class) improves CS correspondence in some comparisons.
- Access and licensing
  - 1 km rasters available via CEH gateway; full vector and 25 m rasters available under licence on request; licensing and potential fees apply.

## Example areas and product overview

- Example areas illustrate diverse habitats (upland montane, calcareous grassland, urban, arable/fenland) and demonstrate how LCM2007 delineates real-world land cover parcels and supports contextual interpretation with ProbList and KBEs.
- Data products are designed to support habitat monitoring, biodiversity policy, landscape planning, and integration with other national datasets.

## Appendices and supporting contexts (high-level)

- Broad Habitat Association (BHA) rules summarize how LCM2007 classes correspond to Countryside Survey categories to improve cross-product comparability.
- Glossary provides definitions for terms such as Aggregate Classes, KBEs, MMU, and other domain concepts.
- Data access and licensing notes, along with a discussion of European links (e.g., Corine, LUCAS) and the role of LCM2007 in broader environmental monitoring.