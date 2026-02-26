# Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 provides continuous parcel-based land cover across the UK at multiple resolutions (vector 23 classes linked to Broad Habitats; 25 m raster; 1 km raster aggregates).
- Class structure maps 23 LCM2007 classes to Broad Habitats; extensive metadata and provenance accompany each parcel.
- Outputs designed to support habitat monitoring, policy, landscape planning, and national-scale analyses; supports change detection and cross-year comparability through a stable cartographic framework.

## Key data products and structure (GIS-friendly formats)
- Vector product: land parcels with attributes including area, source images, Broad Habitat, processing history, KBE (knowledge-based enhancements), ProbList, and projection details.
- Raster products:
  - 25 m resolution with 23 LCM2007 classes.
  - 1 km resolution with two formats: (A) percentage cover per class per pixel; (B) dominant class per pixel.
- Spatial framework and metadata
  - Uses a robust UK cartographic framework (OS MasterMap/LPS boundaries) to improve delineation, change detection, and cross-year comparability.
  - CorePixels and segment-based processing underpin classification; KBE history preserved for transparency.
- Access and licensing
  - 1 km rasters accessible via CEH Information Gateway.
  - Full vector and 25 m rasters available on request under CEH license (fees may apply).
  - Contact: spatialdata@ceh.ac.uk; data portal for licensing.

## Quality and accuracy
- Ground reference validation: 9,127 points collected 2006–2008; overall accuracy around 83% across LCM2007 classes.
- Class-level variability: higher accuracy for common classes (e.g., coniferous woodland, arable) and lower for spectrally confounded or semi-natural classes.
- Countryside Survey (CS) 2007 validation
  - Broad Habitat correspondence varies by habitat; BH-level rules added to improve cross-dataset interpretation.
  - Grasslands and fen areas show notable discrepancies due to spectral variability, mosaic habitats, and small patch sizes.
  - Change mapping challenges: substantial differences in spatial structure and timeframes between LCM versions (LCM1990/2000 vs LCM2007) complicate direct change detection.
- Practical QA notes
  - Parcel-level metadata (KBE history and ProbList) supports targeted, site-level validation.
  - “Plausible” to “certain” assessments recommended when validating at BH-subclass level; useful for independent checks using high-resolution imagery.

## 4.3–4.5: Comparison with Countryside Survey and implications for GIS work
- Dissimilar area estimates (4.3.2)
  - Areas where CS 95% confidence limits and LCM2007 diverge include Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and some coastal habitats.
  - Key drivers of dissimilarity:
    - Differences in what is classified as a given class (classification rules and definitions).
    - Spectral confusion due to broad spectral variability in crops and land-use transitions.
    - Inclusion of Boundary and Linear Features in LCM2007 arable area, inflating arable totals.
    - Boundary mapping differences: Countryside Survey maps many boundaries/segments not captured by MMU constraints in LCM; field-size and geometry differences affect area estimates.
    - Grassland classifications: spectral similarity and soil/altitude information challenge clean separation between Improved/Neutral/Calcareous/Acid grasslands.
    - Fen/Marsh/Swamp: mosaic/mixed-class nature leads to large discrepancies; small patches often misrepresented.
  - Result: interpretation of CS vs LCM2007 areas requires context and, in some cases, use of Broad Habitat Associations (BHAs) to align datasets.
- UK-wide and country-level patterns (4.4)
  - UK: over half the area dominated by intensive land uses (Arable and Horticulture and Improved Grassland) or Built-up areas; significant semi-natural areas remain.
  - England shows highest share of intensive land use; Scotland has the largest share of Coniferous woodland and substantial semi-natural grassland and montane habitats.
  - LCM2007 vs LCM2000 differences include larger arable area and shifts in grassland and woodland distributions, with overall changes not solely due to land cover but also to spatial framework changes.
- Summary and implications (4.5)
  - Agreement with CS varies across Broad Habitats; grassland classifications are particularly challenging due to the one-to-many mapping to BHAs.
  - LCM2007 provides coast-to-coast coverage and a reusable spatial framework that supports consistent national monitoring and change analyses, but users should be cautious with semi-natural habitats and apply context-specific KBEs or validation.
  - Future work could leverage additional data and KBEs to better allocate certain habitats (e.g., Fen, Marsh and Swamp) that CS records differently.

## Practical GIS implications and workflows
- The vector product offers a reusable UK-wide layer with 23 LCM2007 classes linked to Broad Habitats; KBEs and original spectral classifications preserved for flexibility.
- Raster products (25 m and 1 km) enable various scales of analysis, habitat extent estimation, and national-scale reporting; suitable for integration with meteorological, ecological, or inventory data.
- Spatial framework stability improves cross-year comparability and supports more robust change detection than segmentation-based approaches.
- When aligning with CS or similar datasets, using Broad Habitat Associations (BHAs) enhances cross-dataset correspondence, especially in mosaic and upland areas.
- Acknowledged uncertainties remain in semi-natural habitats; users should apply contextual KBEs or bespoke validations for county- or site-level studies.

## Appendix themes informing use
- Bespoke validation (Appendix 4): no absolute truth in geography; parcel-level metadata enables targeted validation; recommends informal Bayesian-like checks against high-resolution imagery to assess plausibility and provide uncertainty bounds.
- Broad Habitat Association rules (Appendix 5): details on BHAs how LCM2007 classes map to CS classifications in edge cases (bog, dwarf shrub heath, montane, fen, water, etc.) to improve interpretation and cross-dataset matching.
- Change detection considerations: meaningful change detection requires reorganising older CEH maps into a common spatial structure or focusing on consistently mapped classes, due to differences in spatial frameworks and class definitions over time.

## Endnotes and practical references for GIS users
- LCM2007 data are designed for policy-relevant habitat monitoring, landscape planning, and ecosystem service analyses, with a focus on transparency, traceability, and reuse in GIS workflows.
- The 1 km raster product and the 25 m raster/vector products are intended to support different scales of analysis, model integration, and policy reporting; consider using the 1 km product for national-scale modelling and the 25 m or vector products for detailed site-level or local analyses.
- Access channels:
  - CEH Information Gateway for 1 km rasters.
  - CEH data portal / licensing for full vector and 25 m rasters (licence may apply).
  - Contact: spatialdata@ceh.ac.uk for licensing and data-use details.