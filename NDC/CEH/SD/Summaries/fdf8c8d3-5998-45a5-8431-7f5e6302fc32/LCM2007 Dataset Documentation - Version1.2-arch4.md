# Land Cover Map 2007 Dataset Documentation

## Overview
- UK land cover classification product (LCM2007), 2007 edition, developed to support diverse user needs.
- Maps land cover (not land use) using 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Parcel-based classification derived from 20–30 m satellite imagery; upgrades LCM2000 with GIS-friendly, object-based parcels.
- Provides a range of data products to suit different applications and scales.

## Data Products and Structure
- Vector data set: ~8.6 million polygons (Great Britain) and ~0.9 million (Northern Ireland) with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Raster data sets:
  - 25 m raster (GB and NI separated by projection); 23 LCM2007 classes; includes 1:1 mapping to vector classes.
  - 1 km raster: derived from 25 m data; provides dominant class and percentage cover for both LCM2007 classes and Aggregate classes (for generalized analyses).
- Minimum mapping unit (MMU): >0.5 ha; parcels <0.5 ha and linear features <20 m dissolved into surrounding landscape.
- Product variety supports different use cases (detailed vector with metadata vs. generalized rasters).

## 23 LCM2007 Classes and Sub-Classes
- Classes are based on Broad Habitats; several Broad Habitat sub-classes (BHSub) add detail (e.g., Built-up Areas subdivided into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Vector attributes include: Parcel_ID, BH (dominant class), BHSub (sub-class), FieldCode (classification code), INTCODE (display class), KBE (processing history), ProbList (top spectral class probabilities), CorePixels, Construct, TotPixels.
- Sub-classes provide additional information but are not validated to the same standard as the main LCM2007 classes; users should validate if using at sub-class level.

## Data Access and Licensing
- 1 km raster data available via the CEH Information Gateway.
- Full vector and 25 m raster products available on request under license from CEH (fees may apply).
- Access details and contact: CEH data portal and spatialdata@ceh.ac.uk.

## Data Quality and Validation
- Ground reference validation: ~9,127 polygons assessed; average accuracy around 83% (context-dependent; local variations possible).
- QA is robust at the 23-class level; Broad Habitat sub-classes are not guaranteed to meet the same QA standards; users should perform their own validation for BHSub.

## Projections and Spatial Coverage
- Great Britain: British National Grid (OSGB 1936/Transverse Mercator).
- Northern Ireland: Irish National Grid (Ireland 1965); NI data transitioning toward Ireland Transverse Mercator (ITM).
- Raster and vector products are provided separately for GB and NI to reflect projection differences.

## Change Mapping and Limitations
- Change detection between LCM1990/2000/2007 is challenging due to differing class definitions, spatial structures, and typical classification errors (~20%).
- LCM2007 products are not well suited for straightforward change detection; caution advised when interpreting temporal changes.

## Data Management and Metadata
- Rich metadata for each polygon, including data sources, processing history (KBE), and probability details (ProbList).
- Parcel_ID retained to preserve traceability and communication across users.

## File Sizes and Formats (Overview)
- Vector (Shapefile, 100 km x 100 km blocks): GB ~4.13 GB; NI ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: GB products up to ~49 MB; various targets (dominant and percentage, 23 and Aggregate classes).
- Formats chosen to balance detail (vector with metadata) and efficiency (raster for broad-scale analyses).

## Data Management, Documentation, and Updates
- Version: 1.2 (May 2014) updates include OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer) additions; water class added to some 1 km products.
- Appendix materials provide detailed class mappings, color schemes, and update logs.

## Appendices (highlights)
- Appendix 1: LCM2007 Class descriptions (Broad Habitat-level explanations and nuances).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and BH-subclasses.
- Appendix 3: Standard color mapping for LCM2007 classes.
- Appendix 4: List of product updates (Version 1.2).

## Acknowledgements
- Data sources from multiple satellite imagery programs and Ordnance Survey data; CEH-led with Countryside Survey Partnership support; copyright and licensing notes included.