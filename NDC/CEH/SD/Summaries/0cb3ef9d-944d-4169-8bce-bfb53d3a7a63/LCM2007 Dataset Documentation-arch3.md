# LAND COVER MAP 2007 DATASET DOCUMENTATION

- UK land cover parcel-based classification (LCM2007) with 23 classes based on Broad Habitats, using 20-30 m satellite imagery to map the UK.
- Built to support a wide user community with multiple data products at different thematic/spatial resolutions.

## Purpose and scope

- Provides guidance on using LCM2007 data products to monitor environmental health, inform policy, and support future decisions.
- Recommends consulting the Final Report (Morton et al., 2011) for a comprehensive assessment; this document focuses on the data products and their usage.
- Clarifies that LCM2007 maps land cover (not always land use) and uses a minimum mapping unit of 0.5 ha (parcels <0.5 ha or lines <20 m dissolved).

## Data products and structure

- Vector Data Set
  - 8.6 million polygons in Great Britain; 0.9 million in Northern Ireland.
  - Each polygon has 10 attributes, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class number for display), KBE history, ProbList, CorePixels, Construct, TotPixels.
  - Features unique Parcel_ID labelling for unambiguous communication.
  - Rich metadata per polygon; Knowledge-Based Enhancements (KBE) captured in processing history.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI extents with appropriate projections.
  - 1 km raster: derived summaries (dominant and percentage cover) for both LCM2007 classes and Aggregate classes.
  - Data products designed to support different applications (e.g., detailed local work with 25 m or broad national-scale modelling with 1 km).
- Class structure and relationships
  - 23 LCM2007 classes based on Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other Littoral sediment).
  - Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 1 details each LCM2007 class concept (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, wetlands, marine/coastal classes).
- QA and validation
  - Ground reference validation against spatially matched polygons.
  - Average accuracy around 83%, acknowledging local discrepancies and that some Broad Habitat sub-classes are less robust than the primary LCM2007 classes.
  - Caution advised when using Broad Habitat sub-classes for analysis; recommended validation prior to use at that level.
- Metadata and processing
  - Data include detailed provenance: source images, spectral classifications, KBE changes, and probability lists for top spectral matches (ProbList).
  - Emphasizes that LCM2007 is a complex dataset; familiarisation with production methodology and metadata is important to avoid inappropriate use.

## Data access, formats, and sizes

- Access
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on license request from CEH; online application process described.
  - Licence fees may apply for some users/applications.
- File sizes (guidance)
  - Vector (100 km x 100 km shapefile):
    - Great Britain: ~4.13 GB
    - Northern Ireland: ~433 MB
  - Raster 25 m:
    - Great Britain: ~1.36 GB
    - Northern Ireland: ~46 MB
  - Raster 1 km: 21 MB to 49 KB (depending on product)
- Projections and data integration
  - Great Britain: British National Grid (OSGB 1936)
  - Northern Ireland: Irish National Grid
  - NI migrating toward ITM projection; reprojecting is supported by GIS tools

## Map accuracy, limitations, and usage guidance

- Purpose: supports a range of monitoring needs, but data are not guaranteed to perfectly separate all land cover types in every context.
- Validation caveats
  - Ground truth indicates an overall ~83% accuracy; expect local variations.
  - Sub-class distinctions (Broad Habitat sub-classes) require careful validation before use for detailed analyses.
- Scale and aggregation considerations
  - 25 m vector/raster products offer detailed mapping suitable for local/derivative analyses.
  - 1 km raster products provide national-scale summaries (dominant class, percentage cover) suitable for policy-level monitoring and modelling.
- Use cautions for monitoring frameworks
  - The extensive metadata and QA/validation information support data governance and traceability.
  - Because some grassland and coastal sub-classes are spectrally challenging, consider aggregating classes or validating sub-class results for policy decisions.
  - Data governance should account for data provenance, update frequency, and transparency of processing steps (KBE history, ProbList).

## Appendices and supplementary information

- Appendix 1: LCM2007 Classes – definitions and notes on key characteristics for each class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grasslands, bog, fen, montane habitats, inland rock, urban/suburban, littoral and coastal types).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping of Gold-standard categories to finer spectral classes).
- Appendix 3: Colour mapping recipe for LCM2007 classes (for visualization in outputs and reports).
- Acknowledgements: data sources including Landsat, SPOT, AWIFS, OS MasterMap, soil and elevation data, and national datasets; CEH and Countryside Survey partnership contributions.

## Practical takeaways for monitoring and policy context

- LCM2007 provides a comprehensive, metadata-rich land cover dataset at multiple resolutions suitable for environmental health monitoring and policy evaluation.
- Choose the product (vector 25 m, raster 25 m, or raster 1 km) based on the policy question, geographic extent, and need for thematic detail versus national-scale summaries.
- Leverage the strong QA framework, provenance data, and ProbList to assess uncertainty in classifications and to justify the use of specific classes/sub-classes in analyses.
- Be mindful of the minimum mapping unit and potential misclassifications in complex habitats (notably certain grassland and coastal classes) when designing monitoring indicators or reporting formats.