# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Delivers a continuous, parcel-based UK-wide land cover map (LCM2007) to support environmental monitoring, policy evaluation, and decision-making.
  - Provides a contextual Broad Habitat framework to aid biodiversity surveillance and habitat-network analyses.
  - Aims to enable policy-relevant analyses across multiple scales (coast-to-coast UK; GB and constituent countries).

- Outputs and data products
  - Vector product: land parcels with 10 documented processing attributes, Broad Habitat (BH) class, and Broad Habitat sub-classes; includes rich metadata for traceability.
  - 25 m raster: 23 LCM2007 classes, aligned to BH mapping.
  - 1 km rasters: two summaries per class—percentage cover and dominant class; plus aggregates for policy-relevant analyses.
  - Accessibility: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters on request under license (fees may apply).

- Spatial framework and data sources
  - Cartographic basis: high-resolution national cartography (OS MasterMap and LPS Large-scale Vector) to define stable, real-world land-cover objects and enable reuse for future monitoring.
  - Minimum mappable unit (MMU) and feature widths: MMU 0.5 ha; MFW 20 m; boundaries generalized from OSMM to maintain consistency over time.
  - Data inputs: Landsat TM/ETM+, SPOT-4/5, AWIFS; integration with OS boundaries, agricultural boundaries, soils, elevation, and coastal context; segmentation integrated with cartography to form parcel-based framework.

- Methodology
  - Image processing: cloud/shadow masking; atmospheric correction; geo-registration; multi-date summer-winter composites.
  - Segmentation and classification: multi-band segmentation, parcel-based supervised maximum likelihood classification using extensive image sets; iterative refinement with ground truth data.
  - Knowledge-based enhancements (KBEs): seven automated rules applied post-classification to resolve spectral confusion and improve thematic resolution (terrain, soils, coastal, urban, water, etc.); can be disabled to reveal original spectral results.
  - Ground data and validation: 9127 ground reference points (2006–2008); overall map accuracy around 83%, with class-level variances; external validation against Countryside Survey (CS) 2007 used to assess correspondence and highlight differences.

- Knowledge-based enhancements and class distinctions
  - KBEs mitigate spectral variability and contextually adjust assignments (e.g., grassland subtypes via soils and altitude; upland montane corrections; coastal/urban context).
  - Grassland classification refined through Broad Habitat Associations to address one-to-many mapping challenges.
  - BH Sub-classes provide finer-grained information; LCM2007 class mappings summarize to 23 main classes aligned with 17 Broad Habitats.

- Change mapping and temporal comparison
  - Change detection is complex due to differing class definitions, spatial structures, and per-pixel error rates across LCM1990, LCM2000, and LCM2007.
  - No definitive method for separating real change from classification or methodological differences; recommended approaches include focusing on aggregated classes or re-organising earlier maps into a common spatial framework.

- Validation and accuracy
  - Comparison with Countryside Survey 2007 shows varying agreement across Broad Habitats; grassland classes are particularly challenging due to spectral variability and the one-to-many mapping with BHs.
  - Fen, Marsh and Swamp areas show substantial discrepancies due to complex mosaics and small patch sizes; some habitats show high correspondence at aggregated levels, others do not.
  - CS 2007 comparisons indicate differences arising from mapping scale, temporal mismatches, and methodology; grassland classifications are central to many disparities.

- UK-wide and cross-country patterns
  - Chapter 4.4 presents UK land-cover distributions and country-level differences; England shows the highest proportion of intensive land use, Scotland has more Coniferous Woodland and upland semi-natural areas.
  - Comparisons to LCM2000 indicate changes in arable and semi-natural grassland proportions; interpretation requires careful consideration of spatial framework changes and classification rules.

- Governance, data sharing, and provenance
  - Extensive metadata and processing traceability support governance and reproducibility.
  - Data licensing applies to vector and 25 m products; access procedures and potential fees noted.
  - The KBEs and cross-data provenance rely on multiple data providers; attribution and licensing considerations are highlighted.

- Monitoring framework implications
  - LCM2007 offers a robust, policy-relevant backbone for monitoring biodiversity, habitat connectivity, and landscape change.
  - Provides a consistent UK-wide reference frame suitable for country comparisons and integration with other data sources (e.g., climate, hydrology, urban planning, carbon accounting).
  - Recognizes and communicates classification uncertainties, enabling users to apply appropriate validation and uncertainty analysis in monitoring workflows.

- Practical considerations for use
  - Ideal for policy areas requiring up-to-date Broad Habitat context, habitat networks, and national-scale monitoring; supports 1 km, 25 m, and vector parcel analyses.
  - Users should account for scale differences, classification uncertainties, and habitat-specific ambiguities (notably grassland and fen-related classes) when interpreting results or comparing with other data sources.

- Appendices and definitions (context for monitoring practitioners)
  - Appendix 1: Broad Habitat definitions and relationships to LCM2007 classes.
  - Appendix 4: Bespoke validation approach and the value of parcel-level metadata for quality assessment.
  - Appendix 5: Broad Habitat Association rules and cross-walks between LCM2007 and Countryside Survey classifications.