# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A comprehensive description of the Land Cover Map 2007 (LCM2007) data products for the UK, including background, product specifications, data access, and supporting documentation.
- Emphasizes data governance aspects such as metadata richness, provenance, and licensing considerations relevant to data stewards.

## Overview and purpose

- LCM2007 is a parcel-based land cover classification for the UK using 23 Broad Habitat-based classes, derived from satellite imagery with 20–30 m pixels.
- Maps land cover (not strictly land use) and uses a minimum mapping unit of 0.5 ha (parcels smaller than 0.5 ha or lines <20 m are dissolved).
- Builds on LCM2000 with a framework aligned to OS cartographic layers to improve compatibility with GIS datasets.
- Not designed for change detection across time due to class and spatial structure differences and typical classification errors (~20%).

## Data products and structure

- Vector data set
  - Polygons with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - ~8.6 million polygons for Great Britain; ~0.9 million for Northern Ireland.
  - Unique Parcel_ID per polygon; KBE history records processing steps.
  - Detailed metadata attached to each polygon, including original spectral classification and processing history.
- Raster data sets
  - 25 m raster (GB and NI; 23 LCM2007 classes; detailed class-to-pixel mapping).
  - 1 km raster products (GB and NI): Dominant class, Percentage cover for classes, and Aggregate-class equivalents (for 1 km).
  - GB and NI rasters use different projections (British National Grid for GB; Irish National Grid for NI).
- Aggregate and mapping details
  - Aggregate classes for 1 km rasters merge LCM2007 classes to enable coarser-scale analyses.
  - Appendix 1–3 provide class definitions, relationships, and standard colour mappings for visualization.

## Metadata, provenance, and processing

- Rich metadata for each polygon includes:
  - Source images, polygon construction history (OSMM-based or segmentation-based), Knowledge-Based Enhancements (KBE) applied, and ProbList (top spectral-class probabilities).
  - CorePixels and TotPixels metrics describing pixel usage in classification.
- Documented processing history and QA lineage to support reproducibility and validation by data stewards and data users.
- Parcel_ID aids unambiguous communication and traceability of polygons back to source data.

## Quality assurance and validation

- Validation performed against ground reference data with 9,127 polygons, achieving an average accuracy of 83% at the 23-class thematic resolution.
- Note: Accuracy figures are averaged; local errors may vary; users should perform their own validation when working at sub-class levels (BHSub) or for specific applications.

## Classification scheme and documentation

- 23 LCM2007 classes based on UK Broad Habitats, with some sub-classes and splits (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland).
- Appendix 1–3 cover:
  - Class descriptions and definitions.
  - Relationship mappings between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Standard colour mappings for class visualization (used in final reports and ArcGIS styles).
- LCM2007 maps land cover rather than land use; examples illustrate differences between cover and use interpretations.

## Data access, licensing, and reuse

- Access options:
  - 1 km raster data sets available via the CEH Information Gateway.
  - Full vector product and 25 m raster product available under license on request from CEH.
- Licensing and fees may apply depending on user and application.
- Contact details for access: CEH Information Gateway and data@ceh.ac.uk.
- Appendix 4 lists product updates (Version 1.2, May 2014), including additions (Fair Isle, Stranraer), water class inclusion, and other minor updates.

## Projections and geographic coverage

- Vector and raster data sets for Great Britain use British National Grid; Northern Ireland uses Irish National Grid.
- NI is transitioning toward the Ireland Transverse Mercator (ITM) projection; reprojection guidance provided for GIS workflows.

## Data volumes and storage considerations

- Vector data: contains almost 10 million polygons with 10 attributes each; large file sizes typical of rich polygon attribute datasets.
- Raster data: Geotiff formats with substantial sizes (e.g., GB 25 m ~1.36 GB; NI 25 m ~46 MB; vector shapefiles ~4.13 GB for GB, ~433 MB for NI in 100 km × 100 km extents).
- Users should plan for substantial storage and processing capacity, especially for vector products with extensive attribute data.

## Practical guidance for data stewards

- Metadata completeness and provenance
  - Preserve Parcel_ID and complete KBE history to ensure traceability and reproducibility.
  - Maintain full metadata for each polygon and raster product, including source imagery and processing steps.
- Data quality and suitability
  - Use the 23-class LCM2007 vector product for detailed thematic analyses; employ 1 km rasters or aggregated classes for coarse-scale modelling.
  - Be aware of limitations in change detection; avoid relying on LCM2007 for detecting subtle land cover changes over time.
- Data governance and access management
  - Align sharing with licensing terms; document access permissions and any fee structures.
  - Ensure version control (e.g., reference to Version 1.2 updates) and maintain records of changes across product releases.
- Interoperability and reuse
  - Retain class mappings and colour legends (Appendix 3) for consistent visualization across platforms.
  - Be prepared to reproject NI data to ITM or other required coordinate systems for integration with local datasets.
- Documentation and user guidance
  - Provide guidance on when to use 25 m vector vs. 25 m raster vs. 1 km rasters, including MMU considerations and class-level accuracy notes.
  - Highlight the recommended QA practice before applying Broad Habitat sub-classes due to lower or variable accuracy at subclass levels.

## Version history and updates

- Version 1.0 (Original, July 2011)
- Version 1.2 (May 2012; updated for dataset updates and change-detection considerations)
- Version 1.2 (May 2014; minor product updates, water class additions, Fair Isle and Stranraer inclusions)

## Acknowledgements and rights

- Documentation and data incorporate data from multiple satellite and cartographic sources.
- Copyrights and licensing managed by NERC CEH and partner organizations; proper permissions required for data reuse and redistribution.