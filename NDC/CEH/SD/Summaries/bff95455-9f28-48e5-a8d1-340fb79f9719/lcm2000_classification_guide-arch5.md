LCM2000: A Broad Habitat Classification and its Calibration Against CS2000 Field Survey

# Overview
- UK-wide project to map Broad Habitats (BHs) by linking a spectral image classification (LCM2000) with field-based definitions (CS2000) to support biodiversity reporting under the UK Biodiversity Action Plan.
- LCM2000 is a thematic classification of satellite data that can be aggregated to BHs and other broader schemes; maps are designed for national/regional use with practical display classes.
- The work distinguishes between BHs, Target classes, Subclasses, and Variants; aggregates are used for reporting where needed.

# Data Model and Classification
- Broad Habitats (BHs) are the primary framework; LCM2000 classes (Target, Subclass, Variant) map to BHs with crosswalks and read-across where exact matches are complex.
- Classes and schemes:
  - Narrow to broad structure: Broad Habitats (BHs) -> Target classes -> Subclasses -> Variants.
  - Aggregate 10-class level used for reporting to align with BH aggregations.
- Display and mapping conventions:
  - Map displays balance reliability and pattern visibility; some rare BHs are aggregated at map scale.
  - Coastal and marine features are treated as aggregates; intertidal areas and detailed coastal distinctions have limited accuracy at 1 km resolution.
- Data resolution and scope:
  - Spatial unit: 1 km squares for CS2000 field data; 25 m image parcels underpin LCM2000.
  - Minimum mappable unit: 0.5 ha for LCM2000 versus 0.04 ha for CS2000 field data.
  - Linear features and some boundaries are not targeted as BHs in LCM2000 due to resolution limits; FS (field survey) captures many of these.

# Calibration and Accuracy Assessment
- Objective: assess how well LCM2000 corresponds to CS2000 field survey data and calibrate BH statistics accordingly.
- Methods:
  - Three comparison levels: per-pixel (overlay), per-segment (dominant FS class within LCM2000 segments), and per-parcel (FS parcel class mapped from LCM2000 segments).
  - Correspondences calculated at BH level (excluding some features), Target class level, and Aggregate class level.
  - Confidence limits produced via bootstrapping to provide 95% intervals.
- Key results (Great Britain, with country-specific details):
  - Per-pixel correspondence (BH level): GB 54% (95% CI 53–56%), England & Wales 60% (58–62%), Scotland 44% (40–47%).
  - Per-segment correspondence: GB 58% (57–60%), England & Wales 64% (62–66%), Scotland 47% (43–50%).
  - Per-parcel correspondence: GB 62% (60–64%), England & Wales 69% (67–72%), Scotland 48% (44–52%).
  - Target class level (weighted by land class): higher than BH level.
    - Per-parcel: GB 65% (GB), England & Wales 73% (England/Wales combined), Scotland 51%.
  - Aggregate (close BH match) level: generally higher concordance; patterns vary by habitat type.
- Interpretation and caveats:
  - Differences arise from:
    - Resolution and MMU mismatches (1 km vs 0.04 ha).
    - Time lags between field surveys (1998–1999 CS2000 vs 1998–2001 LCM2000 imagery).
    - Fundamental classification differences (spectral/class vs field-based definitions; BH vs Target).
    - Some misclassification due to spectral ambiguity (e.g., arable vs grassland, semi-natural vs improved grassland).
  - Overall, LCM2000 is estimated to achieve around 85% accuracy at the Target class level and about 72–87% potential accuracy depending on the level of aggregation and region.
- Notable habitat-specific issues:
  - Broadleaved/mixed woodland and coniferous woodland: good overall coverage but subdivision and boundary outlines differ; many small woodlands fall below LCM2000’s 0.5 ha MMU.
  - Arable and horticultural land: misclassifications with grassland; some rotation effects due to year differences.
  - Grasslands: distinguishing neutral, calcareous, and acid grasslands is challenging spectrally; rough grasslands often misclassified.
  - Semi-natural vs improved grasslands: substantial differences in FS vs LCM2000 mappings due to management history and context not captured spectrally.
  - Bracken, bogs, fen/marsh/swamp, montane, inland bare ground, and coastal categories show notable discrepancies due to definitions (peat depth, altitude, coastal masking) and limited field-plot representativeness.
  - Built up areas and coastal mosaics: LCM2000 separates urban/rural development and vegetated open spaces more explicitly than CS2000; FS tends to map urban land differently.
- Change detection:
  - Satellite-only change detection between 1990 and 2000 is limited and should be interpreted with caution; a robust approach should combine FS benchmarks (1990, 1998) with LCM2000 results to identify probable changes and distinguish them from classification error.
  - Intelligent, pattern-based change analysis is recommended for future work, leveraging historical field surveys to guide interpretation.

# Change Detection and Temporal Considerations
- Real landscape changes between 1990 and 2000 are likely small and often obscured by methodological differences.
- The classification framework precludes direct 1990 BH comparisons; segment-based approaches differ from 1990 raster outputs.
- Future work suggests integrating CS2000/FS data with LCM2000 to identify probable changes and reduce misinterpretation due to data structure.

# Data Availability, Documentation, and Governance Implications
- Output expectations:
  - Direct calibration against field surveys to derive Broad Habitat statistics across the land surface.
  - Documentation of class definitions, image selection, pre-processing, and calibration in the Final Report, with a mid-March release window.
- Metadata and provenance considerations for Data Stewards:
  - Explicit documentation of spatial resolution (1 km; 25 m parcel foundation), MMU differences, and data sources (CS2000 FS vs LCM2000 imagery years).
  - Clear articulation of alignment between BHs, Target classes, Subclasses, and Variants; provide crosswalk tables and color schemes (e.g., Table 2 mappings with color codes) for reproducibility.
  - Transparent reporting of accuracy metrics by region and class level, including confidence intervals and known sources of error (time lags, spectral ambiguity, boundary delineation).
  - Note that “ground truth” is not provided; CS2000 is a calibration dataset with repeatability limitations (88% repeatability for primary FS codes); spatial boundaries in uplands are hard to map consistently.
  - Change-detection results should be presented with caveats about data structure and potential classification bias; use knowledge-based corrections and historical surveys to guide interpretation.
- Appendix I and class explanations:
  - Appendix I provides detailed distinctions for Broad Habitats (e.g., broadleaved/mixed woodland, coniferous woodland, arable, grasslands, bracken, bogs, fen/marsh/swamp, montane, inland rock, built-up areas, coastal habitats, etc.), highlighting where spectral data alone may misclassify and where context (soil pH, peat depth, altitude) informs interpretation.
  - The document includes a comprehensive crosswalk (Table 2) mapping LCM2000 Variant/Alpha codes to BHs with color representations, useful for data integration and visualization.

# Appendix: Broad Habitats and Distinguishing Features (for interpretation)
- Broad Habitats cover a wide range of land covers, with notable complexities in spectral separation (e.g., Neutral/Calcareous/Acid grasslands; rough vs improved grasslands; peat depth distinguishing bogs).
- Key distinctions highlight where LCM2000 can reliably map and where field context is essential for accurate classification.
- This appendix informs Data Stewards about the semantic definitions behind BH labels, aiding consistent metadata creation and cross-dataset interoperability.