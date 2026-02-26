# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide parcel-based land cover classification using 23 classes aligned to UK Biodiversity Action Plan Broad Habitats.
- Data derived from 20–30 m satellite imagery (summer-winter composites).
- Distinguishes land cover (not strictly land use); minimum mappable area >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.
- Data products include vector (polygons with attributes) and raster (25 m and 1 km) formats, covering Great Britain and Northern Ireland separately.

## Production and Interpretation
- Based on generalised OS Master Map/topographic layers and image segments; polygons reflect real-world objects (fields, woodland blocks).
- Rich metadata retained for polygons; 10 attributes per polygon, including processing history and knowledge-based enhancements (KBE).
- Ground reference validation: 9,127 polygons; average thematic accuracy around 83% with local variation.

## Product Specification and Overview
- LCM2007 maps land cover (not land use) using 23 classes; some Broad Habitats subdivided into finer classes (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Thematic resolution is highest at 23 classes; validated QA applies to LCM2007 classes.

## Data Sets

### Vector Data Set
- 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
- 10 attributes per polygon (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class number 1–23), KBE, ProbList (top 5 spectral classes with probabilities), CorePixels, Construct, TotPixels.
- Unique Parcel_ID retained for unambiguous communication; BHSub provides descriptive sub-class information; ProbList informs spectral class likelihood and may require user validation for sub-classes.

### Raster Data Sets
- 25 m raster: 23 LCM2007 classes; GB and NI in separate projections; data size large; pixel values correspond to LCM2007 class numbers.
- 1 km raster: derived from 25 m raster; provides dominant and percentage cover for LCM2007 classes and Aggregate classes (for UK-wide applications).
- Metadata in Tables 3 and related figures describe extents, grid, and data types.

## Map Projections and File Size
- GB vector/raster: British National Grid (OSGB 1936).
- NI vector/raster: Irish National Grid; NI moving toward Ireland Transverse Mercator (ITM) projection.
- File sizes (guidance):
  - Vector in 100 km x 100 km shapefile: GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on product).
- Data access may involve licensing and fees for some users/applications.

## Access and Use
- 1 km raster data: available via CEH Information Gateway.
- Full vector and 25 m raster products: available on request under licence from CEH; online application or contact spatialdata@ceh.ac.uk.
- Users are advised to read production methodology, metadata, and limitations (Final Report Morton et al., 2011) prior to use.

## Appendix and Color Mapping
- Appendix 1: LCM2007 Classes – detailed descriptions and examples of each of the 23 classes, including nuances and potential confusions (e.g., grassland subtypes, bog vs. heath, montane distinctions).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) for LCM2007.
- Appendix 3: Colour mapping recipe (LCM2007 class number to RGB values) used in the Final Report (Morton et al., 2011).

## Data Quality, Validation, and Limitations
- Validation against ground reference data performed; average accuracy ~83% with site-level variability.
- The classification is robust at 23-class resolution; sub-class (BHSub) information exists but may require additional validation due to differing accuracy.
- Important caveats:
  - LCM2007 maps land cover, not always directly inferring land use.
  - Some Broad Habitat sub-classes may be produced for informational purposes but are not QA-validated at that level.
  - MMU and spectral similarity can complicate separation of certain classes (e.g., Neutral/Calcareous vs Improved Grassland).

## Further Information and References
- Core reference: Morton et al. 2011, Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
- Broad Habitat framework reference: Jackson 2000 (JNCC Report 307) for interpretation of the Broad Habitat Classification.
- Acknowledgements include satellite imagery sources (Landsat, SPOT, AWIFS) and cartographic data providers (Ordnance Survey, LPS, SSKIB, soils data, etc.).

## Summary for Analysts
- LCM2007 provides a high-resolution, XML-like rich vector dataset and complementary raster products (25 m and 1 km) mapping 23 land cover classes tied to Broad Habitats, with detailed per-polygon metadata and QA-backed class definitions.
- Suitable for regional to national-scale analyses requiring land cover patterns, with explicit caveats about scale, MMU, and potential sub-class validation needs.
- Access options allow both full-resolution vector data (licensed) and readily accessible 1 km rasters (open via CEH gateway) for modeling, trend analysis, and impact assessment.
- For detailed methodological considerations and validation results, consult Morton et al. 2011 Final Report and Jackson 2000 Appendix materials.