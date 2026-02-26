# Land Cover Map 2007 Dataset Documentation

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land-cover dataset using 23 classes derived from Broad Habitats, based on satellite imagery, and intended to support environmental health monitoring and policy evaluation.
- It updates LCM2000 with an improved spatial framework and richer metadata to aid integration with other GIS datasets.

## Data products and structure

- Vector Data Set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon carries 10 attributes, including: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class code for display), KBE (processing history), ProbList (top 5 spectral matches), CorePixels, TotPixels, and Construct (data source/segmentation method).
  - Unique Parcel_ID allows unambiguous communication; recommended to retain.
  - Sub-classes (BHSub) provide additional detail but are not as rigorously validated as the main LCM2007 classes.

- Raster Data Sets
  - 25 m and 1 km raster products derived from the vector data.
  - Great Britain and Northern Ireland provided separately with their respective projections.
  - 23 LCM2007 classes are available in the 25 m raster; a 1 km raster product set provides:
    - Dominant cover at 1 km for LCM2007 classes and for Aggregate classes
    - Percentage cover at 1 km for LCM2007 classes and Aggregate classes
  - Metadata specifications (dimensions, extents, pixel size, data type, coordinate system) are detailed in the documentation Tables.

- Class relationship and color
  - Table 2 maps LCM2007 classes to Broad Habitat aggregate classes.
  - Appendix 3 provides a standard color mapping for display (RGB values per class).

## Production methodology and validation

- Method
  - Parcel-based classification using summer-winter composite satellite imagery (20–30 m pixels).
  - Production framework uses OS MasterMap/large-scale vector basements refined with image segmentation.
  - Rich metadata capture and knowledge-based enhancements (KBE) applied to polygon attributes.
- Validation
  - Ground reference data used to validate LCM2007 against spatially and thematically aligned data.
  - Overall average accuracy: 83% across 9,127 ground reference polygons; local discrepancies may occur.
- Output discipline
  - LCM2007 maps land cover, not land use; MMU excludes features smaller than 0.5 ha or linear features shorter than 20 m.

## Data access, licensing, and size

- Access
  - 1 km raster data: available via the CEH Information Gateway.
  - Full vector product and 25 m raster product: available under licence on request from CEH.
  - Online data access and licensing may involve fees.
- File sizes (typical guidance)
  - Vector shapefiles (100 km x 100 km): GB ~ 4.13 GB; NI ~ 433 MB.
  - Raster (geotiff) 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
  - 1 km rasters: 21 MB to 49 KB (varies by product).
- Projections
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (transitioning to ITM projection).
- Data management notes
  - Vector products are large; policies advise careful handling and storage planning.
  - Metadata-rich dataset includes detailed processing history and pixel-level provenance.

## Data quality, metadata, and limitations

- Metadata
  - Rich polygon-level metadata including processing lineage, KBE history, and ProbList.
  - Parcel_ID preserves traceability to source imagery.
- Limitations and cautions
  - Broad Habitat sub-classes (BHSub) may be less consistently validated; users should perform their own validation for sub-class analyses.
  - Ground-truth accuracy can vary regionally; use aggregated results for policy-level inferences.
  - Sub-class distinctions (e.g., Heather vs. Heather grassland; various grassland sub-types) can be challenging spectrally and may require aggregation or local validation.
- Appendices provide detailed class definitions, the relationship between Broad Habitats, LCM2007 classes, and sub-classes, and the standard colour mapping used in reports.

## Practical usage for monitoring and policy decisions

- LCM2007 provides a consistent, geo-referenced basis for monitoring land-cover change, biodiversity planning, and environmental health indicators across the UK.
- The combination of high-resolution vector data (with rich metadata) and scalable raster products supports both localized analyses and national-scale assessments.
- When using the data for policy evaluation:
  - Prefer the 23 LCM2007 classes for thematic analyses; use Aggregate 1 km rasters for large-scale modeling where a reduced class set is sufficient.
  - Leverage Parcel_ID and ProbList to assess confidence in classifications and to guide validation efforts.
  - Consult the Final Report Morton et al. (2011) for comprehensive methodological context and caveats, and Jackson (2000) for Broad Habitat definitions.

## References and further information

- Morton et al., 2011. Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L., 2000. Guidance on the interpretation of the Biodiversity Broad Habitat Classification. JNCC Report 307.
- Additional project and data access details are available through CEH and the Countryside Survey partnership resources.