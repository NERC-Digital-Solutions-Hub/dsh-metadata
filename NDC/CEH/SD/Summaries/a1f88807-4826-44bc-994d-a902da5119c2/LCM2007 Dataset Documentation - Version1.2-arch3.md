# LAND COVER MAP 2007 DATASET DOCUMENTATION

- This is a UK land cover product describing Land Cover Map 2007 (LCM2007), a parcel-based classification of land cover used for environmental monitoring and policy evaluation. It updates LCM2000 and is built from satellite imagery (20–30 m pixels) with integration of OS MasterMap and related vector datasets to create object-based parcels. LCM2007 maps land cover (not land use) and uses 23 Broad Habitat-based classes.

## What the dataset contains

- Data products
  - Vector Data Set: polygons with attached attributes for each parcel (8.6 million in GB, 0.9 million in NI; 10 attributes per polygon).
  - Raster Data Sets: 25 m and 1 km resolutions; GB and NI provided separately; 23 LCM2007 classes in the 25 m raster; 1 km rasters provide dominant and percentage cover for both LCM2007 classes and Aggregate classes.
  - Aggregates: 1 km products use merged/aggregate classes to simplify applications.
- Classification and labeling
  - 23 LCM2007 classes, tied to UK Broad Habitats; some classes have sub-classes (e.g., Urban vs Suburban, Heather vs Heather grassland).
  - Broad Habitat Sub-classes (BHSub) exist in vector data and are documented but not always as accurate as the main LCM2007 class.
  - Each vector polygon includes a Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE history, ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Knowledge-Based Enhancements (KBE) capture history of processing changes (e.g., soil, altitude corrections, coastal masking).
- Metadata and QA
  - Rich metadata for polygons, including source images, processing steps, and KBE history.
  - QA/validation against ground reference data shows an average accuracy of about 83% across 9,127 polygons; local variations occur.

## Data structure and access

- Vector vs Raster
  - Vector: polygon-based with detailed metadata per parcel; larger file sizes.
  - 25 m Raster: detailed, with 23 classes; includes pixel-level data but fewer per-polygon attributes.
  - 1 km Raster: summarised products (dominant class, percentage cover) for UK-wide analyses; GB and NI have separate extents and projections.
- Projections and coordinate systems
  - GB: British National Grid (OSGB36).
  - NI: Irish National Grid (with ongoing migration toward ITM for Northern Ireland).
- File size guidance
  - Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: sizes range roughly from 21 MB to 49 KB depending on product.
- Access
  - 1 km raster datasets available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request/licence from CEH; fees may apply.

## Data governance, metadata, and usage notes

- Data governance
  - Datasets come with extensive metadata; users should maintain Parcel_ID and related attributes for traceability.
  - Users are advised to perform their own validation when using Broad Habitat sub-classes.
- Change mapping and limitations
  - Cross-LCM change mapping (1990, 2000, 2007) is complex due to differing class definitions and spatial structures; not well suited for straightforward change detection.
- Use cases and caveats
  - LCM2007 maps land cover, not land use; some land cover types may not directly indicate actual use (e.g., grassland for recreation vs grazing).
  - MMU: minimum mappable unit is >0.5 ha; parcels smaller than 0.5 ha or lines under 20 m are dissolved.
  - The 1 km raster products provide aggregate classifications for larger-scale modelling; the 25 m and vector products preserve finer detail but with larger data volumes.
  - For detailed grassland and sub-habitat classes (e.g., Neutral/Calcareous Grassland, Bog vs Dwarf Shrub Heath), users should refer to Morton et al. 2011 Final Report for methodological notes and consider aggregation where appropriate.

## Appendix and documentation highlights

- Appendix 1: Detailed list of the 23 LCM2007 classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCodes).
- Appendix 3: Colour mappings for visualization (including an ArcGIS .lyr file).
- Appendix 4: Updates to products (Version 1.2, May 2014) including added tiles (e.g., Fair Isle, Stranraer) and water class updates.

## Background, provenance, and references

- Source imagery includes Landsat-TM5, SPOT-4/5, AWIFS, and Ordnance Survey cartography.
- Development collaborative context with Countryside Survey Partnership; key references include Morton et al. 2011 (Final Report) and Jackson 2000 (JNCC habitat guidance).

## Practical implications for monitoring/framework authors

- LC M2007 provides a comprehensive, well-documented set of land-cover classes aligned with UK Broad Habitats, suitable for policy scrutiny, trend analysis, and decision support when paired with its metadata and QA.
- The vector data offers rich provenance and processing history, enabling transparency and reproducibility, while the 25 m and 1 km rasters support scalable, aggregated analyses.
- Given the change-detection caveats, authors should approach longitudinal analyses with careful consideration of class and spatial-structure differences across LCMs and, where possible, validate with ground reference data.