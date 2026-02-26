# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK landed cover classification for 2007 using 23 Broad Habitat-based classes aligned with UK Biodiversity Action Plan (BAP).
- Parcel-based, derived from summer-winter satellite composites at 20–30 m resolution.
- Maps land cover (not necessarily land use) and uses a 0.5 ha minimum mappable unit.
- Built to upgrade LCM2000 with a GIS-friendly structure based on OS master map and spectral segmentation; polygons represent real-world objects (fields, woodland blocks).
- Rich metadata, detailed processing history, and confidence indicators embedded in polygon attributes.

## Data Products and Structure
- Vector data set (GB and NI): ~10 million polygons with 10 attributes each; unique Parcel_ID for each polygon; includes Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (display-friendly class), Knowledge-Based Enhancements (KBE), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct history.
- Raster data sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI separate projections.
  - 1 km raster: summarised to dominant class and percentage cover for both 23 classes and Aggregate classes (based on 25 m data).
- The categories map to UK Broad Habitats with some subclasses and special cases (e.g., Built-up Areas split into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment split into Saltmarsh and other littoral types).

## Classification Details
- 23 LCM2007 classes derived from Ground Reference and spectral signatures; some Broad Habitats further subdivided due to spectral separability.
- Classes and their relationships documented in Appendix 2; colour mappings provided in Appendix 3.
- KBE (Knowledge-Based Enhancements) applied to polygons; ProbList shows top spectral matches.
- Sub-class indicators (BHSub) included but lower confidence; recommended validation if used for sub-class analysis.

## Validation and Accuracy
- Ground reference data employed to validate LCM2007 at the 23-class thematic resolution.
- Average accuracy reported around 83% across validation polygons; individual polygon accuracy may vary.
- Change detection across LCM versions is not straightforward due to class and spatial structure differences and typical image classification error around 20%.

## Access, Formats, and Size
- Access:
  - 1 km raster products available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (licence fees may apply).
- File sizes (guidance):
  - Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: ranges from ~21 MB to ~49 KB for GB products.
- Projections:
  - GB: British National Grid; NI: Irish National Grid (with NI transitioning toward ITM in future tooling).

## Data Access and Usage Considerations
- Data access via CEH gateways and licensing; consult the Final Report for comprehensive methodology and limitations (Morton et al., 2011).
- Vector attributes provide a robust audit trail (source imagery, construction method, KBE history) suitable for reproducibility and QA.
- Broad Habitat subclass data and FieldCode are included for advanced users but require local validation before fine-scale interpretation.

## Appendices (Key Details)
- Appendix 1: LCM2007 23 class descriptions linked to Broad Habitats.
- Appendix 2: Relationship between LCM2007 classes, Broad Habitats, and Broad Habitat subclasses (BHSub).
- Appendix 3: Standard LCM2007 color mapping for visualization.
- Appendix 4: Updates to products (Version 1.2, May 2014) including added tiles and water class inclusion.

## Version History and Updates
- Version 1.0: Original (July 2011).
- Version 1.2: Updated May 2012 for dataset updates and change detection notes.
- Version 1.2 (May 2014): Further updates:
  - GB vector and 25 m rasters updated to include OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer).
  - GB 1 km products updated for Fair Isle and Stranraer; NI products updated similarly.
  - Water class added to 1 km dominant/percentage classes.

## Acknowledgements
- Datasets sourced from Landsat-TM5, SPOT-4/5, AWIFS, and cartographic data from Ordnance Survey and others.
- Produced by CEH with the Countryside Survey Partnership; data use is subject to copyright notices and licensing.

## Practical Takeaways for Analysts Monitoring the Environment
- LCM2007 provides a standardized, machine-readable, 23-class land cover map suitable for long-term environmental monitoring and policy performance assessment.
- The vector product offers rich metadata and a detailed provenance trail, enabling reproducibility and QA checks.
- Use 1 km rasters for large-scale national analyses and 25 m rasters or vectors for fine-grained mapping and validation, keeping in mind file size and processing considerations.
- Be cautious with change detection across LCM generations; validate cross-version changes with ground truth or stable baselines.
- Leverage Appendix 2–3 for class interpretation and color-coding in maps; apply local validation for Broad Habitat subclasses if high detail is required.