# Final Report for LCM2007 - the new UK land cover map

- The LCM2007 delivers a continuous UK-wide parcel-based land cover map with associated raster products and change-context capabilities to support habitat monitoring, policy, and environmental decision-making.
- It provides a single, consistent spatial framework derived from detailed national cartography, enabling improved integration with other datasets and future monitoring.

## Data and methods

- Data sources
  - Satellite imagery: Landsat TM5, IRS LISS-3, SPOT-4/5; AWIFS as backup.
  - Multi-date summer–winter composites (2-date, 91% UK mapped) with 0.5% manual hole-filling.
  - Ground reference points (CEH) and Countryside Survey 2007 (CS) as external validation baselines.
  - External spatial datasets: OS MasterMap topography, NI LPS, agricultural boundaries, urban boundaries, soils, DEMs, etc.
- Processing and classification
  - Pre-processing: cloud masking, atmospheric correction (FLAASH), geo-registration, topographic correction; creation of 6-band 2-date composites.
  - Segmentation and spatial framework: image segments integrated with MasterMap parcels and agricultural boundaries to form a rich spatial framework.
  - Classification: parcel-based supervised maximum likelihood classification using ground truth; top-five class probabilities captured per parcel.
  - Knowledge-based enhancements (KBEs): post-classification rules (about 20% of parcels adjusted) using contextual data (urban/coastal/terrain/soil) to reduce spectral confusion and sharpen thematic resolution.
  - Product assembly: UK-wide vector product built by merging nine production chunks with priority rules to optimize spectral homogeneity.
- Outputs
  - 23 LCM2007 land cover classes mapped to 17 Broad Habitats (BH) with a 0.5 ha minimum mappable unit.
  - Raster products: 25 m resolution (23 classes); 1 km raster products with either percentage cover or dominant class per 1 km pixel.
  - Vector product: full UK coverage with detailed metadata and KBE history (ProbList, CorePixels, Construct, etc.).
  - Access and licensing: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request under licence from CEH (fees may apply).

## Validation and accuracy

- Overall quality
  - 9127 CEH ground reference points used for validation; overall accuracy around 83%.
  - Class-specific performance varies; examples: Bog high accuracy; Neutral Grassland relatively lower due to spectral/landscape ambiguity.
- Validation framework notes
  - Uses a correspondence matrix (LCM2007 classes vs ground reference polygons) with producer’s and user’s accuracies; KBEs and external soils/terrain data can influence class-specific performance.
- Bespoke validation approach
  - Confidence in classifications is context-dependent; the project provides parcel-level metadata and probability listings to help users assess fit-for-purpose in their area.

## Comparison with Countryside Survey 2007

- Level of agreement and correspondences
  - Broad Habitat level correspondences between CS 2007 and LCM2007 vary by BH; overall GB correspondence around 62% at BH level; 76% when considering Broad Habitat associations; aggregate class correspondence around 67%.
  - England, Scotland, and Wales show country-specific patterns; Montane and upland habitats display greater variability due to CS data gaps and differences in spatial representation.
- Grassland and upland complexity
  - Grasslands present one-to-many relationships with Broad Habitats; KBEs help reclassify some grassland types using soil and altitude data.
  - Neutral Grassland and Calcareous/Acid Grasslands show notable discrepancies due to spectral similarity and soil context.
- Fen, Marsh and Swamp
  - CS UK estimates (~4,392 km2) differ dramatically from LCM2007 (~101 km2) due to mosaic nature and patch size; many CS areas mapped as Rough Grassland or Acid Grassland by LCM2007.
- Boundary and boundary-feature treatment
  - Countryside Survey maps many boundaries below LCMMMU; LCM2007 allocates boundary/lines into adjacent land-cover classes, affecting area estimates for Arable/Improved Grassland classes.
- Country-level patterns
  - England shows higher intensity land use; Scotland has more Coniferous Woodland and upland habitat complexity; Wales shows similar grassland and upland patterns with notable differences in habitat assignments.
- Implications for interpretation
  - CS-based estimates align better when grasslands are collapsed to a single grassland category; BH-to-BHA links aid interpretation where MISMATCHES occur due to resolution and classification nuance.
  - Fen/Marsh/Swamp differences suggest future use of KBEs to reallocate certain patches to more accurate fen-related classes.

## Change mapping and limitations

- Change detection challenges
  - LCM1990, LCM2000, and LCM2007 differ in spatial structure and class definitions; cross-map change detection is complex due to map-to-map variability and classification errors (often around 20%).
  - There is no single robust UK-scale method for change detection; options include aggregating to common classes, focusing on consistently mapped classes, or using trajectory-based statistical approaches.
- Spatial framework implications
  - The 2007 spatial framework (based on generalised national cartography) provides a stable baseline for future change monitoring, but cross-comparisons require careful interpretation of class definitions and boundaries.

## UK-wide distribution and country patterns

- Overall distribution
  - UK land cover is dominated by intensive land use (Arable and Horticulture plus Improved Grassland ~51%); urban areas ~6%; semi-natural land and woodlands make up the remainder.
  - Coniferous and Broadleaved Woodlands each around ~6%; Semi-natural Grassland and Mountain/H9/Heath/Bog collectively substantial in some regions.
- Country-level variations
  - England: highest intensive land use (~76%); significant Arable and Horticulture and Urban areas.
  - Scotland: substantial Coniferous Woodland and upland semi-natural areas; montane dynamics more pronounced.
  - Wales and Northern Ireland: variable grassland and upland patterns with KBEs helping to resolve some misclassifications.

## Access, licensing and data provenance

- Access points
  - 1 km raster data: available via the CEH Information Gateway.
  - Full vector and 25 m raster products: available on request under licence from CEH (spatialdata@ceh.ac.uk).
- Provenance and traceability
  - Vector parcels include detailed processing metadata, including the KBE history (e.g., soil corrections, coastal masks, altitude-based corrections).
  - KBEs and ProbList provide transparency about spectral uncertainty and classification decisions.

## Practical implications and use cases

- Policy and biodiversity monitoring
  - Provides up-to-date UK-wide land cover context for biodiversity planning, Natura target evaluation, and habitat-network analyses.
- Habitat mapping and change detection
  - Serves as a consistent UK-wide framework for habitat monitoring and integration with higher-resolution data and models.
- Landscape planning and ecosystem services
  - Supports urban planning, water and catchment analyses, climate and carbon accounting, and broader landscape-scale decision making.
- Data integration
  - The alignment with national cartography (MasterMap, LPS) enhances interoperability with other national datasets.

## Limitations, caveats and guidance for analysts

- Accuracy varies by class; some grassland and wetland classes are spectrally ambiguous.
- Boundary features and fine-scale details may be underestimated due to MMU constraints; CS field surveys capture features not readily resolved by satellite imagery.
- When using KBEs, treat classifications as probabilistic and consider parcel-level metadata and ProbList to assess likelihoods.
- Change detection should be undertaken with awareness of methodological differences between LCM generations; aggregation and trajectory analyses are recommended to avoid misinterpreting spurious changes.

## Summary

- LCM2007 represents a major advancement in the UK’s land cover mapping, combining a coastal-to-coast parcel-based vector product with robust 25 m and 1 km raster outputs and a metadata-rich framework to support change detection and policy-relevant analyses.
- The project demonstrates strong agreement with Countryside Survey for certain classes (notably conifer woodland and some water/built features) but highlights substantial challenges in grassland, fen, montane, and coastal classifications due to spectral ambiguity and differences in spatial structure.
- The Knowledge-Based Enhancements, integration with national cartography, and provision of parcel-level processing history provide analysts with tools to interrogate classifications, validate decisions with high-resolution imagery, and tailor outputs to specific, local decision contexts.
- The reports emphasize the need for careful interpretation when comparing LCM2007 with previous CEH products and CS data, and they advocate combining satellite-derived products with field observations and other data sources to maximize understanding of UK landscapes.