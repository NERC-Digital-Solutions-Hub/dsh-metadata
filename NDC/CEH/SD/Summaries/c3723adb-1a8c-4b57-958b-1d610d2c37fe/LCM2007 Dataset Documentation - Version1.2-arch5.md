# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Document: Land Cover Map 2007 Dataset Documentation, Version 1.2 (May 2014)
- Purpose: Describes the LCM2007 data products, production methodology, metadata, validation, data access, and update history to support data governance and reuse.

## Overview of the Dataset

- LCM2007 is a parcel-based UK land cover classification using 23 Broad Habitat–based classes, derived from satellite imagery (20–30 m pixels).
- It updates LCM2000 with improved spatial framework (OSMM in GB; Large-scale Vector in NI) and image segmentation to better represent real-world objects (fields, woodland blocks).
- Important distinction: maps land cover, not strictly land use; minimum mappable area is >0.5 ha; small parcels are dissolved into surrounding landscape.
- Datasets are provided in multiple formats and resolutions to suit varied applications:
  - Vector data (highly detailed polygons with rich attributes)
  - 25 m raster (full 23-class resolution)
  - 1 km raster products (aggregated outputs: dominant/percentage by class and aggregate classes)
- GB and NI datasets are provided separately with respective coordinate systems (GB: British National Grid; NI: Irish National Grid; NI moving toward ITM).

## Data Products and Structure

- Vector Data Set
  - 8.6 million polygons (GB) and 0.9 million (NI)
  - 10 polygon attributes per record, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (processing history), ProbList (top 5 spectral matches), CorePixels, TotPixels, Construct (data sources and segmentation method)
  - Unique Parcel_ID per polygon; recommended to retain for unambiguous communication
  - Broad Habitat sub-classes provide additional, but not QA-validated, information; ProbList aids interpretation with spectral likelihoods
  - Appendix 2 and Appendix 3 detail class relationships and colour mappings
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI have separate grids
  - 1 km raster: summarises 25 m data to dominant class and percentage cover for each 1 km pixel; available as:
    - Dominant cover by LCM2007 classes
    - Dominant cover by Aggregate classes
    - Percentage cover by LCM2007 classes
    - Percentage cover by Aggregate classes
  - Metadata in tables (dimensions, extents, coordinate extents, pixel sizes, data types, projections, datums)
- Class Structure and Aggregation
  - 23 LCM2007 classes mapped from Broad Habitats (Appendix 1)
  - Aggregate classes used for 1 km rasters; Table 2 documents relationships between LCM2007 classes, Broad Habitats, and Aggregate classes
  - Example: some Broad Habitats subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban)
- Data Access and Licensing
  - 1 km raster data: CEH Information Gateway
  - Full vector product and 25 m raster product: license-on-request from CEH (fees may apply)
  - Data licenses and access details provided on CEH website
- Data Projections and Spatial Details
  - GB: British National Grid; NI: Irish National Grid
  - NI is transitioning to ITM; reprojecting to ITM is supported by GIS packages

## Metadata, Quality Assurance, and Validation

- Rich metadata embedded at polygon level, including:
  - Processing history (KBE), source imagery, and polygon construction details
  - ProbList with top spectral-class matches
  - CorePixels and TotPixels reflecting pixel data used for classification
- Validation
  - Ground reference validation against 9127 polygons yields average accuracy around 83%
  - Local discrepancies may occur; users should perform their own validation, especially at sub-classes
- Change Mapping
  - Cross-temporal comparison (1990/2000/2007) is complex due to changing class definitions and spatial structure
  - Classified image errors around 20% complicate change detection; LCM products are not ideal for straightforward change mapping
- Knowledge-Based Enhancements (KBE)
  - Documented per-polygon KBEs, including corrections for soil, altitude, coastal masks, urban masks, etc.
  - KBE history helps trace adjustments but may require user validation for certain sub-classes

## File Size, Storage, and Management

- Vector dataset: large due to 10 attributes per polygon (GB ~4.13 GB; NI ~433 MB in 100 km x 100 km shapefile)
- Raster datasets:
  - 25 m GB: ~1.36 GB
  - 25 m NI: ~46 MB
  - 1 km products: 21 MB (percentage) to 49 KB (dominant)
- Implication for data governance: substantial storage needs and careful management of multiple formats and versions

## Data Updates and Version History

- Version history and updates (Version 1.2, May 2014) include:
  - Vector GB: OS Tile HZ (Fair Isle) added
  - 25 m GB and 1 km products: include Fair Isle and Stranraer tiles
  - 1 km aggregate/dominant products (GB and NI) updated to include water class
- Appendix 4 lists updates by product and version
- Product line maintained by CEH with attribution to data sources (Landsat, SPOT, AWIFS, OS, etc.)

## Practical Guidance for Data Stewards

- Governance and interoperability
  - Maintain Parcel_ID and associated metadata for traceability and communication
  - Preserve KBE histories and ProbList to enable reproducibility and audit of polygon construction
  - Use Appendices and Morton et al. (2011) Final Report for in-depth methodology and validation context
- Data quality and suitability
  - Use 1 km aggregates when large-area modelling is required; be aware of potential loss of thematic detail
  - Exercise caution with Broad Habitat sub-classes; validate at the desired taxonomic resolution if needed
  - For change analysis, consider the substantial differences among LCM2007, LCM2000, and earlier datasets
- Access, licensing, and lifecycle management
  - Plan for license fees and access procedures for vector and 25 m rasters
  - Track versioning and updates (Version 1.2 onward) to ensure analyses use current data
- Data governance in practice
  - Prepare mapping between LCM2007 classes and user needs, especially for aggregations
  - Document data provenance and processing steps when sharing datasets within an organization or network
  - Provide users with references to primary reports (Morton et al., 2011; Jackson, 2000) for methodological context

## References and Additional Information

- Morton et al. 2011. Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson 2000. Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- Appendices include:LCM2007 classes; relationships between Broad Habitats, LCM2007 classes and sub-classes; colour mappings; and product update history.