# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Parcel-based UK land cover classification (23 classes) derived from satellite imagery (20–30 m resolution).
- Maps land cover (not land use); built to align with Broad Habitats and OS spatial frameworks.
- Provides a range of data products (vector and raster) to support diverse GIS and analytics needs.
- Not ideal for change detection due to cross-walk and structural differences between LCM versions.

## Data Products and Content
- Vector Data Set
  - 8.6 million polygons (Great Britain) and 0.9 million polygons (Northern Ireland).
  - Each polygon includes 10 attributes and a unique Parcel_ID for traceability.
  - Key attributes: BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct.
  - Rich metadata and QA history; recommended to retain Parcel_ID for unambiguous communication.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes (GB and NI separate projections).
  - 1 km raster: Aggregate and dominant class summaries derived from 25 m data; includes:
    - Dominant cover for 23 classes (1 km)
    - Dominant cover for Aggregate classes (1 km)
    - Percentage cover for 23 classes (1 km)
    - Percentage cover for Aggregate classes (1 km)
- Data formats and compatibility
  - 25 m raster provides detailed spatial information without polygon metadata; suitable for memory-constrained apps.
  - 1 km rasters ideal for large-scale UK-wide modelling and integration with other datasets (e.g., meteorology, species distributions).

## Classes and Classification
- 23 Broad Habitat classes based on UK Biodiversity Action Plan Broad Habitats.
- Some classes subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban).
- Appendix 2 provides crosswalks between Broad Habitats, LCM2007 classes, and sub-classes.
- Appendix 3 provides the standard colour mapping for display.

## Production, Metadata, and Validation
- Produced from summer-winter composite satellite imagery with a 0.5 ha minimum mappable area; smaller parcels are dissolved into surrounding areas.
- Each polygon includes extensive metadata: processing history, original spectral classification, KBE history, and ProbList.
- Ground reference validation: average accuracy around 83% (with variation by location); local discrepancies may occur.
- Change mapping across LCM1990, LCM2000, and LCM2007 is not straightforward due to class and spatial differences; not well suited for change detection.

## Map Projection and Data Access
- Projections:
  - Great Britain: British National Grid (OSGB36)
  - Northern Ireland: Irish National Grid (with ongoing move towards ITM in NI)
- Access:
  - 1 km raster products via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; licensing fees may apply.
  Contact: spatialdata@ceh.ac.uk; data portal: www.ceh.ac.uk/data

## File Size and Scope
- Vector (GB, 100 km x 100 km shard): roughly 4.13 GB (GB); 433 MB (NI).
- Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
- 1 km rasters: 21 MB to 49 KB depending on product type.
- Data volumes are large due to ~10 million polygons and per-polygon attributes.

## Practical Guidance for Data Support
- Use 1 km rasters for broad UK-scale analyses and integration with other large-scale datasets.
- Use 25 m vector or raster products when detailed, polygon-level or high-resolution land cover information is required, keeping an eye on file sizes.
- Retain Parcel_ID in vector data to preserve traceability to source imagery and processing steps.
- Apply your own validation when using Broad Habitat sub-classes (BHSub) since QA focuses on LCM2007 classes; sub-classes may be less consistent.
- Consider aggregation to Aggregate classes for applications where cross-year comparability is critical.

## Version History and Updates
- Version 1.2 (May 2014): Updates to include OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer); water class added to newer 1 km aggregate/dominant products; NI/GB updates as applicable.

## Appendix Highlights (Brief)
- Appendix 1: Detailed LCM2007 23 class definitions and interpretation notes.
- Appendix 2: Crosswalk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard LCM2007 colour mapping for display (plus ArcGIS layer).
- Appendix 4: List of product updates (v1.2) and specific tile inclusions.