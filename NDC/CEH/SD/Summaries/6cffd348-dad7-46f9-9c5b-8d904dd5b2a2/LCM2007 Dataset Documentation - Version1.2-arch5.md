# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose: Document the Land Cover Map 2007 (LCM2007) data products to support users and inform decisions about data suitability, provenance, and limitations.
- Scope: UK-wide parcel-based classification of land cover (not land use) across Great Britain and Northern Ireland, using 23 Broad Habitat-based classes derived from 20–30 m satellite imagery. Replaces LCM2000; built with OS-based spatial framework and image segmentation for object-level polygons.
- Key caveat: LCM2007 is complex; users should consult the Final Report for comprehensive methodology, metadata, and limitations.

## Overview of LCM2007 and Outputs

- Classification: Maps land cover using 23 classes aligned to UK Broad Habitats; some classes subdivide into Subclasses for enhanced detail.
- Spatial framework: Polygons represent real-world objects (fields, woodland blocks) with a minimum mappable unit >0.5 ha; smaller features dissolved into surrounding landscape.
- Data products:
  - Vector data set: Polygons with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels). Desktop QA and metadata-rich.
  - Raster data sets: 25 m and 1 km products; separate GB and NI datasets; 1 km products include dominant and percentage cover for LCM2007 classes and aggregates.
  - Aggregates: 1 km raster products offer both 23-class aggregate and 9-class (Broad Habitat-based) aggregates.
- Data scope: Vector and raster products available; data accessed under specific licensing (GB NI distinctions).

## Data Structure and Metadata

- Vector data attributes (Table 1 summary):
  - Parcel_ID: Unique parcel identifier; source image info encoded.
  - BH: Dominant Broad Habitat level.
  - BHSub: Broad Habitat sub-class description.
  - FieldCode: Short text field code (not QA-validated at this level).
  - INTCODE: Integer class code (1–23) for display; QA-validated class.
  - KBE: Knowledge-based enhancements applied to polygon.
  - ProbList: Top 5 spectral class probabilities for the polygon.
  - CorePixels and TotPixels: Pixel counts used in classification.
  - Construct: Methodology history (OSMM generalised data, segmentation, etc.).
- Appendix 2 (relationship mapping) and Appendix 3 (colour mapping) provide crosswalks and visualization guidance.
- Rich metadata: Documentation records data processing steps, KBE history, and spectral/classification details; recommended for end-user validation, especially at Broad Habitat sub-classes.

## Data Quality, Validation, and Limitations

- Validation: Ground reference data used to validate against spatially/thematically aligned polygons; average accuracy around 83% (9127 references). Local discrepancies may occur.
- Change mapping: Complex to detect changes across LCM1990/2000/2007 due to differing classes and spatial structure; typical imagery classification errors (~20%) may exceed actual BH change signals.
- Use guidance: The 23-class resolution is the recommended thematic scale for accuracy; cautions about using Broad Habitat sub-classes without independent validation.
- Additional considerations: MMU and spectral similarity can affect classification consistency across grasslands, wetlands, and shrub categories.

## Data Access, Licensing, and Distribution

- Access points:
  - 1 km raster data (GB and NI): CEH Information Gateway.
  - Full vector product and 25 m raster product: available under licence on request from CEH (via online form or data@ceh.ac.uk). Fees may apply.
- Projections and coordinate systems:
  - GB: British National Grid (transverse Mercator), OSGB 1936.
  - NI: Irish National Grid (transitioning to Ireland Transverse Mercator; ITM planned).
- Data footprint:
  - Vector (GB): ~4.13 GB; NI: ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: smaller sizes (GB NI ranges specified in the documentation).
- Usage notes: licensing and access terms are documented; ensure rights for distribution, storage, and downstream use.

## Projections, File Sizes, and Formats

- Vector: 10 attributes per polygon; large file sizes due to ~10 million polygons (GB) and ~0.9 million (NI).
- Raster:
  - 25 m: detailed land cover at 25 m resolution.
  - 1 km: aggregated products including dominant and percentage cover.

## Version History and Updates

- Version 1.0: Original release (July 2011).
- Version 1.2: Updated May 2014.
  - Notable updates: Includes OS tile HZ (Fair Isle) and OS tile NW (Stranraer) for all GB products; water class added to 1 km dominant/aggregate products; NI updates reflect added water class.
  - Appendices updated accordingly (Appendix 4: List of updates).

## Appendices (Highlights)

- Appendix 1: LCM2007 Classes – detailed definitions and examples for each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various Grasslands, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Urban/Suburban, Saltwater/Freshwater, Littoral and Supra-littoral classes, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (field codes and class mappings).
- Appendix 3: LCM2007 colour mapping (recipe used in Morton et al. 2011 final report) and ArcGIS color file note.
- Appendix 4: Updates to products (Version 1.2) – tile additions and water class inclusion.

## Acknowledgements and References

- Acknowledges data sources and partners (Landsat, SPOT, AWIFS, OS datasets, soils, elevation, etc.).
- References: Morton et al. 2011 Final Report; Jackson 2000 Broad Habitat guidance; Countryside Survey partnership context.

## Governance and Stewardship Takeaways

- Data provenance and metadata: LCM2007 provides a richly documented lineage (KBE history, polygon construction, ProbList, source images) that supports traceability and reproducibility.
- Data quality management: Be aware of the 83% average accuracy and locality issues; validate Broad Habitat sub-class data for critical applications.
- Change management: Use caution with change detection; prefer 1 km aggregate or 25 m raster products with explicit metadata on limitations for temporal analyses.
- Access and licensing controls: Ensure compliance with CEH licensing terms; manage access for internal use and stakeholder sharing; track version updates.
- Interoperability considerations: Projections differ between GB and NI; NI moving toward ITM; reproject as needed for cross-border analyses.
- Stewardship practices: Maintain Parcel_ID and other core attributes to ensure unambiguous data communication; document processing steps and KBE changes; consider integrating with broader data governance frameworks for discovery and reuse.