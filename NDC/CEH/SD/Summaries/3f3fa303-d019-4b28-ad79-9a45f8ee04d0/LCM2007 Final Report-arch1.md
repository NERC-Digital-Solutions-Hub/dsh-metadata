# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presenting LCM2007, the first UK land cover map with a parcel-based spatial framework linked to Broad Habitats and continuous UK-wide coverage.
  - Aim: support habitat monitoring, policy development, landscape planning, and ecosystem assessments across GB and Northern Ireland.

- Data sources and imagery
  - Satellite data: Landsat-TM5, Landsat ETM+, IRS-LISS3, SPOT-4/5 (20–30 m), AWIFS (60 m as backup).
  - Multi-date composites: six-band composites from summer and winter data; about 91% of UK mapped from composites.
  - Ground/truth data and ancillary datasets: over 9,100 ground reference points, Countryside Survey Broad Habitats, national cartography (OS MasterMap GB, NI Large-scale Vector), DEMs (NEXTMap Britain, NI), soils (NSRI Soilscapes), urban and agricultural boundaries.
  - Target year: 2007 imagery; processing 2005–2008 with manual hole-filling where needed.

- Spatial framework and UK coverage
  - Great Britain: spatial framework from OS MasterMap topography, generalized to MMU 0.5 ha and MFW 20 m; enhanced with agricultural boundaries and image segments.
  - Northern Ireland: spatial framework from NI Large-scale Vector data, generalized and integrated with image segments; agricultural boundaries excluded due to landscape structure.
  - Integration of image segments with cartography improves spatial delineation and change-mapping reusability.

- Image processing, segmentation, and pre-processing
  - Pre-processing: cloud/cloud-shadow masking, atmospheric correction (FLAASH/MODTRAN), geo-registration targeting RMSE < 0.3 pixel, topographic correction (Minneart + NEXTMap DEM).
  - Segmentation: 60 composite images segmented; segment-based vector framework merged with cartography; hole-filling applied selectively.
  - Classification framework: parcel-based supervised maximum-likelihood classification applied to 37 composite and 21 single-date images; 23 LCM2007 classes mapped to 17 Broad Habitats.
  - Training data: ground reference points; iterative refinement with reclassification to approach target accuracy.

- Knowledge-Based Enhancements (KBEs)
  - Seven automated algorithms to resolve spectral confusion and improve thematic resolution using contextual data (terrain, soils, coastal proximity, urban context, etc.).
  - Applied sequentially; KBEs affected about 20% of parcels and are fully traceable in vector attributes.
  - KBEs help address spectral variability and improve classification in mixed or confusing landscapes.

- Change mapping and limitations
  - Change mapping is challenging due to differing class definitions and spatial structures across LCM generations; separating real change from classification error remains difficult.
  - LCM2007 emphasizes a move toward a common spatial structure to enable more reliable change detection.

- UK Land Cover (Broad Habitats, accuracy, and comparisons)
  - Accuracy: overall accuracy for LCM2007 classes around the mid-80s percent range; class-specific accuracy varies due to spectral confusion (e.g., Fen, Marsh and Swamp; Montane vs other upland classes).
  - Comparisons with Countryside Survey (CS) 2007:
    - Agreement varies by Broad Habitat; high correspondence for certain classes (e.g., Coniferous Woodland, Built-up Areas and Gardens, Calcareous Grassland) and disparities for others due to methodological differences.
    - UK-wide correspondence: about 62% at Broad Habitat level and 76% at Broad Habitat Association level; higher correspondence (up to ~87–90%) when grasses are generalized to a single grassland class.
  - Reasons for discrepancies:
    - Differences in MMU, boundaries, and how boundary/linear features are treated.
    - Spectral confusion in arable and horticulture classes; temporal variability across multi-year imagery.
    - Fen, Marsh and Swamp areas: CS and LCM2007 show large divergence due to mosaic/nature of fen and small patch sizes; many fen areas map as Rough Grassland or other habitats in LCM2007.
  - Grassland and marsh-related issues addressed via Broad Habitat Association rules (BHAs) to improve cross-dataset correspondence.

- Product scope, access, and data formats
  - Vector product: parcels with 1) area, 2) source images, 3) Broad Habitat, 4) processing history including KBE results.
  - Broad Habitat Sub-classes (BHSub) provide additional descriptive detail; not all are validated at the same level as the main LCM2007 classes.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km rasters provide percentage cover per class or dominant class per pixel.
  - Access:
    - 1 km rasters available via the CEH Information Gateway.
    - Full vector and 25 m rasters available on request under license; fees may apply.
  - Example datasets illustrate the range of products (vector, 25 m, 1 km) and their relative detail and metadata.

- Practical uses and policy relevance
  - LCM2007 provides a robust evidence base for habitat monitoring, biodiversity assessment, ecosystem services, landscape planning, and catchment management.
  - The integration of KBEs and multi-source data enhances thematic detail and spatial coherence, supporting policy development and environmental decision-making.
  - Provides a consistent UK frame of reference for inter-country comparisons and for assessing “naturalness” in catchments and riverine systems.

- European links and broader context
  - UK component contributes to Corine Land Cover 2006 mapping via transformation from the LCM2007 vector product.
  - Builds on European-scale datasets (Corine, LUCAS) and pan-European EO data (IMAGE2006) to support cross-border environmental assessment.

- Bespoke validation and quality assurance
  - Bespoke validation framework emphasizes “fitness for purpose” and uses parcel-level metadata to assess the quality of relevant categories in specific locations.
  - A proposed informal Bayesian-like validation approach uses high-resolution imagery to gauge consistency of LCM2007 attribution with imagery, enabling upper/lower accuracy estimates for target classes.
  - A Python-based toolkit exists to support bespoke validation workflows.

- Broad Habitat Association (BHA) framework
  - Appendix 5 outlines rationale and rules for mapping between LCM2007 classes and CS Broad Habitats, including handling of:
    - Bog, Dwarf Shrub Heath, Montane Habitats, Built up Areas and Gardens, Fen/Marsh/Swamp, Rough Grassland, Water classes, and tidal areas.
  - Rules emphasize reciprocity where feasible and acknowledge complexities at habitat boundaries and transitions.

- Accessibility and documentation
  - Chapter and Appendix materials describe data structure, metadata, and usage considerations to help users interpret and apply LCM2007 data responsibly.
  - CEH provides contact points and licensing details for data access.

- Summary and conclusions
  - LCM2007 marks a significant advancement in UK land cover mapping with a coast-to-coast, parcel-based framework linked to Broad Habitats, extensive metadata, and multiple raster counterparts.
  - Improvements arise from integrating national cartography with multi-temporal imagery and knowledge-based enhancements, enabling stronger data coherence and potential for change detection.
  - While overall accuracy is solid and benefits from KBEs, some habitat classes remain challenging due to spectral ambiguity and differences between field surveys and remote sensing classifications.
  - The dataset provides a foundational platform for policy-relevant environmental analysis, habitat connectivity studies, and long-term land surface monitoring, with an emphasis on harmonising spatial structure to facilitate future monitoring and change detection.