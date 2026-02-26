# Final Report for LCM2007 - the new UK land cover map

## Data governance, accessibility, and provenance
- LCM2007 delivers a single UK-wide land cover vector product plus raster equivalents, with detailed metadata and processing documentation to support traceability and reproducibility.
- Access pathways:
  - 1 km raster products available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; licence fees may apply.
- The dataset provides parcel-level metadata including the sequence of knowledge-based enhancements (KBEs) applied, enabling audit trails and reproducibility for downstream analyses.

## Data quality, comparability, and validation
- LCM2007 area estimates are compared with Countryside Survey (CS) 2007 data to assess agreement and differences across Broad Habitats (BH) and aggregated classes.
- Overall agreement varies by habitat; grassland classes show strongest inconsistencies due to spectral ambiguity and cross-walking between classes (e.g., Neutral, Improved, Calcareous, Acid Grasslands).
- Major factors driving dissimilarities:
  - Differences in class definitions and spatial structure (MMU/aggregation) between LCM2007 and CS.
  - Spectral variability and temporal mismatch, particularly for Arable and Horticulture and Fen, Marsh and Swamp.
  - Boundary and linear features handling; CS maps many boundaries smaller than LCM2007’s MMU, affecting area allocations.
  - Inclusion of boundary/linear features in LCM2007’s Arable and Horticulture may inflate its area relative to CS.
- Key examples:
  - Arable and Horticulture: LCM2007 often overestimates compared with CS upper limits due to spectral variability and boundary feature inclusion.
  - Fen, Marsh and Swamp: CS reports an order of magnitude higher area than LCM2007, largely due to mosaic compositions and small patch sizes that are difficult to map optically; many CS polygons map to Rough Grassland or Acid Grassland in LCM2007.
  - Grassland types (Improved, Neutral, Calcareous, Acid): discrepancies attributed to spectral confusion and soil information limitations affecting grassland classification.
- Implications for governance: Users should be aware of systematic differences arising from methodological and spatial-structural changes when integrating LCM2007 with CS or other datasets.

## Change mapping and limitations
- Change detection between LCM2007 and earlier UK land cover maps is complex due to shifts in class definitions and spatial frameworks, with typical map error rates around 20%.
- Robust change detection remains challenging; recommendations include focusing on aggregated classes, using Broad Habitat Associations (BHAs) for cross-walks, or reorganising older CEH maps into a common spatial structure based on real-world land-use units to improve comparability.

## Data products and licensing
- Products:
  - Vector: 23 LCM2007 classes with 10+ attributes, including processing steps and KBEs.
  - Raster: 25 m resolution covering the 23 LCM2007 classes.
  - 1 km raster: two formats per pixel (percent cover and dominant class) for UK-wide analysis.
- Access and governance:
  - 1 km rasters via CEH gateway; full vector and 25 m rasters via licence (fees may apply).
  - Rich metadata supports traceability, provenance, and reproducibility for policy and planning use.

## Knowledge-based enhancements (KBEs) and validation framework
- KBEs improve thematic resolution by integrating supplementary data (soil type, altitude, urban extent, coastal proximity, terrain) to resolve spectral ambiguities.
- The original spectral classifications are retained in a ProbList-like attribute, enabling users to re-examine alternative outcomes when KBEs are disabled.
- Validation approach:
  - Appendix 4 describes bespoke validation emphasizing fit-for-purpose accuracy, and advocates a two-part assessment: high-probability vs. moderate-probability parcels.
  - Parcel-level metadata and a proposed informal Bayesian validation workflow enable user-driven quality checks using high-resolution imagery; a Python-based tool supports this workflow.

## Broad Habitat Association (BHA) framework and cross-walking
- Appendix 5 outlines Broad Habitat Association rules that link LCM2007 classes with Countryside Survey (CS) Broad Habitats, including reciprocal and non-reciprocal correspondences.
- These rules help interpreters assess cross-dataset correspondences (e.g., Bog ↔ Dwarf Shrub Heath, Acid Grassland, Montane Habitats) and support more robust validation and integration across products.
- Important note: some cross-walks are not reciprocal; the framework guides users on how to interpret and harmonise across datasets for policy-relevant analyses.

## Practical implications for Data Stewards
- Harmonisation and interoperability:
  - When integrating LCM2007 with other national or European datasets (e.g., Corine), rely on the shared spatial framework and documented KBEs to ensure consistent cross-dataset analyses.
- Documentation and transparency:
  - Maintain and communicate the KBEs history, ProbList results, and provenance to enable reproducibility and methodological critique.
- Uncertainty and usage guidance:
  - Provide users with guidance on uncertainties in grassland, fen/marsh, montane, and coastal classes; use BHAs and BHAs to interpret outputs beyond raw class labels.
- Change monitoring and governance:
  - Use the generalised spatial framework to support efficient future updates and change detection, but recognise that genuine land-cover changes must be differentiated from methodological artifacts.
- Access control and licensing considerations:
  - Clarify licensing implications for vector and 25 m products; ensure attribution aligns with national data governance requirements when integrating with external datasets.

## Representative data scope and accessibility
- The dataset covers GB and NI coast-to-coast, with detailed metadata, enabling cross-country comparisons and policy-relevant analyses.
- Example datasets and products demonstrate trade-offs:
  - Vector offers detailed parcel-level attributes but larger files; 25 m raster provides detailed land-cover information with simpler handling; 1 km rasters suitable for national-scale modelling and integration with other geospatial datasets.

## Endnotes for governance and policy use
- LCM2007 plays a central role in habitat monitoring, biodiversity policy support, landscape planning, and catchment management when used alongside complementary datasets.
- The report emphasises the need for sophisticated, cross-dataset methods to separate real change from artefacts, and encourages developing a common spatial structure for national land cover monitoring to facilitate robust change detection over time.