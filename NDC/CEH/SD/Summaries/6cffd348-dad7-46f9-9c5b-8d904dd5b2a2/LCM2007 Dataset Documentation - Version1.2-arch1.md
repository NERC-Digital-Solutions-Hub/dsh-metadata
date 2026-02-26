# LAND COVER MAP 2007 DATASET DOCUMENTATION

- UK-wide parcel-based land cover classification (LCM2007) with 23 Broad Habitat-based classes, built from 20–30 m satellite imagery.
- Improvements on LCM2000 include a framework aligned to OS vector layers (GB) and large-scale NI vectors, yielding polygons that align with real-world objects.
- Purpose: support a range of data users with rich metadata, QA, and multiple data products.

## Key characteristics

- Maps land cover (not always equivalent to land use) with a minimum mapping unit of 0.5 ha; parcels <0.5 ha or lines <20 m dissolved into surroundings.
- Classes based on UK Biodiversity Action Plan Broad Habitats; certain Broad Habitats are subdivided (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediment).
- Validated at 23-class thematic resolution; ground-reference validation against 9,127 polygons yields average accuracy ~83% (with expected local discrepancies).

## Data products and structure

- Vector Data Set (GB and NI)
  - ~8.6 million polygons (GB) and ~0.9 million polygons (NI).
  - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Unique Parcel_ID to support unambiguous communication; Broad Habitat sub-classes (BHSub) included but recommended to validate before use.
- Raster Data Sets
  - 25 m raster: full 23-class LCM2007; used for detailed thematic mapping.
  - 1 km raster: aggregate products using 23-class and Aggregate classes; includes dominant class, percentage cover (both 23-class and Aggregate).
  - GB and NI datasets produced separately with respective projections.
- Data relationships and mappings
  - Appendix 2 provides relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3 provides standard color mapping for visualization.
- Data access
  - 1 km raster products available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (fees may apply).

## Spatial and technical specifications

- Projections
  - GB: British National Grid (OSGB36) for both vector and 25 m raster; 1 km raster uses the same at GB scale.
  - NI: Irish National Grid for vector and 25 m raster; NI is transitioning toward Ireland Transverse Mercator (ITM).
- File sizes (indicative)
  - Vector shapefile (GB 100 km x 100 km): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: GB up to ~49 KB to ~21 MB depending on product.
- Documentation and versioning
  - Version 1.2 (May 2014) updates include new OS tiles (Fair Isle, Stranraer NW) and inclusion of a water class in 1 km products.
  - Appendix 4 lists product updates and version history.

## Methodology and QA

- Derived from summer-winter composite imagery with segmentation-based, parcel-level classification; uses knowledge-based enhancements (KBE) to adjust classifications.
- Ground reference validation performed to align spectral classes with thematic classes; QA supports display with INTCODE for standard display in GIS.
- Limitations for change detection
  - Change mapping is complex due to differing class schemes, spatial structure, and typical per-class misclassification rates (~20% image accuracy error). LCM2007 is not well suited for straightforward change detection.

## Use considerations for analysts

- Distinguish land cover from land use; some land covers do not reveal exact land-use intentions without contextual data.
- Sub-class level (BHSub) should be used with caution; validate against ground data before fine-grained analyses.
- When aggregating to 1 km or using 25 m vs. vector, consider the trade-off between detail (vector/25 m with metadata) and processing efficiency (1 km aggregates).
- Metadata-rich polygons (KBE, ProbList, Construct) enable reconstruction of processing history and spectral reasoning; retain Parcel_ID for traceability.
- Data access may require licensing; 1 km raster data is readily accessible via CEH gateway, while full vector and 25 m raster require a data request.

## Appendices and supporting information

- Appendix 1: LCM2007 23 class definitions ( Broad Habitats with field notes and nuances for each class).
- Appendix 2: Detailed mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode correlations).
- Appendix 3: Standard LCM2007 colour mapping for visualization.
- Appendix 4: Updates to Version 1.2 (May 2014): tile additions and water class inclusion.
- Acknowledgements: lists contributing imagery sources and data providers; CEH and Countryside Survey partnership notes.

## Practical references

- For more information: Morton et al. 2011, Final Report for LCM2007; Jackson 2000 on Broad Habitat classification relationships.
- Data access and licensing inquiries: CEH data portal and spatialdata@ceh.ac.uk.