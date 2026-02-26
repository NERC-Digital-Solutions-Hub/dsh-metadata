# LAND COVER MAP 2007 DATASET DOCUMENTATION

- LCM2007 is a parcel-based UK land cover classification using 23 Broad Habitat classes (based on UK BAP) derived from summer-winter satellite imagery with 20–30 m pixels.
- Improves on LCM2000 by using a spatial framework tied to OS mapping for GB and large-scale vector for NI; polygons correspond to real-world objects (fields, woodland blocks) for GIS compatibility.
- Maps land cover (not strictly land use); minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features are dissolved into surrounding landscape.

Overview of data products
- Vector data set:
  - Approximately 10 million polygons (GB) and 0.9 million (NI); each polygon has 10 attributes.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub ( Broad Habitat sub-class), FieldCode, INTCODE (class code 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID retained for unambiguous communication; datasets include sub-classes and FieldCode with caution for independent QA.
- Raster data sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately; also available as 1 km aggregate products.
  - 1 km raster: derived from 25 m to show Dominant cover and Percentage cover for both full classes and aggregates (GB and NI).
- Access and licensing:
  - 1 km rasters available via CEH Information Gateway.
  - Full vector and 25 m raster available on request under licence; fees may apply.
- Documentation and references:
  - Final Report for LCM2007 (Morton et al., 2011) for detailed methodology.
  - Appendix 1–4 describe classes, relationships, color mappings, and version updates.

LCM2007 classes and data structure
- 23 Broad Habitat classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural Grassland, Montane Habitats, Inland Rock, Urban/Suburban, Coastal/Littoral habitats, Freshwater, Saltwater, etc.).
- Some Broad Habitat sub-classes (BHSub) offer finer distinctions (e.g., Heather vs Heather grassland; Suburban, Urban; Littoral Sediment vs Saltmarsh).
- Appendix 2 explains relationships between Broad Habitats, LCM2007 classes, and BH sub-classes; Appendix 3 provides standard colour mapping.
- Validation and QA:
  - Ground reference validation used 9,127 polygons; average accuracy about 83% (with local variations expected).
  - Change mapping across LCM1990/2000/2007 is complex and not well suited for robust change detection due to class differences, spatial structure changes, and typical classification error around 20%.

Technical specifications and data formats
- Vector dataset:
  - 8.6 million polygons (GB) and 0.9 million (NI); 10 attributes per polygon; Parcel_ID is a critical identifier.
  - Construct attribute notes the segmentation basis (OSMM generalised polygons, with segmentation variants).
- Raster datasets:
  - 25 m raster across GB and NI; 1 km raster products summarize 25 m data (dominant class and percent cover).
  - Data details include grid dimensions, extents, pixel sizes, data types (unsigned 8-bit), coordinate systems (GB: OSGB36/British National Grid; NI: Ireland 1965/ITM transition).
- File size guidance (approximate; varies by format):
  - Vector GB: ~4.13 GB; NI: ~433 MB.
  - Raster 25 m GB: ~1.36 GB; NI: ~46 MB.
  - 1 km products: 21 MB to 49 KB (depending on product type).
- Map projections:
  - GB data in British National Grid; NI data in Irish National Grid; NI gradually moving toward ITM.

Data quality, limitations and usage guidance
- MMU and spatial accuracy:
  - Minimum mappable area >0.5 ha; small parcels and many linear features are dissolved.
  - Accuracy validated at thematic resolution (23 classes); some subclasses and FieldCodes are not QA’d to the same standard; users should validate at subclass level if needed.
- Change detection limitations:
  - Between 1990, 2000, and 2007 datasets, class definitions and spatial structure differ; observed spectral classification errors (~20%) can obscure habitat change signals.
- Grassland and peat-related caveats:
  - Some confusion between Neutral/Calcareous/Acid Grasslands and Improved Grassland; Montane, Bog, and Dwarf Shrub Heath distinctions can be nuanced; soil and peat depth data influence some classifications.
- Data fit for purpose:
  - LCM2007 is ideal for landscape-scale land cover mapping and integration with other GIS datasets; not a direct surrogate for land use or dynamic change without careful validation.
- Metadata richness and data governance:
  - Rich polygon-level metadata, including processing history (KBE), probability lists, and construct details; Parcel_ID supports cross-dataset communication and updates.
  - Access requires governance around licensing; version 1.2 (May 2014) includes tile updates (Fair Isle, Stranraer NW) and includes a water class in 1 km products.

Updates, versioning and acknowledgements
- Version 1.2 (May 2014): updates to GB tiles (Fair Isle, Stranraer NW) and NI; water class added to 1 km products; HZ tile updates included.
- Acknowledges data sources from Landsat-TM5, SPOT, AWIFS, OS, and other mapping and soil data producers; produced by CEH and Countryside Survey Partnership.

Implications for Data Leaders
- Ensure comprehensive metadata and provenance are maintained for all LCM2007 products (vector and raster) to support discoverability and governance.
- Leverage the rich attribute set (BH, BHSub, KBE, ProbList) for advanced data governance, lineage tracking, and quality control.
- Plan for licensing and access controls, particularly for regular updates or full vector/25 m datasets.
- Use 1 km rasters for broad-scale analyses and integrative modelling; use 25 m vector/raster for finer-scale, region-specific assessments, with validation when using BHSub or FieldCode.
- Be cautious about change detection and temporal analyses given differences in class definitions and spatial structure across LCM generations.
- Align with community standards and keep aware of ongoing updates (e.g., improvements in tile coverage, water class inclusion) to ensure datasets remain current for policy or planning needs.