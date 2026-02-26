# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A suite of UK land cover products (LCM2007), a parcel-based classification using 23 classes aligned with UK Broad Habitats (BAP). Based on summer–winter satellite composites with ~20–30 m pixels. Updates and upgrades LCM2000; aims to be GIS-friendly by using object-based polygons and a rich metadata framework.

## What LCM2007 is and what it covers

- Maps land cover (not land use) for Great Britain and Northern Ireland.
- 23 LCM2007 classes derived from Broad Habitats; some classes subdivided (e.g., Built-up Areas, Dwarf Shrub Heath).
- Minimum mappable unit is >0.5 ha; smaller parcels are dissolved into surrounding landscape.
- Validated at 23-class thematic resolution; intended as the highest recommended thematic resolution for use.

## Data products and formats

- Vector Data Set
  - Polygons with 10 attributes each; Parcel_ID, BH (Broad Habitat), BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels, etc.
  - ~8.6 million polygons GB, ~0.9 million NI; includes unique Parcel_ID for unambiguous communication.
  - Rich metadata per polygon; includes processing history and top spectral class probabilities (ProbList).
- Raster Data Sets
  - 25 m raster (23 LCM2007 classes) derived from vector; GB and NI separate projections.
  - 1 km raster products: dominant class, percentage cover (for both classes and aggregates).
  - Aggregates merge classes for 1 km products to simplify applications.
- Spatial coverage
  - GB and NI datasets with distinct projections (GB: British National Grid; NI: Irish National Grid).
  - NI moving toward Ireland Transverse Mercator (ITM) projection; reprojecting supported.

## Data access and licensing

- 1 km raster data: accessible via CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector and 25 m raster products: available on request under licence from CEH; fees may apply.
- Online application process and contact: spatialdata@ceh.ac.uk.

## Data quality, validation, and limitations

- Ground reference validation: 9127 polygons assessed; average accuracy ~83% (with local variation).
- Change detection limitations: LCM1990/2000/2007 change mapping is complex due to class and spatial structure differences; overall classified image error typically ~20%, making robust change detection challenging.
- Differences between land cover (LCM) and land use; spectral classifications may misclassify grasslands (Neutral/Calcareous/Acid) as Improved Grassland; caution advised when using grassland subclasses.
- Broad Habitat subclasses (BHSub) exist but are not QA-validated at the same level as LCM2007 classes; use requires user validation if using BHSub for analysis.

## Data structure and access details

- Vector vs Raster trade-offs
  - Vector: rich polygon metadata, higher detail, larger file sizes; suitable for detailed analyses and communication via Parcel_ID.
  - 25 m raster: compact representation without polygon boundaries; useful for certain modelling and visualisation tasks.
  - 1 km rasters: suitable for UK-scale modelling and integration with other large datasets (e.g., meteorology, species distribution).
- File sizes (illustrative)
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: modest sizes (21 MB to 49 KB for different products in GB).
- Data provenance and naming
  - Parcel_ID includes source image information; core metadata captures construction history and spectral/classification lineage.

## How to use and apply the data

- Retain Parcel_ID for clear communication and traceability.
- Use the KBE (Knowledge-Based Enhancements) history to understand processing steps and corrections applied to each polygon.
- Validate Broad Habitat classifications and, where necessary, use user-driven validation for Sub-class level analyses.
- For applications requiring detailed habitat mapping, prefer the vector product with full metadata; for broader analyses, 25 m or 1 km rasters may be more practical.
- When aligning with other datasets, be mindful of projection differences and the MMU (minimum mapping unit) constraints.

## Appendices and supplementary information

- Appendix 1: LCM2007 Classes with Broad Habitat definitions and nuances (e.g., subdivision of certain Broad Habitats, grassland classifications).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (probable fieldcodes and mappings).
- Appendix 3: Colour mapping for standard LCM2007 classes (used in reports and GIS layers; includes an ArcGIS .lyr file).
- Appendix 4: Updates to products (Version 1.2, May 2014) including OS tile updates, water class inclusion, and other dataset refinements.

## Version history and acknowledgements

- Version history: 
  - Version 1.0 (July 2011) original release.
  - Version 1.2 (May 2012, later linked to 2014 updates) includes dataset updates and change-detection notes.
- Acknowledgements: data sourced from Landsat-TM5, SPOT-4/5, AWIFS, OS datasets, RoR boundaries, soil and elevation data, and collaborations across the Countryside Survey Partnership.

## Key takeaways for Data Leaders

- LCM2007 provides a richly described, parcel-based land cover dataset with extensive metadata and provenance, suitable for governance, strategy, and cross-network data integration.
- The vector product offers deep traceability (Parcel_ID, KBE history, ProbList) but at the cost of larger file sizes; raster products offer scalable, mosaic-friendly options with lower metadata overhead.
- The dataset is best used with validation, particularly when analyzing broad habitat subclasses, and with awareness of MMU limitations and potential grassland misclassifications.
- Access is governed; 1 km rasters are openly accessible via CEH gateway, while full vector/raster detail requires licensing and a formal request.
- Ongoing updates (notably the 2014 v1.2 release) reflect tile additions and improvements, including a water class in some 1 km products, and ongoing data management by CEH and partners.