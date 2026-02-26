# LCM2000 Final Report

- Purpose and scope
  - Assess and calibrate the LCM2000 broad habitat classification against field survey data (CS2000) to support habitat statistics under the UK Biodiversity Action Plan.
  - Map Broad Habitats (BHs) using a 1 km field survey framework and a 25 m satellite-derived classification, with attention to Target classes, Subclasses, and Variants.

- Classification framework
  - BHs are the reference categories; LCM2000 classes are cross-walked to BHs through Target classes, Subclasses, and Variants.
  - Map displays use aggregated levels to balance reliability and pattern clarity; some BHs are grouped for national/regional plotting.
  - The classification includes major groups such as Broadleaved/mixed forests, Coniferous forests, Arable/horticulture, Grasslands (improved, neutral, calcareous, acid), Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland water and bare ground, Montane and Coastal/Habitat components; Boundary/linear features are excluded from BH mapping in calibration.

- Data and sources
  - CS2000 field survey: 569 one-kilometre squares in GB (549 in 1998, others in 1999), detailed field observations; not ground truth but used for calibration.
  - FS vs LCM2000: Differences in resolution (FS ~1 m vs LCM2000 ~25 m), timing, and class definitions; calibration rather than strict validation.

- GIS methodology and tests
  - ARC/Info (BH-labeled) mapping created for all CS2000 squares and equivalent LCM2000 map sections.
  - Three main tests:
    - Per-pixel: direct overlay comparisons (low accuracy due to resolution and MMU differences).
    - Per-segment: dominant FS class within LCM2000 segments.
    - Per-parcel: FS parcels vs LCM2000-derived parcel labels.
  - Correspondence levels evaluated at BH, Target class, and Aggregate class levels; confidence limits derived via bootstrapping.

- Confidence limits and key results
  - Per-pixel correspondence (GB): 54% (95% CI 53–56%); England & Wales: 60% (CI 58–62%); Scotland: 44% (CI 40–47%).
  - Per-segment correspondence (GB): 58% (CI 57–60%); England & Wales: 64% (CI 62–66%); Scotland: 47% (CI 43–50%).
  - Per-parcel correspondence (GB): 62% (CI 60–64%); England & Wales: 69% (CI 67–72%); Scotland: 48% (CI 44–52%).
  - Target class (parcel-based) correspondence: GB 65%; England & Wales 73%; Scotland 51%.
  - Overall assessment: FS repeatability ~88% limits maximum achievable; LCM2000 performance approximates ~72% of that maximum for BH-targeted analyses; realistic ~85% accuracy at the Target class level considered.
  - Major sources of non-correspondence: resolution (MMU differences; FS parcels >0.04 ha vs LCM2000 MMU >0.5 ha), timing differences (1990 vs 1998–2000 imagery), class-definition differences, and specific survey/interpretation variances.

- Issues by habitat type and cross-walk considerations
  - Woodlands: fine-scale boundaries cause mismatches; small woodlands often excluded by MMU, leading to FS woodland appearing as grassland or arable in LCM2000.
  - Arable vs Built-up: spectral confusions; rotation and crop staging affect accuracy.
  - Grasslands: distinguishing improved vs semi-natural and Neutral/Calcareous/Acid grasslands is challenging spectrally; Rough grasslands often mapped as Neutral by LCM2000.
  - Semi-natural vs improved grassland and peat-related distinctions (bogs) show substantial interpretation differences; peat depth and soil acidity maps are used to adjust classifications in some areas.
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bogs: substantial mapping differences due to spectral ambiguity and definitions; peat-depth-based rules used to reclassify some areas (e.g., peat >0.5 m).
  - Montane and inland bare ground: altitude-based and context-based distinctions can lead to misclassifications in upland/extensive areas.
  - Coastal BHs: intertidal zones and tidal state complicate direct mapping; coastal BHs treated as aggregates for national reporting.

- Change detection and temporal considerations
  - Detecting landscape changes between 1990 and 2000 is constrained by data differences; satellite-based mapping alone is insufficient for robust change detection.
  - Segment-based classification yields different change signals than 1990 raster products; integration with field surveys and intelligent change-detection approaches is recommended.
  - Calibration results note under- and over-estimates for 2000, which should inform change analyses.

- Practical implications for GIS use
  - LCM2000 provides broad, consistent national/regional habitat mapping with comprehensive coverage, suitable for map-based data products and policy communication.
  - Calibration to CS2000 enhances ability to derive BH statistics from the broad LCM2000 dataset, leveraging FS-derived precision.
  - Users should account for MMU-related limitations, temporal offsets, and classification ambiguities when using LCM2000 for change detection or fine-scale analyses.
  - The Appendix and Table 2 document cross-walks between LCM2000 Variants and BHs, useful for implementation and legend design in map products.

- Conclusions and future directions
  - LCM2000 achieves substantial correspondence with CS2000 at aggregate and Target class levels, though per-pixel and some habitat-specific mappings show notable discrepancies.
  - A recommended path includes re-examining bogs and heaths with integrated FS and external data, and developing calibrated Broad Habitat statistics directly from LCM2000 plus field data.
  - Ongoing refinement of the classification (especially for Neutral/Calcareous/Acid grasslands, bogs, and rough grasslands) and improved change-detection methods are planned.

- Appendix and mapping details (for GIS implementation)
  - Table 2 presents LCM2000 Variant mappings to BHs with color codes, aiding visualization and legend creation.
  - Appendix I provides a brief review of Broad Habitats with distinguishing features and notes on spectral/classification limitations.