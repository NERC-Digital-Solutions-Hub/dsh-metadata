# Land Cover Map 2007 DATASET DOCUMENTATION

- UK land cover dataset (LCM2007) produced by CEH/NERC to support environmental monitoring and policy assessment over time.
- Parcel-based classification using 23 Broad Habitat–based classes; captures land cover (not strictly land use) from satellite imagery (20–30 m pixels).
- Includes multiple data products (vector and raster) to support diverse applications and GIS workflows.

## What LCM2007 is and how it was made

- Parcel-based land cover classification for Great Britain and Northern Ireland.
- Built from summer-winter composite satellite images with 20–30 m resolution.
- Updates and upgrades LCM2000; uses a generalised cartography framework (OSMM for GB, L&S Large-scale Vector for NI) refined with image segments.
- Objective: map land cover, not land use; 23 classes are aligned with UK Broad Habitats.

## Data products and formats

- Vector Data Set (GB and NI)
  - Polygons with 10 attributes per polygon; Parcel_ID identifies the source image and polygon.
  - Approximately 8.6 million polygons in GB and 0.9 million in NI; includes BHSub (Broad Habitat sub-class) and FieldCode (short codes).
  - Rich metadata: polygon construction, spectral classification, knowledge-based enhancements (KBE), and a ProbList (top 5 spectral class probabilities).
  - Notable attributes: INTCODE (class code 1–23 recommended for display), KBE, CorePixels, TotPixels, Construct, etc.
- Raster Data Sets
  - 25 m raster (derived from vector) at GB and NI projections; two resolutions for analysis purposes.
  - 1 km raster products summarise 25 m data by class:
    - Dominant cover at 1 km (per LCM2007 class)
    - Dominant cover at 1 km (Aggregate classes)
    - Percentage cover at 1 km (LCM2007 classes)
    - Percentage cover at 1 km (Aggregate classes)
  - 1 km products provide a coarser, UK-wide view suitable for large-scale modelling with other datasets (e.g., meteorology, species distribution).
- Data access and licensing
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; online application process provided.

## Spatial characteristics and classification scheme

- Classes
  - 23 LCM2007 classes derived from Broad Habitats (see Appendix 1 for class definitions).
  - Some Broad Habitats are subdivided for more detail (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Aggregation
  - 1 km rasters use Aggregate classes, merging the 23 LCM2007 classes into broader groups for summary statistics.
- Validation and accuracy
  - Ground-reference validation against 9,127 polygons shows an average accuracy of about 83% at the thematic resolution of the 23 LCM2007 classes.
  - Accuracy is an average; local discrepancies may occur.
- MMU and data dissolution
  - Minimum mappable unit is > 0.5 ha.
  - Parcels smaller than 0.5 ha or linear features < 20 m are dissolved into surrounding landscape during production.

## Class structure and interpretation

- 23 LCM2007 classes are tied to Broad Habitat definitions, with specific Sub-classes (BHSub) used for development history and probability listings (ProbList).
- The relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes is documented (Appendix 2), and colour mappings are provided (Appendix 3) for consistent visualization.
- Important caveats
  - LCM maps land cover, not land use; inferring activities (e.g., arable crops vs. grass used for recreation) may be ambiguous.
  - Change mapping across LCM1990/2000/2007 is complex due to class differences and structural changes; LCM2007 is not ideally suited for automated change detection (typical image/classification errors around 20%).

## Data structure details

- Vector data
  - Parcel_ID, BH (dominant class), BHSub (sub-class), FieldCode (short text field codes), INTCODE (display-ready class number 1–23), KBE, ProbList, CorePixels, Construct, TotPixels, etc.
  - FieldCode is not QA-validated at the subclass level; users advised to validate if using Sub-class level information.
- Raster data
  - 25 m and 1 km products with clear metadata on extents, pixel sizes, projections, data types, and coordinate systems (GB: British National Grid; NI: Irish National Grid; NI gradually migrating to ITM).

## Data access, sizes, and documentation

- File sizes (guidance)
  - Vector (GB) ~4.13 GB; Vector (NI) ~433 MB (Shapefile in 100 km × 100 km tiles).
  - Raster 25 m (GB) ~1.36 GB; Raster 25 m (NI) ~46 MB.
  - 1 km rasters vary from ~21 MB to ~49 KB depending on product type.
- Access channels
  - 1 km raster products: CEH Information Gateway.
  - Full vector and 25 m raster: available on request; licensing may apply.
- Documentation and references
  - Final Report for LCM2007 (Morton et al., 2011) for methodology and assessment.
  - Broad Habitat classification guidance (Jackson, 2000) and related appendices detailing class relationships and colour mappings.
- Updates and version history
  - Version 1.2 (May 2014): dataset updates including new OS tiles (Fair Isle, Stranraer) and water class improvements; NI updates as well.
  - Appendices detail updates to products and colour mappings; product versions outlined for GB and NI data.

## Practical considerations for analysts

- Use cases
  - Consistent, geography-wide mapping of land cover to monitor environmental health, habitat distribution, and policy performance over time.
  - Suitable for multi-resolution analyses using vector (detailed boundaries and attributes) or raster (easier integration with other gridded datasets).
- Cautions
  - Not optimized for precise change detection due to class and spatial structure differences across LCM versions.
  - Some grassland and peat-related classes can be misclassified; users should perform validation for specialized sub-classes if needed.
- Best practices
  - Retain Parcel_ID and Related metadata for traceability across analyses and communications.
  - Consider aggregation to 1 km for broad-scale modelling or 25 m/vector detail for site-specific studies, balancing detail and data size.
  - Use QA guidance from Morton et al. (2011) for quality assurance and interpretive caution with Broad Habitat sub-classes.

## Appendices (reference)

- Appendix 1: LCM2007 classes (definitions and examples for each Broad Habitat)
- Appendix 2: Cross-walk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
- Appendix 3: Colour mapping for LCM2007 classes (used in visualizations)
- Appendix 4: Updates to products (Version 1.2, 2014)