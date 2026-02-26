# Land Cover Map 2007 Dataset documentation

## Overview
- UK parcel-based land cover dataset using 23 Broad Habitat–based classes.
- Provides vector and raster data products (25 m and 1 km resolutions) to support diverse GIS applications.
- Maps land cover (not land use) with a minimum mappable unit of 0.5 ha (parcels smaller than 0.5 ha or linear features < 20 m dissolved).
- Updates LCM2000; uses a refined spatial framework based on generalised OS MasterMap/LCMS for GB and NI vector data; designed for GIS compatibility.

## Data products and structure
- 23 LCM2007 classes derived from Broad Habitats; some Broad Habitats subdivided into finer subclasses (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral Sediment vs Saltmarsh).
- Vector data set: polygons with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels). Contains ~8.6 million GB polygons and ~0.9 million NI polygons.
- Raster data sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI separate extensions; pixel values map to LCM2007 classes as per Table 2.
  - 1 km raster: derived by summarising 25 m rasters; provides Dominant cover and Percentage cover for both LCM2007 classes and Aggregate classes.
- Aggregation for 1 km: uses predefined Aggregate classes to simplify the full 23-class schema (Table 2 mappings).
- Appendix mappings:
  - Appendix 1: detailed LCM2007 class descriptions (23 classes).
  - Appendix 2: relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.
  - Appendix 3: official colour mappings for display of each class.

## Spatial reference and projection
- Great Britain: British National Grid (OSGB 1936), Transverse Mercator projection.
- Northern Ireland: Irish National Grid; NI data transitioning toward ITM (prepared for reprojection in GIS).

## Data quality and validation
- Ground reference validation against 9127 polygons yields an average accuracy of 83%, acknowledging local discrepancies.
- Rich metadata retained for polygons, including processing history (KBE) and a top-5 spectral class probability list (ProbList).
- Sub-classBroad Habitats (BHSub) included with caveats: not all sub-classes have the same QA robustness; users should validate for analyses at sub-class level.

## Data access and licensing
- 1 km raster data available via CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; fees may apply.
- Contact: spatialdata@ceh.ac.uk; online application at www.ceh.ac.uk/data.

## File sizes and formats
- Vector (Shapefile, 100 km × 100 km tiles):
  - Great Britain: ~4.13 GB
  - Northern Ireland: ~0.43 GB
- Raster data (geotiff format):
  - 25 m: GB ~1.36 GB; NI ~46 MB
  - 1 km: GB products range from ~21 MB to ~49 KB (per product)
- Large data volumes reflect ~10 million vector polygons with 10 attributes each.

## Usage guidance for GIS specialists
- Use the 23-class LCM2007 vector or 25 m raster for high thematic detail; use 1 km rasters for coarse-scale UK-wide analyses or integration with other datasets.
- Retain Parcel_ID for unambiguous polygon communication and traceability of image inputs (cXX).
- Be mindful that Broad Habitat sub-classes (BHSub) are auxiliary and may require independent validation before use at fine-grained levels.
- The dataset is designed to be integrated with other GIS data; leverage OSMM-based segmentation for GB compatibility and consider KBE history when interpreting classifications.
- Refer to Morton et al. 2011 Final Report for comprehensive methodology, limitations, and validation details (Morton et al., Countryside Survey Technical Report No. 11/07).

## Appendix highlights (summary)
- Appendix 1: LCM2007 23-class definitions and indicative habitat descriptions.
- Appendix 2: mapping of Broad Habitats to LCM2007 classes and sub-classes (field codes and class numbers).
- Appendix 3: standard LCM2007 colour mapping (RGB values per class).