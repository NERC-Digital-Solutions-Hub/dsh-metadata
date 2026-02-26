# Land Cover Map 2007 Dataset documentation

- Overview: A parcel-based UK land cover classification (LCM2007) with 23 classes based on UK Broad Habitats, derived from summer-winter satellite composites (20–30 m pixels). It updates LCM2000 using a spatial framework (OSMM for GB, L&PS for NI) and produces data that map land cover (not strictly land use) as real-world objects (polygons).

- Purpose and scope:
  - Designed to support a broad user community with multiple data products and applications.
  - Emphasizes data provenance, metadata richness, and limitations of different LCM2007 products.
  - Recommends consulting Morton et al. 2011 Final Report for a full assessment.

- Key product characteristics:
  - Coverage: Great Britain and Northern Ireland; 23 LCM2007 classes tied to UK Broad Habitats; some subclasses deeper than the main 23 classes.
  - Minimum mapping unit: >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.
  - Data types: Vector (polygons with attributes) and Raster (25 m and 1 km products).
  - Validation: Ground-reference validation with 9127 polygons, average accuracy ~83%.

- Vector data set details:
  - Contains ~8.6 million polygons (GB) and ~0.9 million polygons (NI).
  - Each polygon includes 10 attributes (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class for display/QA), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID for communication; recommended to retain for data integrity.
  - Sub-classes (BHSub) provide additional information but are not as rigorously QAed as main LCM2007 classes; use with caution and validate for subclass analyses.
  - Rich metadata per polygon, including processing history and the knowledge-based enhancements (KBE).

- Class structure and relationships:
  - 23 LCM2007 classes derived from Broad Habitat classifications; some Broad Habitats split into sub-classes (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and related).
  - Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 1 provides brief reviews for each Broad Habitat (definition, training considerations, field-interpretation challenges).
  - Appendix 3 provides the standard color mapping used for LCM2007 outputs.

- Raster data sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI provided in separate projections.
  - 1 km raster: aggregates of the 25 m data; provides dominant class per 1 km cell and percentage cover for both LCM2007 classes and Aggregate classes.
  - Metadata (Table 3) includes grid dimensions, extents, pixel sizes, data types, coordinate systems (GB: OSGB36; NI: Ireland 1965), projections (TBM/Transverse Mercator variants), and data extents.

- Data access and licensing:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under license; online application or direct contact to CEH Spatial Data.
  - Licence fees may apply for some users/applications.

- Data formats and projections:
  - GB data: British National Grid (OSGB36) with Transverse Mercator projection.
  - NI data: Irish National Grid; NI moving toward Ireland Transverse Mercator (ITM) with API compatibility for reprojection.

- Data size and manageability:
  - Vector dataset is large (nearly 10 million polygons; 10 attributes per polygon); substantial file sizes to consider for distribution and processing (examples given for shapefiles and geotiffs).

- Production and methodology:
  - Based on satellite imagery (Landsat-TM5, SPOT-4/5, AWIFS) with multiple sources integrated.
  - Builds on OSMM generalised cartography and enhanced with image segment data for object-based polygons.
  - Includes Knowledge-Based Enhancements (KBE) and a spectral class probability list (ProbList) to support classification decisions and QA.

- Data quality, QA, and user guidance:
  - Data are validated against ground reference data; average accuracy provided with caveats about local variability.
  - Sub-class and FieldCode attributes exist but their accuracy is not as robust as the primary LCM2007 class; users should validate when using subclass distinctions.
  - The Final Report (Morton et al., 2011) contains comprehensive methodology, limitations, and validation details; recommended for thorough understanding.

- Practical considerations for use:
  - Data are most suitable where land cover mapping with linkage to Broad Habitats is needed; caution advised when inferring land use from land cover.
  - The 0.5 ha MMU and mosaic nature of some habitats mean some small patches and transitional areas may be generalized or misclassified.
  - Large file sizes and licensing requirements should be planned for in project budgets and workflows.

- Appendices and color mapping:
  - Appendix 1: LCM2007 class definitions and training considerations for various Broad Habitats.
  - Appendix 2: Detailed mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3: Standard colour mapping (RGB values) for each LCM2007 class as used in the Final Report.

- Further information and references:
  - Morton et al. 2011: Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
  - Jackson, 2000: Guidance on interpretation of Biodiversity Broad Habitat Classification.
  - Acknowledgments to data providers (Landsat, SPOT, AWIFS, OS, etc.) and licensing details.