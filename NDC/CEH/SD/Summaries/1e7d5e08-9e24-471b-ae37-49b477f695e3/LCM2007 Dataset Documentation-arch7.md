# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes derived from Broad Habitats, produced from summer-winter satellite composites at 20–30 m resolution.
- It maps land cover (not strictly land use) and uses a 0.5 ha minimum mappable area; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved.

## Data products and structure

- Provides a range of data products (vector and raster) to support diverse GIS needs.
- Vector data set: polygons with attached attributes, suitable for rich metadata but larger file sizes.
- Raster data sets: 25 m and 1 km products derived from the vector data; GB and Northern Ireland (NI) delivered separately due to different projections.
- 1 km rasters offer aggregated outputs (dominant class and percentage cover) suitable for national-scale analyses.

## Vector data set (LCM2007 Vector)

- Contains 8.6 million polygons for Great Britain (GB) and 0.9 million for Northern Ireland (NI).
- Each polygon includes 10 attributes (Table 1) and a unique Parcel_ID (includes source image info).
- Key attributes:
  - BH: Dominant Broad Habitat class (e.g., Coniferous Woodland, Arable and Horticulture)
  - BHSub: Broad Habitat sub-class (text description of FieldCode)
  - FieldCode: short field-code string (use with caution; not QA-validated)
  - INTCODE: recommended display class (1–23)
  - KBE: Knowledge-Based Enhancement history
  - ProbList: top 5 spectral class probabilities
  - CorePixels, TotPixels: pixel counts used in classification
  - Construct: data source/or segmentation history (e.g., OSMM-based)
- Sub-classes of Broad Habitats (BHSub) provide additional detail but are not as rigorously QA-validated as LCM2007 classes; validation recommended if sub-class level is used.

## Raster data sets

- 25 m raster: 23 LCM2007 classes; GB and NI provided separately.
- 1 km raster: derived by summarising 25 m data to percentage cover and identifying the dominant class per 1 km pixel.
- Aggregate classes: 1 km rasters use merged (aggregated) classes for applications requiring coarser resolution.

## Class mapping and detail (Appendices)

- Appendix 1: LCM2007 classes described (based on UK Broad Habitats), including nuanced distinctions within Broad Habitats (e.g., Suburban vs Urban; Heather vs Heather grassland; Littoral/Coastal distinctions).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (field-code mappings and class numbers).
- Appendix 3: Colour mapping for standard LCM2007 visualization (RGB values per LCM2007 class).
- Note: The 23 LCM2007 classes correspond to Broad Habitat groupings; some BHSub classes aid interpretation but are not part of the core QA.

## Data access, licensing, and formats

- Access to 1 km raster data: CEH Information Gateway.
- Full vector product and 25 m raster product: available under licence on request from CEH (online application or data@ceh.ac.uk). Licences may apply.
- Projection:
  - GB: British National Grid (OSGB 1936)
  - NI: Irish National Grid (transitioning to ITM in NI; reproject if needed)
- File sizes (approximate guidance):
  - Vector in 100 km x 100 km shapefile: GB ~ 4.13 GB; NI ~ 0.43 GB
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB
  - Raster 1 km: 23-class percentages from ~21 MB to ~49 KB

## Data quality, validation, and limitations

- Validation: ground-reference data yielded an average accuracy of ~83% across 9,127 polygons; local variances may occur.
- LCM2007 is validated at the 23-class thematic resolution (highest recommended resolution for use).
- Some sub-class level detail (BHSub, FieldCode) should be used with caution and validated independently.
- MMU and spectral classification challenges evident in several Broad Habitats (e.g., Fen, Marsh and Swamp; Montane; various grassland types).

## Practical considerations for GIS Specialists

- Choose data product by need:
  - Vector: best for rich attribute analysis, detailed geometries, and metadata per polygon; large file sizes.
  - 25 m raster: good for processing when vector metadata is not required; easier to handle in some workflows.
  - 1 km raster: suitable for national-scale modeling, aggregation with other datasets; lower spatial detail.
- Use Parcel_ID for unambiguous cross-communication between users; retain it in analyses.
- When using Broad Habitat sub-classes, apply your own validation due to QA limitations at subclass level.
- Leverage the knowledge-based enhancements (KBE) history to understand polygon modifications.
- For map styling and visualization, Appendix 3 provides the standard colour mapping per LCM2007 class.
- Consider aggregating to 1 km for certain applications or when integrating with other coarse-resolution datasets (e.g., climate, species distributions).

## Additional information and references

- Final Report for LCM2007 (Morton et al., 2011) for comprehensive methodology and assessment.
- Guidance on Brnh Habitat classifications (JNCC Jackson, 2000) for interpreting Broad Habitats.
- Countryside Survey contributions and related technical reports.

## End notes

- LCM2007 represents a substantial upgrade over LCM2000 with a GIS-friendly, object-based parcel framework designed for compatibility with other GIS data and observed real-world features.
- The dataset emphasizes transparency (rich metadata, QA documentation) and warns about potential misclassifications at the Broad Habitat sub-class level, advising user-driven validation for analyses at that granularity.