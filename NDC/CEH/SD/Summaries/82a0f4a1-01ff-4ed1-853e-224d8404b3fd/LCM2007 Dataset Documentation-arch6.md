# Land Cover Map 2007 Dataset Documentation

- Land Cover Map 2007 (LCM2007) is a UK parcel-based land cover classification using 23 classes derived from Broad Habitats, created from summer-winter satellite composites at 20–30 m resolution.
- It updates LCM2000 with an OS-based spatial framework and segment-based polygons for compatibility with GIS data.
- LCM2007 maps land cover (not land use) and has a minimum mappable area of >0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved into surrounding areas.
- Outputs are designed for broad usability across applications, with emphasis on data provenance, QA, and flexibility for different analyses.

## Data Products and Formats

- Vector Data Set
  - Polygons with 10 attributes per polygon; 8.6 million polygons in GB and 0.9 million in NI.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (1–23), KBE (processing history), ProbList (top 5 spectral-class probabilities), CorePixels, TotPixels, Construct.
  - Unique Parcel_ID for unambiguous communication; BHSub provides sub-class notes but not as robust as the main LCM2007 class.
  - Rich metadata per polygon including processing history and QA history.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; 1 km raster products derived by aggregation of 25 m data.
  - 1 km raster: aggregate-friendly products (dominant class and percentage cover for both LCM2007 classes and Aggregate classes).
  - Separate GB and NI datasets due to different projections; NI moving toward ITM in future workflows.
- Scale and resolution
  - 25 m and 1 km raster products; vector data provide the highest thematic resolution (23 classes) with polygon-level metadata.

## Class Structure and Mapping

- 23 LCM2007 classes based on UK Broad Habitats; some classes subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and other).
- Appendix 2 describes the relationship and mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3 provides standard colour mappings for display (RGB values per LCM2007 class).

## Data Quality, Validation, and Limitations

- Ground reference validation: average accuracy around 83% across 9127 polygons; local discrepancies may occur.
- BHSub classes offer additional information but are not covered by the primary QA and should be validated independently if used at sub-class level.
- Knowledge-based enhancement (KBE) records processing history and clue on changes to classes; ProbList indicates the spectral probability distribution for the polygon.
- The product is designed for thematic resolution rather than perfect locality; use LCM2007 classes for high-confidence classification and consider aggregation or post-processing for some analyses.

## Access, Licensing, and Use

- Data access:
  - 1 km raster data accessible via the CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under licence from CEH; online application process available; licensing fees may apply.
- Usage guidance:
  - Vector data provide detailed attributes and metadata but larger file sizes; 25 m rasters are more compact and easier to process for some workflows.
  1 km rasters are suitable for UK-scale modelling and can be combined with other datasets (e.g., meteorological or species distribution data).
- Projections and compatibility:
  - GB: British National Grid (OSGB36).
  - NI: Irish National Grid (with ongoing transition to ITM); reprojecting may be needed for some GIS workflows.

## Practical Guidance for Data Support

- Choosing data product:
  - For detailed analysis with rich metadata and the ability to query at parcel level, use the vector data.
  - For processing efficiency or large-area modelling, use 25 m rasters; for UK-wide analyses, use 1 km rasters with aggregate classes.
- Data preparation:
  - Preserve Parcel_ID in vector datasets to maintain traceability across analyses.
  - Exercise validation when using Broad Habitat sub-classes (BHSub) for specialized studies.
  - When using 1 km rasters, be mindful of aggregation assumptions and the Reduced thematic detail compared to 25 m or vector products.
- Quality assurance:
  - Refer to the Final Report Morton et al. (2011) for detailed methodology and limitations.
  - Validate Broad Habitat sub-classes against site-specific data if used for fine-scale decision-making.
- Documentation and metadata:
  - Leverage the rich polygon metadata (source images, processing details, KBE history, ProbList) for audit trails and reproducibility.
  - Use Appendix 2 for class-to-habitat context and Appendix 3 for consistent colour display in maps.

## Additional Information and References

- Final Report for LCM2007: Morton et al., 2011 (Countryside Survey Technical Report No. 11/07).
- Broad Habitat classification guidance: Jackson, D.L. 2000 (JNCC Report 307).
- Acknowledgements: datasets from Landsat, SPOT, AWIFS, Ordnance Survey, and other providers; CEH/Countryside Survey partnership.

## Appendices (Overview)

- Appendix 1: LCM2007 Classes – detailed descriptions and Broad Habitat associations.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3: LCM2007 colour mapping – standard RGB display values for each class.

- Acknowledgements and licensing notes about data sources and rights.