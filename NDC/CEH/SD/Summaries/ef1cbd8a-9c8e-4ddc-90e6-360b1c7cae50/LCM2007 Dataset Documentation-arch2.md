# Land Cover Map 2007 Dataset documentation

- A UK parcel-based land cover classification (LCM2007) delivering a set of data products to support diverse monitoring needs. It updates LCM2000 and uses a 23-class schema based on UK Broad Habitats, derived from summer–winter composite satellite imagery at 20–30 m resolution.

## Key purpose and approach for analysts

- Provide standardized land cover outputs to assess environmental health and policy performance over time.
- Emphasize data quality, metadata richness, and compatibility with GIS datasets; map land cover (not land use) to support broad environmental monitoring.

## Background and methodology

- Builds on 23 LCM2007 classes aligned with UK Broad Habitats; some subclasses exist for enhanced detail (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh).
- Parceled-based mapping using satellite imagery (summer–winter composites) at 20–30 m resolution.
- Improves upon LCM2000 by integrating a spatial framework based on Ordnance Survey MasterMap (GB) and Large-scale Vector for Northern Ireland, with segmentation to represent real-world objects (e.g., fields, woodlands).
- Maps land cover, not land use; some covers may resemble land use but are not definitive.

## Data products and formats

- Vector data set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - 10 attributes per polygon (including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
  - Unique Parcel_ID per polygon; recommended to retain for unambiguous communication.
  - Includes Broad Habitat sub-classes (BHSub) and official 1–23 LCM2007 class codes (INTCODE).
  - Rich metadata and knowledge-based enhancements (KBE) detailing processing history and spectral-class probabilities (ProbList).
  - Minimum mapping unit: polygons > 0.5 ha; smaller parcels and linear features dissolved into surrounding landscape.
- Raster data sets
  - 25 m and 1 km products derived from the vector data.
  - 25 m raster: contains the 23 LCM2007 classes; 1 km raster: aggregates to dominant class and percentage cover for 1 km pixels (both for LCM2007 classes and Aggregate classes).
  - Separate data sets for Great Britain and Northern Ireland due to different projections.
- Class relationships and aggregation
  - Table 2 defines relationships between LCM2007 classes, Broad Habitats, and Aggregate classes (used for 1 km rasters).
  - Appendix 2 details the mapping between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.

## Validation and accuracy

- Ground reference validation conducted with 9,127 polygons; overall average accuracy ~83%.
- Accuracy is an average across polygons; local discrepancies may occur.
- Sub-class level (Broad Habitat sub-classes) and FieldCode usage require user validation and caution, as these are not QA-validated to the same standard as the primary LCM2007 classes.

## Data access and licensing

- 1 km raster data available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under license from CEH; fees may apply.
- Data providers emphasize the need to verify licensing terms for commercial or large-scale uses.

## Map projection and spatial details

- GB data: British National Grid (OSGB 1936) / Transverse Mercator projection; NI data: Irish National Grid (likely migrating to ITM).
- NI is transitioning to Ireland Transverse Mercator; tools should reproject NI data as needed.

## File sizes and data scale

- Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI shapefile ~0.433 GB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: 21 MB to 49 KB depending on dataset component.
- Note: Vector files are large due to 10 attributes per polygon; 25 m rasters retain detailed information with more compact metadata absence.

## Data interpretation notes for analysts

- LCM2007 focuses on land cover interpretation; use with caution where land use distinctions are needed.
- The Broad Habitat subclasses provide additional context but are not as rigorously QA-validated as primary LCM2007 classes.
- Knowledge-based enhancements (KBE) applied during processing can cause reclassifications; users should review the KBE history for the polygon of interest.
- Grassland classifications can be particularly challenging (Neutral, Calcareous, Acid grasslands; potential misclassifications with Improved Grassland).

## Further information and references

- Morton et al. (2011). Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson (2000). Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- For color mappings and class-specific details, see Appendix 3 of the LCM2007 documentation.

## Appendix highlights (for quick reference)

- Appendix 1: LCM2007 Classes – detailed definitions and notes for each of the 23 classes.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard LCM2007 color mapping used in the Final Report.