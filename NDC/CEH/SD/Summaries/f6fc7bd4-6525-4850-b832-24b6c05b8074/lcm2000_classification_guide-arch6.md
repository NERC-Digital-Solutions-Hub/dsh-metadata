LCM2000: A Broad Habitat Classification for the UK (Calibration and Assessment against CS2000 Field Survey)

- Purpose and scope
  - LCM2000 is a satellite-derived, thematic classification of UK broad habitats (BHs) intended to support biodiversity planning and reporting under the UK Biodiversity Action Plan.
  - Aims to map widespread terrestrial, freshwater, and coastal BHs while providing contextual data and enabling aggregation to 10-class reporting.
  - BHs are linked to Target classes and Subclasses; aggregates are used for presentation and statistics.

- Data structure and classification framework
  - Spectral classes from satellite data are combined into thematic components (Target classes and Subclasses) to form BHs.
  - Variants represent spectral/contextual components and are recognized where possible (e.g., specific crops).
  - Map displays emphasize reliability and pattern visibility; rare or small classes are aggregated for national/regional maps.
  - BHs are sometimes mapped with compromises in accuracy; differences in definitions can cause read-across mismatches with Target classes.
  - Some BHs are treated as Aggregate Coastal habitats or other aggregates for reporting; linear features and certain boundaries are not targeted as BHs at the same resolution.

- Calibration dataset and approach
  - CS2000 field survey (FS) data used to assess LCM2000 quality and to calibrate BH statistics from LCM2000 data.
  - FS surveyed 569 one-kilometre squares in GB (549 in 1998, others in 1999); additional NI data not digitally available for testing.
  - FS provides detailed information but is not ground truth; inter-method repeatability of primary FS codes was 88%.
  - Calibration focused on aligning LCM2000 with FS to produce BH cover statistics comparable to FS while leveraging the broader coverage of LCM2000.

- Verification and comparison methodology
  - GIS workflow: generated 569 correspondence matrices (one per 1 km square) comparing FS and LCM2000 at multiple thematic levels.
  - Comparison modes:
    - Per-pixel: direct overlay to measure overall differences (low alignment due to resolution and mapping processes).
    - Per-segment: FS-dominant class within LCM2000 segments.
    - Per-parcel: FS parcel labels versus LCM2000-derived labels.
  - Thematic levels of comparison:
    - BH level (excluding boundaries/streams at below LCM2000 resolution)
    - Generalized urban/non-urban (to match FS generalization)
    - Target class level
    - Aggregate class level (closest alignment with BH aggregations)

- Confidence and accuracy assessment
  - Bootstrapping used to establish 95% confidence limits for correspondence.
  - Overall correspondence (GB, per-pixel): ~54% (95% CI 53–56%); England & Wales: ~60% (CI 58–62%); Scotland: ~44% (CI 40–47%).
  - Per-parcel correspondence: GB ~62% (CI 60–64%); England & Wales ~69% (CI 67–72%); Scotland ~48% (CI 44–52%).
  - Per-segment correspondence: GB ~58% (CI 57–60%); England & Wales ~64% (CI 62–66%); Scotland ~47% (CI 43–50%).
  - Target class level correspondence generally higher than BH level (GB parcel ~65%; England & Wales ~73%; Scotland ~51%).
  - Aggregate class level: close matches between LCM2000 and FS; differences largely due to resolution and conceptual mapping differences.
  - Limitations noted:
    - FS resolution (0.04 ha MMU) vs LCM2000 MMU (>0.5 ha) causes mislabellings for small features.
    - Time differences between FS (1998–1999) and LCM2000 imagery (1998–2001).
    - Class-definition differences and spectral/contextual ambiguities (e.g., neutral vs calcareous vs acid grassland; bogs and peat depth).
    - Certain BHs (e.g., Bogs, Montane, Inland bare ground) show substantial classification challenges.
    - Boundary and linear features and some urban elements are not consistently captured in LCM2000.

- Class-level insights and notable differences
  - Woodland:
    - Broadleaved/mixed woodland and coniferous woodland overall coverages similar, but direct per-square agreement is modest due to small woodlands being below LCM2000’s minimum mappable unit.
    - Coniferous woodland shows higher reproducibility in direct correspondence (70%) than broadleaved woodland (lower due to fragmentation and misclassification with grassland/arable).
  - Arable and horticultural land:
    - LCM2000 ~23.4% vs FS ~21.5%; misclassifications occur between arable and improved grassland and between arable and built-up areas.
  - Grasslands:
    - Improved grassland is a major BH; FS often records improvements not always captured by LCM2000, leading to some mismatches where FS sees improved and LCM2000 labels neutral or semi-natural.
    - Semi-natural, neutral, calcareous, and acid grasslands are challenging to separate spectrally; soil pH maps improve separation but remain imperfect.
  - Dwarf shrub heath, bogs, montane, and inland bare ground:
    - Dwarf shrub heath and bog classifications diverge due to peat depth as a key criterion; FS often reflects a broader bog area than LCM2000 when peat depth is considered.
    - Montane habitats are poorly sampled in field reconnaissance; altitude-based delineation may not align well with actual vegetation patterns.
    - Inland bare ground shows discrepancies due to urban context misclassification and inclusion of bare ground in urban contexts by FS versus LCM2000’s focus on larger patches.
  - Water and coastal habitats:
    - Inland water bodies (standing water/canals) are generally well captured (>0.5 ha); smaller water bodies are not mapped consistently.
    - Coastal BHs (supralittoral and littoral) are small and often below resolution; intertidal areas are variably represented; both datasets have limited reliability for coastal BHs.
  - Built-up areas and gardens:
    - LCM2000 differentiates built-up areas, gardens, suburban/rural development, and continuous urban areas to reflect urban heterogeneity beyond FS’s more generalized urban categorization.
  - Boundary/linear features:
    - Not targeted as BHs in LCM2000; FS mapping of these features is not directly mirrored in LCM2000 due to MMU and resolution differences.

- Change detection and temporal analysis
  - Detecting landscape change between 1990 (LCMGB) and 2000 (LCM2000) requires high precision beyond satellite mapping alone.
  - Segment-based results differ from 1990 raster products; some real changes exist but distinguishing them from mapping error is difficult.
  - Proposed approach: use intelligent, pattern-based methods informed by FS data (1990 and 1998) to identify probable changes and reduce false positives.
  - Future work includes integrating FS and external data to refine change detection and generate Broad Habitat statistics with greater precision.

- Data products and future directions
  - The final report (and calibration procedures) will provide enhanced Broad Habitat statistics via direct calibration against FS, enabling robust, nationwide BH estimates.
  - Ongoing follow-up work includes re-examining LCM2000 bogs/heaths and integrating FS data with external datasets to improve accuracy and consistency.
  - Additional R&D suggested for change detection, leveraging historical data and known change directions to improve detection of genuine landscape changes.

- Appendix and terminology notes
  - Appendix I provides a brief review of Broad Habitats and their distinguishing features relative to LCM2000 mapping, including definitions and spectral/field-based considerations for BHs such as broad-leaved woodlands, coniferous woodlands, arable land, grasslands, bogs, fens, bracken, heath, water, and urban/built environments.
  - Emphasizes that some distinctions (e.g., rough grasslands, peat depth) are difficult to resolve with imagery alone and may require contextual or ancillary data.