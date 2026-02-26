# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Introduction and context
- Land Cover Map 2007 (LCM2007) is a UK-wide parcel-based classification of land cover, using 23 classes aligned to Broad Habitats.
- Based on summer–winter satellite imagery with 20–30 m pixels; upgrades LCM2000 with OS MasterMap/large-scale vector framework and image segmentation.
- Maps land cover (not land use); minimum mappable unit >0.5 ha; smaller parcels and lines dissolved into surrounding landscape.
- Provided as a range of data products to support diverse GIS applications; consult the Final Report for a comprehensive assessment.

## Data products overview
- LCM2007 is designed for use across GIS data sets and applications, with a thematic resolution of 23 classes and, in some cases, subdivisions of Broad Habitats.
- Classes are grouped to form Aggregate classes for certain raster products (1 km) to suit different applications.
- Each parcel receives a unique Parcel_ID and carries rich metadata and a probability list of spectral variant classes (ProbList).

## Vector Data Set (LCM2007 vector)
- Polygon-based format with 10 attributes per polygon.
- Large dataset: ~8.6 million polygons in Great Britain and ~0.9 million in Northern Ireland.
- Key attributes include: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display), KBE (processing history), ProbList (top spectral matches), CorePixels, TotPixels, Construct (how polygons were derived), and more.
- Broad Habitat sub-classes (BHSub) are included for informational/detail purposes but are not as rigorously QA-validated as the main LCM2007 classes.
- Parcel_ID should be retained to maintain unambiguous communication; it ties polygons to source imagery and construction history.
- Validation: ground-reference data against LCM2007 polygons yielded an average accuracy of ~83%, though local discrepancies may occur; subclass-level accuracy is not QAed to the same extent.

## Raster Data Sets (LCM2007 25 m and 1 km)
- Derived from the vector data; two spatial resolutions: 25 m and 1 km.
- Great Britain and Northern Ireland provided in separate projections.
- 25 m raster: 23 LCM2007 classes; pixel values correspond to the LCM2007 class numbers.
- 1 km raster: summary products using aggregates:
  - Dominant cover at 1 km for LCM2007 classes
  - Dominant cover at 1 km for Aggregate classes
  - Percentage cover at 1 km for LCM2007 classes
  - Percentage cover at 1 km for Aggregate classes
- 1 km data are useful for national-scale analyses and integration with other datasets (e.g., meteorology, species distributions).

## Class relationships and colour mapping
- Appendix describes the relationship between LCM2007 classes and Broad Habitats (and sub-classes) used for interpretation.
- Appendix 3 provides standard LCM2007 colour mapping for display in GIS, including RGB values for each class.

## Map projection and coordinate systems
- Vector and 25 m raster data for Great Britain: British National Grid (OSGB36).
- Northern Ireland data: Irish National Grid (now transitioning to Ireland Transverse Mercator in NI).
- When converting NI data to newer projections, reproject using appropriate GIS tools.

## File sizes and data formats
- Data sizes are large:
  - Vector (Shapefile) for 100 km × 100 km: GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: ranges from ~21 MB (23-class percentage) to ~49 KB (dominant cover).
- Data formats: vector polygons with attached metadata; 25 m rasters; 1 km rasters.

## Data access and licensing
- 1 km raster data available via CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector product and 25 m raster product available on request under licence from CEH; online application at ceh.ac.uk/data or via data@ceh.ac.uk.
- Licence fees may apply for some users and applications.

## Further information and references
- Final Report for LCM2007 – Morton et al., 2011 (CEH; detailed methodology and assessment).
- Guidance on Broad Habitat classifications – Jackson, 2000 (JNCC).
- Appendices: LCM2007 class descriptions, relationship mappings to Broad Habitats, and colour mappings (as used in the Final Report).

## Practical notes for GIS specialists
- LCM2007 provides rich polygon-level metadata ideal for detailed GIS analyses, but the 25 m raster products can be preferable when metadata overhead is undesirable.
- The 1 km raster products are suitable for national-scale analyses and integration with other large-scale datasets.
- Retain Parcel_ID for traceability and reproducibility; be aware that Broad Habitat sub-classes may require independent validation before use.
- The data are best used with awareness of the 0.5 ha minimum mapping unit, potential classification ambiguities in some Broad Habitats, and the need for validation in subclass analyses.