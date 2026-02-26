# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview and purpose
- UK land cover map (LCM2007) is a parcel-based classification of land cover using 23 classes aligned to UK Biodiversity Action Plan Broad Habitats.
- Maps land cover (not land use); derived from summer-winter satellite composites at 20–30 m resolution.
- Improves on LCM2000 by using a spatial framework based on OS MasterMap/large-scale vector layers and image segmentation.
- Minimum mapping unit is >0.5 ha; parcels smaller than this are dissolved into surrounding landscape.

## Data products and structure
- Vector data set: polygons with 10 attributes per polygon; includes Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (display class), KBE (processing history), ProbList (top 5 spectral matches), CorePixels, TotPixels, and Construct (data source and segmentation history).
- 23 LCM2007 classes are grouped into Aggregate classes for 1 km raster products.
- Vector product contains ~8.6 million polygons in Great Britain and ~0.9 million in Northern Ireland; Parcel_ID helps maintain unambiguous communication between users.
- Raster data sets: 25 m and 1 km products derived from the vector data.
  - 25 m raster: 23 LCM2007 classes (full thematic resolution).
  - 1 km raster: Aggregate classes; provides dominant cover and percentage cover for both LCM2007 classes and Aggregate classes.

## Class structure and mappings
- 23 LCM2007 classes based on Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Appendix 1 details each class; Appendix 2 provides relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mappings for display.

## Data quality and validation
- Ground reference validation used 9,127 polygons; average accuracy ~83% (with local variation expected).
- LCM2007 validation focuses on thematic resolution; Broad Habitat sub-classes carry additional information but are not covered by QA with the same certainty as the main LCM2007 classes.
- Knowledge-Based Enhancements (KBE) applied during classification; ProbList indicates the top spectral matches for each polygon.

## Metadata and provenance
- Rich metadata at the polygon level, including processing history, KBE history, and spectral classification results.
- Parcel_ID preserves traceability to the source imagery and segmentation steps.

## Data access and licensing
- 1 km raster data sets available via the CEH Information Gateway.
- Full vector product and 25 m raster product available under license on request from CEH; fees may apply.
- NI and GB datasets have separate projections (GB National Grid vs Irish National Grid) with future plans for Ireland Transverse Mercator.
- Data sizes are large (vector ~10 million polygons; 25 m raster and vector are sizeable).

## Projections, resolution, and file characteristics
- Vector and 25 m raster data for Great Britain and Northern Ireland provided in respective national grids.
- GB: British National Grid; NI: Irish National Grid (with potential ITM transition).
- 25 m raster data: pixel size 25 m; 1 km raster data: pixel size 1,000 m; GB vs NI extents detailed in metadata tables.
- File sizes reported as guidance; vector files are large due to 10 attributes per polygon.

## Practical use for monitoring frameworks
- Provides a standardized, GIS-compatible set of land cover measures suitable for environmental monitoring and policy evaluation.
- Useful for:
  - Baseline and trend analyses of Broad Habitat distributions and land cover changes.
  - Multi-resolution monitoring: use 1 km rasters for broad UK-wide assessments; use 25 m vector or 25 m rasters for detailed, site-specific analyses.
  - Data integration with other datasets (e.g., meteorological, species distribution) due to explicit object-based parcel labeling and rich metadata.
- Limitations and cautions:
  - 23-class thematic resolution is validated, while some Broad Habitat sub-classes and FieldCode-level details require user validation.
  - Sub-class information (BHSub) is informative but not QA-validated to the same standard as the main LCM2007 classes; users should perform their own validation for sub-class analyses.
  - The product maps land cover, not land use; interpretation should consider that spectral similarity can blur distinctions between certain land-use types.
  - Large data volumes and licensing requirements may constrain access and processing workflows.

## Usage recommendations
- For policy evaluation, align LCM2007 class outputs with monitoring indicators defined in the framework; prefer the main 23-class LCM2007 mapping for comparability and QA-validated results.
- When detailed local analysis is needed, leverage the vector data with Parcel_ID and rich metadata, ensuring appropriate validation for sub-classes.
- Use 1 km rasters for UK-wide assessments and 25 m data (vector or 25 m raster) for finer-scale analyses where metadata and polygon-level context are valuable.

## Additional information and references
- Main documentation: Morton et al., Final Report for LCM2007 (2011).
- Broad Habitat classification reference: Jackson, 2000.
- Detailed appendices: Appendix 1 (LCM2007 classes), Appendix 2 (class/sub-class mappings), Appendix 3 (color mapping).
- Acknowledgements cover data sources (Landsat, SPOT, AWIFS) and data providers (Ordnance Survey, LPS, etc.).

## Summary of key points for monitoring framework authors
- LCM2007 provides a comprehensive, QA-backed land cover dataset across the UK with 23 main classes mapped at ~20–30 m resolution, plus aggregated 1 km raster products and a rich vector attribute set.
- The dataset’s structure (Parcel_ID, BH, BHSub, KBE, ProbList) supports traceability, data governance, and reproducible analyses, but sub-class accuracy requires user validation.
- Data access is available via CEH with licensing options; data volumes are large, and there are cross-border projection considerations (GB vs NI).
- The product offers flexible monitoring applications: detailed site-level analyses (vector/25 m) and broad policy-scale assessments (1 km rasters), with clear caveats about interpretation of land cover vs. land use.
- For robust monitoring, reference the Final Report (Morton et al., 2011) and related methodological documents, and plan for data governance and metadata practices when integrating into monitoring frameworks.