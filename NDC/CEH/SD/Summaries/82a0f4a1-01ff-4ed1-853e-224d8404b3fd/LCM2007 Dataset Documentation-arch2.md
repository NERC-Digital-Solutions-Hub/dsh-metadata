# Land Cover Map 2007 Dataset documentation

- The Land Cover Map 2007 (LCM2007) provides a parcel-based UK land cover classification in 23 classes, aligned to UK Biodiversity Action Plan Broad Habitats, using 20–30 m satellite imagery. It updates LCM2000 with a framework based on OS MasterMap/large-scale vector data and image segmentation to improve GIS compatibility.
- Purpose: to support diverse user requirements with data products described here, while noting the Final Report for a more comprehensive assessment (Morton et al., 2011).

## Key concepts and data integrity

- LCM2007 maps land cover (not strictly land use); minimum mapped unit is >0.5 ha; parcels <0.5 ha or lines <20 m are dissolved into surrounding landscape.
- 23 LCM2007 classes are based on Broad Habitats; some are subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral Sediment and Saltmarsh).
- Each parcel (polygon) has a unique Parcel_ID for unambiguous communication and rich metadata capturing processing history, original spectral classification, and knowledge-based enhancements (KBE).
- Broad Habitat sub-classes (BHSub) and FieldCode provide additional descriptive detail, but BHSub and FieldCode are not part of the QA for final classification accuracy; users should validate if using these details.
- LCM2007 has a high-quality metadata framework with attributes such as INTCODE (display code 1–23), KBE, ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct method (e.g., OSMM-based segmentation).
- Validation against ground reference data used 9,127 polygons, yielding an average thematic accuracy of 83% (subject to local variation).

## Data products and formats

- Vector Data Set
  - ~10 million polygons across Great Britain (GB) and Northern Ireland (NI) with 10 attributes per polygon (Table 1 in the document).
  - Core attributes include Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
  - 8.6 million polygons in GB; 0.9 million in NI.
- Raster Data Sets
  - 25 m raster derived from the vector data (23 LCM2007 classes; linked to Table 2 for class values) and 1 km raster products derived by summarizing 25 m data.
  - Great Britain and Northern Ireland provided in separate projections (GB: British National Grid; NI: Irish National Grid). 1 km rasters include dominant class and percentage cover for both LCM2007 classes and Aggregate classes.
- Spatial coverage and resolution
  - Two main raster resolutions: 25 m and 1 km.
  - GB and NI datasets exist separately due to different projections; NI transitioning to ITM.
- Data sizes
  - Vector (Shapefile, 100 km x 100 km): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on product type).

## Class structure and mapping

- 23 LCM2007 classes are anchored to Broad Habitats; some Broad Habitats are further subdivided into sub-classes to reflect spectral differentiation.
- Appendix 1 summarizes each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, etc.).
- Appendix 2 details the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) used during classification.
- Appendix 3 provides the standard LCM2007 colour mapping used in the Final Report (Morton et al., 2011) for display purposes.

## Access, distribution, and licensing

- 1 km raster data sets are openly available via the CEH Information Gateway.
- The full vector product and the 25 m raster product are available under licence on request from CEH (licences may apply; online application or contact details provided).
- Data can be re-projected to common GIS formats, with the note that some NI data may require ITM projection in the future.

## Map projection and technical notes

- GB data use British National Grid (OSGB36); NI data use Irish National Grid (and moving toward ITM for NI).
- The documentation highlights that 0.5 ha MMU and pixel-level accuracy imply that some small patches may be underrepresented; accuracy and class separability vary by habitat type.
- LCM2007 is designed to be used at the thematic resolution of the 23 classes (highest recommended thematic resolution); Broad Habitat sub-classes are provided mainly for ProbList context and require local validation if used for analysis.

## Practical considerations for analysts

- LCM2007 supports monitoring and policy evaluation through standardized datasets with robust metadata and QA, enabling consistent time-series analysis when combined with other data sources.
- The vector dataset offers rich attribute data for detailed analyses, but file sizes are large; 25 m rasters are more manageable for broad-scale analysis, while 1 km rasters suit regional or national modeling.
- The product emphasizes data provenance (Parcel_ID, original image source, KBE history) to support reproducibility.
- Users should validate Broad Habitat subclasses and be aware that grassland classifications (Neutral, Calcareous, Acid) can be misclassified as Improved Grassland in some cases; regional and project-specific validation is advised.

## References and further information

- Morton, D. et al. 2011. Final Report for LCM2007 - the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. 2000. Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).