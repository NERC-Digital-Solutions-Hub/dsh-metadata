# Final Report for LCM2007 - the new UK land cover map

## Key takeaways for Data Leaders
- Provides a robust, repeatable, parcel-based land cover dataset suitable for habitat monitoring, policy support, and landscape planning across the UK.
- Uses a generalised spatial framework derived from detailed national cartography to improve cross-year comparability and future change detection.
- Integrates diverse data sources (spectral imagery, field surveys, urban boundaries, soils, elevation) with knowledge-based enhancements to improve thematic resolution beyond spectral classification alone.
- Delivers a range of data products (vector parcels, 25 m raster, 1 km raster) with accompanying metadata and a traceable processing history; access is controlled (open 1 km raster) or licensed (vector and 25 m raster).
- Faces ongoing data challenges common to large-scale land cover mapping: spectral confusion (notably with grasslands and arable land), fragmentation vs. MMU, data protection barriers, and varying data standards/metadata quality.

## Data landscape and inputs
- Core project: LCM2007, built as part of Countryside Survey 2007, mapping 23 land cover classes aligned to Broad Habitats (BH) and 17 BH groupings.
- Spatial framework: Northern Ireland integrated with image segments; GB topography generalised to land parcels; MMU set at 0.5 ha; nine UK chunks used to create seamless UK vector coverage.
- Data sources:
  - Satellite imagery: Landsat TM/ETM+, SPOT-4/5, IRS LISS-III and AWIFS; multi-date composites (summer/winter) for spectral classification.
  - Ground truth and validation: CEH field references; Countryside Survey data (2007).
  - Additional spatial data: OS MasterMap topography, LPS vector, agricultural boundaries, urban outlines, soils, soils and terrain data, NEXTMap Britain DEM.
- Data structure and processing:
  - Image pre-processing: cloud masking, atmospheric and topographic corrections.
  - Image segmentation: segmentation into image segments, integrated with cartographic boundaries to form a segment-based vector framework.
  - Classification: parcel-based supervised maximum likelihood classification with training areas from ground references; output includes top five spectral class probabilities per parcel.
  - Knowledge-based enhancements (KBE): seven automated algorithms (e.g., Terrain, Soil, Urban context) applied to ~20% of parcels to improve thematic resolution and reduce spectral confusion.

## Products, metadata, and access
- Vector product: land parcels with 10 processing attributes (e.g., Construct, ProbList, KBE history), Broad Habitat classification (BH) and BHSub (sub-classes), FieldCode, CorePixels, and reconstruction details.
- Raster products:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: UK-wide, with either percentage cover per class or dominant class per pixel.
- Metadata and provenance: extensive metadata enabling users to trace processing steps for each polygon; KBEs and classification history explicitly recorded.
- Access:
  - 1 km raster datasets available via the CEH Information Gateway.
  - Full vector and 25 m raster datasets available on request under licence; fees may apply.

## Data quality, validation, and comparability
- Validation: broad ground truth with overall accuracy around 83%; class-level accuracy varies by habitat type, with some classes performing better (e.g., certain woodland and arable types) and others worse (e.g., some grasslands, montane habitats).
- Countryside Survey comparisons (2007 CS data):
  - UK-wide Broad Habitat (BH) correspondence with CS2007 around 62% at BH level; 76% when considering BH-associated levels.
  - Grassland associations are particularly challenging due to the one-to-many relationship between observed grass cover and multiple BHs; Broad Habitat Association rules were developed to improve interpretation.
  - Arable and Horticulture: CS2007 vs LCM2007 show substantial differences; LCM2007 often includes boundary/linear features within arable areas, and spectral variability of crops causes misclassifications.
  - Fen, Marsh and Swamp: large discrepancies attributed to complexity and small patch sizes; CS often maps as Rough Grassland or Acid Grassland rather than Fen-related classes in LCM2007.
- Change mapping and methodological differences:
  - Changing spatial structures across LCM generations (1990, 2000, 2007) complicates direct change detection; robust change detection requires aggregating classes or reorganising maps into a common spatial framework.
  - LCM2007’s generalised spatial framework improves cross-year comparability but makes interpretation of direct class-for-class changes non-trivial.
- 4.5 Summary notes:
  - Agreement between LCM2007 and CS varies by broad habitat; grassland categories are particularly problematic.
  - LCM2007 aligns well with CS for Arable and Horticulture in certain contexts but shows higher overall arable area estimates in BH-based totals.
  - The report highlights the importance of integrating LCM with field surveys and other data sources for a fuller understanding of land cover dynamics.

## Strategic implications for data leaders
- LCM2007 provides a scalable, repeatable data foundation for habitat monitoring, policy support (e.g., Natura targets), and landscape planning, with a clear pathway for cross-year comparability.
- The knowledge-based enhancement approach demonstrates a scalable method to improve thematic resolution by integrating contextual data (soil, elevation, urban proximity) beyond spectral classification alone.
- The parcel-based vector framework, anchored to a robust spatial cartographic foundation, enables better integration with other national datasets and supports future monitoring and change detection, albeit with licensing controls for certain products.
- For broad stakeholder use, plan for licensing, data governance, and licensing costs, while leveraging freely accessible 1 km raster data for initial analyses and modelling.
- Recognize limitations in grassland, fen, montane, and coastal classifications; consider supplementary data or bespoke KBEs to refine these areas for policy and planning needs.

## Appendix highlights (relevant to data governance and interpretation)
- Broad Habitats and associations (Appendix 5) provide rules to interpret correspondences between LCM2007 BHs and Countryside Survey classifications, acknowledging complexities in grasslands, fen, and montane transitions.
- The report emphasizes the need for caution when extrapolating results beyond their intended use and suggests combining satellite-derived data with field surveys and other data sources for robust decision-making.

## Bottom line for Data Leaders
- LCM2007 delivers a detailed, parcel-based UK land cover map with multiple data products, strong documentation, and a clear framework for cross-year analysis and policy support. Its strengths lie in spatial coherence, integration potential, and knowledge-based enhancements, while key challenges remain around grassland/fen classification, data fragmentation, and change-detection complexities across different data structures.