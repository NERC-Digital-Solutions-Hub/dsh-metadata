# Land Cover Map 2007 Dataset Documentation

## Introduction
- Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs for UK land cover data.
- Describes 23 classes based on UK Broad Habitats, derived from summer-winter composite satellite images at 20–30 m resolution.
- Updates LCM2000 with a spatial framework tied to Ordnance Survey cartography and image segmentation.
- Focuses on land cover (not strictly land use); final, comprehensive detail available in Morton et al. 2011 Final Report.
- This document covers LCM2007 data products; refer to appropriate documentation for LCM2000 and LCM1990.

## Background
- LCM2007 is parcel-based, classifying UK land cover into 23 classes aligned with Broad Habitats (JBAP-based).
- Uses 20–30 m imagery; polygons correspond to real-world objects (fields, woodland blocks).
- Maps land cover rather than land use (e.g., arable land cover vs. actual land use may differ).
- Minimum mappable unit: >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m were dissolved.
- Some Broad Habitats are subdivided into sub-classes when spectrally separable (e.g., Built-up Areas into Suburban and Urban).
- Validated at 23-class thematic resolution; provides rich metadata for polygons and a top-level QA process.

## LCM2007 Product Overview
- Available in multiple data formats and resolutions to support varied applications.
- Products include vector data, 25 m raster, and 1 km raster, with separate GB and Northern Ireland (NI) datasets and distinct projections.
- Aggregate classes exist for the 1 km raster products to simplify use where full thematic detail isn’t needed.

## Example Data Sets
- Vector data set: polygons with attached metadata; 8.6 million polygons in GB and 0.9 million in NI.
- 25 m raster data set: aligned with the vector data; retains detailed land cover with less metadata overhead.
- 1 km raster data set: derived by aggregating 25 m rasters to provide dominant and percentage cover at 1 km resolution.
- Vector vs. raster trade-offs:
  - Vector: rich polygon metadata; larger files; more detailed, but heavier to process.
  - 25 m raster: similar land cover detail with no polygon boundaries; easier for certain workflows.
  - 1 km raster: suitable for national-scale modelling, e.g., combining with meteorological or species data.

## Vector Data Set
- Contains 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Parcel_ID: unique identifier per parcel; includes source image reference.
- BH (Broad Habitat) and BHSub (Broad Habitat sub-class) describe dominant land cover and sub-class details.
- FieldCode: short field code string; not validated for accuracy at this level.
- INTCODE: integer display class (1–23), the class used for QA and display.
- KBE: Knowledge-Based Enhancement history (processing history and changes).
- ProbList: top five spectral-class probabilities for the polygon’s spectral signature.
- CorePixels and TotPixels: pixel counts used in classification.
- Construct: how the polygon was derived (OSMM generalised data, segmentation, etc.).
- The vector dataset includes BHSub and FieldCode, but users should validate Broad Habitat sub-classes if used for critical analyses.
- 1) The 23 LCM2007 classes map to Broad Habitats; 2) Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and sub-classes; 3) Appendix 3 provides the colour-mapping palette.

## Raster Data Sets
- 25 m raster: 23 LCM2007 classes; GB and NI provided separately with appropriate projections.
- 1 km raster: summarizes 25 m data to produce dominant class and percentage cover per 1 km cell; includes both 23-class and Aggregate-class variants.
- Metadata in Table 3 (dimensions, extents, pixel sizes, data types, coordinate systems) guides data handling and reprojection.
- Projections:
  - GB: British National Grid (BNG), Transverse Mercator; OSGB 1936 datum.
  - NI: Irish National Grid, transitioning toward ITM; older data in Ireland 1965 datum.
- Data sizes:
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB, NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB, NI ~46 MB.
  - 1 km rasters: sizes range from ~21 MB to ~49 KB depending on product.
- Data access is governed by licensing and access controls (see Data Access).

## Map Projection
- LCM2007 vector and raster datasets use GB: British National Grid and NI: Irish National Grid projections.
- NI is transitioning to the Ireland Transverse Mercator (ITM) projection; software should reproject NI data as needed.
- Projections align with respective coordinate systems for accurate geographic analysis.

## File Size
- Vector data: large due to polygon count and attributes; plan for substantial storage and processing power.
- Raster data: sizable but more manageable for certain applications; 1 km products are relatively compact for national-scale work.

## Data Access
- 1 km raster data sets are accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product are available on request under license from CEH; fees may apply.
- Access process involves online application or direct contact (spatialdata@ceh.ac.uk).

## Further Information
- Morton et al. 2011 Final Report for LCM2007: comprehensive methodology and validation details.
- Jackson 2000: guidance on Broad Habitat classifications and definitions.
- Appendix references provide detailed mappings and colour mappings for display and analysis.

## Appendix 1: LCM2007 Classes
- Descriptions and notes for each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grassland, etc.).
- Sub-class distinctions (e.g., Heather vs Heather grassland; Montane Habitats; Calcareous/Acid Neutral grasslands) and caveats about separation from ground truth data.
- Guidance on limitations and field considerations for specific classifications (e.g., bog vs. dwarf shrub heath, vegetation density thresholds).

## Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat subclasses for LCM2007
- Detailed mapping between Broad Habitats, LCM2007 class numbers, and Broad Habitat sub-classes and field codes.
- Includes numerous examples for how LCM2007 classes align with BH and field codes, and notes on classification nuances and validation considerations.

## Appendix 3: Recipe for standard LCM2007 colour mapping
- Colour (RGB) mappings for each LCM2007 class number (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, etc.).
- Palette used in the LCM2007 Final Report for consistent display of classes.

## Acknowledgements
- Datasets sourced from Landsat-TM5, SPOT imagery, AWIFS, and OS cartographic data, among others.
- Data use governed by rights from Ordnance Survey and various data providers; CEH acknowledges licensing and source contributions.
- The Countryside Survey partnership and CEH lead the publication and distribution of LCM2007 data.