# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK parcel-based land cover dataset (LCM2007) using 23 classes derived from Broad Habitats.
- Maps land cover (not strictly land use) from summer-winter satellite composites with 20–30 m pixels.
- Supports GIS map-based data products; designed to be integrated with other datasets and used in diverse applications.
- Not a substitute for the Final Report; consult Morton et al. (2011) for comprehensive methodology and limitations.

## Data products and formats
- Vector data set (GB and NI): polygons with attached attributes per parcel (approx. 10 attributes per polygon; 8.6M polygons GB, 0.9M NI).
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct.
  - Includes unique Parcel_ID for unambiguous communication; recommended to retain.
- Raster data sets:
  - 25 m raster (GB and NI): 23 LCM2007 classes; 25 m pixel values; derived from vector.
  - 1 km raster (GB and NI): aggregate products (dominant class, percentage cover) and both for target and aggregate classes.
- Aggregates (1 km): simplified products using 1 km pixels to reduce thematic complexity.
- Colour mapping and display: Appendix 3 provides standard color mappings; ArcGIS .lyr file available for classnames/colors.

## Spatial resolution, extent, and data structure
- 23 LCM2007 classes mapped from 20–30 m imagery; minimum mappable unit > 0.5 ha; parcels < 0.5 ha or linear features < 20 m dissolved into surrounding landscape.
- Vector: ~10 attributes per polygon; detailed metadata per polygon.
- Raster: 25 m and 1 km products; GB and NI provided separately with respective projections (GB: British National Grid; NI: Irish National Grid; NI transitioning towards ITM).
- Coverage: Great Britain and Northern Ireland; vector has 8.6M GB polygons and 0.9M NI polygons.

## Classification and classes
- 23 classes based on UK Broad Habitats; some subclasses available (e.g., Built-up Areas subdivided into Suburban/Urban; Dwarf Shrub Heath split into Heather and Heather grassland; Littoral Sediment split into Saltmarsh and Littoral sediment).
- Appendix 1 details each Broad Habitat class; Appendix 2 describes relationships between Broad Habitats, LCM2007 classes, and sub-classes.
- Broad Habitat sub-classes (BHSub) exist but are not as reliably validated as the main LCM2007 classes; use ProbList and validation cautiously at subclass level.
- LCM2007 class numbers (INTCODE) are recommended for display and QA.

## Metadata, quality, and validation
- Rich metadata: per-polygon processing history, KBE (Knowledge-based enhancements), and probability list (top 5 spectral class matches).
- Validation: ground reference data against 9127 polygons; average accuracy ~83%, acknowledging local variability and potential higher/lower accuracies in places.
- Change mapping across LCM1990/2000/2007 is complex and not recommended for robust change detection due to differing class definitions, spatial structures, and typical image classification errors (~20%).

## Data access and licensing
- Data access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request; licensing may apply.
- License considerations: fees may apply for some users/applications; contact CEH for details.

## Projections and coordinate systems
- GB data: British National Grid (OSGB 1936), Transverse Mercator projection.
- NI data: Irish National Grid; moving toward Ireland Transverse Mercator (ITM) projection.
- Reprojection may be required depending on GIS workflow.

## File sizes and data footprint
- Vector (GB shapefile, 100 km x 100 km blocks): ~4.13 GB; NI: ~433 MB.
- Raster 25 m:
  - GB: ~1.36 GB; NI: ~46 MB.
- Raster 1 km:
  - Range: ~21 MB to ~49 KB depending on the product (dominant/percentage/aggregate targets).
- Large data volumes; plan storage and processing accordingly.

## Practical guidance for GIS workflows
- Use the vector product when you need detailed polygon boundaries, rich attributes, and per-polygon QA history; retain Parcel_ID for traceability.
- Use 25 m rasters for detailed spatial analysis where polygon metadata is less critical, or when working with raster-only tools.
- Use 1 km rasters for large-area modelling and when interfacing with other gridded environmental datasets; apply appropriate aggregation (classes vs. aggregates) for your analysis.
- For display, rely on INTCODE for class labeling; ProbList provides spectral class confidence for validation or filtering.
- When working with Broad Habitat sub-classes, perform independent validation if subclass-level accuracy is critical.

## Appendices (summary)
- Appendix 1: Detailed LCM2007 classes with descriptive brief reviews and ecological notes.
- Appendix 2: Mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode references).
- Appendix 3: Standard LCM2007 colour mapping (including an ArcGIS .lyr file for ease of use).
- Appendix 4: Version updates (Version 1.2, May 2014) including added OS Tile updates and water class inclusion for some 1 km products.

## Additional context and references
- For a comprehensive understanding of methodology, limitations, and product specifics, consult the Final Report for LCM2007 (Morton et al., 2011).
- Related Broad Habitat framework references: Jackson (2000) guidance on interpretation of Broad Habitat classifications.