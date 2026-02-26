# Land Cover Map 2007 Dataset Documentation

## Overview
- Parcel-based land cover dataset for the UK, using 23 Broad Habitat-based classes.
- Maps land cover (not land use); minimum mappable unit >0.5 ha; smaller parcels dissolved into surrounding landscape.
- Designed to be compatible with GIS, built from image segments and OS-based vector frameworks; supports various applications via multiple data products.
- Provides rich metadata and is validated against ground reference data.

## Data Products

### Vector Data Set
- Polygons with attached attributes: area, source images, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (LCM2007 class for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
- 8.6 million polygons in Great Britain; 0.9 million in Northern Ireland.
- 10 attributes per polygon; includes Parcel_ID for unique communication (parcel_id: image reference).
- BHSub provides text description of field codes; recommended to validate if using at subclass level.
- Large file sizes; vector data suitable for detailed analysis but may be heavy to process.

### Raster Data Sets
- 25 m and 1 km products derived from vector dataset.
- Separate data sets for Great Britain and Northern Ireland due to different projections.
- 23 LCM2007 classes for 25 m; 1 km products provide dominant and percentage cover for both LCM2007 classes and Aggregate classes.
- Metadata in Table 3 (spatial extents, pixel counts, coordinates, projections, datums, and data type).
- Projections: GB in British National Grid; NI in Irish National Grid (with NI transitioning toward ITM).

## Data Quality and Validation
- Ground reference validation allowed comparison against 9127 polygons; average accuracy approximately 83%.
- Local discrepancies may occur; accuracy varies by area and subclass.
- QA is based on the Morton et al. 2011 Final Report and supports confidence in the 23-class thematic resolution.

## Classification and Mapping Details

### LCM2007 Classes (Appendix 1)
- 23 Broad Habitat classes including Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grasslands (Neutral, Calcareous, Acid), Montane Habitats, Inland Rock, Urban/Suburban, Littoral/Littoral Sediment, Saltmarsh, Fen/Marsh/Swamp, Bog, Heather/Heather grassland, Montane, and others.
- Some Broad Habitats are subdivided into sub-classes (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).

### Appendix 2: Relationship with Broad Habitats and Sub-classes
- Maps LCM2007 class numbers to Broad Habitat categories and sub-classes (BHSub) to FieldCode.
- Provides guidance on how sub-classes relate to main LCM2007 classes and their use, including cautions about accuracy at the sub-class level.

### Appendix 3: Colour Mapping
- Standard RGB mappings for display of each LCM2007 class, used in the Final Report (Morton et al. 2011) to ensure consistent visualization.

## Data Access, Licensing, and Usage
- 1 km raster data sets accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; license fees may apply.
- Access channels: CEH gateway, CEH data portal (data@ceh.ac.uk or spatialdata@ceh.ac.uk).

## Projections, File Sizes, and Formats

### Projections
- Great Britain vector and 25 m raster: British National Grid (OSGB36).
- Northern Ireland vector and 25 m raster: Irish National Grid; NI is transitioning to ITM.

### File Sizes (guidance)
- Vector (Shapefile, 100 km x 100 km): GB ~4.13 GB; NI ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: 21 MB to 49 KB depending on product.
- Note: sizes vary by format and data access method.

## Production Methodology and Limitations
- Based on summer-winter composite satellite imagery (20–30 m pixels).
- Uses OS Master Map generalised topographic data and segmentation to create polygons representing real-world objects.
- LCM2007 maps land cover (not land use); some land cover types may not directly indicate land use.
- KBE (knowledge-based enhancements) applied to refine classifications; detailed provenance recorded in KBE histories.
- Limitations include difficulty distinguishing certain grassland types and fen/marsh/swamp complexities; montane mapping relies on altitude in some cases.
- Broad Habitat sub-classes may provide additional information but are not as rigorously QA’d as primary LCM2007 classes; users should validate if using subclass level data.

## Further Information and References
- Primary documentation: Morton et al., Final Report for LCM2007 (2011).
- Broad Habitat classification reference: Jackson, 2000.
- Acknowledgements include supporting satellite data sources and data providers.

## Data Governance Considerations for Data Stewards
- Maintain Parcel_ID and rich polygon metadata to preserve communication clarity and provenance.
- Retain BH and BHSub attributes with awareness of their differing QA levels; validate subclass usage.
- Ensure licensing terms are adhered to for vector and 25 m raster data; track access permissions.
- Consider aggregation to 1 km raster where appropriate for large-scale analyses; maintain awareness of aggregation impacts on class interpretation.
- Preserve the detailed metadata and processing history (KBE) for reproducibility and governance.
- Leverage the 83% average QA as a baseline, but perform local validation for critical applications, especially when using Broad Habitat sub-classes.