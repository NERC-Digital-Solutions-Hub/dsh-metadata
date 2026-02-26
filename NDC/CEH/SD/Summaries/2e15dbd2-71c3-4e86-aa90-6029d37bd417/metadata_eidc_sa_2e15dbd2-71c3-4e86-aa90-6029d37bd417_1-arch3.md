# Parma2009_LandslideInventory_UTM_JJReviewed

## Overview
- Single shapefile-based inventory of 2040 landslide polygons.
- Polygons mapped from high- to very high-resolution satellite imagery (0.5–10 m) within Oct 2019–Mar 2020.
- Analysis period Aug–Oct 2020.

## Data Collection and Methods
- Mapping conducted by two people using visual observation of pre/post-typhoon evidence of landslides.
- GIS-based compilation using the inventory plus other layers (Digital Elevation Model, Geology map, etc.).

## Data Structure and Documentation
- Main dataset components:
  - Parma2009_LandslideInventory_UTM_JJReviewed.shp (2040 polygons; FID)
  - Parma2009_LandslideInventory_UTM_JJReviewed.dbf (attribute data)
  - Parma2009_LandslideInventory_UTM_JJReviewed.cpg (UTF-8 encoding)
  - Parma2009_LandslideInventory_UTM_JJReviewed.prj (WGS84 UTM Zone 51N projection)
  - Parma2009_LandslideInventory_UTM_JJReviewed.qpj (projection metadata)
  - Parma2009_LandslideInventory_UTM_JJReviewed.shx (polygon indexes)
  - Parma2009_LandslideInventory_UTM_JJReviewed.xml (version/changes for geodatabase/external systems; inventory version 1.0)

## Quality Assurance and Data Integrity
- Inventory quality checked by two people after generation.
- Date of analysis of the data: August–October 2020.
- No explicit Standard Operating Procedures (SOPs) documented for methods.

## Relevance to Monitoring Frameworks
- Provides a concrete GIS-based environmental health indicator (landslide inventory) suitable for policy scrutiny and decision-making.
- Illustrates practical data handling considerations: data provenance, metadata completeness, and version control via XML.
- Highlights interoperability and governance aspects: shapefile format with multiple related files, obviating some barriers but requiring robust data governance and documentation.

## Key Considerations for Policymaking and Monitoring
- Data resolution and extent appear adequate for regional risk assessment but require clear metadata to ensure usability.
- Metadata completeness across all file types (SHP, DBF, PRJ, CPG, QPJ) supports transparency and reuse.
- Versioning and change logs (XML) aid reproducibility and governance.
- Need for documented SOPs to standardize procedures and facilitate cross-project comparability.
- Timeliness: data collection and analysis periods span 2019–2020; timely updates needed for ongoing monitoring.