# Parma2009_LandslideInventory_UTM_JJReviewed

- Purpose and content
  - Landslide inventory polygons mapped in Parma2009, identified by visual evidence of change pre- and post-typhoon.
  - Mapping conducted by two people; dataset comprises 2040 polygons with IDs (FID) and associated attributes.
  - Polygon areas range from 6 to 40,000 m².
  - Temporal scope: imagery window Oct 2019–Mar 2020; analysis performed Aug–Oct 2020.

- Data collection and methods
  - Measurements and GIS processing performed within a Geographical Information System (GIS) using inventory layers (e.g., Digital Elevation Model, geology map).
  - Mapping used high- and very high-resolution satellite imagery (0.5 m to 10 m) for evidence of landslides.
  - SOPs for methods are not available; quality Assurance conducted by two reviewers.

- Data structure and files
  - Core dataset is a single shapefile with multiple supporting files:
    - Parma2009_LandslideInventory_UTM_JJReviewed.shp (main polygons)
    - Parma2009_LandslideInventory_UTM_JJReviewed.dbf (attribute data)
    - Parma2009_LandslideInventory_UTM_JJReviewed.cpg (UTF-8 encoding)
    - Parma2009_LandslideInventory_UTM_JJReviewed.prj (WGS84 UTM Zone 51N projection)
    - Parma2009_LandslideInventory_UTM_JJReviewed.qpj (additional projection info)
    - Parma2009_LandslideInventory_UTM_JJReviewed.shx (spatial index)
    - Parma2009_LandslideInventory_UTM_JJReviewed.xml (versioning information, here 1.0)
  - Data stored as a shapefile set, with 2040 polygons and FID-based IDs.

- Spatial and technical details
  - Projection: WGS 84 / UTM Zone 51N.
  - Encoding: UTF-8.

- Data quality and provenance
  - Inventory quality checked by two people after creation.
  - No explicit SOPs documented for the techniques used.
  - Mapping anchored in the integration of inventory layers and external GIS datasets (e.g., DEM, geology).

- Data readiness and reuse
  - Dataset designed to support data-driven analysis and self-service GIS exploration through standard shapefile formats.
  - Compatible with combining with other GIS layers for enriched analysis and visualization.

- Limitations and considerations for data support
  - Methods rely on visual interpretation; potential subjectivity without documented SOPs.
  - Updates and provenance tracked through the accompanying XML file (version 1.0); ongoing changes may require access to the XML for change history.

- Potential applications for data products
  - Hazard and risk assessment, landslide susceptibility analyses, integration with terrain and geological layers.
  - Use in dashboards or GIS-based reports enabling end users to explore the inventory data.