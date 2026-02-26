# Final Report for LCM2007 - the new UK land cover map

## Overview and aims
- Presents the UK Land Cover Map 2007 (LCM2007): a UK-wide, parcel-based land cover map aligned with UK Biodiversity Action Plan Broad Habitats.
- Provides 23 land cover classes (mapped to 17 Broad Habitats) with a continuous vector framework of about 10 million land parcels.
- Delivers UK-wide, high-resolution data products (parcels, 25 m raster and 1 km summaries) to support habitat monitoring, planning, and policy development.

## Data sources, inputs and processing
- Satellite imagery and data fusion
  - Multitemporal imagery from Landsat TM5, IRS LISS3, SPOT-4/5 (20–30 m pixels); AWIFS (60 m backup).
  - 91% of UK classified from summer+winter composites; remainder from single-date imagery.
- Spatial frameworks and ancillary data
  - National cartography inputs (OS MasterMap GB; LPS NI), agricultural boundaries, digital elevation model, soils, urban extents.
  - Ground reference data: CEH field points (2006–2008) for training/validation; Countryside Survey (CS) 2007 for comparisons.
- Image processing and segmentation
  - Pre-processing: cloud/shadow masking, atmospheric and topographic correction, six-band composites, geo-registration.
  - Segmentation to create parcel-based vector framework with MMU of 0.5 ha; integration with OS MasterMap and agricultural boundaries.
- Classification and enhancements
  - Parcel-based supervised maximum likelihood classification to 23 classes; iterative refinement with ground truth and KBEs.
  - Seven Knowledge-Based Enhancements (KBEs) applied to resolve spectral confusions using contextual data (urban, topography, soils, proximity to coastline, etc.).
  - KBEs improve resolution for semi-natural grasslands, bogs, montane habitats; can be reversed for spectral-only assessment.
- Products and metadata
  - Vector product with 10 processing attributes; KBEs and probabilities tracked per parcel.
  - 25 m raster with 23 classes; 1 km data products (percent cover and dominant class).
  - Access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters on request (licensing may apply).
- Quality assurance
  - Ground reference validation: 9,127 polygons (2006–2008); overall accuracy around 83%; class-specific Producer’s and User’s accuracies reported.

## Key findings from CS (Countryside Survey) comparisons
- Very similar area estimates (CS within CS 95% confidence limits across all of GB) for:
  - Coniferous Woodland, Freshwater, Built-up Areas and Gardens, Calcareous Grassland.
- Similar area estimates (UK level) for:
  - Broadleaved woodland, Acid Grassland, Inland Rock.
- Dissimilar area estimates (UK level) for:
  - Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, coastal habitats; Fen, Marsh and Swamp also problematic.
- Causes of discrepancy
  - Differences in class definitions and spatial structures between CS and LCM2007.
  - Spectral confusion (notably Arable and Horticulture and grassland types) and temporal range of imagery.
  - Boundary and linear features handling; CS maps include certain features that may be below LCM’s minimum mappable unit, causing area estimation differences.
  - Different approaches to mapping Fen, Marsh and Swamp due to mosaic nature and small patch sizes.
- Broad Habitat Association (BHA) rules
  - Developed to improve cross-walk between CS and LCM2007 by accounting for one-to-many relationships (e.g., grasslands and their associated Broad Habitats).
  - Used to enhance interpretability beyond strict one-to-one class correspondences.

## UK-wide patterns and policy relevance
- LCM2007 indicates more than half of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens; remaining land is semi-natural, with woodlands around 12% and semi-natural habitats making up a substantial portion in Scotland.
- Regional differences
  - England shows the highest share of intensive land use; Scotland has more semi-natural/mo ntane land and a larger share of Coniferous Woodland.
  - The distribution and representativeness of Fen, Marsh and Swamp differ notably between CS and LCM2007 due to methodological contrasts and landscape structure.
- Historical context
  - LCM2007 builds on LCM2000 and the earlier CEH mappings, with improved spatial structure from detailed national cartography, enabling better integration with other national datasets and future monitoring.

## Change mapping, limitations and methodological notes
- Change detection is challenging due to:
  - Temporal spectral differences, differing class definitions, and distinct spatial frameworks across LCM1990, LCM2000, and LCM2007.
  - The need to distinguish real ecological change from classification or data-structural changes.
- Recommendations for analysts
  - Use aggregated (e.g., Broad Habitat) trends and consider Broad Habitat Associations (BHAs) to improve comparability with field surveys.
  - Exercise caution when interpreting Fen, Marsh and Swamp and grassland classes; consult KBEs and BHAs for robust interpretation.
  - Consider reorganizing older CEH maps into a common spatial framework for more effective change detection.

## Data products and practical use
- Products
  - Vector: parcel-based land cover with 10 attributes (including processing history and KBE records).
  - 25 m raster: 23 LCM2007 classes.
  - 1 km rasters: UK-wide aggregates, offering either percentage cover or dominant class per 1 km cell.
- Applications
  - Landscape-scale analyses, habitat monitoring, biodiversity assessments, ecosystem services, and policy planning.
  - Potential cross-walks with field surveys (CS) and policy frameworks (e.g., Natura targets, habitat connectivity).

## Validation, limitations, and guidance for use
- Validation
  - Overall accuracy around 83% with class-specific accuracy varying by habitat type (e.g., high for some coniferous/bog-related classes; more variable for Neutral/Calcareous Grasslands).
- Guidance for analysts
  - Treat class-level accuracies as variable; leverage KBEs and BHAs to understand uncertainty and improve interpretation.
  Use 1 km aggregates for broad, country-scale modeling; combine with higher-resolution data where fine-scale detail is essential.
  Validate using parcel-level metadata (KBE history and probability lists) to assess fit for purpose in specific locales.
- Appendix insights
  - Bespoke validation emphasizes fit-for-purpose accuracy and proposes informal Bayesian-style checks using high-resolution imagery to gauge consistency with LCM2007 attributes.
  Broad Habitat Association (Appendix 5) outlines how LCM2007 classes relate to CS categories, particularly for complex mosaics (Bog, Dwarf Shrub Heath, Montane Habitats, Fen, etc.).

## Practical implications for analysts
- LCM2007 provides a robust, UK-wide, parcel-based land cover dataset suitable for monitoring, planning, and policy support, with improved integration potential due to cartographic-derived spatial structure.
- The Knowledge-Based Enhancements materially improve thematic resolution, especially for grasslands, bogs, and montane habitats, but some classes remain challenging.
- When comparing with field surveys (CS), account for differences in spatial structure and class definitions; use BHAs and the CS cross-walk to interpret correspondences more reliably.
- For change assessment, adopt a cautious, aggregated approach and exploit the unified spatial framework in future monitoring and re-mapping efforts.