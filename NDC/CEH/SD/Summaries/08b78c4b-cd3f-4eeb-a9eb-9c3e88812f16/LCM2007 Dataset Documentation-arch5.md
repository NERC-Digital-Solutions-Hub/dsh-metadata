# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Purpose and Scope
- UK-wide parcel-based land cover classification intended to support diverse user needs with high-quality metadata and interoperability considerations.
- Maps land cover (not land use) using 23 Broad Habitat-based classes, updated from LCM2000 with improved spatial framework (OSMM-derived) and segmentation.
- Provides vector and raster data products at multiple thematic/spatial resolutions to suit various applications.

## Data Content and Structure

- LCM2007 Classes and Broad Habitats
  - 23 LCM2007 classes based on UK Broad Habitats; some Broad Habitats subdivided (e.g., Built-up Areas into Urban/Suburban).
  - Some subclasses (BHSub) provide additional information but are not covered by QA at the subclass level.
  - Appendix 1 details class definitions; Appendix 2 maps Broad Habitats and subclass relations; Appendix 3 colour mappings.
- Vector Data Set
  - Polygons with 10 attributes each (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - ~8.6 million polygons in GB and ~0.9 million in NI; unique Parcel_ID per polygon for traceability.
  - Includes processing history (KBE), spectral class probabilities (ProbList), and metadata on polygon construction.
- Raster Data Sets
  - 25m raster: 23 LCM2007 classes; detailed pixel-level representation.
  - 1km raster: derived by summarising 25m data to dominant and percentage cover per 1km cell; supports aggregation through 1km Aggregate classes.
  - GB and NI datasets are provided separately due to different projections; typical file sizes vary by format and access method.
- Spatial and Temporal Context
  - Built from summer-winter composite satellite images with 20–30 m pixels.
  - MMU: minimum mappable area > 0.5 ha; parcels < 0.5 ha dissolved into surrounding landscape.
- Metadata and Provenance
  - Rich polygon-level metadata, including source images, KBE history, and probable spectral classes (ProbList).
  - Parcel_ID and FieldCode aid communication; FieldCode accuracy is not QA-assessed at class level.

## Data Quality and Validation

- Validation
  - Ground reference validation against 9127 polygons; average accuracy approximately 83% (variability exists by area).
  - Local discrepancies may occur; users should perform own validation for subclass-level analyses.
- Accuracy and Limitations
  - LCM2007 only provides a thematic resolution at 23 classes; some Broad Habitat subclasses may have lower consistency/accuracy.
  - LCM2007 is designed for compatibility with other GIS datasets and general cartographic objects through OSMM-based segmentation.

## Data Access and Licensing

- Access
  - 1km raster data via CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25m raster product available under licence on request from CEH (spatialdata@ceh.ac.uk).
- Licensing and Fees
  - Licence fees may apply for some users and applications; online application process available on CEH website.
- Data Use Guidance
  - This documentation advises consulting Morton et al. (2011) Final Report for a comprehensive description and assessment.
  - For detailed interpretation of Broad Habitat classifications, refer to Jackson (2000) guidance.

## Spatial Reference and File Details

- Projections
  - GB: British National Grid (OSGB96/OSGB 1936 variant) for vector and 25m rasters; 1km rasters share the GB projection.
  - NI: Irish National Grid; NI 1km products transitioning to Ireland Transverse Mercator (ITM) in progress.
- File Size and Structure (typical guidance)
  - Vector (GB): ~4.13 GB; NI vector: ~433 MB.
  - Raster 25m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1km: Broad classes and percentages; sizes range from ~21 MB to ~49 KB depending on product.
- Data Storage and Access Notes
  - Vector datasets contain up to 10 attributes per polygon and ~9–10 million total polygons.
  - 25m rasters provide same thematic detail with less metadata overhead; 1km rasters provide coarse-grained summaries for broad-scale modelling.

## Appendix Highlights (useful for data stewardship)

- Appendix 1: LCM2007 Classes – precise definitions and features of Broad Habitat categories.
- Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (FieldCode mappings).
- Appendix 3: Standard LCM2007 colour mapping (as used in Final Report) for visual consistency and QA.

## Governance, Provenance, and Usage Considerations

- Data Governance and Traceability
  - Parcel_ID enabled for unambiguous communication and traceability across datasets and versions.
  - Maintain FieldCode and BH/BHSub attributes to support reproducibility; perform own validation for subclass usage.
- Standards and Interoperability
  - 23-class thematic resolution aligned with UK Broad Habitats; designed to be interoperable with OSMM-based spatial frameworks.
  - Clear notes on land cover versus land use and on minimum mapping units to avoid misinterpretation.
- Updates and Reuse
  - LCM2007 updates LCM2000; final interpretation should reference Morton et al. 2011 Final Report.
  - For specific grassland, montane, or littoral subclasses, validate against field or supplementary data before use in sensitive analyses.
- Access Controls and Licensing Compliance
  - Vector and 25m products available by licence; ensure license terms are followed; 1km rasters accessible via CEH gateway.
  - Acknowledge CEH and partner datasets and adhere to copyright/licensing notices.

## Further Information

- Morton, D. et al. (2011). Final Report for LCM2007 - the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- Contact: CEH data services and spatialdata@ceh.ac.uk; CEH Gateway for 1km rasters; additional details in the CEH data portal.