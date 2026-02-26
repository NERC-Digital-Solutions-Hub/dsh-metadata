# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification with 23 classes, based on UK Broad Habitats.
- Data are provided in vector and raster formats at multiple resolutions to support diverse GIS applications.

## Overview and purpose
- Purpose: support diverse GIS needs with map-based data products; intended for policy colleagues, clients, and the public.
- LCM2007 maps land cover (not strictly land use) from summer-winter satellite composites with 20–30 m pixels.
- Replaces LCM2000 using a spatial framework built on OS MasterMap and relevant vector data for improved GIS compatibility.
- Not designed for direct change detection; cross-era changes are difficult due to class/spatial differences and typical image classification error (~20%).

## Data structure and content

- Vector data set
  - 8.6 million polygons (GB) and 0.9 million (NI).
  - Each polygon has 10 attributes (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class for display/QA), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID for each parcel; parcel-level provenance and processing history retained.
  - 23 LCM2007 classes mapped to Broad Habitats; some Broad Habitats subdivided (e.g., Urban/Suburban, Heather/Heather grassland).
- Raster data sets
  - 25 m and 1 km products derived from the vector data.
  - 25 m raster: 23 LCM2007 classes (GB and NI separately projected); 8-bit unsigned, 25 m pixels.
  - 1 km raster: aggregates for dominant class and percentage cover (both for LCM2007 classes and aggregates).
  - Metadata includes grid dimensions, extents, projections, pixel size, and data type; GB and NI have separate projections (GB: British National Grid; NI: Irish National Grid).

## Classifications and interpretation

- 23 LCM2007 classes tied to Broad Habitats (Appendix 1); some Broad Habitats subdivided for more detail.
- 1 km rasters provide:
  - Dominant cover at 1 km (for both 23 classes and aggregate classes).
  - Percentage cover at 1 km for both 23 classes and aggregates.
- Appendix 2 provides the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3 provides standard color mapping for LCM2007 classes (also available as an ArcGIS .lyr file).

## Data quality, validation, and limitations

- Validation: ground-reference polygons (9127) yield an average thematic accuracy of ~83% for the 23 classes; local discrepancies may occur.
- QA: rich metadata per polygon; Knowledge-Based Enhancements (KBE) applied during polygon construction; ProbList shows top spectral-class matches.
- Change mapping is not well suited due to:
  - Different class definitions across years (LCM1990/2000/2007).
  - Differing spatial structures and typical classification errors (~20%).
- LCM2007 is a land-cover product, not a direct map of land-use; some land-use inferences may be ambiguous from spectral data alone.
- Minimum mappable area: >0.5 ha; parcels <0.5 ha and lines <20 m dissolved into surrounding landscape.

## Projections, data formats, and file sizes

- Projections
  - GB vector and 25 m raster use British National Grid (OSGB36) Transverse Mercator.
  - NI vector and 25 m raster use Irish National Grid; NI is transitioning toward ITM (EPSG ITM) in some tools.
- File sizes (typical guidance)
  - Vector GB: ~4.13 GB; NI: ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km raster: GB products range from ~21 MB to ~49 KB (depending on product).
- Data access
  - 1 km 1 km raster products available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence (data access may involve fees).
  - Contact CEH or apply via www.ceh.ac.uk/data.

## Usage guidance for GIS specialists

- Data selection and use
  - Choose vector vs raster based on project needs: vector offers rich per-polygon metadata; raster is lighter and easier for large-area modeling.
  - For nationwide modeling, 1 km raster aggregates are suitable; for detailed mapping, use 25 m raster or vector with full attributes.
- Data integrity and workflow considerations
  - Retain Parcel_ID for unambiguous communication and traceability.
  - Use BHSub and FieldCode only with validation; INTCODE is recommended for display.
  - Consider applying your own validation when using Broad Habitat sub-classes due to potential accuracy differences.
- Application notes
  - Be aware of substantial data sizes; plan storage and processing accordingly.
  - When integrating with other datasets, ensure consistent projection and alignment; NI data may require reprojection if ITM is used.
  - For change detection purposes, preferentially use compatible, year-to-year datasets or perform robust cross-walking between classes.

## Additional information and resources

- Appendix 4: Updates (Version 1.2, May 2014) including new tiles (Fair Isle, Stranraer) and introduction of water class in 1 km products.
- References
  - Morton et al. 2011 Final Report for LCM2007.
  - Jackson 2000 guidance on Broad Habitat interpretation.
- Acknowledgements: data sources from Landsat, SPOT, AWIFS, OS datasets, soils and land-use data partners; CEH and Countryside Survey collaboration.

## Document lineage and acknowledgments

- Documentation version: Version 1.2 (May 2014); originally released July 2011 with updates in 2012 and 2014.
- Acknowledges data providers and licensing constraints; CEH distributes and licenses data under specified arrangements.

## Summary of end-to-end relevance

- LCM2007 provides a robust, multi-format UK land-cover data product suite suitable for GIS visualization and analysis, with rich per-polygon metadata and multiple raster aggregation levels.
- It is well-suited for map-based data products and GIS-driven explorations, provided users heed limitations around change detection, subs-class accuracy, and data volume requirements.