# LCM2000 Final Report

- Purpose and scope
  - Aimed to support UK Biodiversity Action Plan by mapping Broad Habitats (BHs) and relating them to the LCM2000 spectral classification.
  - Developed BH framework and mapping to enable national/regional reporting; introduced 10-class BH aggregates for reporting.

- Key concepts and classifications
  - Broad Habitats (BHs): conceptual habitat categories defined by JNCC (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland rock, Water, Built up areas, Coastal BHs, etc.).
  - LCM2000 classes: spectral/thematic classes mapped from satellite data; can be aggregated to BHs or further into Target classes, Subclasses, and Variants.
  - Target classes, Subclasses, Variants: hierarchical distinctions to retain useful detail when possible; Variants capture spectral components (e.g., crops, plantation types).
  - Aggregates: 10-class level where Target/Subclasses align closely with BH aggregations for reporting.
  - Map displays: designed for national/regional patterns, with some BHs aggregated or simplified to improve readability at map scale.

- Data sources and calibration approach
  - CS2000 field survey (FS) data used to assess LCM2000 map quality and to calibrate BH statistics.
  - FS data cover 569 one-kilometre squares (Britain); field details richer than LCM2000, not a ground truth.
  - Bootstrapped confidence limits developed to quantify correspondence across GB, England/Wales, and Scotland.
  - Inter-comparison rather than strict validation due to resolution differences and timing.

- Methodology and testing
  - GIS workflow: ARC/Info coverage files created for all FS squares and LCM2000 map-sections; generated 569 correspondence matrices (one per 1 km square).
  - Three main tests:
    - Per-pixel comparisons (direct overlay across 25 m pixels; sensitive to resolution and MMU differences).
    - Per-segment comparisons (dominant FS class within LCM2000 segments).
    - Per-parcel comparisons (FS parcels vs. LCM2000-derived labels).
  - Correspondences evaluated at multiple thematic levels:
    - BH level (excluding boundaries/linear features, and major rivers/streams)
    - Generalised urban/land-use levels (to align with FS generalisations)
    - Target class level
    - Aggregate class level

- Confidence limits and key results
  - Bootstrapped 95% confidence ranges reported; general pattern: per-pixel measures are lower due to resolution differences, while per-parcel/target-level measures improve.
  - By country (GB overall):
    - Per-pixel: about 54% correspondence (CI ~53–56%)
    - Per-segment: about 58% (CI ~57–60%)
    - Per-parcel: about 62% (CI ~60–64%)
  - England & Wales:
    - Per-pixel: ~60% (CI ~58–62%)
    - Per-parcel: ~69% (CI ~67–72%)
    - Per-segment: ~64% (CI ~62–66%)
  - Scotland:
    - Per-pixel: ~44% (CI ~40–47%)
    - Per-parcel: ~48% (CI ~44–52%)
    - Per-segment: ~47% (CI ~43–50%)
  - Target class level (parcel-based, weighted):
    - GB: ~65%
    - England & Wales: ~73%
    - Scotland: ~51%
  - Overall interpretation: NS/FS repeatability of about 88% sets an upper bound; LCM2000 achieving roughly 72% of maximum potential accuracy is plausible; ~5% of mis-match attributed to 25 m MMU vs FS 0.04 ha, ~15% to time/dataset structure, with remaining differences due to class-definition and data processing.

- Class-level findings and notable differences
  - Woodland (Broadleaved/mixed and Coniferous): similar UK coverage totals, but direct agreement in 569 squares is modest (roughly 44% for Broadleaved/mixed; higher correspondence for Coniferous ~70% due to larger, contiguous blocks and higher detectability). Small woodlands often fall below LCM2000’s 0.5 ha MMU, causing misclassification as grassland/arable in FS.
  - Arable and horticulture: LCM2000 ~23.4% vs FS ~21.5% UK cover; misclassifications occur between arable and improved semi-natural grass and between arable and built-up contexts.
  - Improved vs semi-natural grassland: FS often distinguishes improved vs semi-natural; LCM2000 more frequently records rough/neutral grass as Neutral grassland, leading to notable differences (~20% mis-match in improved grassland).
  - Neutral, Calcareous, and Acid grasslands: difficult to separate spectrally; spectral data alone show poor separation; spectral mask and coarse 1 km resolution mask contextual differences (soil acidity) limit accuracy.
  - Bracken, Dwarf shrub heath, Bogs, Montane, Inland bare ground: significant differences due to definitional alignment with BHs and peat/soil-context masking; peat depth used as a primary criterion to separate bog from heath, but this yields conservative bog estimates compared with FS.
  - Water and coastal habitats: Inland water/standing water broadly similar for larger bodies, but smaller features are under-represented; coastal BHs are small and often at or below resolution, treated as aggregates for reporting.
  - Built up areas and gardens: LCM2000 mapping captures heterogeneity within urban areas (Suburban vs Continuous Urban), while FS treats urban land broadly; this contributes to differences in urban vs non-urban classifications.
  - Boundary/linear features: not targeted by LCM2000; FS maps these as distinct BHs, contributing to a portion of the mismatch.

- Change detection
  - Detecting landscape changes (1990–2000) with satellite data is challenging due to resolution, timing, and methodological differences.
  - Real changes likely occurred, but robust detection requires integrating FS historical data (e.g., Haines-Young et al. 2000) and implementing intelligent methods to separate change from error.
  - Calibration results indicate under- and over-estimates in 2000; future work will refine change detection by leveraging known patterns of change.

- Data management and accessibility
  - Data sources are tracked, and datasets created in the calibration process are intended to be made discoverable with metadata.
  - Final report promises direct calibration to produce Broad Habitat statistics using FS precision while maintaining the broad coverage of LCM2000.

- Appendix I (distinguishing features and mapping challenges)
  - Provides high-level notes on how each BH (e.g., Broad-leaved woodland, Coniferous woodland, Arable, Grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane, Inland rock, Built up areas, Coastal BHs) is defined and the practical limitations of remote sensing for distinguishing many of these categories.
  - Emphasises that many fine distinctions (e.g., semi-natural vs improved grassland, peat depth for bog vs heath) are difficult to resolve spectrally and may require supplementary data or knowledge-based corrections.

- Table 2 and mapping details
  - Provides examples of how LCM2000 class Variants map onto Broad Habitats (codes, colors, and structural mapping notes).
  - Illustrates the complexity of linking spectral classes to BH concepts and the need for contextual corrections.

- Overall conclusions for analysts
  - LCM2000 provides comprehensive national coverage and useful BH aggregates, but substantial scale-, time-, and definition-related mismatches exist with the CS2000 field survey.
  - Target/class-level accuracy is plausible around mid-80s (relative to FS repeatability ceiling), with per-pixel measures significantly lower due to resolution and MMU differences.
  - For change detection or trend analysis, integrating historical field data and applying intelligent, pattern-based approaches is essential.
  - The continued integration of LCM2000 with FS and external data sources is planned to improve accuracy and produce robust BH statistics for reporting.