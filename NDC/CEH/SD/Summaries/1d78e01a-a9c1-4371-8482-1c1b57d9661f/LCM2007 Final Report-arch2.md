# Final Report for LCM2007 - the new UK land cover map

- The study compares LCM2007 with Countryside Survey (CS) 2007 to assess area estimates, accuracy, and how well satellite-derived broad habitat maps align with field-based survey data.
- LCM2007 provides UK-wide, parcel-based land cover mapped to Broad Habitats, derived from multi-temporal satellite imagery and enhanced with knowledge-based rules; it aims to support long-term environmental monitoring and policy assessment.

## Dissimilar area estimates ( CS 2007 vs LCM2007 )

- Dissimilarity identified for several broad habitat classes when CS 2007 95% confidence limits are exceeded by LCM2007, including:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Example: Arable and Horticulture
  - CS UK area: 46,574 km2 vs LCM2007: 63,005 km2
  - Possible causes: differences in what is classified as Arable/Horticulture, spectral confusion, inclusion of Boundary/Linear Features in LCM2007, and differences in temporal image composition (multiple-year imagery used by LCM2007).
  - DEFRA 2007 figures show a combined arable and horticultural area around 63,840 km2, suggesting temporary grass or uncropped land may be included in LCM2007’s Arable and Horticulture class.
  - Temporal range expansion in LCM2007 can shift field classifications (grass vs arable) between composites, increasing spectral variability.
- Other notable discrepancies:
  - Improved Grassland and Neutral Grassland: LCM2007 shows about 10,000 km2 more (Improved) and 10,000 km2 less (Neutral) than CS, likely due to different handling of Neutral Grassland vs Improved Grassland signatures and soil context.
  - Dwarf Shrub Heath vs Bog: differences largely due to reallocation between these habitats.
  - Fen, Marsh and Swamp: CS UK estimate (~4,392 km2; CS 2007) vs LCM2007 (~101 km2) differ by orders of magnitude; fen areas in CS often appear as Rough Grassland or Acid Grassland in LCM2007 due to spectral and patch-size complexities.
  - Montane Habitats and coastal habitats: CS data are sparse for these classes, so differences are expected.
- Additional contributing factors:
  - Differences in minimum mapping unit (MMU) and how boundaries are treated (field vs parcel mapping).
  - Patch size effects: many CS parcels are below LCM2007’s MMU, influencing area estimates, especially for Fen and similar mosaics.
  - The need for further work to assign grassland mosaics to Fen, Marsh and Swamp using additional knowledge-based rules.

## Discussion highlights (4.3.3)

- Agreement between LCM2007 and CS varies widely across Broad Habitats; grassland classifications are particularly challenging due to a one-to-many relationship between observed grass in the field and the Broad Habitat categories.
- Broad Habitat Association (BHA) rules were developed to improve cross-comparisons at BH, Aggregate, and BHA levels.
- LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture at 1 km scale, but overall Broad Habitat extent estimates for Arable and Horticulture are higher in LCM2007 than CS.
- Fen, Marsh and Swamp estimates diverge significantly; many fen areas in CS map to Rough Grassland or Acid Grassland in LCM2007. Future work could use knowledge-based enhancements to reallocate some of these grassland areas to Fen, Marsh and Swamp.
- Patch-size effects and differences in spatial framework between the two products complicate direct change detection and trend analysis.

## UK Land Cover overview (4.4)

- UK-wide distribution: More than 50% of land is intensive (Arable and Horticulture plus Improved Grassland) or Built-up Areas; about 12% Broadleaved and Coniferous Woodland; roughly 30% semi-natural (including 1% freshwater, 30% semi-natural grassland/mountain, heath and bog).
- Country patterns:
  - England: highest intensive land-use share (~76%; 40% Arable and Horticulture; 27% Improved Grassland; 9% Built-up Areas and Gardens).
  - Scotland: largest share of Coniferous Woodland; 36% Mountain, Heath and Bog; 20% semi-natural grassland; lower overall intensive land-use than England.
  - Northern Ireland and Wales: substantial intensive land-use (Improved Grassland and Arable) but different spatial allocations of boundaries and features.
- Comparison with LCM2000:
  - LCM2007 shows changes in the relative shares of Arable and Semi-natural Grassland compared to LCM2000; Coniferous Woodland slightly increases; urban areas are similar but marginally lower in LCM2007.
  - Unclear how much of the observed differences are due to the spatial framework versus thematic changes.

## Summary and implications for monitoring (4.5)

- LCM2007 delivers a robust, UK-wide land cover map aligned to Broad Habitats, built from extensive satellite data and external datasets, with QA and knowledge-based enhancements to improve thematic discrimination.
- It is valuable for long-term habitat monitoring, policy evaluation, and cross-sector environmental analyses, with outputs across vector, 25 m raster, and 1 km summaries.
- Caution for users:
  - Class-level accuracy varies; grassland and fen-related classes show notable uncertainties due to spectral similarity and patch-size issues.
  - Change detection across LCM versions is non-trivial because of differing spatial structures and class definitions; cross-validation with field data (CS-type surveys) or use of Broad Habitat Associations can help interpret results.
  - Boundary and linear features may inflate some Arable/Horticulture or Grassland estimates in LCM2007 relative to CS.
- Recommendations for analysts:
  - Use Broad Habitat Association rules to relate LCM2007 classes to CS data and interpret overlaps more reliably.
  - Consider corroborating satellite-derived change with field surveys, especially for grassland and fen-dominated habitats.
  - Leverage the KBEs to refine grassland and fen classifications where spectral signatures are ambiguous.
  - When monitoring change, rely on aggregated levels or BH associations to reduce misinterpretation from class-level noise.
- Data access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request from CEH (licensing may apply).

## Example areas and data formats (5.x)

- The report includes example areas illustrating LCM2007 performance across upland, calcareous, urban, arable, and fenland landscapes.
- Data products:
  - Vector: polygons with 10 attributes documenting processing steps, KBE history, and classification context.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summary formats per pixel (percentage cover by class; dominant class).
- Each product supports different monitoring applications, from high-resolution habitat mapping to national-scale trend analysis.

## Access to the data

- CEH Information Gateway provides the 1 km raster data.
- Full vector and 25 m raster products are available on request; licensing may apply.