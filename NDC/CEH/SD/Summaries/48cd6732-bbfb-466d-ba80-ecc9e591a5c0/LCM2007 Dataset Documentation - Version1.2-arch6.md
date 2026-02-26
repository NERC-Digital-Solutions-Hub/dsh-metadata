# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A parcel-based UK land cover classification (LCM2007) using 23 Broad Habitat-based classes, derived from summer-winter satellite imagery at 20–30 m pixel size.
- Provides a range of data products to support diverse GIS and analysis needs (vector, 25 m raster, and 1 km raster formats) and to enable various end-use applications, including policy support and public data exploration.
- Not a land use map; a given class denotes spectral-dominant land cover, with site-specific interpretation needed to infer land use.

## What LCM2007 Is and How It Is Built

- Built on high-resolution polygons representing real-world objects (fields, woodland blocks) using OS Master Map and related segmentation; improves compatibility with other GIS datasets.
- Uses 23 classes tied to UK Biodiversity Action Plan Broad Habitats; some classes are subdivided (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediment).
- Minimum mappable unit is >0.5 ha; parcels smaller than 0.5 ha or very short linear features are dissolved into the surrounding landscape.
- Each parcel gets a unique Parcel_ID; Broad Habitat (BH), Broad Habitat subclass (BHSub), FieldCode, and an IntCode (1–23) for display and QA.
- Rich metadata per polygon, including processing lineage (KBE history), probability list for spectral variants (ProbList), and core pixels used for classification (CorePixels).

## Data Products and Formats

- Vector Data Set (GB and NI)
  - GB: ~8.6 million polygons; NI: ~0.9 million polygons; 10 attributes per polygon.
  - Key attributes: Parcel_ID, BH, BHSub, FieldCode, INTCODE (class number for display), KBE, ProbList, CorePixels, Construct, TotPixels.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI separate projections; pixel values correspond to LCM2007 classes (Table 2 crosswalk).
  - 1 km raster: aggregations from the 25 m raster (dominant class, and percentage cover) using Aggregate classes (1 km products include dominant and percentage for both LCM2007 classes and Aggregate classes).
- Summary visuals
  - Vector vs. 25 m raster provide similar detail; vector includes rich metadata; 25 m raster omits polygon boundaries and extensive metadata for some applications.
  - 1 km products are suitable for national-scale modeling and integration with other large-scale datasets (e.g., meteorology, species distributions).

## Spatial Coverage and Projections

- Great Britain (GB) and Northern Ireland (NI) datasets provided separately.
- Projections: GB uses British National Grid; NI uses Irish National Grid (with some NI data transitioning toward Ireland Transverse Mercator in future GIS workflows).
- File characteristics:
  - Vector: large files (GB ~4.13 GB; NI ~433 MB in 100 km x 100 km shapefile example).
  - Raster: GB 25 m (~1.36 GB) and NI 25 m (~46 MB); 1 km products smaller (tens of MBs).

## Data Access and Licensing

- 1 km raster data accessed via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; online application or direct contact provided.
- Licences may incur fees for some users/applications.

## Data Quality, Validation, and Limitations

- Ground reference validation: average thematic accuracy around 83% (based on 9,127 ground reference polygons); local discrepancies may occur.
- QA applies to the 23 LCM2007 classes; Broad Habitat subclasses are provided but may require independent validation for sub-classes due to varying accuracy.
- Change mapping is not well suited for LCM change detection due to class and spatial-structure differences across LCM1990/2000/2007 and typical spectral change errors (~20%).
- Outputs should be used with awareness of:
  - LCM2007 maps land cover (not necessarily land use) and may not distinguish certain land-use nuances (e.g., recreation grass vs. grazed grass).
  - Sub-class accuracy may be lower than primary LCM2007 classes; validate sub-classes if used for fine-grained analyses.

## Classification System and Metadata Details

- 23 LCM2007 classes mapped to Broad Habitats; some BH are subdivided (e.g., Urban/Suburban, Heather vs. Heather grassland).
- Appendix 1 outlines each Broad Habitat with brief interpretation notes; Appendix 2 maps relationships between Broad Habitats, LCM2007 classes, and BH-subclasses; Appendix 3 provides standard colour mapping for display; Appendix 4 documents product updates.
- Broad Habitat Sub-classes (BHSub) are included for additional information (not always covered by QA); ProbList provides top 5 spectral matches with probabilities.
- Important for data users: retain Parcel_ID for unambiguous communication and cross-dataset linking.

## Updates and Version History

- Version 1.2 (May 2014) updates GB NI OS Tile coverage (Fair Isle, Stranraer), includes water class in 1 km aggregates, and reflects other minor dataset updates.
- Ongoing references: Final Report for LCM2007 (Morton et al., 2011) and related guidance on Broad Habitat interpretations (Jackson, 2000).

## Practical Considerations for Data Support

- Data integration:
  - Use Parcel_ID to join with other attribute datasets or GIS layers for richer analysis.
  - Combine 25 m and 1 km rasters with vector attributes to support multi-scale analyses; leverage ProbList for uncertainty-aware modeling.
- Data quality management:
  - Validate Broad Habitat sub-classes if used for fine-scale decisions; rely primarily on the 23 LCM2007 classes for QA-underpinned analyses.
- Use cases:
  - Baseline land cover mapping for planning, environmental assessments, and public-facing data products.
  - Support for policy work and spatial planning with a consistent UK-wide land cover framework.
- Access considerations:
  - 1 km rasters readily accessible via CEH gateway; full vector and 25 m raster require licensing and direct request.