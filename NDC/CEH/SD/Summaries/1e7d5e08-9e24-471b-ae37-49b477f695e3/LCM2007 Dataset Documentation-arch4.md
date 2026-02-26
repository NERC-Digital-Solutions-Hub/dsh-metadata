# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A comprehensive, parcel-based UK land cover classification (LCM2007) built from 20–30 m satellite imagery, using 23 classes aligned to UK Broad Habitats.
- Provides a range of data products (vector and raster) to support diverse user needs and applications; final report Morton et al. 2011 is the authoritative description.

## Overview and purpose
- Used to map land cover (not land use) across Great Britain and Northern Ireland; updates LCM2000 with a geography-based framework (OSMM, L&PS) and image segments.
- Aids interoperability with other GIS datasets by mapping to real-world objects (polygons) and providing rich metadata.
- Recommended to consult the Final Report for detailed methodology and limitations.

## Data products and structure
- Vector Data Set
  - Polygons with 10 attributes per parcel; unique Parcel_ID for communication across users.
  - 8.6 million polygons (Great Britain) and 0.9 million (Northern Ireland).
  - Key attributes: BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class number 1–23), KBE (processing history), ProbList (top 5 spectral class matches), CorePixels, TotPixels, construction history (OSMM-based, segmentation history).
  - Includes Broad Habitat sub-classes and FieldCode details, but quality assurance is strongest at the main 23 LCM2007 classes.
  - Notable: high metadata richness and traceable processing history; guidance to apply user validation for Broad Habitat sub-classes.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; derived from vector data; useful where polygon metadata is undesirable or unwieldy.
  - 1 km raster: aggregated products (dominant class, percentage cover for both LCM2007 classes and Aggregates); suited for national-scale modelling and combining with other datasets.
  - GB and NI have separate datasets with appropriate projections.
- Projections and coordinate systems
  - Great Britain: British National Grid (OSGB 1936)
  - Northern Ireland: Irish National Grid (moving toward ITM)
- File sizes (indicative)
  - Vector (Shapefile, GB 100 km x 100 km): approx. 4.13 GB; NI approx. 433 MB
  - Raster 25 m: GB approx. 1.36 GB; NI approx. 46 MB
  - Raster 1 km: 21 MB to 49 KB depending on product
- Data access
  - 1 km raster datasets: CEH Information Gateway
  - Full vector and 25 m raster: available on request under licence from CEH (data access portal and contact provided)

## Data quality, validation, and limitations
- Validation: ground reference data used to compare against 9127 polygons; average accuracy around 83% (acknowledging variability across areas).
- The product is validated at 23 LCM2007 classes; Broad Habitat sub-classes exist but require caution and user validation for use.
- LCM2007 maps land cover and not always precise land use; some crops and grassland may be spectrally similar to other uses.
- Minimum mappable unit: parcels >0.5 ha; parcels <0.5 ha or lines <20 m dissolved into surrounding landscape.
- Knowledge-based enhancements (KBE) applied during processing; ProbList provides top spectral-class likelihoods (not a QA guarantee).
- Users should validate Broad Habitat sub-classes if used beyond the main LCM2007 classes.

## Classification and mapping details
- 23 LCM2007 classes derived from 21 Broad Habitats (with some subdivisions, e.g., Urban vs Suburban; Heather vs Heather grassland).
- Table 2 (and Appendix 2) documents the relationships between Broad Habitats, LCM2007 classes, and sub-classes; Appendix 3 provides the standard colour mapping used in outputs.
- Appendix 1 provides full descriptions of the 23 LCM2007 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, etc.).
- LCM2007 is designed to be compatible with other GIS datasets via its polygon-based structure and rich metadata, facilitating integration and cross-reference.

## Practical guidance for data leaders
- Data strategy and governance
  - Plan for large data volumes, especially vector products; retain Parcel_ID and metadata to enable traceability and reproducibility.
  - Use 25 m vector-derived data where rich polygon metadata are valuable; use 25 m or 1 km raster for scalable UK-wide analyses.
  - Maintain awareness of MMU (0.5 ha) and potential under-representation of small fields or narrow linear features.
- Data quality and use
  - Rely on the 23-class LCM2007 framework for official UK land cover mapping; exercise additional validation for Broad Habitat sub-classes if used for policy or fine-scale decisions.
  - Consider combining with other datasets (meteorology, species distributions) for enhanced analyses at 1 km scale; use 25 m data for detailed mapping where feasible.
- Access and licensing
  - 1 km raster data accessible via CEH gateway; full vector and 25 m products available on licence by application.
  - Be prepared for licensing fees for certain users or applications; ensure compliance with data rights and citations (Morton et al. 2011; appendices for class mapping).

## Appendices (highlights)
- Appendix 1: LCM2007 Classes – detailed definitions and Broad Habitat interpretations for each of the 23 classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings and class numbers).
- Appendix 3: Colour mapping recipe for standard LCM2007 class visualization (RGB values per class).

## Final notes
- LCM2007 provides a robust, metadata-rich, multi-resolution dataset intended to support diverse data-driven strategies and collaborations within the data community.
- For full methodological depth and limitations, refer to Morton et al. 2011 Final Report and the detailed appendices within this documentation.