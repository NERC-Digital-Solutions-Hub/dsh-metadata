# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) provides a range of data products for UK-wide land cover mapping, designed for GIS-based data exploration and map-based visualisation. It updates LCM2000 with an object-based, polygonal framework and broad habitat classification aligned to UK Biodiversity Action Plan Broad Habitats. Final detailed methodology and assessment are in Morton et al. (2011).

## Key concepts for GIS work

- Maps land cover (not land use); may not always infer land use from spectral/class signatures.
- Data are parcel-based classifications with a minimum mapping unit (MMU) of >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved.
- 23 LCM2007 classes are based on Broad Habitats; several are further subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

## Data products and formats

- Vector Data Set
  - Polygons with attached attributes (10 attributes per polygon; Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Parcel_ID is unique per polygon and should be retained for communication and traceability.
  - KBE: Knowledge-based enhancements detailing processing history; ProbList provides top spectral class probabilities.
  - CorePixels and TotPixels describe pixel counts used in classification.
  - Construction methods include OSMM generalised data, segmentation, and agricultural boundary vectors.
  - Broad Habitat sub-classes (BHSub) provide additional descriptive detail but are not as rigorously validated as LCM2007 classes.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; derived from the vector dataset.
  - 1 km raster: aggregates of the 25 m data, with dominant class and percentage cover per 1 km pixel; also available for aggregate Broad Habitats.
  - Separate geographic products for Great Britain (GB) and Northern Ireland (NI) with appropriate projections.
  - Metadata-rich rasters include dominance and percentage metrics for both 23 classes and aggregate classes.

## Class structure and relationships

- 23 LCM2007 classes correspond to Broad Habitats (Appendix 1). Some Broad Habitats are further subdivided into subclasses (BHSub) for informational or probability purposes.
- Table 2 (Appendix 2) maps LCM2007 classes to Broad Habitats and aggregate groupings used in 1 km rasters.
- Appendix 3 provides a color-mapping recipe used in the Final Report to visualize classes.
- The 1 km rasters use Aggregate classes, merging several LCM2007 classes to simplify national-scale analyses.

## Data quality and validation

- Ground reference validation involved 9,127 polygons; average accuracy around 83% (recognizing local variations and the general QA context).
- The polo highlighting: Broad Habitat sub-classes and FieldCode are primarily for additional information and spectral-class probabilities; users should perform their own validation when using sub-classes for critical analyses.
- Rich metadata accompanies the vector product, enabling traceability of data sources, processing steps, and KBE history.

## Data access and licensing

- 1 km raster data sets are accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product are available under licence on request from CEH; license fees may apply.
- Access process: online CEH data application or contact spatialdata@ceh.ac.uk.

## Geographic projection and coverage

- GB vector and 25 m rasters use British National Grid (OSGB36); NI uses Irish National Grid.
- NI is transitioning to the Ireland Transverse Mercator (ITM); data can be reprojected to ITM with GIS tools.

## File sizes and data volumes

- Vector (Shapefile, 100 km x 100 km blocks): GB ~4.13 GB; NI ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: ranges from ~21 MB (23-class percentage cover) to ~49 KB (dominant cover).
- Large data footprints reflect nearly 10 million polygons and rich per-polygon attributes.

## Production and methodological highlights

- LC M2007 is parcel-based, created from 20–30 m satellite imagery with pan-European segmentation, producing polygons representing real-world objects (fields, woodland blocks).
- Polygon construction derives from OSMM generalised data and segmentation; KBE rules applied to refine classifications; ProbList documents spectral-class likelihoods.
- Data are described as “land cover” rather than “land use,” with cautions about inferring use from cover.

## Practical guidance for GIS specialists

- Choose data type by use case:
  - Vector: rich attributes, ideal for detailed per-polygon analysis, querying, and integration with other vector datasets; expect large file sizes.
  - 25 m raster: suitable for processing when polygon boundaries and metadata are not required; smaller workflows and easier raster analyses.
  - 1 km raster: best for national-scale analyses, modelling, and quick overlays, with aggregated class information.
- Retain Parcel_ID and KBE/ProbList data for provenance and validation workflows.
- Validate Broad Habitat sub-classes if used for decision-making; consider aggregating to 23-class or aggregate levels if necessary.
- Be aware of the recommended usage resolution: LCM2007 thematic resolution is 23 classes for QA and interpretation; the 1 km rasters provide a coarser but more scalable product.
- Reference Morton et al. (2011) Final Report for detailed methodology and assessment; consult Appendix 2 and Appendix 3 for class relationships and colour mapping.

## Additional information and references

- Morton, D. et al. (2011). Final Report for LCM2007 - the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on the interpretation of the Biodiversity Broad Habitat Classification.
- For more details and data access: CEH Information Gateway and CEH data portal.