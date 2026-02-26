# Land Cover Map 2007 Dataset Documentation

## Overview
- UK parcel-based land cover classification using 23 classes linked to UK Biodiversity Action Plan Broad Habitats.
- Based on summer-winter satellite composites with 20–30 m pixels; updates LCM2000 with a framework aligned to OS MasterMap/topographic layers.
- Maps land cover (not strictly land use); minimum mappable parcel >0.5 ha; smaller parcels dissolved.
- Validated at 23-class thematic resolution; ground reference validation yielded an average accuracy of 83% across 9127 polygons.

## Data Products and Coverage
- Vector Data Set: polygons with 10 attributes each; 8.6 million polygons in Great Britain, 0.9 million in Northern Ireland.
- Raster Data Sets:
  - 25 m raster: derived from the vector; 23 LCM2007 classes; GB and NI provided separately with appropriate projections.
  - 1 km raster: summary products for UK-wide applications; includes dominant cover and percentage cover for both LCM2007 classes and Aggregate classes.
- Spatial framework: uses OSMM generalised cartography for GB and Large-scale Vector for NI; polygons represent real-world objects (fields, woodland blocks).

## Key Attributes and Metadata (Vector)
- Parcel_ID: unique parcel identifier (includes source image details).
- BH: Broad Habitat (dominant level, 1–23).
- BHSub: Broad Habitat sub-class (described by FieldCode).
- FieldCode: short description of sub-classes; recommended for use only with user validation.
- INTCODE: integer code (1–23) for display and QA-validated class.
- KBE: Knowledge-Based Enhancements history.
- ProbList: top 5 spectral class probabilities for the polygon.
- CorePixels / TotPixels: pixel counts used in classification.
- Construct: history of polygon construction (e.g., OSMM, segmentation variants).
- Additional attributes include details on data sources, processing, and segment construction.

## Classification and Relationships
- LCM2007 uses 23 classes based on Broad Habitat classifications; several Broad Habitats are subdivided (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediments) for higher spectral resolution.
- Appendix mappings outline relationships between LCM2007 classes and Broad Habitats and sub-classes, including FieldCodes and interpretation notes.
- Aggregate classes exist to support 1 km raster products (simplified category groupings).

## Data Access and Licensing
- 1 km raster data sets are publicly available via the CEH Information Gateway.
- Full vector product and 25 m raster product are license-based on request from CEH; online application or direct contact (spatialdata@ceh.ac.uk). Licences may apply.

## Data Formats, Size, and Projections
- Vector: large files (approx. 4.13 GB GB shapefile for 100 km × 100 km extents; NI ~433 MB).
- Raster (25 m): GB ~1.36 GB; NI ~46 MB.
- Raster (1 km): 21 MB to 49 KB depending on product.
- Projections:
  - Great Britain: British National Grid (OSGB36), Transverse Mercator.
  - Northern Ireland: Irish National Grid, later ITM transition; reprojecting supported by GIS software.
- Note: Data volumes are large due to ~10 million polygons and rich metadata per polygon.

## Production Methodology and Limitations
- Production relies on polygon-based segmentation of OSMM-derived boundaries, image segmentation, spectral classification, and knowledge-based enhancements (KBE).
- Minimum mapping unit effectively >0.5 ha; sub-0.5 ha features are dissolved into surrounding landscape.
- Broad Habitat subclass information (BHSub) adds detail but may not have QA-level reliability comparable to main LCM2007 classes; users are advised to validate subclass-level results for specific applications.
- Ground reference validation indicates varying local accuracy; users should consider local QA when interpreting fine-scale subclasses or corner cases.

## Example Data Sets and Interpretation
- Vector vs. Raster trade-offs:
  - Vector: richer attribute metadata per polygon but larger file sizes and more complex processing.
  - 25 m raster: simpler, metadata-free per-pixel data, efficient for some analyses.
  - 1 km raster: suitable for national-scale modelling; provides dominant and percentage covers for both 23 classes and aggregates.
- Example visuals illustrate distribution of Broadleaved Woodland and other habitats across the UK.

## Appendices (Supplementary Details)
- Appendix 1: Detailed LCM2007 class definitions and brief notes on habitat characteristics.
- Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCodes and class numbers).
- Appendix 3: Standard LCM2007 colour mapping (RGB values) by LCM2007 class for visualization.

## Further Information
- Final Report for LCM2007 (Morton et al., 2011) recommended for comprehensive methodology and assessment.
- Related Broad Habitat guidance (Jackson, 2000) provides definitions and relationships to other classifications.
- Data and Countryside Survey context provided by CEH and partner organizations.