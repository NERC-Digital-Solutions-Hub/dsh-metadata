# Parma2009_LandslideInventory_UTM_JJReviewed

- Overview
  - A landslide inventory dataset mapped as polygons, originally from Parma2009, with versioned updates (UTM Zone 51N, WGS84). Mapping performed using high- and very high-resolution satellite imagery for Oct 2019–Mar 2020; analysis of the dataset occurred Aug–Oct 2020.
  - Two observers performed the polygon delineation by visually identifying evidence of change before and after the referenced typhoon.

- Data Collection and Provenance
  - Polygons were mapped by two people based on visual evidence of landslide occurrence around the typhoon event.
  - Measurements and GIS-based processing were conducted using a combination of the inventory and other GIS layers (Digital Elevation Model, Geology map, etc.).
  - Imagery resolution used for mapping ranges from 0.5 m to 10 m spatial resolution.

- Data Structure and Formats
  - Single shapefile package comprising:
    - Parma2009_LandslideInventory_UTM_JJReviewed.shp (ge geometry) with 2040 polygons (FID).
    - Parma2009_LandslideInventory_UTM_JJReviewed.dbf (attribute data).
    - Parma2009_LandslideInventory_UTM_JJReviewed.cpg (UTF-8 encoding).
    - Parma2009_LandslideInventory_UTM_JJReviewed.prj (projection: WGS84 UTM Zone 51N).
    - Parma2009_LandslideInventory_UTM_JJReviewed.qpj (additional projection information).
    - Parma2009_LandslideInventory_UTM_JJReviewed.shx (shape index).
    - Parma2009_LandslideInventory_UTM_JJReviewed.xml (versioning/changes between geodatabases and external systems; version 1.0).

- Spatial and Temporal Coverage
  - Spatial: Polygon inventory covering landslides within the Parma context (originating from Parma2009 dataset).
  - Temporal: Mapping window Oct 2019–Mar 2020; analysis/date of data processing Aug–Oct 2020.

- Data Quality and Validation
  - Quality control performed by two individuals after inventory creation.
  - SOPs for techniques are not provided in this metadata; no sample storage or treatment records.

- Accessibility, Metadata, and Versioning
  - Data provided as a complete shapefile package with explicit encoding (UTF-8) and projection details (WGS84 UTM Zone 51N).
  - XML file documents changes/updates between geodatabases and external systems (version 1.0 present).

- Usage, Assumptions, and Limitations
  - Based on visual interpretation of landslide evidence; relies on high-resolution imagery and GIS layers for positional accuracy and attribution.
  - No explicit standard operating procedures (SOPs) or data storage protocols documented.
  - The dataset’s utility hinges on accurate georeferencing, consistent attribute schema (in the DBF), and clear versioning for future updates.

- Implications for Data Leaders
  - Demonstrates end-to-end handling of a geospatial inventory: collection via visual assessment, GIS integration, multi-file shapefile packaging, and explicit versioning metadata.
  - Highlights importance of documentation (projection, encoding, version history) to support discoverability and reuse.
  - Suggests need for accompanying SOPs and data stewardship practices to improve reproducibility and cross-institution collaboration.