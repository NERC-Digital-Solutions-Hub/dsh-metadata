# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover classification (LCM2007) is parcel-based with 23 classes, aligned to UK Biodiversity Action Plan Broad Habitats.
- Uses summer-winter satellite composites at 20–30 m pixel resolution.
- Updates and upgrades LCM2000; outputs are designed to be compatible with GIS datasets (polygon-based objects).

## Data Products and Structure
- Vector Data Set
  - ~8.6 million polygons (GB) and ~0.9 million polygons (NI).
  - 10 attributes per polygon including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code 1–23), KBE, ProbList, CorePixels, Construct, TotPixels.
  - Polygons carry a unique Parcel_ID for traceability; recommended to retain this field.
  - Includes Broad Habitat sub-classes (BHSub) and a probability list (ProbList) of spectral matches; these sub-classes are not QA-validated at the same level as LCM2007 classes.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; derived from vector data.
  - 1 km raster: aggregates 23 classes into dominant and percentage cover (both for GB and NI aggregation).
  - GB and NI data are provided separately with appropriate projections.
- Data Formats and Metadata
  - Rich metadata per polygon detailing processing history and KBEs (knowledge-based enhancements).
  - Includes probability of spectral variants and original spectral classifications.

## Classification and Validation
- 23 classes based on Broad Habitats; some Broad Habitats are split into sub-classes (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
- Ground reference validation using 9,127 polygons yielded an average accuracy of ~83%.
- Local discrepancies may occur; Broad Habitat sub-classes (BHSub) are provided but may require user validation for analysis at that level.

## Change Mapping and Temporal Considerations
- Change mapping across LCM1990/2000/2007 is complex due to differing class definitions and spatial structures.
- Classified images have typical errors around 20%, while real ecosystem changes (BH change) are often smaller; LCM2007 is not optimized for robust change detection.

## Spatial Coverage, Resolution, and Projections
- GB and NI datasets differ in projection:
  - GB: British National Grid (TM) for vector and raster.
  - NI: Irish National Grid; NI is transitioning to Ireland Transverse Mercator (ITM) in progress.
- Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha or lines <20 m dissolved into surrounding landscape.

## Data Access and Licensing
- 1 km raster 1km target/dominant class products available via CEH Information Gateway.
- Full vector product and 25 m raster available on request under licence from CEH; fees may apply.
- Access details: contact spatialdata@ceh.ac.uk or apply via CEH data portal.

## File Size and Storage Considerations
- Vector (GB) ~4.13 GB; Vector (NI) ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- 1 km raster products: smaller in size (21 MB to 49 KB, depending on product type).

## Appendices and Technical Details
- Appendix 1: LCM2007 23 class definitions (Broad Habitats) and notes on classification nuances (e.g., grassland distinctions, bogs, montane habitats, and inland rock).
- Appendix 2: Mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping recipe for LCM2007 classes (as used in the Final Report).
- Appendix 4: Version updates (e.g., May 2014 updates including Fair Isle and Stranraer tiles; addition of water class in 1 km products).

## Updates and Version History
- Version 1.2 (May 2014): 
  - Vector/25 m/1 km products updated to include new OS tiles (Fair Isle, Stranraer NW).
  - Water class added to 1 km dominant/aggregate products.
  - Minor dataset updates across GB and NI products.
- Version history notes reference the original 2011 publication and 2012 updates.

## Data Quality, Use Recommendations, and Acknowledgements
- Users should consult the Final Report for comprehensive methodology and limitations (Morton et al., 2011).
- The dataset is best used for thematic analysis at the 23-class level; sub-class use warrants independent validation.
- Acknowledges multiple satellite sources (Landsat, SPOT, AWIFS) and cartographic data from Ordnance Survey and partner agencies.