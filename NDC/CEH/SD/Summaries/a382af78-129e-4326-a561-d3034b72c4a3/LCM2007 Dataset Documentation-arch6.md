# Land Cover Map 2007 Dataset Documentation

- Purpose and scope
  - Parcel-based UK land cover classification using 23 classes, based on UK Biodiversity Action Plan Broad Habitats.
  - Satellite imagery (summer-winter composites) at 20–30 m pixels.
  - Maps land cover (not land use); provides products for diverse GIS applications; aims to upgrade LCM2000 with OS-based spatial framework and segmentation.

- Key characteristics
  - 23 thematic classes mapped from 20–30 m imagery; some broad habitats are subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Minimum mapping unit: parcels >0.5 ha; smaller patches dissolved into surrounding landscape.
  - Parcel_ID attribute gives a unique label for each polygon; recommended to retain for communication and provenance.
  - Rich metadata: processing history, knowledge-based enhancements (KBE), and a top-5 spectral class probability list (ProbList) per polygon.
  - Ground-reference validation: average accuracy ~83% across 9,127 polygons; local discrepancies may occur.

- Data products and formats
  - Vector data set
    - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - 10 attributes per polygon (Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
    - Broad Habitat sub-classes (BHSub) provide additional detail but are not QA-validated at the same level as LCM2007 classes; use with validation for sub-class level analyses.
  - Raster data sets
    - 25 m and 1 km products derived from the vector data.
    - Separate projections for Great Britain (British National Grid) and Northern Ireland (Irish National Grid).
    - 25 m raster: 23 LCM2007 classes; 1 km raster: aggregates of classes and dominant/percentage covers.
    - Table 3 provides grid dimensions, extents, pixel sizes, and coordinate systems for GB and NI.
  - Aggregates and class mapping
    - Table 2 defines the relationship between Aggregate classes, Broad Habitats, and LCM2007 classes (used for 1 km rasters).
    - Appendix 2 details the mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Colour mapping
    - Appendix 3 provides the standard LCM2007 colour mapping (RGB) for display.

- Data access and licensing
  - 1 km raster data available via the CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25 m raster available by license on request from CEH; online application via ceh.ac.uk/data.
  - Licence fees may apply for some users and applications.
  - Large file sizes: vector (~GBs per region) and rasters (GBs for GB; smaller for NI).

- Projections and data characteristics
  - Vector and 25 m rasters for Great Britain in British National Grid; Northern Ireland in Irish National Grid.
  - NI transitioning to Ireland Transverse Mercator (ITM); ability to reproject with GIS tools.
  - MMU and data quality considerations highlighted; outputs are designed for compatibility with other GIS datasets.

- Usage guidance and limitations
  - LCM2007 maps land cover, not strictly land use; some land-use inferences may be ambiguous from spectral data alone.
  - High thematic resolution (23 classes) is recommended for validated analyses; Broad Habitat sub-classes and FieldCodes require user validation due to lower QA coverage at that level.
  - Known classification nuances in grassland types (Neutral/Calcareous/Acid), bogs, and heaths; consider aggregating classes if appropriate for your use case.
  - 0.5 ha MMU means very small patches may be dissolved; be mindful in analyses requiring fine-grained fragmentation.

- Documentation and further information
  - Final report: Morton et al. 2011 (Final Report for LCM2007).
  - Broad Habitat guidance: Jackson 2000 (JNCC Report 307).
  - Appendix content:
    - Appendix 1: LCM2007 classes with brief class definitions.
    - Appendix 2: Detailed mapping between Broad Habitats, LCM2007 classes, and sub-classes.
    - Appendix 3: Colour mapping recipe for display.
  - Acknowledgements and data provenance from Landsat, SPOT, AWIFS, and Ordnance Survey-derived datasets.

- Endnotes and contact
  - Subject to copyright notices; CEH and Countryside Survey Partnership publish and license terms.
  - For further information and access details: Morton et al. (2011) Final Report; CEH data portal and contact (spatialdata@ceh.ac.uk).