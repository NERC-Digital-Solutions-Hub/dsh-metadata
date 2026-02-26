# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a UK parcel-based land cover classification using 23 Broad Habitat-based classes, derived from 20–30 m satellite imagery, and produced in multiple data formats (vector and raster) to support GIS map-based analysis.
- It updates LCM2000 with a framework built on generalised OS mapping, improving compatibility with GIS datasets and object-based parcel delineation.
- LCM2007 maps land cover (not land use) with a minimum mappable unit of 0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved into surrounding areas.

## Data Products and Formats

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 polygon attributes per polygon (including area, source images, Broad Habitat, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
  - Unique Parcel_ID assigned to each parcel for unambiguous communication.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with respective projections.
  - 1 km raster: aggregated products derived from 25 m data (dominant class, percentage cover for 23 classes; and aggregate classes for 1 km).
  - 1 km products include both GB and NI variants.
- Aggregation and Sub-classes
  - 1 km products also include aggregate (merged) classes for simplified analysis.
  - Some Broad Habitat sub-classes are provided (BroadHabSub) but are not as rigorously QA’d as primary LCM2007 classes; use with caution and validate for sub-class level analyses.
- Additional resources
  - Appendix 3 provides standard LCM2007 colour mapping (and an ArcGIS .lyr file).
  - Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 1 lists the 23 LCM2007 classes (with brief habitat descriptions).

## Class Structure and Key Characteristics

- 23 LCM2007 classes are grounded in UK Broad Habitats (as per Jackson 2000) with some subdivisions:
  - Built-up Areas and Gardens subdivided into Urban and Suburban.
  - Dwarf Shrub Heath subdivided into Heather and Heather grassland.
  - Littoral Sediment subdivided into Littoral sediment and Saltmarsh (Priority Habitat).
- LCM2007 is validated at thematic resolution of the 23 classes; detailed sub-classes (BHSub) exist but are less consistently validated.
- The 25 m and 1 km raster products provide different thematic and spatial resolutions, catering to both detailed mapping and national-scale modelling contexts (e.g., 1 km for UK-wide modelling).

## Data Quality, Validation, and Limitations

- Validation against ground reference data (9127 polygons) yielded an average accuracy of 83%, with local discrepancies possible.
- Change mapping across CEH land cover products (1990, 2000, 2007) is complex due to class and spatial structure differences; LCM products are not well suited for change detection without careful reconciliation.
- KBE (Knowledge-Based Enhancements) applied during polygon construction, with a ProbList showing the top five spectral class matches; users should validate sub-class level information if used for detailed discrimination.

## Spatial Framework, Projections, and Coverage

- Vector and raster products for Great Britain use the British National Grid; Northern Ireland uses the Irish National Grid.
- NI is transitioning toward ITM in some datasets; reprojecting to ITM is supported where required.
- MMU and segmentation are based on OS mapping bases (OSMM and related vector layers) to create coherent parcel-level boundaries.

## Data Access, Licensing, and Size

- Data access:
  - 1 km raster data sets are available via the CEH Information Gateway.
  - The full vector product and 25 m raster product are available on request under licence; fees may apply.
- File size guidance (approximate and format-dependent):
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
  - 25 m raster: GB ~1.36 GB; NI ~46 MB.
  - 1 km products: range from ~21 MB (percentage cover for 23 classes) to ~49 KB (dominant cover) per area.
- Licensing notes: Some data are licensed; applications may require CEH data agreements and fees.

## Practical Guidance for GIS Specialists

- Use Parcel_ID to maintain traceability of polygons and ensure consistent communication across analyses and colleagues.
- Choose data product based on workflow:
  - Vector dataset: rich attribute data and metadata per parcel; suitable for precise, object-based GIS work but larger file sizes.
  - 25 m raster: efficient for large-area analyses where polygon boundaries and metadata are less critical.
  - 1 km rasters: suitable for national-scale modelling and comparisons when high thematic resolution is not required.
- For NI users, be mindful of projection transitions (Irish National Grid to ITM in some NI datasets) and reproject as needed for interoperability.
- When using Broad Habitat sub-classes (BHSub) and FieldCode, apply your own validation if sub-class level accuracy is critical; primary LCM2007 class (INTCODE) is the recommended display/classification.
- Expect limitations in change detection; consider reclassification or reconciliation when comparing LCM2007 with older CEH products.
- Review Appendix 1 for class definitions and Appendix 3 for colour mappings to ensure consistent visualisation and interpretation in GIS outputs.

## Appendices and References

- Appendix 1: LCM2007 Classes (descriptions and Broad Habitat mappings)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
- Appendix 3: LCM2007 colour mapping (and ArcGIS .lyr file)
- Appendix 4: Updates to products (Version 1.2, May 2014)
- Key references: Morton et al. (2011) Final Report for LCM2007; Jackson (2000) Broad Habitat definitions
- Acknowledgements: data sources from Landsat, SPOT, AWIFS, OS, and other datasets; CEH and Countryside Survey Partnership support