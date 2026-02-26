# Land Cover Map 2007 Dataset Documentation

- Provides a range of land cover data products for the UK (LCM2007), built from summer-winter satellite composites at 20–30 m resolution.
- Updates LCM2000; uses OS-based spatial framework refined with image segmentation to produce polygons representing real-world objects (fields, woodland blocks).
- Maps land cover (not strictly land use) and enforces a minimum mappable unit of >0.5 ha (parcels <0.5 ha and linear features <20 m dissolved).

## Data Content and Structure

- 23 LCM2007 classes based on UK Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh).
- Two main data formats:
  - Vector data: polygons with 10 attributes per polygon, including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels; ~8.6 million polygons GB, ~0.9 million NI.
  - Raster data: 25 m and 1 km products derived from the vector data; GB and NI provided separately due to different projections.
- Parcel_ID provides a unique, traceable identifier for communication and data provenance.
- Metadata-rich dataset: includes processing history (KBE), top five spectral class probabilities (ProbList), and links to source images; recommended to retain Parcel_ID for communications and data lineage.
- 1 km rasters summarize 25 m data (dominant class and percentage cover for both LCM2007 classes and Aggregate classes).

## Data Quality and Validation

- Validated against ground reference data with 9,127 polygons; average accuracy 83% (note: overall accuracy is an average; local discrepancies may occur).
- Broad Habitat subclasses (BHSub) are included but are not uniformly covered by QA; users are advised to perform their own validation if utilizing Broad Habitat subclass level classifications.
- Designed for thematic resolution at 23 LCM2007 classes; Broad Habitat classes map to LCM2007 classes with sub-class relationships detailed in appendices.

## Data Access and Licensing

- 1 km raster data available via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; online application or direct contact required; licence fees may apply.
- File size considerations:
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21 MB to 49 KB depending on product.
- Projections:
  - GB: British National Grid (OSGB 1936; Transverse Mercator).
  - NI: Irish National Grid (Ireland 1965; transitioning to ITM in NI).
- Data are land cover (not land use) and the 0.5 ha MMU may exclude smaller patches.

## Technical Details

- Product overview includes multiple data products with varying spatial/thematic resolutions to support different applications.
- LCM2007 classes are tied to Broad Habitats; Appendix 1 provides brief class definitions and criteria; Appendix 2 maps relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 details standard colour mappings.
- Geospatial attributes and construction details:
  - BH: dominant Broad Habitat class per polygon.
  - BHSub: Broad Habitat sub-class (describes FieldCode).
  - FieldCode: short codes used during LCM2007 production; not QA-assessed.
  - KBE: knowledge-based enhancements applied during processing.
  - ProbList: top five spectral-class probabilities for the polygon.
  - CorePixels/TotPixels: pixel counts used in classification.

## Usage Guidance for Data Leaders

- Consider end-user needs and ensure data products support co-ownership of data products and iterative validation.
- Use the rich metadata to track data provenance, processing steps, and uncertainty (ProbList) for transparency and reproducibility.
- Acknowledge limitations: Broad Habitat subclasses require independent validation if used beyond the primary 23-class schema; small patches and some habitats may be challenging to classify remotely.
- Plan for data governance: manage formats (vector with attributes vs. raster with summaries), discoverability (Parcel_ID retention), and updates via the official data access channels.

## Appendices (Reference)

- Appendix 1: LCM2007 class definitions (Broad Habitats with notes on morphology and mapping limitations).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3: Colour mapping recipe for standard LCM2007 visualization.

## Additional Information

- Final Report for LCM2007 (Morton et al., 2011) recommended for a comprehensive description and assessment; counterpart details for LCM2000 and LCM1990 are in their respective documents.
- Acknowledgements cover satellite data sources, cartographic data, and institutional contributions; data usage is subject to Crown Copyright and dataset licensing terms.