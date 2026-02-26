# LCM2000 Final Report

- Purpose: Calibrate and assess the LCM2000 Broad Habitat (BH) classification against CS2000 field survey (FS) data to enable BH cover statistics and improve mapping interpretation across GB, England/Wales, and Scotland.
- Scope: Comparison between satellite-derived LCM2000 classifications and detailed FS data across multiple thematic levels (BH, Target class, Aggregate class) using three correspondence methods (per-pixel, per-segment, per-parcel).

## Data and Methods

- Data sources:
  - CS2000 field survey (FS): 569 one-kilometre squares in GB (1998–1999; NI data not digitised for testing).
  - LCM2000: Thematic classification of spectral satellite data with external context; aims to map BHs and provide Target class details and Variants.
- GIS and analysis:
  - ARC/Info coverage files created for FS squares and LCM2000 map sections.
  - 569 correspondence matrices generated (one per 1 km square).
  - Three main tests:
    - Per-pixel: direct overlay comparison (spatial differences).
    - Per-segment: LCM2000 segment labels vs FS dominant class.
    - Per-parcel: FS parcels vs LCM2000-derived parcel labels.
  - Correspondence levels:
    - BH level (excluding boundaries, rivers/streams)
    - Generalised urban vs non-urban adjustments
    - Target class level
    - Aggregate class level
- Confidence limits:
  - Bootstrapping to produce 95% confidence intervals for correspondence measures.
- Regional splits:
  - GB, England/Wales, Scotland; results weighted by National Land Classes.

## Key Findings

- Overall correspondence (GB, weighted bootstrapped):
  - Per-pixel: 54% (95% CI 53–56%)
  - Per-segment: 58% (95% CI 57–60%)
  - Per-parcel: 62% (95% CI 60–64%)
- Regional breakdown:
  - England & Wales:
    - Per-pixel: 60% (CI 58–62%)
    - Per-parcel: 69% (CI 67–72%)
    - Per-segment: 64% (CI 62–66%)
  - Scotland:
    - Per-pixel: 44% (CI 40–47%)
    - Per-parcel: 48% (CI 44–52%)
    - Per-segment: 47% (CI 43–50%)
- BH-level vs FS:
  - BH-level match: Britain 58% (CI 57–60%), England/Wales 64% (CI 62–66%), Scotland 47% (CI 43–50%)
- Target class level:
  - Higher correspondence than BH level:
    - GB (parcel-based): 65%
    - England/Wales: 73%
    - Scotland: 51%
- Interpretation of accuracy:
  - FS repeatability: 88% for primary FS codes (ground-truth-like repeatability is limited).
  - LCM2000 performance relative to maximum potential: about 72% alignment with FS; realistic target around 85% accuracy at the Target class level.
  - Time and resolution differences contribute to mismatches:
    - FS higher original spatial resolution; LCM2000 MMU of >0.5 ha vs FS >0.04 ha
    - Images largely from 1998–2001 vs FS mainly 1998
    - Class-definition differences and potential FS labeling errors
- Change detection:
  - Between 1990 and 2000 changes likely small; satellite mapping alone has limits for precise change detection.
  - Segment-based LCM2000 results differ from 1990 raster products; integration with FS and other data recommended for change analysis.

## Class-Level Assessments and Issues

- Woodland (Broadleaved/mixed and Coniferous):
  - FS records many small woodlands excluded by LCM2000’s 0.5 ha minimum; leads to woodland features mapped as grassland or arable in FS and vice versa.
  - Coniferous woodland shows higher direct correspondence (70%) when present in larger blocks.
- Arable and horticultural land:
  - Misclassification between arable and built-up areas; rotation differences across years impact spectral signatures.
- Grasslands:
  - Improved vs semi-natural grassland distinctions are challenging; around 20% FS improved grassland appears as semi-natural in LCM2000.
  - Neutral, Calcareous, and Acid grasslands: spectral distinctions are weak; soil pH and soil acidity masking affect separation.
  - Bracken and dwarf shrub heath: spectral mapping differs; bog vs heath distinctions depend on peat depth and context.
- Fen, marsh, swamp; bogs:
  - FS shows more fen/marsh than LCM2000, largely due to differences in how rush pastures and wetlands are classified.
  - Peat depth used to separate bogs; LCM2000 peat mask often yields a smaller bog extent than FS.
  - Montane and inland rock issues due to accessibility and altitude-based definitions.
- Inland water and coastal habitats:
  - Inland water (standing water/canals) generally aligns with FS for >0.5 ha; narrow waterways less well captured.
  - Coastal BHs (supra-littoral and littoral) are small; most data are aggregated for reporting due to resolution limits.
- Urban and built-up:
  - FS treated urban land as continuous, while LCM2000 separates built-up areas from open spaces (suburban/rural development vs continuous urban). This leads to differences in urban extent mapping.

## Change Detection and Future Work

- Intelligent change detection approaches:
  - Use FS-derived change expectations (e.g., from Haines-Young et al. 2000) to better distinguish real change from classification error.
  - Calibrate LCM2000 change signals against FS trends and other external data sources.
- Follow-up improvements:
  - Re-examine bogs and heath with integrated data (FS, peat datasets, other maps) to refine peat-related classifications.
  - Expand calibration to generate Broad Habitat statistics directly from calibrated HS vs FS data.
  - Continue development of methods to unify multi-source data with differing resolutions and scales.

## Practical Summary for Analysts

- LCM2000 provides broad, national-scale BH maps with substantial coverage and improved consistency, but notable mismatches exist due to scale, time, and classification differences.
- Expect around 60%–70% per-pixel/segment/parcel correspondence at GB level, with higher alignment at the Target class level (around 65%+ GB; ~73% England/Wales; ~51% Scotland for parcels).
- The approach to accuracy should be contextualized: FS is not ground truth; its 88% repeatability bounds achievable accuracy of LCM2000 to around 72% of maximum potential, with 85% plausible at the Target class level.
- When using LCM2000 data for change analyses or policy decisions, account for known biases in woodland, grassland, bogs, and urban classifications, and leverage integrated datasets and intelligent change-detection methods to improve reliability.