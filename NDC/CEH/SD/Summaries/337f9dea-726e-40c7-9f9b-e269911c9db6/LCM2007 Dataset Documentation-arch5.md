# Land Cover Map 2007 Dataset Documentation

## Introduction and Background
- Land Cover Map 2007 (LCM2007) is a parcel-based classification of UK land cover using 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Maps land cover (not land use) from summer-winter satellite composites at ~20–30 m pixels.
- Replaces LCM2000 with improvements in spatial framework (OSMM for GB, L&S Large-scale Vector for NI) and segmentation to match real-world objects (fields, woodland blocks).
- LCM2007 supports diverse GIS applications and is complemented by a final technical report for full methodology and limitations.

## Data Products and Structure
- LCM2007 provides a range of data products to suit different applications, with detailed documentation and metadata.
- Key distinction: LCM2007 maps land cover, not necessarily land use; some land use inferences (e.g., crops) may not align with land use in field.
- Minimum mappable unit: >0.5 ha; parcels <0.5 ha or linear features <20 m are dissolved into surrounding landscape.

### Vector Data Set
- 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
- 10 attributes per polygon (Table 1): Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
- Parcel_ID provides unique communication about the source imagery; recommended to retain.
- BHSub and FieldCode provide additional sub-class information; not all are QA’d to LCM2007 class level.
- KBE (Knowledge-Based Enhancement) records processing history; ProbList lists top 5 spectral class candidates; CorePixels and TotPixels document pixel counts.
- Vector products include rich metadata to document polygon construction and processing history.
- Data volume: GB ~4.13 GB; NI ~433 MB (per 100 km x 100 km shapefile packaging).

### Raster Data Sets
- 25 m and 1 km raster products derived from the vector dataset.
- Separate datasets for Great Britain and Northern Ireland to accommodate different projections.
- 25 m raster: 23 LCM2007 classes; 1 km raster products summarize 25 m data (dominant class, percentage cover) using Aggregate classes for 1 km.
- 1 km raster products include:
  - Dominant cover for 23 LCM2007 classes
  - Dominant cover for Aggregate classes
  - Percentage cover for 23 LCM2007 classes
  - Percentage cover for Aggregate classes
- Raster metadata (per Table 3) includes grid size, extents, pixel counts, coordinate systems, projections, datums, and data types (unsigned 8-bit).

## Data Quality and Validation
- Ground reference validation used 9,127 polygons to assess LCM2007 against spatial and spectral-resolution data; average accuracy around 83% (with local variability).
- The accuracy figure is an average; individual areas may perform better or worse.
- Sub-class level (BHSub) and FieldCode are included but not consistently QA’d at the same level as 23 LCM2007 classes. Users are advised to validate at sub-class level before use.
- Grassland classifications (Neutral/Calcareous vs Improved) exhibited some confusion; section 3.9 and Chapter 4 of Morton et al. (2011) provide more detail for users needing these specifics.
- The Broad Habitat classifications and their relationships to LCM2007 classes are described in Appendices (Appendix 1–3).

## Metadata, Provenance and Documentation
- LCM2007 includes a rich set of polygon attributes detailing processing history (KBE), spectral class probabilities (ProbList), and source imagery (Construct: OSMM, OSMM:SEG, OSMM:AGC:SEG).
- Unique parcel-level labeling (Parcel_ID) supports traceability and reproducibility.
- Detailed Appendices:
  - Appendix 1: LCM2007 classes (descriptions and habitat interpretations)
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat sub-classes
  - Appendix 3: Colour mapping recipe for LCM2007 classes

## Access, Licensing and Availability
- Data access:
  - 1 km raster data sets are available via the CEH Information Gateway.
  - Full vector product and 25 m raster product are available on request under a license; online CEH data application process exists.
  - Licensing may incur fees; some uses may require approval.
- Projections:
  - GB data: British National Grid (OSGB 1936)
  - NI data: Irish National Grid (and moving toward ITM for NI)
  - GIS tools can reproject NI data to ITM as needed.
- Section on data access emphasizes that the full vector and 25 m products require a license; 1 km rasters are publicly accessible via gateway where permitted.

## Spatial and Technical Details
- Spatial resolution:
  - Vector: polygons with detailed attribute metadata
  - Raster: 25 m and 1 km products
- Coverage:
  - GB and NI, with separate datasets and coordinate systems
- Classification scheme:
  - 23 Broad Habitat classes (based on UK BAP), with some sub-classes (BHSub) for enhanced detail
  - Some classes subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban)
- MMU considerations and limitations:
  - Patches smaller than 0.5 ha typically dissolved
  - Fen, Marsh and Swamp, Saltmarsh, Montane Habitats areas require careful interpretation due to spectral ambiguity
- File sizes and formats:
  - Vector shapefiles (100 km x 100 km) GB ~4.13 GB; NI ~433 MB
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB
  - 1 km rasters: 21 MB to 49 KB (varies by product)

## Appendices and Colour Mapping
- Appendix 1: Detailed LCM2007 class descriptions and Broad Habitat interpretations (e.g., Broadleaved woodland, Arable and Horticulture, Improved Grassland, Fen/Marsh/Swamp, Bog, Montane, Inland Rock, Urban, Saltmarsh, Littoral categories, etc.)
- Appendix 2: Recipe for mapping Broad Habitats to LCM2007 classes and their sub-classes (FieldCode relationships)
- Appendix 3: Standard RGB color mappings for each LCM2007 class (as used in the Final Report)

## References and Further Information
- Morton et al. (2011) Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07)
- Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification
- Additional datasets and licensing details acknowledged (OS, Landsat, SPOT, etc.)