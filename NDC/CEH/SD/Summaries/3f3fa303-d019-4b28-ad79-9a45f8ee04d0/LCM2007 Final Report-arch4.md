# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based UK land cover map (LCM2007) with 23 land cover classes mapped to 17 Broad Habitats (BH).
- Provides UK-wide coverage via a continuous vector framework (GB and NI) and accompanying raster products (25 m, 1 km).
- Vector product: land parcels with 10 attributes documenting processing steps and provenance; 0.5 ha minimum mapping unit (MMU).
- Raster products: 25 m resolution (23 LCM2007 classes) and 1 km summaries (percent and dominant class per pixel).
- Data access: 1 km rasters openly via CEH gateway; full vector and 25 m rasters available on request under licence (fees may apply).

## Data Sources and Spatial Framework
- Satellite imagery: Landsat-5 TM, SPOT-4/5, IRS LISS-III; 20–30 m resolution; multi-date summer/winter composites used for ~91% of GB; remaining 9% from single-date imagery.
- External spatial data: ground reference points (CS campaigns 2006–2008), Countryside Survey Broad Habitat data, national cartography (OS MasterMap for GB; LPS for NI), agricultural boundaries, urban datasets, soils, and elevation.
- Spatial framework and MMU: GB based on OS MasterMap; NI on LPS Large-scale Vector; integration with agricultural boundaries; MMU 0.5 ha; minimum feature width 20 m.

## Production Workflow
- Image pre-processing: cloud masking, atmospheric correction, georeferencing; 6-band, 2-date composites produced.
- Image segmentation: 60 composites segmented using a 3-band combination; NI segments derived from single-date imagery.
- Classification: parcel-based supervised maximum likelihood across 37 composites and 21 single-date images; training from ground references; top-5 spectral class probabilities recorded (ProbList).
- Knowledge-Based Enhancements (KBEs): seven automated rules using contextual data (urban boundaries, coastal proximity, terrain, soils) to reclassify parcels and improve thematic resolution; designed to resolve spectral confusion (e.g., grassland types) and align with BHs; KBEs are documented in vector attributes and are reversible by users.
- Post-processing and assembly: nine-chunk UK-wide assembly to manage sensor heterogeneity and optimize quality; hierarchical prioritization yields seamless UK-wide layer.

## Data Products and Access
- Vector product: UK-wide land parcels (MMU 0.5 ha) with 10 attributes (including Construct, ProbList, KBE indicators).
- Raster products: 25 m resolution with 23 LCM2007 classes; 1 km rasters with two formats:
  - Percent: for each 1 km cell, the percentage cover of each LCM2007 class.
  - Dominant: the most abundant class per 1 km cell.
- Metadata: extensive metadata accompanying vector products to track processing steps.
- Access details: 1 km rasters via CEH gateway; vector and 25 m rasters on request under licence (fees may apply).

## Validation, Accuracy, and Limitations
- Validation: ground-reference points ~9,127; overall LCM2007 accuracy around 83%, with class-level variations.
- Strong performers: Coniferous Woodland, Arable and Horticulture, Littoral Rock, Urban/Street-scale classes.
- More variable classes: Neutral Grassland, Calcareous Grassland, Montane Habitats due to spectral ambiguity and reliance on ancillary KBEs.
- Limitations: spectral variability (e.g., Arable and Horticulture), complexity of combining multiple years of imagery, and differences in spatial structure relative to older maps challenge direct change mapping and cross-product comparisons.
- Change detection: non-trivial due to differences in spatial/thematic structures across LCM generations; recommended approaches include focusing on aggregated classes or re-organising older maps into a common spatial framework.

## Comparison with Countryside Survey (CS)
- CS 2007 comparison uses 591 1 km squares and national estimates to assess LCM2007.
- Agreement varies by Broad Habitat; Grassland types show notable discrepancies due to one-to-many relationships and spectral variability.
- BH correspondence UK-wide about 62%; aggregates about 67%; BH Associations around 76%.
- Grassland harmonisation (grouping subtypes) improves correspondence to ~87–90% for certain levels.
- Regional differences: Scotland shows upland discrepancies (Bog, Montane Habitats) but higher BH associations when linked to habitats; Fen, Marsh and Swamp areas show substantial variance due to mosaic nature and mapping scale.
- Differences arise from: classification boundaries, spectral confusion, inclusion of boundaries/lines in LCM near Arable vs. Horticulture, and how CS maps some features below MMU of LCM.

## UK Land Cover Snapshot and Implications
- UK-wide distribution: over 50% intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas; woodlands ~12% (split between Broadleaved and Coniferous); remaining semi-natural with coastal, grassland, and mountain/heaths.
- Country-level patterns: England most intensive; Scotland with the largest Coniferous Woodland and higher semi-natural mountain/grassland areas; NI and Wales show different balances but similar scale of intensive use.
- Comparison with LCM2000 indicates shifts in Arable, Semi-natural Grassland, and Coniferous Woodland proportions, reflecting methodological differences and landscape change.

## Data Use, Governance, and Data Leaders’ Considerations
- For data leaders, LCM2007 offers a robust, policy-relevant evidence base for habitat monitoring, biodiversity reporting, ecosystem services, and landscape planning.
- Use of KBEs and BH Associations is key to interpreting correspondences with field data; the BH framework provides a structured approach to cross-walking land cover to habitat types.
- Change mapping requires careful handling due to differing spatial structures; consider re-aligning maps to a common spatial framework based on real-world land-use units for robust trend analysis.
- Data access and licensing: institutional access via CEH; 1 km data openly available; higher-resolution vector and 25 m rasters require licensing and application.
- The parcel-level metadata (including KBE history and probability distributions) enables targeted quality assessment and flexible, location-specific validation approaches.

## European Context and Future Outlook
- LCM2007 contributes to pan-European assessments (e.g., Corine Land Cover) by providing a UK-wide high-resolution, policy-relevant base that can be transformed for European reporting.
- Alignment with European datasets (e.g., IMAGE 2006) and ongoing European land-cover initiatives supports cross-border environmental policy and monitoring.

## Appendices and Technical Details (Highlights)
- Broad Habitat Associations (BHAs): rules guiding how LCM2007 classes correspond to Countryside Survey Broad Habitats, addressing issues like Bog–Dwarf Shrub Heath–Acid Grassland continua, Montane adjustments, Water classes, and Built-up Areas.
- Data structure: detailed descriptions of vector attributes (BH, BHSub, ProbList, KBE history, etc.) and raster metadata at 25 m and 1 km resolutions.
- Validation methodology: bespoke validation approach emphasizing fit-for-purpose assessment using parcel-level metadata and image-consistency checks with high-resolution imagery.

## Concluding Takeaways for Data Leaders
- LCM2007 delivers coast-to-coast UK land cover mapping with a reusable, stable spatial framework and multi-resolution data products suitable for policy, planning, and ecosystem assessments.
- The combination of high-quality inputs, a robust KBEs framework, and parcel-level metadata enhances transparency and traceability of classifications.
- While overall accuracy is strong, specific habitat classes exhibit spectral ambiguity and rely on ancillary data; interpretation should leverage Broad Habitat Associations for robust decision-making.
- Change detection across LCM generations remains complex; adopting a unified spatial framework is recommended for future monitoring and trend analysis.
- Access to data is structured: open 1 km rasters with licensing for higher-resolution vector and 25 m products; licensing considerations should be planned in data governance and cost models.