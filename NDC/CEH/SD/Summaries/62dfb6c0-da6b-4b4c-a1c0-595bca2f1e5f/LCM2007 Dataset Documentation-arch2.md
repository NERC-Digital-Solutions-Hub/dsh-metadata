# Land Cover Map 2007 Dataset Documentation

## Overview
- UK-wide parcel-based land cover classification (LCM2007) built from summer-winter composite satellite imagery at 20–30 m pixels.
- Provides 23 classes based on UK Biodiversity Action Plan Broad Habitats to support environmental monitoring and policy evaluation.
- Differentiates land cover from land use; focuses on cover as observed in spectral data.
- Data available in vector (polygons) and raster formats (25 m and 1 km), with separate GB and NI products and projections.

## Data Production, Scope, and Limitations
- Improvements over LCM2000 include a spatial framework using OSMM for GB and L&S Large-scale Vector for NI, segmented into polygons representing real-world objects.
- Minimum mappable unit: >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.
- 23 LCM2007 classes derived from Broad Habitats; some Broad Habitats subdivided into sub-classes (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh in some cases).
- Unique Parcel_ID attribute retained for communication and traceability; rich per-polygon metadata captured.
- Validation against ground reference data: average accuracy around 83% across 9,127 polygons; local deviations may occur.

## Data Products and Structure

### Vector Data Set
- ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
- 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- BHSub provides a text description of Broad Habitat sub-class; ProbList lists top spectral class probabilities; KBE records processing history and changes.
- Includes Broad Habitat sub-classes for enhanced classification, though not all are QA-validated at the sub-class level; users should validate if using sub-class level.
- Useful for detailed mapping, analytics, and integration with other GIS datasets, albeit with larger file sizes.

### Raster Data Sets
- 25 m raster (23 LCM2007 classes) and 1 km raster products derived from the vector data.
- Separate datasets for Great Britain and Northern Ireland; 1 km rasters provide dominant class, aggregate class, and percentage cover at 1 km resolution.
- Metadata specifics (extent, pixel counts, coordinates, projections) detailed in the product documentation.

### Relationships and Aggregates
- Table 2 and Appendix 2 describe the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- 1 km rasters use Aggregate class mappings to enable broader-scale analyses; 25 m rasters retain the full 23-class thematic resolution.

## Map Projections and File Sizes
- Vector and raster data for GB use British National Grid; NI uses Irish National Grid.
- NI is transitioning toward the Ireland Transverse Mercator (ITM) projection.
- File sizes (indicative):
  - GB vector (100 km x 100 km shapefile): ~4.13 GB
  - NI vector: ~433 MB
  - GB 25 m raster: ~1.36 GB
  - NI 25 m raster: ~46 MB
  - 1 km rasters: 21 MB to 49 KB depending on product
- Large data volumes imply careful planning for storage and processing.

## Data Access and Usage
- 1 km raster data accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under license from CEH; fees may apply.
- Instructions and contact for data access provided in the documentation.

## Production Methodology and Documentation References
- Final report Morton et al., 2011 provides comprehensive methodology, validation details, and limitations; recommended for users requiring in-depth understanding of QA and processing steps.
- Appendix 1–3 provide detailed class definitions, the relationship to Broad Habitats, and the standard color mappings used in outputs.

## Practical Use for Environmental Monitoring
- Standardized 23-class land cover framework aligned with UK Broad Habitats enables consistent monitoring of environmental health and policy performance over time.
- Rich vector metadata (including KBE history and ProbList) supports reproducibility and traceability in monitoring workflows.
- Ability to aggregate to 1 km or work with full 25 m/23-class resolution supports both national-scale modelling and local area assessments.
- Data quality note: apply local validation when using Broad Habitat sub-classes due to variable QA coverage at that level.

## Appendices at a Glance
- Appendix 1: LCM2007 classes with qualitative descriptions and habitat context.
- Appendix 2: Mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCodes).
- Appendix 3: Color mapping recipe for LCM2007 classes (RGB values per class).