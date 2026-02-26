# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based classification of UK land cover, encompassing 23 classes aligned with UK Broad Habitats, produced from 20–30 m satellite imagery (summer-winter composites). It supersedes LCM2000 with improved GIS compatibility via OS-based spatial frameworks and segment-based polygons.
- Purpose for analysts: provide multi-resolution data products to support diverse applications, enabling analysis of land cover distributions, change, and modeling.

## Data Products and Structure

- Vector data set
  - 8.6 million polygons (Great Britain) and 0.9 million (Northern Ireland)
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels)
  - Unique Parcel_ID per polygon; retains field-level subclass descriptors (BHSub, FieldCode) for advanced use
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; separate GB and NI projections
  - 1 km raster: aggregate products derived from 25 m data (dominant class, percentage cover for both LCM2007 classes and Aggregate classes)
  - Data access targets: GB and NI differ in resolution and metadata; 1 km products designed for broad-scale UK modeling
- Data formats and resolution
  - 25 m vector vs. 25 m raster vs. 1 km raster
  - 1 km products include dominant cover and percentage cover (both class-based and Aggregate-based)
- File sizes (approximate)
  - Vector GB: ~4.13 GB; NI: ~433 MB
  - Raster 25 m GB: ~1.36 GB; NI: ~46 MB
  - 1 km products: ~21 MB to ~49 KB (GB)

## Classification and Metadata

- 23 LCM2007 classes based on Broad Habitats; certain broad habitats subdivided (e.g., Built-up Areas into Suburban/Urban; Dwarf Shrub Heath into Heather/Heather grassland)
- Core attributes
  - Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct (data source and segmentation method)
- Sub-class data
  - BHSub provides additional context but is not consistently validated at the subclass level; users advised to validate before use at Sub-class level
- Colour mapping
  - Appendix 3 provides standard colour mapping for each LCM2007 class (also available as an ArcGIS .lyr file)
- Data lineage and processing
  - Knowledge-Based Enhancements (KBE) applied during polygon construction; complete KBE history accessible in the KBE field

## Validation, Accuracy, and Limitations

- Validation
  - Ground reference validation against ~9,127 polygons yielded an average accuracy of ~83% (spatial/thematic resolution aligned to 23 LCM2007 classes)
  - Local discrepancies possible; accuracy is an average across the dataset
- Change detection and mapping
  - Change mapping across LCM1990–2007 is complex due to differing class definitions and spatial structure; typical spectral class error ~20%, while expected BH change may be smaller
  - LCMS not well suited for robust change detection between different LCMs
- General caveats
  - LCM2007 maps land cover (not strictly land use)
  - Minimum mappable unit: parcels >0.5 ha; linear features <20 m dissolved into surrounding landscape
  - Some grassland and habitat distinctions (e.g., Neutral/Calcareous/Acid Grassland) can be misclassified; users should perform validation or aggregation as needed
  - Broad Habitat sub-classes offer additional information but may not match the accuracy of primary LCM2007 classes

## Spatial and Temporal Coverage

- UK-wide coverage (Great Britain and Northern Ireland)
- Data derived from CEH and multiple satellite sources (Landsat-TM5, SPOT, AWIFS, etc.)
- Timeliness: LCM2007 reflects 1990–2007 periods for change considerations; not fully suited for rapid temporal monitoring without careful cross-walk to other datasets

## Projections, Coordinate Systems, and Projections Details

- Vector and raster datasets
  - Great Britain: British National Grid (BNG), Transverse Mercator
  - Northern Ireland: Irish National Grid; anticipated transition to ITM
- Pixel geometry and metadata
  - Table 3 provides pixel counts, extents, and coordinate references; notes that pixel origin is the south-west corner of the lower-left pixel

## Access, Licensing, and Usage

- Access
  - 1 km raster data via CEH Information Gateway
  - Full vector product and 25 m raster product available under license on request
  - Application process via CEH data portal or spatialdata@ceh.ac.uk; license fees may apply
- Documentation and references
  - Primary methodological details in Morton et al. (2011) Final Report for LCM2007
  - Broad Habitat definitions and relationships described in Jackson (2000) JNCC report
- Acknowledgements and credits
  - Datasets from Landsat, SPOT, AWIFS; OS, and other collaborative data sources acknowledged

## Appendices and Updates

- Appendix 1: LCM2007 Classes (definitions and Broad Habitat context)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
- Appendix 3: Colour mapping (LCM2007 colour recipe)
- Appendix 4: Updates to products (Version 1.2, May 2014)
  - OS tile updates (Fair Isle, Stranraer areas)
  - Water class additions for 1 km products; updates to NI products

## Summary for Practical Use

- LCM2007 provides a comprehensive, multi-resolution UK land cover dataset aligned to Broad Habitat classifications, with rich metadata for each parcel and multiple data products suited to different scales and applications.
- For analysts, key considerations include:
  - Use the 23-class LCM2007 vector or raster products for high-detail analyses, with caution regarding the Sub-class level accuracy
  - Leverage 1 km raster products for broad-scale modeling or integration with climate, species distribution, or other geospatial datasets
  - Validate Broad Habitat sub-classes if used for fine-grained classification or policy-relevant decisions
  - Be mindful of data access rights and licensing requirements; plan for large file sizes when working with vector data
  - Consult Morton et al. (2011) Final Report for methodology, QA procedures, and baseline change analysis guidance; use Jackson (2000) for Broad Habitat definitions
  - Expect limitations in change-detection applications across different LCM versions due to class and spatial structure differences