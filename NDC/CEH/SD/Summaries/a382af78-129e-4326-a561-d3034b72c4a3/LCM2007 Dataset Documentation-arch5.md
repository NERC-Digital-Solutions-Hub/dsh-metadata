# Land Cover Map 2007 Dataset Documentation

## Overview
- UK parcel-based land cover classification using 23 classes based on Broad Habitats; updated from LCM2000 with a framework based on Ordnance Survey data.
- Data products support diverse user needs; maps land cover (not land use); minimum mappable unit >0.5 ha; small parcels (<0.5 ha) dissolved.
- Validation shows average accuracy around 83% against ground reference polygons; some local discrepancies may occur.
- Documentation covers LCM2007 products; refers to detailed Final Report for comprehensive methodology and limitations; note separate documents exist for earlier LCM2000/1990 datasets.

## Data products and structure
- Vector Data Set
  - 8.6 million polygons (GB) and 0.9 million (NI); each polygon includes 10 attributes.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class code for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID aids unambiguous communication; BHSub provides additional subclass information; ProbList used with caveats (not QA’d at subclass level).
- Raster Data Sets
  - 25m and 1km resolutions; GB and NI provided separately due to different projections.
  - 23 LCM2007 classes in 25m raster; 1km rasters provide dominant class, and percentage cover for both LCM2007 classes and Aggregate classes.
  - 1km products include: Dominant cover (classes and aggregates) and Percentage cover (classes and aggregates).
- Metadata and provenance
  - Rich metadata at polygon level, including processing history and knowledge-based enhancements (KBE).
  - Ground reference validation data documented; image sources and processing steps described.
- Appendices
  - Appendix 1: LCM2007 classes (class definitions and notes).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.
  - Appendix 3: Color mapping for LCM2007 classes.
- Final guidance emphasizes consulting Morton et al. (2011) Final Report for comprehensive methodology and limitations.

## Quality, validation, and limitations
- QA/validation: average accuracy ~83% against 9127 ground reference polygons; field-level variability expected.
- Sub-class level: Broad Habitat subclasses (BHSub) may not meet the same QA standards as primary LCM2007 classes; user validation recommended if subclass-level usage is required.
- MMU and spectral interpretation: MMU excludes parcels <0.5 ha and linear features <20 m; some land cover types (e.g., water, moss, peat) may be challenging to classify consistently.
- Spatial resolution considerations: 25m and 1km rasters provide varying detail; vector offers rich metadata but larger file sizes.

## Data governance, provenance, and metadata
- Production relies on satellite imagery (20–30 m) and OS cartographic data (OSMM) with segmentation producing real-world polygon boundaries.
- Classification records include knowledge-based enhancements and a ProbList of top spectral matches; FieldCode is provided but not QA’d at that level.
- Parcel_ID and polygon-level metadata enable traceability from source imagery to final polygon.
- Documentation warns that Broad Habitat subclasses reflect spectral classification and are not guaranteed at the same accuracy as core LCM2007 classes; users should validate prior to high-stakes use.

## Access, licensing, and reuse
- 1km raster data accessible via CEH Information Gateway.
- Full vector product and 25m raster product available under licence on request from CEH; online application process; licence fees may apply for some users/applications.
- Data use subject to copyright and consortium acknowledgments; detailed licensing terms provided by CEH.

## Spatial reference and data formats
- Vector: polygon-based dataset (millions of features) with 10 attributes per polygon; formats typically align with shapefile/geodatabase conventions; large file sizes.
- Raster: 25m and 1km products; GB in British National Grid; NI in Irish National Grid; some NI data migrating to ITM projection; geotiff format used for raster files.
- Coordinate extents and pixel sizing documented; Table of metadata provides specifics on extents, pixel size, and projections.

## File sizes and data footprint
- Vector (GB): approximately 4.13 GB; Vector (NI): ~433 MB.
- Raster 25m: GB ~1.36 GB; NI ~46 MB.
- Raster 1km: ranges from ~21 MB (percentage cover for all classes) to ~49 KB (dominant cover).
- Large file sizes should be planned for in storage and data transfer.

## Usage notes and cautions
- LCM2007 measures land cover, not land use; be cautious when inferring land management or usage from cover classes.
- Some classes (e.g., Neutral/Calcareous Grassland) may be misclassified relative to ground truth datasets; consider aggregating grassland classes if needed.
- Broad Habitat subclasses can provide additional context but may require separate validation for high-precision requirements.
- Users should consult the Final Report (Morton et al., 2011) for detailed methodological notes and limitations.

## Governance considerations for Data Stewards
- Ensure robust metadata standards are maintained, including processing history, KBE lineage, and ProbList documentation.
- Establish clear licensing terms and access pathways, including license fees where applicable and user eligibility.
- Manage data quality expectations by communicating QA outcomes, accuracy ranges, and recommended validation for subclass usage.
- Maintain traceability through Parcel_ID and source imagery documentation to support data provenance.
- Plan for data updates and versioning, given the data’s multi-product structure (vector, 25m raster, 1km raster) and potential regional projection differences.
- Provide guidance on appropriate data products for different applications (e.g., high-detail vector vs. compact 1km raster for nationwide modelling).
- Recognize interoperability considerations when integrating LCM2007 with other datasets (e.g., OSMM, ground-truth maps) and advise on appropriate reprojection practices.