# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover map (LCM) 2007, parcel-based classification using 23 Broad Habitat classes.
- Maps land cover (not land use) derived from 20–30 m satellite imagery; updates LCM2000.
- Products include vector (polygons with rich metadata) and raster datasets (25 m and 1 km; GB and NI separately).
- Minimum mappable unit: parcels >0.5 ha; smaller parcels dissolved.
- Validation: ground reference data (9127 polygons) yielding average accuracy of 83%.

## Data Structure and Products
- Vector Data Set
  - Approximately 8.6 million polygons (GB) and 0.9 million (NI).
  - 10 attributes per polygon including: Parcel_ID, BH (Broad Habitat), BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode; Parcel_ID retained for clear communication.
  - Rich metadata capturing processing history and spectral/class information (KBE, ProbList).

- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI separate projections.
  - 1 km raster: Aggregate classes (for broader analyses) plus dominant/percentage targets for both LCM2007 classes and Aggregate classes.
  - Metadata includes grid dimensions, pixel counts, coordinates, projection, datum, and data type (Unsigned 8-bit).

- Relationships and Mappings
  - Appendix 2 provides the mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3 provides the standard colour mapping for classes.

## Methodology and Limitations
- 23 classes aligned with UK Broad Habitats; some Broad Habitats split into sub-classes based on spectral signatures (e.g., Built-up Areas subdivided into Suburban/Urban).
- Change detection across LCM1990/2000/2007 is complex due to differing class schemes, spatial structures, and typical classification errors (~20%); not well suited for change mapping.
- Ground validation indicates overall accuracy around 83%, with possible local discrepancies.

## Data Access and Licensing
- Data Access
  - 1 km raster datasets available via CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under licence from CEH (licence fees may apply).
  - Application process available via CEH data portal or by contacting spatialdata@ceh.ac.uk.

- Projections and Coverage
  - GB products use British National Grid; NI products use Irish National Grid (with NI transitioning toward ITM projection).
  - Separate data sets for GB and NI to reflect different projections.

## File Sizes and Format Notes
- Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: GB products range ~21 MB to 49 KB (dominant/percentage targets and aggregates).

## Appendices (Key Details)
- Appendix 1: LCM2007 Classes
  - Detailed descriptions of each Broad Habitat class and notable complexities (e.g., distinctions within woodland, grasslands, wetlands, montane habitats, coastal habitats).
- Appendix 2: Class Relationships
  - Detailed cross-walk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes with FieldCode mappings.
- Appendix 3: Colour Mapping
  - Standard RGB color codes for each LCM2007 class for visualization (also available as ArcGIS .lyr).
- Appendix 4: Updates to Products (Version 1.2, May 2014)
  - Updates to include OS tiles Fair Isle, Stranraer; water class addition; 1 km products updated accordingly.

## Product Version History
- Version 1.0 (July 2011): Original release.
- Version 1.2 (May 2012/2014): Dataset updates, change-detection caveats, inclusion of water class; NI/GB tile updates.

## Relevance for Environmental Monitoring Analysts
- Provides a standardized, high-coverage UK land-cover baseline aligned with Broad Habitats for long-term environmental health monitoring.
- Supports multi-resolution analytics (detailed 25 m vector/raster vs. 1 km aggregates) suitable for national-scale assessments and integration with other datasets (e.g., meteorology, species distribution).
- Rich metadata and QA history enable reproducibility and traceability of dataset construction and classifications.
- Data storage and portal access align with the aim of making underlying data accessible to users for scrutiny and policy monitoring.