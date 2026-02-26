# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose: UK-wide parcel-based land cover classification (LCM2007) providing 23 classes aligned with UK Biodiversity Action Plan Broad Habitats, based on summer-winter satellite imagery at 20–30 m resolution. Designed to support environmental monitoring and policy performance assessments with rich metadata and a standardized data structure. Notes that LCM maps land cover (not strictly land use) and uses a minimum mapping unit (MMU) of >0.5 ha.

- What it is: An upgraded, parcel-based land cover product that improves on LCM2000 by using a spatial framework derived from OS MasterMap/large-scale vector layers and spectral segmentation, yielding polygons that correspond to real-world objects (fields, woodland blocks) to facilitate GIS integration.

- Thematic resolution and classes:
  - 23 LCM2007 classes, based on Broad Habitats, with some subclasses for finer detail (e.g., Suburban vs Urban; Heather vs Heather grassland; Littoral sediment vs Saltmarsh).
  - Some Broad Habitat subclasses are used for classification but may not have QA-level consistency; users should validate if working at the subclass level.
  - Appendix 1 provides class descriptions; Appendix 2 explains cross-walks between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mappings.

- Data products and formats:
  - Vector Data Set: 8.6 million polygons (Great Britain) and 0.9 million polygons (Northern Ireland); 10 attributes per polygon (Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels). Parcel_ID enables traceability to input imagery. Includes Broad Habitat sub-classes (BHSub) with usage cautions.
  - Raster Data Sets:
    - 25 m raster: 23 LCM2007 classes; GB and NI separately; pixel-to-class mapping provided (Table 2 in the document).
    - 1 km raster: derived by summarizing 25 m data to dominant class and percentage cover; available as both 1) Dominant cover at 1 km for LCM2007 classes, and 2) Percentage cover at 1 km for LCM2007 and Aggregate classes.
  - Spatial coverage: GB and NI supplied separately due to different projections.

- Projections and coordinate systems:
  - Great Britain: British National Grid (OSGB 1936), Transverse Mercator.
  - Northern Ireland: Irish National Grid (with ongoing shift toward ITM); users should reproject as needed.

- Validation and accuracy:
  - Ground reference validation against a design-matched set of 9,127 polygons yields an average accuracy of 83% (recognizing that accuracy is an average across polygons and local variations exist).
  - The 23-class thematic resolution is recommended for QA-supported usage; error may occur at subclass level.

- Data quality, provenance, and metadata:
  - Rich polygon metadata capturing processing history, original spectral classification, KBE (Knowledge-Based Enhancements), and ProbList (top spectral class probabilities).
  - Each polygon carries a unique Parcel_ID for traceability; KHBE and ProbList support assessment of classification confidence.
  - Validation and QA processes described in Morton et al. (2011) Final Report; detailed methodology and limitations documented.

- Data access and licensing:
  - 1 km raster data accessible via the CEH Information Gateway.
  - The full vector product and 25 m raster product are available under licence on request from CEH (data access form and contact provided in the document).
  - Licence fees may apply to some users or applications.

- Practical considerations for analysts:
  - Use the 1 km rasters for national-scale modelling and integration with other datasets (e.g., meteorology, species distributions); use 25 m rasters or vector for finer-scale habitat analysis where metadata and polygon detail are valuable.
  - Preserve Parcel_ID and consider Broad Habitat sub-classes with caution; validate subclass results if used for decision-making or reporting.
  - When combining datasets, leverage the explicit metadata and KBE history to understand classification steps and potential biases.
  - Be mindful of the MMU and patch size: objects smaller than 0.5 ha are dissolved into surrounding areas during production.

- Guidance and references:
  - Primary documentation: Morton et al., Final Report for LCM2007 – the new UK Land Cover Map (2011).
  - Broad Habitat framework reference: Jackson, 2000.
  - Additional notes: Appendix materials detailing class mappings, subclass relationships, and colour mappings.

- Endnotes and acknowledgements:
  - Acknowledges satellite imagery sources (Landsat, SPOT, IRS, AWIFS) and Ordnance Survey/cartographic datasets; CEH and Countryside Survey Partnership responsible for production and dissemination of LCM2007 data.