LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover classification (LCM2007) providing parcel-based maps across Great Britain and Northern Ireland.
- 23 classes based on UK Broad Habitats; derived from summer-winter satellite imagery (20–30 m pixels).
- Maps land cover (not directly land use) with a minimum mapping unit of >0.5 ha; small parcels dissolved into surrounding areas.
- Supersedes LCM2000; uses OS MasterMap/large-scale vector frameworks and image segmentation to align with real-world objects.
- Data products are offered in vector and raster formats to support a range of applications; detailed methodological context is in Morton et al. 2011 Final Report.

## Data Products and Coverage
- Vector data set: polygons with 10 attributes per polygon; about 8.6 million polygons (GB) and 0.9 million (NI).
- Raster data sets: 25 m and 1 km products; GB and NI provided separately due to projections.
- 1 km rasters include:
  - Dominant class per 1 km cell
  - Percentage cover per class
  - Aggregated (1 km) classes for simplified analyses
- 25 m rasters and vector data include 23 LCM2007 classes, with 1 km rasters supporting broader-scale analyses.
- Examples illustrate that vector data carry rich metadata per polygon, while 25 m rasters provide the same thematic detail without polygon boundaries.

## Data Model and Key Attributes
- Vector data attributes (example):
  - Parcel_ID: unique identifier for each parcel
  - BH: Broad Habitat (dominant level)
  - BHSub: Broad Habitat sub-class description
  - FieldCode: short text field codes
  - INTCODE: recommended display/class code (1–23)
  - KBE: Knowledge-Based Enhancements history
  - ProbList: top 5 spectral class probabilities
  - CorePixels/TotPixels: pixel counts used in classification
  - Construct: polygon construction history (OSMM-derived or segmented)
- Sub-classes (BHSub) provide additional, but not QA-validated, detail; ProbList aids user validation.
- Tables link LCM2007 classes to Broad Habitats (Appendix 2) and provide standard colour mappings (Appendix 3).
- Data design emphasizes retaining Parcel_ID for unambiguous communication.

## Quality, Validation, and Limitations
- Ground-reference validation: average accuracy around 83% across 9,127 polygons; local discrepancies may occur.
- Change detection: not well suited due to differences in classes, spatial structure, and typical error rates (~20% for imagery vs BH change).
- Grassland and coastal/subclass areas present notable classification challenges; BHSub and certain grassland classes require user validation and possible aggregation for reliable use.
- Metadata-rich QA records accompany polygons; users advised to perform their own validation on Broad Habitat sub-classes if used beyond the primary LCM2007 classes.

## Data Access, Licensing, and Use
- Data access:
  - 1 km raster products available via CEH Information Gateway.
  - Full vector product and 25 m raster product available under licence on request from CEH; fees may apply.
- Licensing considerations: use often requires licensing through CEH; ensure compliance with OS/Ordnance Survey data licenses incorporated in the dataset.
- Users should reference Morton et al. (2011) Final Report for comprehensive methodology and applications.

## Technical Details and Projections
- Projections:
  - Great Britain: British National Grid (OSGB 1936)
  - Northern Ireland: Irish National Grid (Ireland 1965); NI moving toward Ireland Transverse Mercator (ITM)
- Data structure and file sizes:
  - Vector: large files (GB shapefile ~4.13 GB; NI ~433 MB)
  - 25 m raster: GB ~1.36 GB; NI ~46 MB
  - 1 km rasters: relatively small (GB 21–49 KB range for different products)
- Data construction:
  - 23 LCM2007 classes derived from segmentation of OSMM-based generalised polygons and spectral classifications
  - 1 km rasters summarize 25 m data per cell to identify dominant and percentage cover per class or aggregate class

## Updates, Versioning, and Provenance
- Version history:
  - Version 1.0 (July 2011)
  - Version 1.2 (May 2012; updated for dataset updates and change detection)
  - Version 1.2 (May 2014; GB/NI tiles, water class addition, Fair Isle/Stranraer updates)
- Appendix 4 details product updates (notable additions include water class, newly added OS tiles, and updated tile references).
- Acknowledgements cover multiple satellite sources, OS data, and other datasets underpinning LCM2007 production.

## Governance and Stewardship Considerations for Data Stewards
- Metadata completeness and accessibility: ensure rich per-polygon metadata is preserved, including Parcel_ID and KBE history, for traceability.
- Data quality management: maintain awareness of classification uncertainties, particularly for Broad Habitat sub-classes; document validation steps when integrating BHSub data.
- Data interoperability: use documented class mappings (Appendix 2) and colour mappings (Appendix 3) to support consistent visualization and cross-dataset comparisons.
- Licensing and data sharing: manage licensing with CEH for vector/25 m products and ensure compliant distribution and reuse, including OS-origin data.
- Change management: given limited suitability for change detection, plan complementary methods if long-term change analysis is required.
- Long-term preservation: be mindful of projection changes (NI ITM transition) and ensure reprojection capabilities are in place; retain historical versions and update trails (Version History).
- Publication and discovery: leverage the 1 km raster products for broad-scale discovery and the vector/25 m products for detailed analyses, while clearly communicating the distinctions between land cover (not land use) and potential metadata caveats.