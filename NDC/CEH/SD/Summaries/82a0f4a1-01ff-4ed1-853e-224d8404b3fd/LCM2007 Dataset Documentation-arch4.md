# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose: Documentation for Land Cover Map 2007 (LCM2007) data products, describing production methodology, data products, metadata, limitations, and access. Recommends consulting the Final Report for comprehensive assessment (Morton et al., 2011).

## Key context and purpose of LCM2007

- Parcel-based classification of the UK across 23 land cover classes derived from UK Biodiversity Action Plan Broad Habitats.
- Uses 20–30 m satellite imagery; built upon refined OSMM/landscape vector frameworks and image segmentation.
- Maps land cover (not strictly land use); minimum mappable unit >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m dissolved into surrounding landscape.
- Designed to support interoperability with GIS datasets; offers rich metadata and a communication framework via unique parcel identifiers (Parcel_ID).

## Data products and thematic resolution

- Vector data set (GB and Northern Ireland):
  - ~8.6 million polygons in GB and ~0.9 million in NI.
  - 10 attributes per polygon (including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode descriptions; INTCODE is the recommended display class (1–23).
  - Knowledge-based enhancements (KBE) recorded; ProbList provides the top 5 spectral matches.
  - Unique Parcel_ID enables unambiguous cross-communication; advised to retain this field.
- Raster data sets:
  - 25 m and 1 km resolutions; GB and NI datasets provided separately due to different projections.
  - 25 m rasters map the 23 LCM2007 classes; 1 km rasters provide aggregated outputs (dominant and percentage cover for classes and aggregates).
  - 1 km products facilitate UK-wide modelling; 25 m and 1 km rasters can be combined with other data (e.g., meteorology, species distributions).

## Class structure and mapping

- 23 LCM2007 classes based on Broad Habitats; some Broad Habitats are subdivided into sub-classes (e.g., Built-up Areas; Dwarf Shrub Heath; Littoral Sediment).
- Appendix 1 (LCM2007 classes) provides brief definitions for each class; Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mapping for display.
- LCM2007 is validated at the 23-class thematic level; Broad Habitat sub-classes are included primarily for ProbList context and should be validated by users before analysis at that level.

## Data quality, limitations, and guidance

- Validation: ground reference data used to assess performance; average accuracy ~83% across 9127 polygons; regional discrepancies may occur.
- Sub-class and grassland distinctions (e.g., Neutral/Calcareous/Acid Grasslands) are challenging and may misclassify; users requiring these sub-classes should consult Morton et al. 2011 sections 3.9 and 4.
- Broad Habitat sub-classes are not guaranteed to have QA-level accuracy equivalent to the main LCM2007 classes; validation is recommended if using sub-classes.
- LCM2007 maps land cover (spectral signatures) rather than strictly land use; interpretation should consider context and potential ambiguity (e.g., arable cover vs. land use).

## Metadata, data provenance, and processing history

- Vector polygons include:
  - Source images, processing details, KBE history, and a probability list for top spectral matches.
  - CorePixels and TotPixels indicating pixel counting for classification.
  - Construct methods: OSMM-derived, OSMM:SEG, or OSMM:AGC:SEG.
- Rich metadata accompany polygon attributes; KBE codes document processing changes and corrections (e.g., soil corrections, altitude corrections, coastal masks, urban masks).

## Map projection, coordinate systems, and data sizing

- Projections:
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (moving toward ITM in NI; reprojectable with modern GIS).
- Raster metadata (Table 3 details):
  - Great Britain: 25 m and 1 km rasters; 25 m uses British National Grid; 1 km uses same grid with 1,000 m pixel size.
  - Northern Ireland: 25 m and 1 km rasters; correspond to Irish National Grid.
- File sizes (typical guidance; formats affect size):
  - Vector shapefile (100 km x 100 km): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 23-class products range from ~21 MB to ~49 KB.
- Data access formats:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (online application or direct contact).

## Access, licensing, and further information

- Data access:
  - CEH Information Gateway for 1 km rasters.
  - Full vector and 25 m raster available on request; licensing may apply.
- References:
  - Morton et al. 2011, Final Report for LCM2007.
  - Jackson 2000, Guidance on the Biodiversity Broad Habitat Classification.
- Acknowledgments for data sources (Landsat, SPOT, AWIFS, OS mapping, soils, etc.) and copyright notices.

## Practical notes for data leaders

- Consider using the 23-class LCM2007 vector or 25 m raster for detailed analyses; use 1 km rasters for UK-wide aggregations.
- Retain Parcel_ID for clear communication and traceability across datasets.
- Prior to applying sub-class analyses, perform local validation due to potential QA limitations at the sub-class level.
- When integrating with other data, be mindful of the different projections (GB vs NI) and coordinate systems; ensure reprojection is handled consistently.
- Leverage the extensive metadata and KBE/ProbList information to understand classification history and uncertainty.