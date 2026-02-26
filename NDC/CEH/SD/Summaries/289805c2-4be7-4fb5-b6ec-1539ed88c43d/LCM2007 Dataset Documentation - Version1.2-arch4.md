# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Introduction
- Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs; final report (Morton et al., 2011) is recommended for comprehensive context.
- This documentation covers LCM2007 data products (not LCM2000 or LCM1990).

## Background
- LCM2007 is a parcel-based classification of UK land cover using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Created by classifying summer-winter satellite composites (20–30 m pixels); improved spatial framework based on OS MasterMap/large-scale vector data and segmentation.
- Maps land cover (not strictly land use); minimum mappable unit is >0.5 ha (parcels smaller than 0.5 ha or linear features <20 m are dissolved).
- Classes include subdivisions within Broad Habitats (e.g., Built-up Areas into Suburban/Urban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Unique Parcel_ID labels are assigned to each parcel for unambiguous communication; rich metadata and a QA-focused. Knowledge-based enhancements (KBE) applied to polygons; ProbList provides top spectral class probabilities.
- Validation against ground reference data: average accuracy ~83% across 9,127 polygons; local discrepancies may occur.
- Change mapping across LCM1990/2000/2007 is complex due to differing classes/structures; data are not well suited for change detection (typical image error around 20%).

## LCM2007 Product Overview
- Distributed as multiple data formats with varying thematic and spatial resolutions to support diverse applications.
- Available products include 25 m raster, 1 km raster (aggregate and target/dominant classes), and vector data (polygons) for GB and NI separately.
- Raster products include 25 m (23 LCM2007 classes) and 1 km (dominant and percentage cover for both LCM2007 classes and their Aggregate equivalents).

## Vector Data Set
- Provided as polygons with attached attribute lists (area, source images, Broad Habitat, processing history, KBE, etc.).
- GB: ~8.6 million polygons; NI: ~0.9 million polygons.
- 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- BHSub (Broad Habitat sub-class) offers additional descriptive information; not all sub-classes are as accurate as the primary LCM2007 class.
- PARCEL_ID is the key identifier; recommended to retain for communication and future developments.
- KBE records processing history and changes; ProbList lists the top spectral matches for each polygon.
- QA/validation-backed class display uses INTCODE (class number 1–23) as the recommended display class.

## Raster Data Sets
- 25 m raster: derived from vector; GB and NI datasets provided separately with consistent projections; 23 LCM2007 classes encoded.
- 1 km raster: summarises 25 m rasters to produce:
  - Dominant cover at 1 km for LCM2007 classes.
  - Dominant cover at 1 km for Aggregate classes.
  - Percentage cover at 1 km for LCM2007 classes and for Aggregate classes.
- Metadata includes grid dimensions, extents, pixel size, data type, projection, spheroid, and datum for GB and NI.

## Map Projection
- GB vector/raster use British National Grid; NI uses Irish National Grid.
- NI is transitioning to Ireland Transverse Mercator (ITM); GIS tools should reproject as needed.

## File Size
- Vector (GB) ~4.13 TB? (Note: actual text states 4.13 GB for vector in 100 km x 100 km tile; NI ~433 MB).
- 25 m raster: GB ~1.36 GB; NI ~46 MB.
- 1 km products: 21 MB to 49 KB (depending on product).
- Large file sizes particularly for vector data; plan storage accordingly.

## Data Access
- 1 km raster data available via CEH Information Gateway.
- Full vector and 25 m raster products available under licence on request from CEH; licensing fees may apply.

## Further Information
- Final Report for LCM2007 – Morton et al. 2011 (Countryside Survey Technical Report No. 11/07) for comprehensive methodology.
- Detailed description of Broad Habitat classifications: Jackson 2000 (JNCC).

## Appendix 1: LCM2007 Classes
- 23 Broad Habitat classes (e.g., Broadleaved woodland; Coniferous woodland; Arable and Horticulture; Improved Grassland; Semi-natural grassland; Neutral/Calcareous/Acid Grasslands; Fen, Marsh and Swamp; Bog; Montane Habitats; Inland Rock; Saltwater/Freshwater; Supra-littoral/ Littoral; Built-up Areas and Gardens with Urban/Suburban splits; etc.).
- Some classes subdivided or enhanced (e.g., Heather vs. Heather grassland; Saltmarsh; Montane habitats; variations within grasslands).

## Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat sub-classes
- Mappings between Broad Habitat categories and LCM2007 class numbers, including detailed sub-class relationships and FieldCodes.
- Provides guidance on how Broad Habitat sub-classes relate to final LCM2007 class labels and potential caveats when using sub-classes for analysis.

## Appendix 3: LCM2007 Colour Mapping
- Standard color mappings for each LCM2007 class (RGB values) and display guidance.
- Includes an ArcGIS .lyr file for easy visualisation.

## Appendix 4: List of Updates to Products (Version 1.2, May 2014)
- Updates to include OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer) for GB vector and 25 m/1 km products.
- NI updates to include water class in 1 km dominant/aggregate products.
- Indicates updates to reflect new tiles and water class inclusion. 

## Product Version History
- GB: Vector v1.2 (May 2014); 25 m raster v1.2; 1 km aggregates/dominant v1.2; etc.
- NI: Vector v1.2 (May 2014); 25 m raster v1.2; 1 km aggregates/dominant v1.2; etc.

## Acknowledgements
- Acknowledges satellite imagery sources (Landsat-TM5, SPOT-4/5, AWIFS) and cartographic/data partners (Ordnance Survey, Rural Payments Agency, Welsh/Scottish/Northern Ireland agencies), among others.
- Reproduction permissions and licensing notices outlined; publication and data use governed by CEH/NERC copyright.