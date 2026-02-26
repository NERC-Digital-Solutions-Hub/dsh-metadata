# Land Cover Map 2007 Dataset Documentation

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land-cover classification using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Sentinel imagery: 20–30 m pixels; built from summer-winter composites; vector polygons with OS MasterMap-derived framework; maps land cover (not always land use); minimum mapped unit is >0.5 ha.
- Provides a range of data products to support diverse users; recommended consulting Morton et al. 2011 Final Report for full methodology and limitations.

## Data Products and Coverage

- Data formats: vector (polygons with attributes) and raster (25 m and 1 km) for Great Britain and Northern Ireland (NI).
- 23 LCM2007 classes; some Broad Habitats subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- 1 km rasters summarize 25 m data by dominant class and percentage cover; 25 m rasters retain full 23-class detail.
- Vector product contains ~8.6 million GB polygons and ~0.9 million NI polygons; 10 attributes per polygon.

## Classes and Classification

- 23 LCM2007 classes based on Broad Habitats (Appendix 1 in the document).
- Some Broad Habitats can be further divided by spectral signatures for sub-classes (e.g., built-up, heather vs. heather grassland).
- Parcel labeling: each polygon has a unique Parcel_ID for traceability.
- Broad Habitat sub-classes (BHSub) and FieldCode provide additional, but not QA-validated, detail; ProbList shows top 5 spectral class probabilities for each polygon.
- Minimum mapping unit and exteriorization rules apply during production (parcels <0.5 ha or lines <20 m dissolved).

## Data Structure and Metadata

- Vector data attributes (Table 1): Parcel_ID, BH, BHSub, FieldCode, INTCODE (for display), KBE (processing history), ProbList (top 5 spectral classes), CorePixels, Construct, TotPixels.
- BHSub provides sub-class descriptions; FieldCode offers short codes used in construction but with caution advised for accuracy.
- 10 attributes per polygon; BHSub and FieldCode help convey additional classification details.
- Rich metadata accompany polygons, including data sources, processing steps, and Knowledge-Based Enhancements (KBE).

## Validation and Accuracy

- Ground reference validation: 9,127 polygons assessed; average accuracy ~83%.
- Figures reflect average accuracy; expect local discrepancies; caution advised when interpreting individual polygons.

## Map Projection and Georeferencing

- Great Britain: British National Grid (OSGB36); Northern Ireland: Irish National Grid.
- NI transitioning to Ireland Transverse Mercator (ITM); re-projection supported by GIS packages.

## Raster Data Details and File Sizes

- 25 m raster: 23 LCM2007 classes; provides 25 m pixel values mapped to classes.
- 1 km raster: derived from 25 m data; provides dominant cover and percentage cover for both 23 classes and aggregated classes.
- File size (typical guidance, varies by format):
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB range depending on product.

## Data Access and Licensing

- 1 km raster data available via CEH Information Gateway.
- Full vector product and 25 m raster product available on license, by request from CEH.
- Access process: online application at CEH data site or contact spatialdata@ceh.ac.uk; licence fees may apply.

## Practical Guidance for Analysts

- Choose the level of thematic resolution appropriate to your application:
  - Use 23-class LCM2007 for detailed habitat analysis.
  - Use 1 km rasters for broad national patterns or to integrate with other nationwide datasets.
- For vector data, retain Parcel_ID to enable unambiguous communication and traceability; BHSub and FieldCode can be used with validation.
- Exercise caution with Broad Habitat sub-classes; they are not QA-proven at the same level as LCM2007 classes.
- When working with grassland classes (Neutral, Calcareous, Acid), consult Morton et al. 2011 for guidance on potential mis-classifications and aggregation options.
- Validate Broad Habitat subclass interpretations with local knowledge or ground truth if high-precision subclass mapping is required.
- Be mindful of the MMU: patches smaller than 0.5 ha or lines under 20 m are dissolved, potentially underrepresenting small features.

## Appendices and Colour Mapping

- Appendix 1: LCM2007 Classes — detailed brief reviews for each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Grassland types, Wetlands, Coastal and Littoral classes, Built-up areas, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping table and examples).
- Appendix 3: Colour mapping recipe for LCM2007 classes (used in the Final Report) to aid visualization.

## Further Information

- Morton et al. 2011: Final Report for LCM2007 – the new UK Land Cover Map ( Countryside Survey Technical Report No. 11/07).
- Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).
- Data provenance and acknowledgments detail satellite imagery sources, cartographic data, boundaries, and collaborators.
- For more information on Countryside Survey and LCM2007, visit the provided project and data portals.