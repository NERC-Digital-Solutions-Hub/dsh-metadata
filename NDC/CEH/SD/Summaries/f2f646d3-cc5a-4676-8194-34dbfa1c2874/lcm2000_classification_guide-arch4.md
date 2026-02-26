# LCM2000 Final Report

- Overview and purpose
  - Aimed to support UK Biodiversity Action Plan by mapping Broad Habitats (BHs) across the UK using the LCM2000 satellite-derived classification, while also recording detailed habitat information beyond BHs where possible.
  - Intended to calibrate LCM2000 outputs against CS2000 field survey data to enable BH statistics from comprehensive satellite coverage.
  - Emphasises integration of satellite data with field observations and external datasets to refine classifications and support reporting.

- Data, classifications and map display
  - LCM2000 is a thematic classification derived from satellite spectral data, with external/contextual data added to refine classifications.
  - BHs are the primary framework; Target classes and Subclasses provide more detailed distinctions, with Variants capturing within-class spectral/contextual differences.
  - Aggregate classes combine Target/Subclass data to 10-class levels for reporting and crosswalks to BHs.
  - Map displays prioritize reliability and pattern visibility; some rare or highly detailed classes are aggregated at national/regional scales to maintain legibility.
  - Several habitat categories are treated as aggregates (e.g., coastal BHs, inland water bodies) due to resolution constraints; linear boundaries (Boundaries and rivers) are not targeted in LCM2000.

- CS2000 field survey calibration and methodology
  - CS2000 field survey covered 569 one-km squares in Great Britain (549 in 1998, rest in 1999); Northern Ireland data not digitally available for testing.
  - Field survey data are detailed but not “ground truth”; they serve for calibration rather than validation.
  - An independent QA check showed 88% repeatability for primary codes used to generate BH labels.
  - Three comparison modes were used: per-pixel (pixel-level), per-segment (segment dominance by FS labels), and per-parcel (FS parcels vs LCM2000-derived parcels).
  - Comparisons were conducted at multiple thematic levels: BH level (excluding certain features), urban/generalized, Target class level, and Aggregate class level.

- Confidence and accuracy findings
  - Per-pixel correspondence (Britain): ~54% (95% CI 53–56%); England & Wales ~60% (CI 58–62%); Scotland ~44% (CI 40–47%).
  - Per-segment correspondence (Britain): ~58% (CI 57–60%); England & Wales ~64% (CI 62–66%); Scotland ~47% (CI 43–50%).
  - Per-parcel correspondence (Britain): ~62% (CI 60–64%); England & Wales ~69% (CI 67–72%); Scotland ~48% (CI 44–52%).
  - Target class level correspondence is higher than BH level for all tests: GB parcel-based ~65%, England & Wales ~73%, Scotland ~51%.
  - Overall interpretation: maximum achievable alignment is limited by intrinsic differences in resolution, timing, and class definitions; FS repeatability (88%) bounds the ceiling. Realistic expectation for Target class accuracy is around 85% (roughly 87% suggested for some measures).

- Key habitat-specific insights
  - Woodland: LCM2000 and FS show similar broad cover for Broadleaved/mixed and Coniferous woodland, but direct agreement is lower due to small woodlands often below LCM2000’s 0.5 ha minimum mapping unit.
  - Arable and horticultural land: LCM2000 estimates are slightly higher due to generalized representation of small features; misclassification with grassland and improved grassland exists.
  - Grasslands: Distinguishing Improved vs Semi-natural (Neutral/Calcareous/Acid) is challenging; Rough grasslands are treated differently by FS and LCM2000, producing notable differences.
  - Semi-natural vegetation (neutral, calcareous, acid grasslands) and Bracken: spectral methods struggle to consistently separate these; field observations use species and management context not available to imagery alone.
  - Fen, marsh, swamp, bogs: FS identifies more of these than LCM2000; peat depth is a key criterion used to distinguish bog from heath, with peat-based masks potentially underestimating bog extent.
  - Montane and Inland bare ground: altitude-based definitions and context lead to mismatches (e.g., Montane areas and inland bare ground often poorly aligned with FS classifications).
  - Coastal habitats: small, often at or below resolution; inter-tidal areas and shoreline mapping are not consistently matched between FS and LCM2000.
  - Water and built-up areas: inland water bodies are mapped when they exceed 0.5 ha and width criteria; FS often records more urban/open spaces, causing differences in Built up vs grassland/water allocations.
  - Boundary and linear features: not targeted by LCM2000; FS captures these as distinct BHs, creating notable differences in corresponding measurements.

- Change detection and future work
  - Between 1990 and 2000 changes are expected to be small; satellite data alone is insufficient for robust change detection at national scale.
  - An intelligent, coordinated approach is recommended: combine LCM2000 outputs with FS data and other external datasets to attribute observed changes to real habitat shifts vs classification errors.
  - The project plans to refine calibration by directly linking Broad Habitat statistics to field survey data, enabling more accurate large-scale BH quantities.
  - Future work includes re-examining LCM2000 bogs and heaths with integrated FS and external data to improve consistency and accuracy.

- Limitations and data governance considerations
  - The 25 m pixel grid and 0.5 ha minimum mapping unit create inherent differences from the field-scale FS data (0.04 ha), affecting small features and patch-level accuracy.
  - Time differences between field surveys (1998–1999) and satellite imagery (1990s–2000s) introduce discrepancies due to landscape changes and seasonal effects.
  - Spectral similarity and lack of site-specific context (management practices, soil chemistry) limit reliable separation of several semi-natural grassland and peatland categories.
  - The document emphasizes that LCM2000’s accuracy should be assessed at Target class level rather than BH level for most practical purposes.

- Appendix I: Broad Habitats and mapping considerations
  - Provides a detailed guide to distinguishing features of BHs (e.g., woodland types, arable vs non-rotational crops, improved vs semi-natural grasslands) and notes the limitations of remote sensing for fine-scale discrimination.
  - Highlights the role of field knowledge, soil maps (e.g., peat depth, soil pH), and contextual corrections in achieving more accurate classifications.
  - Describes the behavior of several BH categories under spectral classification and how some categories (like rough grassland, bog, and fen) are treated or challenging to separate in LCM2000.
  - Emphasizes the need for integrated analysis and potential refinements (e.g., Variant-level distinctions) to improve future mapping accuracy.

- Data governance and accessibility
  - The Final Report promises full details on image selection, preprocessing, classification, and calibration in a forthcoming release.
  - The integration approach aims to leverage the broad coverage of LCM2000 with the precision of field surveys to produce Broad Habitat statistics for reporting and planning.