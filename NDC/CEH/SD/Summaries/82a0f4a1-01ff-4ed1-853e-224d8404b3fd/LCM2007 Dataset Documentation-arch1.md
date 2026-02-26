# Land Cover Map 2007 Dataset Documentation

- UK-wide parcel-based land cover classification using 23 classes derived from Broad Habitats
- Spatial resolution and data products
  - Vector data: polygons for Great Britain and Northern Ireland with rich metadata
  - Raster data: 25 m and 1 km products derived from vector
- Purpose and scope
  - Maps land cover (not land use) with a minimum mapping unit of 0.5 ha
  - Updates LCM2000 using OSMM/large-scale vector frameworks and image segments
  - Designed to support a range of applications and GIS interoperability

## Data Products and Structure

- Vector Data Set
  - Contains 8.6 million polygons (GB) and 0.9 million polygons (NI)
  - Each polygon has 10 attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels
  - Parcel_ID provides unique communication across users; recommended to retain
  - BH and BHSub classify at Broad Habitat and sub-class levels; FieldCode provides detailed codes
  - INTCODE gives a display-friendly 1-23 class code; KBE tracks processing history
  - ProbList lists top 5 spectral-class candidates with probabilities
  - Construct indicates source framework (OSMM, segmentation, etc.)
- Raster Data Sets
  - 25 m and 1 km products derived from the vector data
  - GB and NI provided in separate projections
  - 25 m raster uses 23 LCM2007 classes; 1 km raster provides dominant cover and percentage cover for both LCM2007 classes and Aggregated classes
  - Metadata includes grid extent, pixel size, data type (unsigned 8-bit), projection, and datum
- Data Access and Availability
  - 1 km raster data accessible via CEH Information Gateway
  - Full vector and 25 m raster products available on request under licence
  - Licence fees may apply for some users and applications

## Thematic Classification and Sub-Classes

- 23 LCM2007 classes are based on UK Broad Habitats
- Some Broad Habitats are subdivided to improve spectral discrimination:
  - Built-up Areas and Gardens: Urban and Suburban
  - Dwarf Shrub Heath: Heather and Heather grassland
  - Littoral Sediment: Saltmarsh (Priority Habitat) and other Littoral sediment
- Broad Habitat Sub-Classes (BHSub) and FieldCode provide more detailed classifications, though not all sub-classes have the same QA-level reliability
- Users are advised to validate sub-class level classifications if used for detailed analysis

## Data Quality, Validation, and Limitations

- Validation
  - Ground reference validation against 9127 polygons
  - Average accuracy around 83%
  - Local discrepancies may occur; accuracy is an average across the dataset
- Limitations and cautions
  - LCM2007 maps land cover, not strictly land use
  - Minimum mappable unit and dissolved small features (0.5 ha and <20 m lines)
  - Broad Habitat sub-classes are not guaranteed to match QA quality of main LCM2007 classes
  - Grassland sub-classes (Neutral/Calcareous/Acid) and other nuanced distinctions may require user validation or aggregation
  - Montane Habitat mapping uses altitude-based rules; users should consider potential validity differences between spectral classification and altitude-based rules
  - Some coastal and fen/marsh/swamp classes present classification challenges due to mosaic or patch sizes
- Data scale considerations
  - Local-scale analyses may face data gaps or scale mismatches; unifying multiple data sources may be necessary

## Spatial, Temporal, and Technical Details

- Projections and coordinate systems
  - Great Britain: British National Grid (OSGB 1936), Transverse Mercator
  - Northern Ireland: Irish National Grid (Ireland 1965), Transverse Mercator
  - NI moving toward ITM projection; reprojecting recommended as needed
- File sizes and formats
  - Vector shapefile (100 km x 100 km tiles): GB ~4.13 GB; NI ~433 MB
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB
  - 1 km rasters: 21 MB (23-class percentage) to 49 KB (dominant cover)
- Data extent and resolution
  - 25 m rasters: ~28,000 x ~52,000 cells (GB); 25 m pixel
  - 1 km rasters: ~700 x 1,300 cells (GB); 1 km pixel
- Data access notes
  - 1 km rasters publicly accessible via CEH gateway
  - Full vector and 25 m data available on licence by application to CEH

## Practical Use and Guidance

- Appropriate use by product
  - 23-class vector and 25 m rasters for detailed, localized analyses and cross-dataset integration
  - 1 km rasters for UK-wide modelling and integration with meteorological or species-distribution data
- Metadata and traceability
  - Rich polygon metadata and KBE history support reproducibility and audit of classification decisions
  - Parcel_ID and BH/BHSub enable precise communication and re-assembly of results
- Color and presentation
  - Appendix 3 provides standard RGB color mappings for LCM2007 classes (as used in the Final Report)
- Reference materials
  - Final Report for LCM2007 (Morton et al., 2011) for detailed methodology
  - Broad Habitat classifications and relationships (Jackson, 2000) for interpretation context

## Appendices (Summary)

- Appendix 1: LCM2007 classes with brief definitions and characteristics for each Broad Habitat
- Appendix 2: Relationship mappings between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub and FieldCode)
- Appendix 3: Colour mapping recipe (RGB) for LCM2007 classes used in presentation and reporting

## Additional Information and Contacts

- Acknowledgements to data providers (Landsat, SPOT, AWIFS, Ordnance Survey, various agencies)
- For further information and licensing:
  - Morton et al. 2011 Final Report for LCM2007
  - CEH information and data access portals
  - Spatialdata@ceh.ac.uk for licensing and data access questions