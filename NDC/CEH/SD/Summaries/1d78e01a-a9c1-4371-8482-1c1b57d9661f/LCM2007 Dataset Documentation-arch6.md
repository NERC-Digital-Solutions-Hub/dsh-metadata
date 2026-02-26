# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Comprehensive documentation for UK Land Cover Map 2007 (LCM2007) data products, including methodology, classifications, formats, access, and limitations.
- Version: 1.0, 06 July 2011. © NERC (CEH) 2011; various copyright/licence notes.

## Overview and purpose
- Parcel-based land cover classification of the UK using 23 classes aligned with UK Broad Habitats.
- Derived from summer-winter composite satellite imagery at 20–30 m resolution.
- Upgrades LCM2000 using a spatial framework based on OS MasterMap/large-scale vector data, refined with image segments.
- Maps land cover (not strictly land use); minimum mappable unit is >0.5 ha; smaller parcels dissolved into surrounding landscape.

## Data products and formats
- Vector data set
  - Polygons with 10 attributes each; 8.6 million polygons GB, 0.9 million NI.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display/QA), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct (data sources like OSMM), etc.
  - Unique Parcel_ID retained for unambiguous communication.
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; GB and NI separated by projection.
  - 1 km raster: Summary products derived from 25 m data (dominant class, and percentage cover) using Aggregate classes for 1 km resolution.
- Class relationships and metadata
  - Appendix 2 provides the mapping between Broad Habitats, LCM2007 classes, and sub-classes.
  - Appendix 3 provides standard color mapping for display.

## Classification and accuracy
- 23 classes based on UK Broad Habitats; some subclasses exist (e.g., Built-up Areas subdivided into Urban/Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral/Coastal subclasses).
- Validation against ground reference data: average accuracy ~83% across 9,127 polygons; local variations may occur.
- KBE and ProbList help convey processing history and spectral class likelihood; user validation recommended for Broad Habitat subclass level.

## Spatial reference, extent, and data size
- Vector and raster data are provided in separate GB and NI datasets.
- Projections: Great Britain data in British National Grid; Northern Ireland data in Irish National Grid (with NI transitioning toward ITM in the future).
- File sizes (guidance):
  - Vector shapefile (GB 100 km x 100 km): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: range from ~21 MB to ~49 KB depending on product.
- MMU and topographic integration improve compatibility with other GIS datasets.

## Data access and licensing
- 1 km raster data: available via CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector product and 25 m raster product: available on request under licence from CEH.
- Online application: www.ceh.ac.uk/data; contact: spatialdata@ceh.ac.uk.
- Fees may apply for certain users/applications.

## Production methodology and caveats
- Produced from satellite imagery with integration of OSMM/Land & Property Services vector data and segmentation.
- Rich polygon metadata captures processing history, original spectral classification, and knowledge-based enhancements (KBE).
- Users should consult the Final Report for LCM2007 (Morton et al., 2011) for detailed methodology and limitations.
- Sub-class level accuracy is not guaranteed to the same standard as the base LCM2007 classes; validation recommended for subclass analyses.

## Practical guidance for use
- Choose data product based on need for detail vs. metadata:
  - Vector (with detailed attributes) for rich analysis and self-serve exploration, at the cost of larger file size.
  - 25 m raster for simpler processing with no polygon boundaries but same land cover detail and reduced metadata overhead.
  - 1 km rasters suitable for UK-wide modelling and integration with other large-scale datasets (e.g., meteorology, species distributions).
- Use Appendix 2 mappings to interpret Broad Habitat sub-classes alongside LCM2007 classes.
- Retain Parcel_ID and BH/INtcODE fields for traceability and communication among users.
- Validate Broad Habitat subclasses if using sub-class level information or ProbList-derived classifications.

## Appendices and colour mapping
- Appendix 1: LCM2007 classes with Broad Habitat definitions and examples.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard LCM2007 colour mapping for display (class-specific RGB values).

## Acknowledgements and references
- Acknowledges multiple data sources ( Landsat-TM5, SPOT, AWIFS, Ordnance Survey, etc.).
- Key references:
  - Morton et al. 2011: Final Report for LCM2007.
  - Jackson 2000: Guidance on Biodiversity Broad Habitat Classification.
- Contact CEH for data access, usage rights, and further information.
- Subject to Crown Copyright and third-party rights; usage allowed for research, private study, and internal organizational use with proper attribution.