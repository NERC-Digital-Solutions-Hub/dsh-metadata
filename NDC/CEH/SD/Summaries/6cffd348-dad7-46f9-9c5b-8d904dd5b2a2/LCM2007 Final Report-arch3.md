# Final Report for LCM2007 - the new UK land cover map

## 1. Overview
- Presents the UK Land Cover Map 2007 (LCM2007), the first UK land cover map with a parcel-based spatial framework derived from national cartography.
- Maps 23 LCM2007 classes to Broad Habitats, providing UK-wide land cover data for monitoring, policy, and planning.
- Delivers multiple data products (vector parcels, 25 m raster, and 1 km summaries) to support environmental monitoring and decision-making.

## 2. Data and spatial framework
- Spatial framework built from national cartography:
  - Great Britain: Generalised OS MasterMap topography, agricultural boundaries, image segments; integrated segmentation.
  - Northern Ireland: LPS-LSV polygons generalized and integrated with image segments.
- External datasets support framework, KBEs, and processing (e.g., elevation, soils, urban and agricultural boundaries).
- Satellite data and processing:
  - Primary sensors: Landsat-TM5, SPOT-4/5, IRS LISS3; AWIFS as backup.
  - 34 multi-date summer–winter composites; detailed segmentation improves spectral coherence and change detection.
- Knowledge-based enhancements (KBEs):
  - Seven automated KBEs applied in sequence to resolve spectral confusion (especially grasslands and montane areas).
  - KBEs altered ~20% of land parcels; changes are recorded in vector attributes for transparency and reversibility.

## 3. Product formats and access
- Vector product: land parcels with attributes (area, source images, Broad Habitat, processing history, KBE history, etc.). Includes Broad Habitat sub-classes (BHSub) and FieldCode; recommended validated at class level.
- Raster products:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: derived from 25 m; provides either percent cover per 1 km cell or the dominant class.
- Minimum mappable unit (MMU) and feature width:
  - MMU of 0.5 ha; minimum feature width 20 m; segmentation designed to support consistent change monitoring.
- Access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data on request under licence from CEH (licence fees may apply).

## 4. Validation, accuracy, and QA
- Ground reference data collected 2006–2008; 9127 points used for validation.
- Overall LCM2007 accuracy: 83% (class-level accuracy varies by habitat type).
- Provides producer’s and user’s accuracies per class; highlights reliability and potential biases.
- Validation results support transparency around class-specific uncertainty and inform users about data quality.

## 5. Comparison with Countryside Survey 2007
- Similar area estimates (within CS 95% confidence limits) for: Broadleaved woodland; Acid Grassland; Inland Rock.
- Dissimilar area estimates (beyond CS 95% limits) for: Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; coastal habitats; Fen, Marsh and Swamp shows substantial discrepancies.
- Key factors driving differences:
  - Differences in what counts as Arable and Horticulture; inclusion of boundary and linear features in LCM2007.
  - Spectral confusion, especially for arable and grassland classes.
  - Boundary/linear features often below LCM MMU; CS maps many of these as separate field features.
  - Variation in grassland classifications (Improved vs Neutral vs Calcareous/Acid) and limited utility of soil data for discriminating neutral vs improved grassland.
  - Fen, Marsh and Swamp areas are mosaics and often small; spectral identification challenges lead to large UK-scale discrepancies.
- Broad Habitat Association (BHA) rules developed to improve cross-dataset correspondence for grassland and upland categories.

## 6. Change detection and methodological considerations
- Change mapping is complex due to differences in spatial structures and class schemes across LCM1990, LCM2000, and LCM2007.
- Image classification accuracy is affected by spectral variability, land-use mosaics, and multi-date imagery; robust change detection methods are still evolving.
- KBEs and multi-date composites help reduce misclassification but can’t fully resolve all uncertainties, especially in upland and semi-natural landscapes.

## 7. Implications for monitoring frameworks
- LCM2007 provides a robust, metadata-rich, parcel-based UK land cover base aligned to Broad Habitats, with multiple data formats suitable for policy monitoring, trend analysis, and scenario assessment.
- Strengths:
  - Continuous vector coverage and a reusable spatial framework enable national-scale monitoring and future UK-wide mapping.
  - Integration potential with other data (e.g., CS) for policy-relevant analyses and habitat connectivity studies.
- Limitations to consider:
  - Data availability and metadata gaps can hinder reuse and verification; some data are sensitive to sharing.
  - Siloed data between organisations can impede data sharing; publicly sharing underlying data poses barriers.
  - Spectral confusion (notably grasslands) and changing spatial structures complicate change detection and cross-dataset comparisons.
  - Differences in spatial representation (parcel-based vs field-based) affect comparability with field surveys like CS.

## 8. Data governance, metadata, and accessibility
- Parcel-level metadata provides transparency on processing history and probabilities for top spectral variants, enabling users to assess quality in their location.
- Clear data provenance supports reproducibility; vector data includes KBE histories and ProbList for trackability.
- Data licensing may restrict some access; 1 km raster is openly accessible via CEH Gateway, while vector and 25 m raster require licences.

## 9. Broad Habitat Association (BHA) and knowledge-based enhancements
- BHA framework links LCM2007 classes with Countryside Survey (CS) broad habitat correspondences to better interpret cross-dataset relationships.
- KBAs address spectral confusion and habitat mosaics (e.g., Bog, Dwarf Shrub Heath, Montane, Fen, Marsh and Swamp) by allowing cross-walks with CS categories.
- Practical note: BH adjacency rules are not always reciprocal; some LCM2007 categories can map to multiple CS types, and vice versa, depending on context.

## 10. Practical recommendations for monitoring framework authors
- When aligning with CS or similar datasets, consider aggregating grasslands into a single Grassland class to improve correspondence and use BHA rules for cross-dataset interpretation.
- Account for licensing and provenance of data; emphasise metadata to ensure traceability and reproducibility.
- Use the parcel-level metadata to validate classifications in specific study areas with high spectral ambiguity; consider supplementary high-resolution imagery for validation.
- Recognise that Fen, Marsh and Swamp and upland habitats require cautious interpretation due to mosaic nature and small patch sizes.
- For national-scale monitoring, leverage the consistent spatial framework and multi-format outputs (vector, 25 m, 1 km) to support diverse policy analyses and ecosystem assessments.

## 11. Conclusion
- LCM2007 delivers a comprehensive, parcel-based UK land cover product with rich metadata, multiple data formats, and coast-to-coast coverage.
- It represents a significant advancement in alignments with national biodiversity frameworks and cross-dataset compatibility, enabling policy-relevant monitoring, trend analysis, and scenario evaluation.
- While offering substantial strengths, users should navigate classification uncertainties, cross-dataset differences, and data-sharing constraints through careful interpretation, BH Association guidance, and robust validation.