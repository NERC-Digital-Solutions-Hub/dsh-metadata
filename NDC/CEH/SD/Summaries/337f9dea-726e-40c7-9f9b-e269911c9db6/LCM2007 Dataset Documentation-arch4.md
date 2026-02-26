# Land Cover Map 2007 Dataset Documentation

- Provides UK land cover data products (LCM2007) to support diverse user needs; recommends consulting the Final Report (Morton et al., 2011) for comprehensive methodology, limitations, and QA.
- Built as an update to LCM2000 with a parcel-based, 23-class classification rooted in UK Broad Habitats; maps land cover (not strictly land use) from satellite imagery (20–30 m pixels) and refined with OS master maps and segmentation.
- Distinguishes between data products (vector and raster) and provides guidance on when to use each (e.g., high detail with vector, lighter metadata with 25 m raster; 1 km rasters for national-scale modeling).

## Data Products

- Vector Data Set
  - Contains roughly 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon includes 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Parcel_ID provides a unique polygon identifier tied to the source imagery; BH/Sub-class information supports detailed classification and downstream mapping.
  - Includes Broad Habitat sub-classes (BHSub) and a probability list (ProbList) for the top five spectral classes; QA primarily applies to the main LCM2007 class, with caution advised for subclasses.
  - Rich metadata capturing processing history, data sources, and knowledge-based enhancements (KBE).

- Raster Data Sets
  - Derived from the vector product to produce 25 m and 1 km products.
  - Separate data sets for Great Britain and Northern Ireland due to different projections.
  - 23-class 25 m raster; 1 km rasters provide dominant class, aggregate class, and percentage cover (both for LCM2007 classes and aggregates).

## Class and Mapping Details

- LCM2007 uses 23 classes aligned to UK Broad Habitats; some broad habitats are further subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh variants).
- Appendix 2 describes how Broad Habitats map to LCM2007 classes and sub-classes; Appendix 3 covers standard color mapping for visualization.
- Map interpretation note: LCM2007 aims to map land cover, not strictly land use; e.g., arable crops indicate arable land use, but grass areas may not reveal exact land use.

## Spatial Framework and Data Structure

- GB data use the British National Grid; NI data use the Irish National Grid (with NI transitioning to ITM).
- Minimum mappable unit (MMU) is >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m are dissolved into surrounding areas.
- LCM2007 is validated at the 23-class thematic resolution; Broad Habitat sub-classes are provided but may have lower accuracy and require user validation.

## Data Access and Licensing

- 1 km raster data is available via the CEH Information Gateway.
- Full vector product and 25 m raster product are available under license on request from CEH (data access via online application or direct contact).
- License fees may apply for some users or applications.

## Data Quality, Validation, and Limitations

- Ground reference validation against 9,127 polygons yields an average accuracy of 83%, acknowledging regional variability.
- Some classes (especially Broad Habitat sub-classes) are not covered to the same QA rigor as the main LCM2007 class; users should perform their own validation for subclass-level analyses.
- Certain habitat distinctions (e.g., Neutral vs Calcareous Grassland, Bog vs Dwarf Shrub Heath) can be challenging spectrally; consult Morton et al. 2011 for guidance and potential aggregation options.

## Projections, File Sizes, and Technical Notes

- File sizes reflect large polygon counts and rich metadata:
  - Vector (100 km x 100 km shapefile) GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters are smaller (latest products 21 MB to 49 KB, depending on metric).
- Data formats are designed for broad GIS use, with detailed attribute tables (including BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).

## Further Information and References

- Final Report for LCM2007: Morton et al. (2011) – comprehensive methodology, QA, and limitations.
- Broad Habitat classification guidance: Jackson (2000) – definitions and relationships to other classifications.
- Acknowledgements cover data sources and licensing from various agencies and satellite data providers.

Key takeaways for Data Leaders:
- LCM2007 provides rich, trackable land-cover assets with strong metadata, enabling governance, provenance, and cross-system integration.
- Use the vector product for detailed, attribute-rich analyses; use 25 m or 1 km rasters for scalable, lower-detail modeling and broad-scale decision-making.
- Plan for large data volumes and licensing considerations; ensure alignment with data strategy for data discovery, governance, and cross-agency collaboration.
- Leverage the robust QA narrative, but conduct your own validation for subclass-level analyses and when integrating Broad Habitat sub-classes into critical decisions.