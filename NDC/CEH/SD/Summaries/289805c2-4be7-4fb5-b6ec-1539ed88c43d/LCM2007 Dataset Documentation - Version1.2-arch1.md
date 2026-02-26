# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a UK parcel-based land-cover classification using 23 Broad Habitat-based classes, derived from summer-winter satellite composites at 20–30 m pixels.
- Built to support a range of GIS applications with multiple data products (vector and raster) and rich metadata.

## Scope and Product Overview

- LCM2007 maps land cover (not land use) and uses 23 classes linked to UK Broad Habitats; some classes are further subdivided for spectral reasons.
- Minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved into surrounding areas.
- Produced as multiple data formats and resolutions to suit diverse applications (vector, 25 m raster, 1 km raster).
- Change mapping across LCMs (1990/2000/2007) is not straightforward due to class/spatial differences and typical classification error (~20%).

## Data Sets and Class Structure

- Vector data set: ~8.6 million GB polygons and ~0.9 million NI polygons; 10 attributes per polygon (including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- 23 LCM2007 classes, based on Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Broad Habitat Sub-classes (BHSub) provide additional descriptive detail but are not QA-validated to the same standard as LCM2007 classes; recommended validation if used at subclass level.
- Raster data: derived 25 m raster and 1 km aggregated rasters (GB and NI separated due to different projections). 1 km rasters provide dominant class and percentage cover; 25 m rasters provide full 23-class detail.
- Aggregate classes for 1 km rasters merge LCM2007 classes to support broader-scale analyses.

## Data Access and Licensing

- 1 km raster data (GB and NI) available via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under license from CEH; licensing may apply.
- Contact: spatialdata@ceh.ac.uk or CEH data portal for application details.

## Product Details and Technical Specs

- Vector data product:
  - 10 attributes per polygon; Parcel_ID includes source image identifier.
  - BH: Broad Habitat level; BHSub: Broad Habitat sub-class; FieldCode: short sub-class identifiers (for potential validation use only).
  - INTCODE: class code for display (1–23) and QA validation.
  - KBE: knowledge-based enhancements history; ProbList: top 5 spectral class probabilities.
  - Construct: history of polygon construction (OSMM-derived segmentation, etc.).
  - CorePixels / TotPixels: pixel counts related to segment.
- 25 m raster product:
  - 23 LCM2007 classes; GB and NI have separate grids; 25 m resolution with Unsigned 8-bit data.
- 1 km raster products:
  - Dominant target class, dominant aggregate class, percentage cover per class, and percentage cover per aggregate class.
  - Metadata includes grid dimensions, extents, pixel sizes, projections, data types, and coordinate systems (GB: OSGB36/British National Grid; NI: Ireland grid/ITM transition in progress).

## Map Projections and Data Size

- GB vector: British National Grid; NI vector: Irish National Grid.
- GB 25 m raster: OSGB 1936; NI 25 m raster: Ireland 1965.
- Vector data size: GB ~4.13 GB; NI ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- 1 km raster products: GB ~21 MB to ~49 KB (varies by product); NI similar small footprint.
- Data size emphasizes the large scale of the vector product due to detailed polygon attributes.

## Validation, Accuracy, and Limitations

- Ground reference validation against 9,127 polygons yielded average thematic accuracy around 83%, with acknowledged local variations.
- Change detection between LCM generations is challenging due to class/spatial differences and typical image classification error rates.
- Broad Habitat sub-classes and field codes require independent validation for use at finer subclass levels.

## Data Quality, Provenance, and Metadata

- Final report for LCM2007 (Morton et al., 2011) recommended for comprehensive methodology, metadata, and limitations.
- Rich metadata accompanying vector polygons includes processing steps, KBE history, and top spectral class probabilities; supports traceability and reproducibility.
- Appendix materials provide detailed mappings:
  - Appendix 1: LCM2007 classes (definitions and brief reviews).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and BH-subclasses.
  - Appendix 3: LCM2007 colour mapping for visualization.
  - Appendix 4: Update log for Version 1.2 (May 2014) including new OS tiles and water class updates.

## Appendices and Updates

- Appendix 1–3: Detailed class descriptions, mappings, and color schemes for standard visualization and interpretation.
- Appendix 4: Version 1.2 (May 2014) updates:
  - Vector GB updated for OS Tile HZ (Fair Isle); 25 m raster GB updated for HZ and NW Stranraer.
  - 1 km products updated similarly; water class added to some 1 km products for GB.
  - NI products updated to include water class where applicable.

## Guidance for Analysts

- Use LCM2007 as a high-resolution, parcel-based land-cover reference aligned with Broad Habitats; leverage vector attributes for detailed analyses and KBEs, or use 25 m / 1 km rasters for scalable modeling.
- Be mindful of the MMU, dissolution of small features, and the distinction between land cover and land use.
- Validate Broad Habitat sub-classes if used beyond the main 23 LCM2007 classes.
- Consult the Final Report (Morton et al., 2011) for methodological context, QA, and limitations to ensure appropriate interpretation and application.
- For large-scale modeling, 1 km rasters offer efficient aggregated data; for detailed discovery and communication, the vector product provides the most comprehensive information.