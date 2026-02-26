# LCM2000 Final Report

- Purpose and context
  - Aimed to support UK Biodiversity Action Plan by mapping Broad Habitats (BHs) across terrestrial, freshwater, and coastal systems.
  - LCM2000 is a thematic classification of Landsat-based spectral data, integrated with external datasets to refine mapping and support reporting against BHs and related land-cover schemes.
  - The report discusses calibration of LCM2000 against CS2000 field survey data and the development of BH statistics from comprehensive LCM2000 coverage.

- BHs and LCM2000 classes
  - BHs are broad habitat types defined by vegetation/community structure; LCM2000 classes are spectral, with Subclasses and Variants providing finer distinctions where possible.
  - Variants reflect thematic components of Target BH classes; where distinctions are ambiguous, Aggregate classes are used for reporting to align with BH concepts.
  - Map displays use BH nomenclature, with some aggregation to ensure patterns are visible at regional/national scales.
  - Specific coastal BHs (Supralittoral/Littoral) and linear features are treated as aggregates or context-dependent due to resolution limits.

- Map display and data integration
  - Displays align with BHs but may aggregate rare/dissected classes to improve readability at national/regional scales.
  - Some distinctions (e.g., semi-natural vs. improved grasslands; flora/fauna indicators) are more precisely captured in Subclasses or Variants rather than BH level.

- Calibration against CS2000 field survey (FS)
  - FS surveyed 569 one-km squares in GB (549 in 1998; rest in 1999); NI data not digitally available for testing.
  - FS provides detailed field classifications, not ground truth; calibration addresses how well LCM2000 maps correspond to FS classifications.
  - Calibration approach includes per-pixel, per-segment, and per-parcel comparisons between FS labels and LCM2000 outputs, across BH, Target class, and Aggregate class levels.
  - Three comparison schemes:
    - Per-pixel: direct overlay differences (sensitive to resolution and MMU differences).
    - Per-segment: dominant FS class within LCM2000 segments.
    - Per-parcel: FS parcels versus LCM2000-derived parcel labels.

- Confidence limits and accuracy assessment
  - Bootstrapping used to estimate 95% confidence intervals for correspondence measures.
  - Overall GB per-pixel correspondence: ~54% (95% bounds 53–56%); England & Wales ~60% (bounds 58–62%); Scotland ~44% (bounds 40–47%).
  - Per-segment correspondence: GB ~58% (bounds 57–60%); England & Wales ~64% (bounds 62–66%); Scotland ~47% (bounds 43–50%).
  - Per-parcel correspondence: GB ~62% (bounds 60–64%); England & Wales ~69% (bounds 67–72%); Scotland ~48% (bounds 44–52%).
  - Target-class correspondence generally higher than BH-level due to aggregation and FS generalisation; online figures show GB parcel-based ~65% and England & Wales ~73%.
  - Key factors in mismatches: higher FS spatial resolution, time differences between FS and LCM2000 imagery, differences in class definitions, and MMU differences (FS >0.04 ha vs LCM2000 >0.5 ha).

- Major findings by class and region
  - Woodland (Broadleaved/mixed and Coniferous)
    - Similar total woodland cover between LCM2000 and FS, but significant differences in mapped boundaries due to small stands (<0.5 ha) being excluded by LCM2000.
    - Coniferous woodland shows relatively high direct correspondence (~70%) when present in larger blocks.
    - Broadleaved/mixed woodland shows lower direct agreement due to small patches being captured by FS but not by LCM2000.
  - Arable and horticultural land
    - LCM2000 and FS estimates differ; misclassifications between grass, arable, and improved grassland contribute to errors (roughly 20% of FS arable recorded as semi-natural by LCM2000 and vice versa).
    - Confusion between arable and built-up land also occurs, often linked to spectral signatures of part-grown crops.
  - Grasslands
    - Improved grassland is generally well-classified, but distinguishing Neutral/Calcareous/Acid grasslands is difficult spectrally.
    - Rough grasslands are problematic; FS often records these as Improved grassland, while LCM2000 treats many rough swards as Neutral grassland, contributing to differences.
  - Semi-natural/ericaceous swards and peat-related habitats
    - Distinctions among Neutral, Calcareous, and Acid grasslands are challenging; spectral masks (including soil acidity) limit accuracy.
    - Bracken mapping is challenging; much bracken is recorded only at Subclass level and may be misclassified in some habitats.
    - Bogs (deep peat) show strong sensitivity to peat-depth assumptions; LCM2000’s peat-mask approach tends to under-represent peatlands compared with FS, prompting planned follow-up integration with external peat maps and FS data.
  - Montane, Inland bare ground, and coastal habitats
    - Montane habitats are difficult to capture accurately due to limited field access and altitude-based criteria.
    - Inland bare ground contributions are relatively small but can be overrepresented in LCM2000 due to urban-context misclassifications; FS includes more urban open spaces.
    - Coastal BHs (Supralittoral/Littoral) are minor and sensitive to tidal timing; both methods have limited accuracy at the 1-km scale for these features.

- Change detection
  - Detecting landscape change between 1990 and 2000 with satellite data alone is challenging due to resolution, timing, and classification differences.
  - The segment-based BH approach helps, but robust change detection requires intelligent fusion with FS data and prior knowledge of known change patterns.
  - Future work proposes using FS-based change expectations and probabilistic classification to better distinguish real change from error.

- Data integration and follow-up
  - Full calibration report details (image selection, preprocessing, classification) are in the forthcoming Final Report.
  - Planned re-examination of bogs and heaths with integrated LCM2000, FS, and external datasets to improve peat-related classifications.
  - Development of direct Broad Habitat statistics through calibration against field data to leverage the comprehensive coverage of LCM2000 with field precision.

- Appendix and supplementary material
  - Appendix I provides a brief review of Broad Habitats with distinguishing features and notes on spectral and contextual mapping limitations.
  - Table 2 maps LCM2000 class Variants to BHs with color codes and descriptive aliases.

- Overall interpretation
  - LCM2000 provides broad, nationally coherent habitat maps with substantial coverage but not a perfect match to detailed field classifications.
  - The approach emphasizes aggregation (Target/Aggregate BHs) where necessary to maintain robust, usable outputs for national and regional reporting, while acknowledging limitations due to resolution, timing, and spectral ambiguity.
  - The results indicate a realistic expectation of approximately 85% Target-class level accuracy, given FS repeatability and data constraints, with room for improvement through integrated data analyses and future calibration efforts.