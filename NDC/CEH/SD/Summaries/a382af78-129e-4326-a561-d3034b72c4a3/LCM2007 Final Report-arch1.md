# Final Report for LCM2007 - the new UK land cover map

- Summary of purpose and product
  - First UK land cover map delivered as a continuous parcel-based dataset for the whole UK, with a spatial framework derived from national cartography.
  - Mapped 23 land cover classes aligned to Broad Habitats (17 Broad Habitats) at a 0.5 ha minimum mapping unit, with 25 m raster and 1 km aggregated products.
  - Data products include full vector (parcels with metadata), 25 m raster, and 1 km summary products; extensive metadata accompanies polygons to enable traceability.

- Data sources and spatial framework
  - Multi-sensor imagery: Landsat-5 ETM+, SPOT-4/5, Landsat-LISS-3, with over 70 images processed; composites (2-date summer–winter) used to sharpen spectral signatures.
  - Ground truth and validation datasets: CEH ground reference points; Countryside Survey (CS) Broad Habitats for validation.
  - Spatial frameworks: Great Britain uses OS MasterMap topography; Northern Ireland uses LPS Large-scale Vector boundaries; integration of image segments with cartographic boundaries to standardise UK-wide units.

- Methods and classifications
  - Image processing: cloud masking, atmospheric correction, geometric correction, topographic correction; multi-band composites created for robust classification.
  - Segmentation and framework integration: 60 composites segmented and integrated with cartography and boundaries; 0.5 ha MMU applied.
  - Classification and knowledge-based enhancements (KBEs): parcel-based supervised maximum likelihood with 37 composites and 21 single-date images; KBEs applied to resolve spectral ambiguities using contextual data (urban, terrain, soils, coastal proximity).
  - Outputs: 23 LCM2007 classes mapped to 17 Broad Habitats; 10 attributes documented per parcel; 25 m raster at 23 classes; 1 km products (percent cover and dominant class).

- Accuracy, validation, and interpretation
  - Overall accuracy: 83% across LCM2007 classes based on 9,127 ground-reference polygons.
  - Class-specific performance varied; some classes very robust (e.g., certain wetlands), others less so due to spectral ambiguity and KBEs limitations.
  - Ground-reference vs. wall-to-wall mapping caveats: alignment issues and mixed-class polygons influence accuracy metrics; KBEs can reduce some errors but may introduce others.
  - Comparison with Countryside Survey (CS) 2007 revealed varying agreement by Broad Habitat; notable discrepancies for certain grassland, arable, and fen categories due to differences in spatial structure, MMU, and how mixed habitats are represented.
  - Broad Habitat Association (BHA) rules improve cross-dataset correspondence for grassland-related classes and help align CS vs LCM2007 results.

- Comparison with Countryside Survey (CS) 2007: key insights
  - Very similar area estimates: Coniferous Woodland, Freshwater, Built-up Areas and Gardens, and Calcareous Grassland show close correspondence with CS 2007 within CS confidence limits.
  - Similar area estimates: Broadleaved woodland, Acid Grassland, Inland Rock also show alignment.
  - Dissimilar area estimates: Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; coastal habitats, with detailed reasons including definitional differences, spectral confusion, and boundary handling.
  - Fen, Marsh and Swamp exhibits major differences due to mosaic nature and small patch sizes; CS areas often below the MMU or mapped as other habitats in LCM2007.
  - Country-level patterns reflect dominant habitats and differences in how Broad Habitats are represented or aggregated.

- Change mapping and temporal considerations
  - Change detection is challenging due to differences in base products (LCM1990, LCM2000, LCM2007) and the UK-wide spatial framework; typical per-pixel error rates around 20%.
  - Difficult to separate real change from methodological and spatial inconsistencies; robust approaches may rely on aggregated classes or re-aligning to a common real-world spatial framework for monitoring.

- UK land cover overview and historical context
  - UK distribution: over half of UK land cover is intensive (Arable and Horticulture plus Improved Grassland) or Built-up areas; Scotland has the most Coniferous Woodland and the largest share of semi-natural habitats; variation exists across England, Scotland, Wales, and Northern Ireland.
  - LCM2007 continues from LCM1990 and LCM2000, with improved spatial framework (cartography-based) and enhanced reusability for future change detection and monitoring.
  - UK-wide linkage to European datasets (e.g., Corine) via generalisation and transformation, supporting pan-European environmental assessments.

- Access, licensing, and data products
  - 1 km raster LCM2007 data available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; licensing fees may apply.
  - Multiple data formats available to support varied applications, from detailed vector parcels with processing history to 25 m rasters suitable for wide-area modelling, and 1 km products for coarse-scale national analyses.

- Applications and policy relevance
  - Supports habitat monitoring, biodiversity assessment, ecosystem services analysis, landscape planning, and catchment management.
  - Provides a standard UK-wide spatial framework for land cover referencing, facilitating national and country comparisons and integrated monitoring when combined with other data sources.
  - The accompanying metadata and validation framework enable users to assess and tailor applicability to specific research or policy needs, including potential Bayesian-style quality checks using high-resolution imagery.

- Accessibility of broader context
  - LCM2007 is designed to be integrated with other data (soil, climate, hydrology, LiDAR, ground surveys) to inform evidence-based policy across sectors such as climate, water, ecology, agriculture, urban planning, and biodiversity targets.

Note: This summary encapsulates the core content and conclusions presented across the document, including data sources, methodologies, accuracy assessments, cross-dataset comparisons, change considerations, product formats, access, and policy relevance, as described in the provided material.