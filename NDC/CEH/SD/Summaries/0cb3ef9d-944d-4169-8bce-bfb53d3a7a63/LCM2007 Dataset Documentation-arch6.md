# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a UK parcel-based land cover classification using 23 Broad Habitat–based classes, derived from summer–winter satellite composites with 20–30 m pixels. It updates LCM2000 and uses an OS-based spatial framework, producing data that map land cover (not necessarily land use) and are designed for GIS compatibility. The final report Morton et al. (2011) is recommended for comprehensive methodology and limitations.

- Key characteristics
  - Parcel-based, 23 classes aligned with UK Broad Habitats (with some refinements for sub-classes).
  - Produced from satellite imagery and image segmentation, using a topographic framework (OSMM/OS large-scale vector for GB/NI).
  - Minimum mappable unit (MMU) of >0.5 ha; parcels <0.5 ha or lines <20 m dissolved into surrounding area.
  - Distinguishes land cover from land use; e.g., arable crop may imply arable land but not guaranteed land use.

- Product structure and content
  - Vector Data Set
    - Contains ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
    - Each polygon has 10 attributes (including area, source images, Broad Habitat, and processing details).
    - Includes Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct history.
    - BHSub and FieldCode provide additional, but not QA-validated, detail; ProbList informs spectral likelihoods and should be validated for sub-classes.
  - Raster Data Sets
    - 25 m raster: Derived from the vector dataset; contains the 23 LCM2007 classes.
    - 1 km raster: Aggregated products (dominant class, and percentage cover) for broader scale analyses.
    - Separate datasets for Great Britain and Northern Ireland due to different projections.
  - Class relationships
    - Aggregation to 1 km uses 1) Dominant cover for LCM2007 classes and 2) Dominant/Percentage cover for Aggregate classes.
    - Table 2 (in the document) maps relationships between Broad Habitats, LCM2007 classes, and their aggregate equivalents.
  - Sub-class detail caveat
    - Broad Habitat sub-classes (BHSub) are included for potential detail but are not validated to the same standard as LCM2007 classes; users should validate if using sub-classes for critical analyses.

- Data quality and validation
  - Ground-reference validation: 9,127 polygons evaluated; average accuracy ~83% (regional variations may occur).
  - High thematic resolution (23 LCM2007 classes) is validated; some sub-class distinctions (BHSub) require user validation for accuracy.

- Map projection and geographic coverage
  - Great Britain: British National Grid (OSGB 1936 datum; Transverse Mercator projection).
  - Northern Ireland: Irish National Grid (datum Ireland 1965; projection Transverse Mercator; NI transitioning to ITM).
  - Table 3 details the exact grid, extents, pixel sizes, datums, and projections for GB NI datasets.

- File sizes and formats
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: ranges from ~21 MB (23-class percentage cover) to ~49 KB (dominant cover).
  - Note: Vector polygons are large due to 10 attributes per polygon.

- Data access and licensing
  - 1 km raster data accessible via the CEH Information Gateway.
  - Full vector and 25 m raster products available under licence on request from CEH.
  - Online application available through CEH data portal; fees may apply for some users/applications.

- Practical guidance for use (Data Support perspective)
  - Use the 23-class LCM2007 vector or 25 m raster for detailed analyses; use 1 km rasters for UK-wide modeling or when computational efficiency is priority.
  - Retain Parcel_ID for unambiguous communication and traceability of polygons.
  - Prefer the 23-class resolution for thematic analyses; consider aggregation to 1 km if consistency with other datasets is required.
  - Validate Broad Habitat sub-classes if used in decision-making, due to their lower QA coverage.
  - Be mindful of the MMU and dissolving rules when interpreting small patches or linear features.
  - Consult Morton et al. 2011 Final Report for comprehensive methodology, limitations, and detailed class descriptions.

- Appendix highlights
  - Appendix 1: LCM2007 Classes – detailed definitions and some caveats per Broad Habitat (e.g., Broadleaved vs. Coniferous Woodland, various grassland types, Fen/Marsh/Swamp, Bog, Montane, Inland Rock, coastal and urban classes).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping guidance and FieldCode descriptions).
  - Appendix 3: Colour mapping recipe used for standard LCM2007 color visualization (RGB values per LCM2007 class).

- Further information and references
  - Morton et al., 2011: Final Report for LCM2007 – the new UK Land Cover Map (technical report; CEH project number C03259).
  - Jackson, 2000: Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
  - Acknowledgements include data sources ( Landsat, SPOT, AWIFS, Ordnance Survey, soil and environmental datasets) and copyright/licensing details.

- Data use context and caveats
  - LCM2007 is land-cover-focused and not universally equivalent to land use; some spectral classes may not map cleanly to actual land-management categories.
  - Some classes (notably Broad Habitat sub-classes) should be used with validation, as accuracy varies.
  - The dataset provides rich metadata for polygons, enabling traceability of processing steps and data provenance, aiding data quality assessment and reproducibility.