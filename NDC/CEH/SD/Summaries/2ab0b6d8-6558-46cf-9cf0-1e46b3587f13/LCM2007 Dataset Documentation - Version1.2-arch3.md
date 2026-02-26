# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- LCM2007 is a UK-wide, parcel-based land cover classification using 20–30 m satellite imagery.
- Provides 23 Broad Habitat (BH)-based classes, serving as a land cover map (not land use) and updating LCM2000.
- Spatial units are polygons with a minimum mappable area of >0.5 ha; smaller parcels are dissolved.
- Designed to support diverse monitoring needs, but not a single universal standard—consult the Final Report for detailed methodology and limitations.

## Data Products

### Vector Data Set
- GB: ~8.6 million polygons; NI: ~0.9 million polygons.
- Each polygon carries 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Parcel_ID provides a unique identifier for communication between users; recommended to retain.
- Rich metadata per polygon, including processing history, Knowledge-Based Enhancements (KBE), and a top-5 spectral class probability list (ProbList).
- Contains Broad Habitat sub-classes (BHSub) and FieldCode; INTCODE is the class recommended for display and QA-validated class.
- Large file sizes; vector dataset is highly descriptive but more storage-heavy than rasters.

### Raster Data Sets
- 25 m raster: 23 LCM2007 classes (GB and NI separately).
- 1 km raster: aggregated products (dominant class, and percentage cover) for both LCM2007 classes and 1 km Aggregate classes.
- GB and NI projections differ: GB uses British National Grid; NI uses Irish National Grid.
- Detailed metadata includes grid dimensions, extents, pixel size, data type, projection, and datum.

## Data Structure and Metadata
- LCM2007 classes are based on UK Broad Habitats; some BHs are subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland).
- Appendix 2 maps relationships between BH, BHSub, and LCM2007 class numbers.
- Appendix 3 provides standard LCM2007 color mapping for visualization.
- Change mapping across LCM1990/2000/2007 is not straightforward due to differing class schemes and spatial structures; not well suited for direct change detection.

## Validation and Quality
- Ground reference validation against 9127 polygons yields an average accuracy of 83%.
- The 83% figure is an average across the dataset; local variances may be higher or lower.
- Users should perform their own validation, especially when using Broad Habitat sub-classes (BHSub) or sub-class level information, which QA does not fully certify.

## Use and Limitations for Monitoring
- Suitable for environmental health monitoring, policy scrutiny, and informing future actions, with robust metadata and data provenance.
- Limitations to consider:
  - Change detection is complex due to mismatches in classes and spatial structure across LCM versions.
  - Some classes (e.g., certain grassland subclasses) can be misclassified without additional validation.
  - Data governance considerations apply when sharing underlying polygons or field-level codes.

## Access, Formats, and Licensing
- Access:
  - 1 km raster products available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request; licence fees may apply.
  - Contact: spatialdata@ceh.ac.uk; online applications at www.ceh.ac.uk/data.
- File sizes (illustrative):
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
  - Raster 25 m (GB): ~1.36 GB; Raster 25 m (NI): ~46 MB.
  - 1 km products: modest in size (tens of MB to KB range).
- Projections:
  - GB: British National Grid; NI: Irish National Grid (moving toward ITM for NI).
- Data access and licensing may involve fees and licensing terms.

## Appendices and Updates
- Appendix 1: LCM2007 Classes – detailed descriptions of each BH and its subclasses (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grasslands, wetlands, urban classes, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and BH-subclasses (crosswalk and field codes).
- Appendix 3: Color mapping recipe for standard visualization (and ArcGIS .lyr equivalents).
- Appendix 4: Updates to Products (Version 1.2, May 2014) – updates include additional OS Tiles (Fair Isle, Stranraer NW) and introduction of water class in 1 km aggregates.
- Version history highlights:
  - Vector GB updated May 2014 (v1.2) to include Fair Isle; 25 m and 1 km products updated similarly.
  - Water class added to certain 1 km aggregate products.

## Technical References
- Morton et al. (2011): Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
- Jackson (2000): Guidance on interpretation of Biodiversity Broad Habitat Classification (for BH to LCM mappings and interpretations).

## Further Information
- Countryside Survey project collaboration and data stewardship details available at www.countrysidesurvey.org.uk.
- More information and detailed methodology are contained in the Final Report and appendices referenced above.