# Parma2009_LandslideInventory_UTM_JJReviewed

- Overview
  - Landslide polygons mapped by two people using visual observation of pre- and post-typhoon evidence indicating landslide occurrence.
  - Mapping performed within GIS, incorporating inventory and other GIS layers (e.g., Digital Elevation Model, geology map).
  - Analysis conducted August–October 2020.

- Data collection and methods
  - Data collection method: visual interpretation of change events in satellite imagery to identify landslide polygons.
  - GIS integration: measurements and mapping performed in GIS with inventory layers plus ancillary GIS data (DEM, geology, etc.).
  - Imagery used: high to very high-resolution satellite imagery in the 0.5–10 m range.
  - Temporal scope: imagery window Oct 2019–Mar 2020 used for polygon delineation; analysis completed Oct 2020.

- Data content and structure
  - Core dataset: one shapefile set representing the Parma2009 Landslide Inventory (UTM JJReviewed).
  - Main file: Parma2009_LandslideInventory_UTM_JJReviewed.shp containing 2040 polygons (FID as identifier).
  - Attribute data: Parma2009_LandslideInventory_UTM_JJReviewed.dbf (associated dBase table for attributes).
  - Encoding: Parma2009_LandslideInventory_UTM_JJReviewed.cpg indicates UTF-8.
  - Projection: Parma2009_LandslideInventory_UTM_JJReviewed.prj specifies WGS 1984 UTM Zone 51N.
  - Additional projection info: Parma2009_LandslideInventory_UTM_JJReviewed.qpj.
  - Indexing: Parma2009_LandslideInventory_UTM_JJReviewed.shx (polygon indexes).
  - Versioning/changes: Parma2009_LandslideInventory_UTM_JJReviewed.xml documents changes or updates between geodatabases and external systems (inventory version 1.0).

- Data quality and validation
  - Quality control: inventory checked by two people after creation.

- Data characteristics
  - Polygon sizes: 6–40,000 m².
  - Spatial resolution of inputs: 0.5–10 m from satellite imagery.
  - Location scope: landslide polygons compiled within Parma (as per dataset naming).

- Notes and considerations for GIS use
  - No SOPs or methods documentation provided (N/A).
  - Data are packaged as a comprehensive shapefile set with full GIS-ready attributes and metadata for integration with other spatial layers.
  - The dataset emphasizes visual-based identification and GIS-based integration rather than field-measured samples.