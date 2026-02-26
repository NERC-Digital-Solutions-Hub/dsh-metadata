# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Summary for Analysts Monitoring the Environment

- Purpose: Provides a parcel-based UK land cover classification (LCM2007) to support monitoring of environmental health and policy performance over time. Based on Broad Habitats; maps land cover (not land use) from 20–30 m satellite imagery; improves on LCM2000 using OS-based spatial framework; suitable for GIS integration and standardised outputs.
- Coverage and scale: UK-wide mapping with 23 LCM2007 classes; data available as vector (parcels), 25 m raster, and 1 km raster products; GB and Northern Ireland provided separately for their respective projections.
- Key principle distinctions:
  - LCM2007 maps land cover, not strictly land use (e.g., arable land cover may not equal arable use).
  - Minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surroundings.
  - Uses unique Parcel_ID for each polygon and retains extensive metadata for traceability and QA.
- Data quality and validation:
  - Ground-reference validation: 9,127 polygons evaluated; average thematic accuracy around 83%.
  - Change mapping across LCM1990, LCM2000, and LCM2007 is not straightforward due to class/structure differences and typical spectral-change errors (~20%).
- Data products overview:
  - Vector data set: ~8.6 million GB polygons and ~0.9 million NI polygons; 10 attributes per polygon including Parcel_ID, BH (Broad Habitat), BHSub (sub-class), FieldCode, INTCODE (display code), KBE (processing history), ProbList (top 5 spectral matches), CorePixels, TotPixels, and Construct (source/segmentation). Includes Broad Habitat sub-classes for enhanced detail with a caution on QA reliability at that level.
  - Raster data sets (GB and NI):
    - 25 m raster: 23 LCM2007 classes; detailed per-pixel classification.
    - 1 km raster: aggregates (dominant class, percentage cover) for both LCM2007 classes and Aggregate classes; used for broad-scale analyses and integration with other datasets (e.g., meteorology, species distribution).
  - Metadata richness: detailed attributes for polygon construction, spectral classification, KBE history, and probability lists; supports validation and custom analysis.
- Practical implications for monitoring:
  - Provides standardized, thematically rich land cover data aligned with UK Broad Habitats for cross-temporal environmental assessments.
  - Offers multiple data formats and resolutions to suit different modelling needs (high-detail vector for precise mapping; raster products for landscape-scale modelling and integration).
  - Users should validate Broad Habitat sub-classes if used for fine-grained analyses; QA focuses on the primary LCM2007 class.
  - Change detection is not recommended from LCM2007 alone due to classification and structural differences between versions.
- Access and licensing:
  - 1 km raster data accessible via CEH Information Gateway.
  - Full vector product and 25 m raster product available on request; licensing may involve fees.
  - All products come with extensive references and are supported by the Final Report Morton et al. (2011) for detailed methodology and accuracy assessments.
- Additional context for interpretation:
  - The classification framework links LCM2007 classes to Broad Habitats (Appendix 2) and includes a colour-mapped palette (Appendix 3).
  - Updates since initial release (Version 1.0) include additions such as OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer), and inclusion of water classes in 1 km products (Version 1.2, 2014).

## Introduction and Background

- LCM2007 is a UK parcel-based land cover classification (23 classes) derived from summer-winter composite satellite imagery (20–30 m pixels).
- Builds on LCM2000 with a spatial framework based on OS MasterMap and Large-scale Vector datasets; polygons correspond to real-world objects (fields, woodland blocks) for GIS compatibility.
- Distinction: maps land cover, not direct land use; minimum mapping unit is 0.5 ha; smaller features are dissolved into surrounding areas.

## LCM2007 Product Specification and Overview

- 23 classes anchored to UK Broad Habitats; some classes subdivided using spectral signatures (e.g., Built-up Areas split into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Validation and QA: thematic validation performed at 23-class level; accuracy around 83% on average against ground reference polygons.
- Change mapping caveat: complex to compare across LCM versions due to differing class definitions and spatial structure; typical spectral classification error around 20%.

## Data Sets

- Vector Data Set:
  - 8.6 million polygons (GB) and 0.9 million polygons (NI); 10 attributes per polygon.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (discrete class for display), KBE (processing history), ProbList, CorePixels, TotPixels, Construct.
  - Sub-classes (BHSub) provide additional, though less robust, detail and should be validated independently if used.
- Raster Data Sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI data sets separately projected.
  - 1 km raster: dominant class and percentage cover for both LCM2007 classes and Aggregate classes.
  - Metadata for rasters includes grid dimensions, extents, pixel size, data types (Unsigned 8-bit), coordinate systems (GB: OSGB36; NI: Ireland 1965), projections (Transverse Mercator), and data extents.
- File Size:
  - Vector (100 km x 100 km blocks): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: sizes vary from ~21 MB to ~49 KB depending on product.
- Map Projection:
  - GB data: British National Grid; NI data: Irish National Grid; ongoing potential ITM transition for NI.

## Data Access

- 1 km raster products available via CEH Information Gateway.
- Full vector product and 25 m raster available on request; licensing may apply.
- Applications and users should consult the CEH data portal and potentially contact spatialdata@ceh.ac.uk for licensing details and access.

## Further Information and References

- Morton et al. 2011: Final Report for LCM2007 – detailed methodology and assessment.
- Jackson 2000: Guidance on interpretation of Broad Habitat Classification (for cross-walks and definitions).

## Appendices (Key Details)

- Appendix 1: LCM2007 Classes – definitions and notes for each Broad Habitat, including specific distinctions (e.g., coniferous vs broadleaved woodland, various grassland types, bogs, heaths, and coastal/marine classes).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings included; e.g., Arable and Horticulture, Improved Grassland, Neutral Grassland, etc.).
- Appendix 3: LCM2007 colour mapping – standard RGB values used for each class (helps with rapid visual interpretation and GIS symbology).
- Appendix 4: Updates to Products (Version 1.2, May 2014) – includes additions of OS tiles (Fair Isle, Stranraer) and updates to water class inclusion across 1 km products.

## Considerations for Analysts

- Leverage the 1 km raster products for broad-scale monitoring and cross-dataset integration; use the 25 m raster or vector for higher-resolution mapping and field-validated analyses where appropriate.
- Retain Parcel_ID in vector products to maintain traceability and enable unambiguous communications across teams.
- Use the 23 LCM2007 classes for analyses aligned with Broad Habitat frameworks; for some grassland and shrub-related classes, consider validating Broad Habitat sub-classes before detailed interpretation.
- Be cautious with change-detection and time-series analyses across LCM versions due to differences in class definitions and spatial structure; where possible, use the Final Report and cross-walks (Appendix 2) to guide comparisons.
- For data integration with policy performance monitoring, complement LCM2007 with metadata-rich attributes (KBE, ProbList) and QA notes to support reproducibility and methodological transparency.