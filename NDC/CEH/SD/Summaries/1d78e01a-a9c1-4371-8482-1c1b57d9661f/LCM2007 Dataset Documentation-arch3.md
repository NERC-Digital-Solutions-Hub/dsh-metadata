# LAND COVER MAP 2007 DATASET DOCUMENTATION

- The Land Cover Map 2007 (LCM2007) dataset provides a parcel-based UK land cover classification to support environmental monitoring, policy scrutiny, and future decision-making. It builds on LCM2000 with a refined, object-based framework and a 23-class taxonomy aligned with UK Broad Habitats.

## Key features and scope

- Outputs include vector (parcel-based polygons) and raster products (25 m and 1 km resolutions).
- 23 LCM2007 classes are based on UK Broad Habitats; some Broad Habitat groups are subdivided (e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral sediment vs Saltmarsh).
- LCM2007 maps land cover (not land use) using summer-winter satellite composites at 20–30 m.
- Minimum mappable unit is >0.5 ha; parcels <0.5 ha or lines <20 m are dissolved into the surrounding landscape.
- The dataset is validated at the 23-class level with an average accuracy of ~83% against ground reference data.

## Data products and structure

- Vector data set: ~8.6 million polygons (GB) and ~0.9 million (NI); 10 polygon attributes per record, including:
  - Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class number for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
- Raster data sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI differ in projection; data types are unsigned 8-bit.
  - 1 km raster: derived by summarising 25 m data to dominant and percentage cover for both 23 LCM2007 classes and 9 Aggregate classes.
- Data provenance and construct: the Polygon_ID links to source images and processing steps; KBE records document knowledge-based enhancements applied during classification.

## Class relationships and metadata

- Appendix 1 provides LCM2007 class definitions; Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 outlines the color mapping used for visuals.
- Broad Habitat sub-classes (BHSub) add descriptive detail but are not part of the QA for the 23-class final product; users should validate sub-classes if used for analysis.
- The 1 km raster products are designed for UK-scale modelling and aggregation, while the 25 m/vector products support finer-scale analysis.

## Validation, accuracy, and caveats

- Ground reference validation involved 9,127 polygons, yielding an average accuracy of 83%, with local discrepancies expected.
- LCM2007 maps land cover and not always land use; interpreting classes requires careful consideration of spectral ambiguity (e.g., grassland types and arable vs pasture).
- Grassland classifications such as Neutral and Calcareous Grassland may be mis-classified as Improved Grassland in some cases; users should consult Morton et al. 2011 for detailed accuracy notes and potential aggregation options.

## Data access, formats, and licensing

- Data access:
  - 1 km raster products are publicly available via the CEH Information Gateway.
  - Full vector and 25 m raster products are available on request under licence; fees may apply.
- File sizes (typical):
  - Vector (100 km x 100 km, GB shapefile): ~4.13 GB; NI ~0.43 GB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on product).
- Projections and coordinate systems:
  - GB data: British National Grid (OSGB 1936) with Transverse Mercator projection.
  - NI data: Irish National Grid (moving toward ITM).
- Parcel_ID retention is recommended to maintain unambiguous communication about features and provenance.

## Usage guidance for monitoring frameworks

- Purpose and limitations:
  - Use LCM2007 to monitor land cover dynamics, assess policy outcomes, and inform land management decisions.
  - Distinguish clearly between land cover (LCM2007) and land use; avoid over-interpreting spectral classes as exact land use.
- Data governance and quality:
  - Rich metadata and a detailed processing history (KBE) support transparency and reproducibility.
  - The 23-class product is QA-validated; BHSub-level details require independent validation if used for decision-making.
- Practical recommendations:
  - For national-scale modelling or trend analysis, 1 km raster products are efficient; for detailed site-level assessments, use the 25 m vector or raster data with attention to metadata and classification uncertainties.
  - Consult Morton et al. 2011 Final Report for comprehensive methodology, accuracy assessments, and usage guidance.

## Appendices (high-level)

- Appendix 1: LCM2007 Classes – definitions and description for each of the 23 classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) with mapping examples.
- Appendix 3: Standard colour mapping (RGB codes) for visualization of LCM2007 classes.

## Further information and references

- Primary reference: Morton, D. et al. 2011. Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Related classification framework: Jackson, D.L. 2000. Guidance on Broad Habitat Classification (JNCC Report 307).
- Data sources include Landsat, SPOT, AWIFS, OS MasterMap, and various cartographic datasets; CEH administers access and licensing.