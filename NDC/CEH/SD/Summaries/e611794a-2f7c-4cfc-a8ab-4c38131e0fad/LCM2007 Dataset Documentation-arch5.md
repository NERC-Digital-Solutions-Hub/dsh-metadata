# Land Cover Map 2007 Dataset Documentation

## Overview and purpose
- Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs and is intended to aid dataset discovery, sharing, and use.
- LCM2007 is a parcel-based classification of UK land cover using 23 classes aligned with UK Broad Habitats; it maps land cover (not strictly land use) from 20–30 m satellite imagery.
- The document emphasizes consulting the Final Report (Morton et al., 2011) for a comprehensive description and cautions that LCM2007 data products come with production methodology, metadata, and limitations.

## Data products and structure

### Vector data set
- Contains 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
- 10 attributes per polygon, including:
  - Parcel_ID: unique parcel label for each polygon, indicating source image; recommended to retain for traceability.
  - BH: Broad Habitat (dominant level).
  - BHSub: Broad Habitat sub-class (FieldCode); provides additional descriptive context.
  - FieldCode: short text field codes; not validated at all levels.
  - INTCODE: integer class code (1–23) for display and QA.
  - KBE: Knowledge-Based Enhancement history (processing history and changes).
  - ProbList: ranks top 5 spectral class candidates with probabilities.
  - CorePixels and TotPixels: pixel counts used in classification.
  - Construct: method used to derive polygons (OSMM-based data, segmentation, etc.).
- 23 LCM2007 classes map to Broad Habitats; Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and sub-classes.
- Sub-classes (BHSub) add descriptive detail but are not always as reliable as the main LCM2007 classes; users are advised to validate sub-classes when used for analysis.
- Rich metadata accompanies polygons, including processing history and KBE details.

### Raster data sets
- Derived from the vector data to produce 25 m and 1 km products.
- Separate projections for Great Britain and Northern Ireland.
- Aggregate classes used for 1 km rasters (merged from 23 classes).
- 25 m rasters maintain 23 LCM2007 classes; 1 km rasters provide:
  - Dominant cover at 1 km for LCM2007 classes and Aggregate classes.
  - Percentage cover at 1 km for both LCM2007 classes and Aggregate classes.
- File sizes summarized (vector ~9–10 million polygons; 25 m rasters large; NI and GB sizes differ).

## Data access, licensing, and governance

### Access and licensing
- 1 km raster data accessible via the CEH Information Gateway.
- Full vector product and 25 m product available under licence on request from CEH.
- Online application process or direct contact (spatialdata@ceh.ac.uk); license fees may apply for some users/applications.

### Projections and interoperability
- GB data: British National Grid (OSGB 1936) for vector and 25 m raster.
- NI data: Irish National Grid; NI is transitioning toward Ireland Transverse Mercator (ITM); reprojecting to ITM is supported by GIS tools.
- Data is designed to be interoperable with GIS datasets, but users should note the MMU and segmentation steps that affect small features.

### Data quality and limitations
- Minimum mappable unit (MMU) > 0.5 ha; parcels < 0.5 ha and linear features < 20 m dissolved into surrounding landscape.
- Validation against ground reference data yielded an average accuracy of 83% (based on 9127 polygons); field-level discrepancies are possible.
- LCM2007 maps land cover rather than strictly land use; examples include arable crops vs. how land is used (e.g., recreation grass vs. grazed grass may appear similar).

## Metadata, provenance, and quality assurance

- LCM2007 provides a rich metadata framework for polygons, including source imagery, KBE history, and spectral class probabilities.
- QA process validates the primary LCM2007 class (INTCODE) and highlights that Broad Habitat sub-classes (BHSub) are not always as reliably validated; users should perform their own validation if using sub-classes.
- The document stresses understanding production methodology and inherent limitations to guard against inappropriate use.

## Practical guidance for data stewards and users

- Retain Parcel_ID to maintain traceability and communication about specific parcels and source images.
- Use LCM2007 class numbers (INTCODE) for standard display and QA; exercise caution with BHSub for decision-making unless validated locally.
- When working with grassland classes, be aware of known misclassifications between Neutral, Calcareous, Acid Grasslands, and Improved Grassland; consider aggregating classes if appropriate.
- For high-detail analyses, vector data provides rich attributes and per-polygon metadata, but may be large and less performant; 25 m rasters offer a more streamlined alternative with similar thematic detail.
- For broad-scale modelling, 1 km rasters provide summarized dominance/percent cover suitable for national-scale analyses.
- Consult the Final Report (Morton et al., 2011) for in-depth methodology and validation results; Appendix 1–3 offer detailed class definitions, cross-walks, and color mappings.

## Key governance considerations (archetype alignment)

- Standards and interoperability:
  - LC Map 2007 adheres to a structured classification aligned with Broad Habitats; ensure alignment with current governance frameworks when integrating with other datasets.
- Metadata and documentation:
  - Highly metadata-rich vector data support data lineage, processing steps, and validation context—essential for data stewardship and reuse.
- Data availability and access control:
  - Distributed as both open 1 km rasters (gateway) and licensed full vector/25 m products; manage access control and licensing appropriately.
- Data quality management:
  - Acknowledge MMU constraints, potential misclassifications (especially grasslands), and the reliance on QA around the primary LCM2007 class; plan for user-driven validation where high accuracy is critical.
- Updates and provenance:
  - The dataset is historical (LCM2007); when integrating into current workflows, document the version, date, and reference Morton et al. 2011; consider linkage to the broader Countryside Survey lineage.

## Appendix highlights (for governance and understanding)

- Appendix 1: LCM2007 Classes
  - Descriptions and nuances of each Broad Habitat class (e.g., Broadleaved Woodland, Coniferous Woodland, Arable, Grassland types, Wetlands, Montane, Inland Rock, Coastal, Built-up Areas).
  - Notes on classification challenges (e.g., distinguishing open-canopy woodland, peat depth for bog vs. heath, spectral similarity among grassland types).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Detailed mappings between Broad Habitats, their sub-classes, and corresponding LCM2007 class numbers; used to interpret BHSub and FieldCode in the vector data.
- Appendix 3: LCM2007 colour mapping
  - Color coding for each LCM2007 class (useful for visualization, QA, and cross-dataset comparison).

## Summary of core points for Data Stewards
- LCM2007 delivers a rich, GIS-friendly land-cover dataset for the UK with 23 standardized classes tied to Broad Habitats, plus detailed per-polygon metadata and a robust QA framework.
- Data are available as 25 m and 1 km rasters, plus a large vector product; governance should account for licensing, data sizes, and projection handling.
- The dataset emphasizes traceability (Parcel_ID), validation needs for sub-classes, and caution when interpreting grassland categories due to known misclassification patterns.
- Data stewardship should document versioning, provenance, and study-specific validation when integrating LCM2007 into broader data ecosystems.