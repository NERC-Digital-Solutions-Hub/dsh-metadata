# Land Cover Map 2007 Dataset Documentation

- Provides a range of Land Cover Map 2007 (LCM2007) data products to support diverse user needs; final report Morton et al. 2011 recommended for comprehensive evaluation.
- Note: This documentation covers LCM2007 data products; for LCM2000 and LCM1990 refer to appropriate dataset documentation.

## Overview and background

- LCM2007 is a parcel-based land cover classification of the UK using 23 classes, based on UK Biodiversity Action Plan Broad Habitats.
- Derived from summer-winter composite satellite imagery at 20–30 m pixels.
- Upgrades LCM2000 with a spatial framework from OS MasterMap/OSMM and Landsat segments; aims for polygon-based, object-like mapping aligned with other GIS datasets.
- Maps land cover (not strictly land use); arable land cover can differ from land use in some cases.
- Minimum mappable unit: >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.

## LCM2007 product specification and overview

- 23 LCM2007 classes aligned with Broad Habitats; some subclasses offer finer distinctions (e.g., Built-up Areas subdivided into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh).
- Unique object labeling: Parcel_ID attribute retained for each polygon to support unambiguous communication and product development.
- Rich metadata: per-polygon metadata on processing, spectral classification, and knowledge-based enhancements (KBE); ProbList shows top 5 spectral class probabilities.
- Validation: ground reference data used to validate 9127 polygons; average accuracy around 83%, acknowledging local variations.
- The dataset supports multiple product formats and resolutions to cover a wide range of applications (vector, 25 m raster, 1 km raster).

## Data products and formats

- Vector Data Set
  - Polygons with 10 attributes each (e.g., area, source images, Broad Habitat, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels).
  - Contains ~8.6 million GB polygons and ~0.9 million NI polygons.
  - Key attributes:
    - Parcel_ID: unique identifier including source image
    - BH: Broad Habitat (LCM2007 class)
    - BHSub: Broad Habitat sub-class (FieldCode descriptions)
    - INTCODE: class code (1–23) used for display and QA
    - KBE: knowledge-based enhancement history
    - ProbList: top five spectral class probabilities
    - Construct: polygon construction basis (OSMM-derived or segmented)
    - CorePixels/TotPixels: pixel counts used in classification
- Raster Data Sets
  - 25 m and 1 km raster products derived from the vector dataset.
  - Great Britain and Northern Ireland provided in separate projections.
  - 25 m raster uses the 23 LCM2007 classes (Table 2 describes pixel-class mapping).
  - 1 km raster provides:
    - Dominant cover at 1 km for LCM2007 classes
    - Dominant cover at 1 km for Aggregate classes
    - Percentage cover at 1 km for LCM2007 classes
    - Percentage cover at 1 km for Aggregate classes
- Map projections and extents
  - GB: British National Grid; NI: Irish National Grid
  - NI switching to Ireland Transverse Mercator (ITM) in progress; reprojecting may be needed for some software.
- File sizes
  - Vector in 100 km x 100 km shapefile ~ GB 4.13 GB; NI 433 MB
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB
  - 1 km rasters: up to ~49 KB to ~21 MB depending on product
- Data access
  - 1 km raster data via CEH Information Gateway
  - Full vector and 25 m raster data available on request under licence from CEH (data access via online application or contact)
  - Licence fees may apply for some users and applications

## Classification and data quality details

- 23 LCM2007 classes derived from Broad Habitats; some subclasses provide finer subdivisions when spectrally separable.
- Validation and QA
  - Ground reference polygons used for validation; average accuracy 83% across the sample.
  - Local discrepancies possible; users should expect some misclassifications in certain Broad Habitat sub-classes.
  - Sub-class level (BHSub) not covered by QA; users should validate if using those levels.
- Metadata richness
  - Per-polygon metadata captures data sets involved, processing history (KBE), and top spectral candidates (ProbList).
- Relationship and mapping guidance
  - Appendix 2 explains the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3 provides the standard colour mapping (RGB values) used for LCM2007 classes.

## Practical considerations for data leaders

- System-wide view: LCM2007 provides a robust, GIS-friendly land cover framework aligned with national habitat classifications; suitable for integration with other datasets and policy-facing analyses.
- Data availability and access
  - 1 km raster data is openly accessible via the CEH gateway.
  - Full vector and 25 m raster data require a licence; consider licensing constraints in data strategy and budgeting.
- Asset management and standards
  - Parcel_ID and rich metadata support traceability and data lineage.
  - High-resolution vector data offers detailed polygon-level information but results in large file sizes and potentially complex processing.
- User needs and co-ownership
  - 23-class classification and BH/BHSub structure align with diverse policy and planning needs; however, validation is recommended at sub-class levels before policy use.
  - Data are designed to support cross-dataset analysis, given the alignment to OSMM and high-quality polygon boundaries.
- Data limitations and considerations
  - LCM2007 maps land cover, not always definitive land use; use caution when interpreting land use from land cover alone.
  - Small or narrow water bodies may be below minimum mapping units; some spectral classes (e.g., Montane Habitats, Saltmarsh) require careful interpretation in coastal or high-altitude regions.
  - Data may have paywall/licence restrictions for certain formats; plan licensing and data governance accordingly.
- Recommendations for use
  - For national-scale analyses, 1 km raster products provide efficient summaries (dominant and percentage covers).
  - For detailed, site-specific work, 25 m raster or vector products offer finer resolution and richer metadata; balance against file size and processing requirements.
  - Use Appendix 1–3 materials to understand class definitions, relationships, and colour scheming for visualization and reporting.

## Appendices (highlights)

- Appendix 1: LCM2007 Classes – detailed descriptions of each Broad Habitat and its LCM2007 representation (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various Grassland types, Wetlands, Coastal and Littoral habitats, Built-up areas, etc.).
- Appendix 2: Relationship mapping – correlates Broad Habitats, LCM2007 class numbers, and Broad Habitat sub-classes (FieldCode) to support interpretation and cross-walks to other classifications.
- Appendix 3: Colour mapping – standard RGB values for each LCM2007 class (used in final reports and visualizations).

- Acknowledgements – credits data sources and licensing partners; notes that content is © NERC (CEH) 2011 and related licensing terms.