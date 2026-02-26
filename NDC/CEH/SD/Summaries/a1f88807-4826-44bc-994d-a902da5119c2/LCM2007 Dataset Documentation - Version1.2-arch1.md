LAND COVER MAP 2007 DATASET DOCUMENTATION

- Overview
  - UK parcel-based land cover classification using 23 Broad Habitat–based classes (LCM2007), produced from summer-winter satellite imagery at ~20–30 m resolution.
  - Upgrades LCM2000; provides a GIS-friendly feature set aligned to OS digital cartography for robust object-based mapping.

- Data products and formats
  - Vector data set (GB and NI)
    - GB: ~8.6 million parcels; NI: ~0.9 million parcels.
    - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
    - Unique Parcel_ID and Broad Habitat subclass (BHSub) descriptors; designed for clear communication and traceability.
  - Raster data sets
    - 25 m raster: 23 LCM2007 classes (GB and NI separate projections).
    - 1 km raster: aggregate/summary products (dominant class, percentage cover) for GB and NI.
    - Relationships: 25 m detailed classes; 1 km products provide dominant/percentage for both full classes and aggregated (BH-based) classes.
  - Example data and guidance on when to use vector vs raster (detailed vs broad-scale applications).

- Class structure and interpretation
  - 23 LCM2007 classes based on UK Broad Habitats; some classes subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh).
  - Maps land cover (not strictly land use); minimum mappable unit is >0.5 ha; discards parcels <0.5 ha or linear features <20 m.
  - Validation notes emphasize thematic accuracy at 23-class level.

- Key attributes and data accessibility
  - Vector attributes (Table 1): Parcel_ID, BH, BHSub, FieldCode, INTCODE (class number for display), KBE, ProbList, CorePixels, Construct, TotPixels.
  - Appendix 2 explains the relationship between Broad Habitats, LCM2007 classes, and sub-classes; Appendix 3 provides standard color mapping for visualization.
  - Data access: 1 km raster via CEH Information Gateway; full vector and 25 m raster available on request under licence from CEH (fees may apply).

- Data quality, validation, and caveats
  - Ground reference validation yielded an average accuracy of ~83% for the polygons; results are an average and local discrepancies may occur.
  - Change mapping across LCM1990/2000/2007 is complex due to differences in class definitions and spatial structure; LCM2007 products are not well suited for change detection.
  - KBE (Knowledge-Based Enhancements) and ProbList indicate likely spectral class matches but require user validation for subclass interpretations.

- Projections, scale, and file size considerations
  - Vector/GB: British National Grid; Vector/NI: Irish National Grid.
  - Northern Ireland is transitioning toward the Ireland Transverse Mercator (ITM) projection.
  - File sizes (illustrative):
    - Vector GB: ~4.13 GB; NI: ~433 MB.
    - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
    - 1 km rasters: GB up to ~49 KB (dominant/percentage products), etc.
  - Large data volumes, especially vector with 10 attributes per polygon; plan storage and processing accordingly.

- Practical usage guidance for analysts
  - Choose product type based on analysis scale and data requirements:
    - Vector: detailed polygon-level analysis, rich metadata, higher data volume.
    - 25 m raster: efficient per-cell analysis with consistent class resolution but less metadata.
    - 1 km raster: suitable for national-scale modelling and integration with other large datasets (e.g., meteorology, species distribution).
  - For rigorous mapping work, retain Parcel_ID and KBE history to track processing steps and provenance.
  - Exercise caution with Broad Habitat sub-classes; use with validation if the analysis depends on subclass-level distinctions.
  - When comparing across time, anticipate class definition changes and spatial structure differences that complicate direct change detection.

- Appendix highlights
  - Appendix 1: Detailed descriptions of the 23 LCM2007 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various grassland types, Wetlands, Urban/Suburban, etc.).
  - Appendix 2: Mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (includes FieldCode mappings and interpretation notes).
  - Appendix 3: Colour mapping recipe for standard visualization (class number to RGB); ArcGIS .lyr file option available.
  - Appendix 4: Updates to products (Version 1.2, May 2014) including new tiles (Fair Isle, Stranraer) and inclusion of water classes for 1 km products.

- Further information and acknowledgments
  - Primary technical reference: Morton et al., 2011, Final Report for LCM2007.
  - Supporting classifications and definitions: Jackson, 2000 (JNCC guidance on Broad Habitat classifications).
  - Acknowledges imagery and cartographic data sources (Landsat, SPOT, AWIFS, OS datasets, etc.) and CEH as the data custodian.

- Bottom line for analysts
  - LCM2007 provides a rich, multi-resolution UK land cover data product with robust metadata and documented classification logic.
  - It supports both detailed, asset-level (vector) analysis and scalable, grid-based (raster) analyses, with clear caveats around change detection and subclass interpretation.
  - Access is available via CEH with licensing; documentation and appendices supply class definitions, color mapping, and provenance to enable rigorous data-driven decision making.