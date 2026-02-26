# LCM2000 Final Report

- Purpose and scope
  - Develop a UK-wide Broad Habitat (BH) framework to support the Biodiversity Action Plan (BAP) and map terrestrial, freshwater, and coastal habitats using satellite-derived spectral data (LCM2000) with external contextual datasets.
  - Calibrate LCM2000 against CS2000 field survey data to produce BH cover statistics comparable to field results.

- Broad Habitats and LCM2000 classifications
  - LCM2000 is a spectral-classification map with thematic components (Target classes, Subclasses, Variants) that are aggregated to BHs for reporting.
  - BHs include Broad-leaved/mixed/yew woodland, Coniferous woodland, Arable and horticultural land, Improved and Neutral grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog (deep peat), Montane habitats, Inland bare ground, Built-up areas/gardens, Coastal habitats (Supralittoral/Littoral), Water (inland), and Boundaries/linear features (not targeted as BHs).
  - Mapping compromises: spectral similarity between BHs, peat depth for bog vs heath, and management-driven distinctions (e.g., neutral vs calcareous vs acid grasslands) introduce interpretive differences with field data.

- Map display and data integration
  - Display classes balance reliability and pattern visibility; some small or rare BHs are aggregated at national/regional scales.
  - Distinctions between BHs and LCM2000 classes reflect reading across spectral data, with some components shown at Variant level for utility.

- CS2000 field survey calibration data and methods
  - CS2000 field survey (FS) provides detailed ground information for 569 one-kilometre squares (Britain), with a separate NI dataset not digitally accessible for testing.
  - Not ground-truth: FS has higher spatial resolution and different data structure; calibration emphasizes understanding correspondence and calibration rather than pure validation.
  - Three main testing approaches:
    - Per-pixel: direct overlay of FS and LCM2000.
    - Per-segment: LCM2000 segment labels aligned with FS dominant class.
    - Per-parcel: FS parcels labeled against LCM2000-derived parcel labels.

- Calibration tests and measures of correspondence
  - Bootstrapped confidence limits (95%) developed to quantify correspondence across GB, England/Wales, and Scotland.
  - Correlation measures by level:
    - Per-pixel correspondence at BH level: GB 54% (95% CI 53–56%), England/Wales 60% (58–62%), Scotland 44% (40–47).
    - Per-segment correspondence (BH level): GB 58% (57–60%), England/Wales 64% (62–66%), Scotland 47% (43–50).
    - Per-parcel correspondence (BH level): GB 62% (60–64%), England/Wales 69% (67–72%), Scotland 48% (44–52).
  - At Target class level, correspondence improves:
    - GB: about 65% (parcel-based)
    - England/Wales: about 73%
    - Scotland: about 51%
  - Differences arise from FS’s higher resolution, timing differences between FS and LCM2000 imagery, class-definition differences, and MMU disparities (FS ~0.04 ha vs LCM2000 >0.5 ha).

- Class-level and aggregate accuracy
  - Broadleaved/mixed and Coniferous woodland cover is similar in UK totals between LCM2000 and FS, but per-square agreement is lower due to small woodland features falling below LCM2000’s minimum mapping unit.
  - Arable and horticultural land: LCM2000 slightly higher than FS; confusion between arable and improved grassland contributes to error.
  - Improved vs semi-natural grasslands: significant mismatch; FS often labels improved grassland where LCM2000 assigns neutral grassland due to spectral limitations in distinguishing management practices.
  - Neutral, calcareous, and acid grasslands: poor separation by spectral data; underlying soil acidity maps can improve but residual misclassifications remain.
  - Bracken, bogs, montane habitats, inland bare ground: notable mismatches driven by timing (May imagery for bracken, peat-depth masking for bogs) and contextual rules; deep peat bogs require peat-depth context to distinguish from heath.
  - Water bodies and coastal BHs: generally small and challenging to map consistently; inland water results align reasonably with FS for standing water on a broad scale; coastal BHs are difficult due to tidal state and resolution limits.
  - Boundary and linear features: FS captures many of these; LCM2000 intentionally excludes most linear features (>0.5 ha area threshold) and rivers/streams in calibration, contributing to differences.

- Change detection
  - Between 1990 and 2000, landscape changes are likely small and challenging to detect with satellite mapping alone; timeliness and resolution differences complicate change detection.
  - An intelligent, pattern-informed approach is recommended to separate true changes from classification and data-structure errors, leveraging CS2000/FS baselines and other data sources.
  - Future work aims to generate Broad Habitat statistics through direct calibration against field surveys to improve change analyses.

- Practical implications and future work
  - Recognize that LCM2000 provides comprehensive coverage but with accuracy limitations at finer scales, especially for small or spectrally similar BHs.
  - Integrate FS data with LCM2000 and external datasets to refine BH distributions, particularly for peat/bog, semi-natural vs improved grasslands, and urban/suburban heterogeneity.
  - Develop improved change-detection methodologies that account for known calibration biases (e.g., MMU, timing, and class-definition differences).
  - Appendix and Appendix I offer detailed mappings of LCM2000 variants to BHs and articulations of distinguishing features to guide future refinement and potential reclassification efforts.

- Appendix I: distinguishing features overview
  - Highlights why spectral data alone cannot reliably separate many BHs (e.g., broad-leaved vs coniferous woodland, neutral vs calcareous vs acid grassland).
  - Emphasizes the role of non-spectral information (site conditions, soil pH maps, peat depth, land management) to improve classification accuracy.
  - Outlines target-class and subclass distinctions and their practical mapping implications for various BHs, including woodland, arable land, grasslands, bracken, bogs, wetlands, water, and urban areas.