# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose: Provides a range of UK land cover data products (LCM2007) to support diverse user needs, enabling analysis and data products for exploration of land cover across Great Britain and Northern Ireland. Based on 23 Broad Habitat classes and satellite imagery (20–30 m pixels) from summer-winter composites; upgrades LCM2000 and aligns with OS cartography for GIS compatibility.
- Recommendation: Refer to the Final Report for comprehensive methodology, metadata, and limitations; this document focuses on LCM2007 data products and usage.

## What LCM2007 is and what it maps

- Parcel-based classification of UK land cover (not land use) using 23 classes derived from UK Biodiversity Action Plan Broad Habitats.
- Output units are polygons (vector) built from image segments; minimum mappable area is >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.
- Some Broad Habitats are further subdivided into sub-classes for certain classes (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

## Data products and formats

- Vector data set: polygons with 10 attributes per polygon; approximately 8.6 million polygons in GB and 0.9 million in NI.
- Raster data sets:
  - 25 m raster: 23 LCM2007 classes (GB and NI separate projections).
  - 1 km raster: dominant class, and percentage cover for both LCM2007 classes and aggregate classes.
- Aggregates: 1 km rasters use Aggregate classes (merged from 23 LCM2007 classes) for broader analyses.

## Attributes and metadata (Vector product)

- Parcel_ID: unique parcel identifier (includes source image); recommended to keep for communication clarity.
- BH: Broad Habitat (dominant level, e.g., Broadleaved woodland).
- BHSub: Broad Habitat sub-class description.
- FieldCode: short text field code (used in construction; user validation advised for sub-classes).
- INTCODE: integer class code (1–23) recommended for display; linked to QA.
- KBE: Knowledge-based enhancements applied during processing.
- ProbList: top 5 spectral class probabilities for the polygon.
- CorePixels / TotPixels: pixel counts used in classification.
- Construct: history of polygon construction (OSMM-derived or segmentation-based).
- Other attributes include related metadata about data sources and processing steps.

## Classification and interpretation

- 23 LCM2007 classes aligned with Broad Habitats; Appendix 2 provides mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3 includes standardized colour mapping (useful for visualization in GIS).
- LCM2007 validation: ground reference data across 9127 polygons yielded an average accuracy of 83% (average; local variations may occur).

## Usage considerations and limitations

- Change mapping: comparing LCM2007 with prior products is complex due to differing class definitions and spatial structure; typical spectral/classification error around 20% reduces reliability for change detection.
- LCM maps land cover (not strictly land use); some land covers may reflect land management or spectral signatures rather than actual use.
- Sub-class information (BHSub) requires user validation for reliable interpretation; Broad Habitat sub-classes may be less consistently accurate than main LCM2007 classes.
- Output sizes are large (vector and 25 m rasters); 1 km rasters are smaller and suitable for national-scale modelling.
- Northern Ireland is transitioning to ITM; GIS software should be able to reproject NI data as needed.

## Data access and licensing

- 1 km raster data (target/percentage and dominant class) available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; apply via CEH website or contact spatialdata@ceh.ac.uk; some licenses may apply.
- Acknowledges multiple data sources and copyright restrictions; documentation notes that data are complex and should be consulted with Morton et al. (2011) for detailed methodology.

## Spatial reference and data structure details

- Projections:
  - GB: British National Grid (OSGB 1936)
  - NI: Irish National Grid (Ireland 1965), with transition to ITM ongoing
- Raster specifications (GB NI differences):
  - 25 m rasters: pixel size 25 m; coordinates based on south-west corner; 8-bit unsigned values.
  - 1 km rasters: pixel size 1000 m; percentages and dominant class per 1 km cell; 8-bit unsigned values.
- File sizes (guidance):
  - Vector GB shapefile: ~4.13 GB
  - Vector NI shapefile: ~433 MB
  - Raster GB 25 m: ~1.36 GB
  - Raster NI 25 m: ~46 MB
  - 1 km rasters: tens of MBs to KBs (depending on product)
- Data access details:
  - CEH gateway hosts the 1 km raster products.
  - Full vector and 25 m raster products require licence on request.
  - Licence fees may apply; contact CEH for specifics.

## Appendices and updates

- Appendix 1: Detailed LCM2007 classes descriptions and interpretation guidance for each Broad Habitat.
- Appendix 2: Detailed mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping for standard visualization (also provided as ArcGIS .lyr file).
- Appendix 4: Version updates (Version 1.2, May 2014) including tile additions (Fair Isle, Stranraer), water class inclusion for 1 km products, and other minor updates.

## Additional references

- Morton et al. 2011: Final Report for LCM2007.
- Jackson 2000: Guidance on interpretation of Biodiversity Broad Habitat Classification.

## Acknowledgements

- Data derived from Landsat-TM5, SPOT, AWIFS, and OS cartography; CEH acknowledges contributing organisations and data providers; copyright notices apply.