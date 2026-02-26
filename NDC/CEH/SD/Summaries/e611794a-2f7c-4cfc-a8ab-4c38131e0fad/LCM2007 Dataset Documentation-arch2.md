# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK parcel-based land cover classification using 23 Broad Habitat-based classes.
- Created from summer-winter composite satellite imagery at ~20–30 m resolution.
- Maps land cover (not land use) with a minimum mappable unit of >0.5 ha; smaller parcels and very short linear features are dissolved.
- Supports a range of data products and applications, including GIS integration and environmental monitoring.

## Data products and structure
- Vector data set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct (origin of polygon).
  - Parcel_ID enables unique communication between users; recommended to retain.
  - Sub-classes (BHSub) provide additional information but are not as rigorously QA-validated as the LCM2007 classes.
- Raster data sets
  - 25 m and 1 km raster products derived from the vector data.
  - 23 LCM2007 classes for 25 m; 1 km rasters provide dominant class and percentage cover for LCM2007 classes and aggregates.
  - Great Britain and Northern Ireland provided in separate projections and extents.
- Class structure and mappings
  - 23 LCM2007 classes based on UK Broad Habitats; some broad habitats are further divided into sub-classes (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other).
  - Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3 provides standard colour mappings for visualization.

## Methodology and data quality
- Created from segmented image data and generalised OS mapping framework, refined with image segments and knowledge-based enhancements (KBE).
- Ground reference validation: average accuracy around 83% across 9,127 polygons; local variability expected.
- Data are validated at the 23-class thematic level; caution advised when using Broad Habitat sub-classes due to varying accuracy.
- LCM2007 is designed to be compatible with a wide range of GIS datasets and to reflect real-world objects (e.g., fields, woodland blocks).

## Data formats, access, and storage
- Vector data: high fidelity but large file sizes; recommended for applications needing full attribute detail.
- 25 m raster: detailed land cover with simpler data structure and smaller metadata load.
- 1 km raster: suitable for national-scale modelling and integration with other datasets (e.g., meteorology, species distribution).
- File size guidance (approximate; varies by format):
  - Vector in 100 km x 100 km shapefile: GB ~4.13 GB; NI ~0.43 GB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on product).
- Coordinate systems
  - GB vector/raster: British National Grid; NI data: Irish National Grid.
  Northern Ireland is transitioning toward ITM projection; reprojecting is supported by GIS tools.
- Data access
  - 1 km raster data sets available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH; online application process and potential licence fees.

## Practical guidance for users
- LCM2007 maps land cover, not land use; interpret with awareness that some cover may not indicate current management (e.g., grass for recreation vs grazing).
- Minimum mapping unit and dissolution rules can affect small fields and linear features; consider this in analysis.
- Use QA guidance and consult the Final Report (Morton et al., 2011) for in-depth methodology and limitations.
- For detailed subclass information or validation at sub-classes, perform your own validation, as Broad Habitat sub-classes may have lower validation confidence.

## Appendices (highlights)
- Appendix 1: LCM2007 Classes – descriptions and interpretation of the 23 Broad Habitat classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3: Colour mapping recipe for standard visualisation of LCM2007 classes.

## Further information and acknowledgements
- Project: Final Report for LCM2007 – Morton et al. (2011). Countryside Survey Technical Report No. 11/07.
- Basis imagery from Landsat, SPOT, and other sensors; extensive data provenance and licensing details acknowledged.
- Documentation, data access, and contact: CEH (Centre for Ecology & Hydrology) and Countryside Survey partnership.