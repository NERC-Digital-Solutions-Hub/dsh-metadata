LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover parcel-based classification (LCM2007) mapping 23 Broad Habitat-based classes across Great Britain and Northern Ireland.
- Based on summer-winter satellite composites with 20-30 m pixel size; updates LCM2000 with a framework aligned to OS mapping data and image segments.
- Provides a range of data products (vector, 25 m raster, 1 km raster) to support diverse monitoring and policy evaluation needs.

## What LCM2007 is and how it’s structured
- Maps land cover (not directly land use); a minimum mappable unit of >0.5 ha; parcels smaller than 0.5 ha or lines under 20 m are dissolved into surrounding areas.
- 23 classes derived from UK Broad Habitats; some Broad Habitats are split into sub-classes for enhanced classification (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediment).
- Each parcel in the vector product has a unique Parcel_ID and a rich metadata profile; vector data includes 10 attributes per polygon.
- The 23 LCM2007 classes are linked to Broad Habitat categories (Table 2 in the document), enabling alignment with broader habitat schemes.
- Validation against ground reference data yielded an average accuracy of 83% across 9,127 polygons, with local variation.

## Data products and formats
- Vector Data Set
  - Polygons with attached attributes (area, source images, Broad Habitat, KBE history, etc.).
  - Approximately 8.6 million polygons in GB and 0.9 million in NI.
  - Core attributes include Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code for display), KBE (processing history), ProbList (top 5 spectral classes with probabilities), CorePixels, Construct, TotPixels.
  - Includes Broad Habitat sub-classes for enhanced detail; Sub-class data should be validated before use due to variance in accuracy.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; derived from the vector data.
  - 1 km raster: summary products derived from 25 m raster (dominant class, and percentage cover for both LCM2007 classes and Aggregate classes).
  - GB and NI datasets use separate projections (GB: British National Grid; NI: Irish National Grid).
  - 1 km products include: Dominant cover (23 classes and Aggregate classes) and Percentage cover (23 classes and Aggregate classes).
- Data characteristics
  - Data access varies by product type; 1 km rasters are openly available via the CEH Information Gateway; the full vector and 25 m rasters are licence-based on request.

## Projections, extents, and metadata
- Vector and raster products for GB and NI have distinct coordinate systems and projections; GB uses British National Grid (OSGB36), NI uses Irish National Grid (and moving toward ITM in NI data).
- Extensive metadata is provided per polygon (processing steps, KS history, ProbList, etc.) to support data provenance and quality assessment.
- Parcel_ID enables traceability back to the original satellite image and segmentation workflow.

## Data access and governance
- 1 km raster data are openly accessible via CEH gateway.
- Full vector and 25 m raster products are available under licence on request; licensing terms vary by user and application.
- Strong emphasis on data provenance, reproducibility, and data governance: retain Parcel_ID, unit-level metadata, and KBE processing history; use ProbList to guide validation when using Broad Habitat sub-classes.

## Data quality considerations and caveats
- LCM2007 maps land cover, not necessarily land use; caution when inferring land use from cover attributes.
- Accuracy is validated at the thematic level (23 classes); Broad Habitat sub-classes may be less reliable and require independent validation.
- The 0.5 ha minimum mapping unit means small features may be dissolved or generalized.
- Ground reference validation shows an average accuracy of 83%, with potential local discrepancies due to spectral similarity, terrain, and landscape context.
- Users should consult the Final Report (Morton et al., 2011) for detailed methodology and Section 3.9/Chapter 4 for grassland subclass validation nuances.

## Appendix highlights (context for implementation)
- Appendix 1: LCM2007 classes (brief descriptions of Broad Habitats such as Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various Grasslands, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Saltwater/Freshwater, Urban/Suburban, etc.).
- Appendix 2: Relationship mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (illustrates how 23 LCM2007 classes align with Broad Habitats and their sub-classes; includes FieldCode mappings and descriptive notes).
- Appendix 3: Colour mapping (standard RGB representations for each LCM2007 class as used in the Final Report).

## Map projection and spatial specifics
- Great Britain: GB 25 m and 1 km rasters in British National Grid; vector data in the same framework.
- Northern Ireland: NI 25 m and 1 km rasters in Irish National Grid; NI vector data correspondingly projected.
- Northern Ireland is transitioning toward ITM; re-projection is typically supported in GIS environments.

## Data sizes and practical considerations
- Vector: nearly 10 million polygons; large file sizes (GB approximately 4.13 GB in shapefile format for vector; NI ~ 433 MB).
- Raster:
  - 25 m rasters: GB ~ 1.36 GB; NI ~ 46 MB.
  - 1 km rasters: data sizes range from tens of kilobytes to tens of megabytes depending on product (dominant vs. percentage cover for classes).
- Given the data volume, plan for storage, processing capacity, and appropriate software compatibility when integrating LCM2007 into monitoring frameworks.

## Further information
- Final Report for LCM2007 (Morton et al., 2011) provides a comprehensive methodology and assessment.
- Broad Habitat Classification guidance (Jackson, 2000) informs interpretation and cross-walking with LCM2007 classes.
- Contact and licensing details for data access and usage are provided by CEH (spatialdata@ceh.ac.uk; CEH data portal).