# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Land Cover Map 2007 (LCM2007) is a parcel-based classification of the UK land cover using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Based on summer–winter satellite imagery with 20–30 m pixels; updates LCM2000 with a framework using OSMM-derived boundaries and image segments.
- Maps land cover (not strictly land use) and uses a minimum mappable unit of >0.5 ha; parcels smaller than 0.5 ha or lines <20 m are dissolved.

## Data Content and Structure

### Vector Data Set
- 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
- 10 attributes per polygon (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class code for display), KBE (processing history), ProbList (top spectral class probabilities), CorePixels, Construct, TotPixels.
- Parcel_ID provides a unique label for each parcel; recommended to retain for unambiguous communication.
- Sub-classes (BHSub) provide additional information but are not as rigorously QA’d as the 23 LCM2007 classes.
- Rich polygon metadata capturing processing steps, original spectral classification, and knowledge-based enhancements (KBE).

### Raster Data Sets
- 25 m raster and 1 km raster products derived from the vector data.
- Separate data sets for Great Britain and Northern Ireland due to different projections.
- 1 km rasters include:
  - Dominant cover for 1 km pixels (23-class and Aggregate-class variants).
  - Percentage cover at 1 km for both 23-class and Aggregate classes.
- 25 m rasters map the 23 LCM2007 classes; 1 km rasters summarize 25 m data.

## Data Quality and Validation
- Ground reference validation used 9,127 polygons; average accuracy about 83%.
- Local discrepancies may appear; accuracy is an average across polygons.
- Change mapping across LCMs (1990, 2000, 2007) is complex due to differing classes and spatial structure; LCM products are not well suited for automated change detection.

## Classification and Classes
- 23 LCM2007 classes defined from Broad Habitats (Appendix 1).
- Some Broad Habitats split into sub-classes (e.g., Built-up Areas split into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Appendix 2 maps relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mapping.
- 1 km rasters utilize Aggregate classes for broader-scale applications; 23-class resolution retained in 25 m rasters and vector data.

## Spatial Details and Projections
- Vector and 25 m rasters for Great Britain use British National Grid; Northern Ireland uses Irish National Grid.
- Northern Ireland is transitioning to Ireland Transverse Mercator (ITM); bring-your GIS tools should reproject NI data as needed.
- Pixel geometry notes: values in Tables refer to the south-west corner of the lower-left pixel.

## Data Access and Licensing
- 1 km raster data sets available via the CEH Information Gateway.
- Full vector product and 25 m raster product are available on request under licence from CEH; fees may apply.
- Contact CEH Spatial Data or apply via the CEH data site for access.

## File Sizes and Formats
- Vector (GB): ~4.13 GB; Vector (NI): ~433 MB (Shapefile bundle).
- Raster 25 m: GB ~1.36 GB; NI ~46 MB (GeoTIFFs).
- 1 km raster products: 21 MB to 49 KB depending on product type.
- Data are large; consider storage and processing implications for GIS workflows.

## Usage Guidance and Limitations
- Use 23-class LCM2007 for detailed thematic mapping; aggregate classes suitable for 1 km-scale analyses.
- Retain Parcel_ID for clear communication and reproducibility.
- Use ProbList and KBE histories with caution; Broad Habitat sub-classes may require independent validation due to QA limitations.
- Change detection between LCM2007 and earlier/later products is not straightforward due to class/spatial structure differences.

## Colour Mapping and Appendices
- Appendix 3 provides standardized colour mappings for the 23 classes (also available as an ArcGIS .lyr file for quick styling).
- Appendix 2 details the relationship between Broad Habitats, LCM2007 classes, and sub-classes.
- Appendix 4 lists product updates (e.g., v1.2 in May 2014 with new tiles and water class inclusion).

## Version History and Updates
- Version 1.0: Original (July 2011).
- Version 1.2: Updated May 2012; includes dataset updates, change detection discussion; later reflected in 2014 updates.
- Version 1.2 (May 2014): GB vector and 25 m raster updated for OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer); 1 km products updated; water class added for some GB 1 km products; NI updates included for water class.

## Acknowledgements
- Data derived from multiple satellite sources (Landsat-TM5, SPOT-4/5, AWIFS, etc.) and Ordnance Survey cartographic data.
- Developed by CEH with contributions from Countryside Survey partners; funded and documented in CEH technical reports.