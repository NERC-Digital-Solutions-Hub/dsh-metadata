# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Classic GIS data product documentation for a parcel-based land cover map of the UK, available in vector and raster formats, intended for map-based data visualisation and spatial analysis.

## Overview and purpose
- Land Cover Map 2007 (LCM2007) maps land cover (not land use) across the UK using 23 classes based on Broad Habitats.
- Created from summer-winter satellite imagery at 20–30 m resolution; builds on a spatial framework using OS MasterMap/large-scale vector data.
- Designed to support GIS analyses and map-based data products; recommended consulting the Final Report for full methodology and limitations.

## Data products and formats
- Vector Data Set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon has 10 attributes; unique Parcel_ID labels are assigned and should be retained.
  - Rich metadata per polygon, including processing history and a top-5 spectral class ProbList.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately.
  - 1 km raster: aggregate products (dominant class, percentage cover) for both GB and NI.
  - 1 km products include both class-based and aggregate-class summaries (dominant and percentage).

## Classes and taxonomy
- 23 LCM2007 classes aligned with Broad Habitats; includes subdivisions in some broad habitats (e.g., Suburban vs Urban; Heather vs Heather grassland; Littoral sediment vs Saltmarsh).
- Appendix 1 provides class definitions; Appendix 2 maps Broad Habitats to LCM2007 classes and sub-classes; Appendix 3 color mapping.
- LCM2007 includes a BHSub (Broad Habitat sub-class) attribute and FieldCode; INTCODE provides a recommended display class (1–23).

## Data attributes and QA
- Vector attributes (examples): Parcel_ID, BH (dominant class), BHSub (sub-class), FieldCode, INTCODE, KBE (knowledge-based enhancements), ProbList, CorePixels, Construct, TotPixels.
- High-level QA: validated against ground reference polygons; average accuracy ~83% across 9127 polygons; local inconsistencies may occur.
- Warning: Broad Habitat sub-classes are not always as accurately validated as the main LCM2007 classes; users should validate if using sub-classes.

## Spatial resolution, projection, and extent
- GB vector/raster in British National Grid; NI data in Irish National Grid.
- NI moving toward Ireland Transverse Mercator (ITM) projection; re-projection supported by GIS tools as needed.
- Minimum mapped unit: polygons > 0.5 ha; dissolves parcels smaller than 0.5 ha and linear features < 20 m.

## Data access and licensing
- 1 km raster data (GB/NI) available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH (with possible fees).
- Online application process described; contact spatialdata@ceh.ac.uk for details.

## Data sizes (guidance)
- Vector (GB): ~4.13 GB; NI: ~433 MB (Shapefile bundle for 100 km x 100 km extents).
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- 1 km raster: GB 21 MB to 49 KB depending on product; NI similarly small for some products.

## Use cases, limitations, and best practices
- Suitable for detailed map-based analyses and integration with other GIS datasets; vector format offers rich attribute data and metadata but larger file sizes.
- 1 km raster products provide higher-level summaries suitable for large-scale modelling or when data volume is a concern.
- LCM2007 is designed for land cover mapping; not ideal for change detection between different years due to class/structure differences and typical 20% image/class error.
- When using the vector, retain Parcel_ID for traceability and communication; interpret Broad Habitat sub-classes with caution and consider field validation for sub-class analyses.
- Data packaging challenges: large datasets; consider 25 m raster for simpler processing or 1 km rasters for UK-wide analyses; ensure appropriate data management for large vector datasets.

## Documentation, updates, and further information
- Version history: Version 1.0 (2011); Version 1.2 (May 2012) and updates published; Version 1.2 (May 2014) includes additional tile updates and water class inclusion in some 1 km products.
- Appendices provide class mappings, color schemes, and change-log updates (e.g., Fair Isle, Stranraer, water class additions).
- Acknowledgements note multiple data sources and licensing partners (Landsat, SPOT, OS, soil, elevation, and administrative datasets).

## Practical guidance for GIS specialists
- Start with 1 km raster products for broad UK-scale analyses; transition to 25 m or vector data for finer-scale, attribute-rich analyses.
- Use the 23-class LCM2007 schema for detailed habitat-based mapping; for broader analyses, leverage the Aggregate classes in 1 km rasters.
- Retain Parcel_ID and KBE/ProbList metadata to support reproducibility and provenance; validate Broad Habitat sub-classes when used for decision-support.
- Be mindful of projection conversions when integrating GB and NI datasets; plan for reprojection to ITM/other targets as needed.
- Consult Morton et al. 2011 Final Report for in-depth methodology and Appendix guidance on class definitions and color mapping.