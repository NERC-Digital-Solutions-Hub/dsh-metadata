# LCM2000 CALIBRATION AGAINST CS2000 FIELD SURVEY DATA

- Overview
  - Purpose: Assess and calibrate the LCM2000 broad habitat map by comparing it with CS2000 field survey data to estimate map accuracy, generate BH statistics, and support change detection and data integration.
  - Scope: Britain-wide assessment using CS2000 field survey data (569 one-kilometre squares; 1998–1999 data; Northern Ireland data not digitally available for testing).

- Data and classification framework
  - LCM2000: Thematic classification from satellite imagery with aggregate and target classes, including Broad Habitats (BHs), Target classes, and Aggregate classes.
  - CS2000 Field Survey (FS): Detailed, high-resolution ground data used for calibration, not treated as ground truth; differences in resolution, timing, and methodology drive discrepancies.
  - Map display and compatibility: BHs, Target classes, and Variants mapped with crosswalks to BHs; display conventions balance reliability and pattern visibility.

- Calibration approach and methods
  - Comparisons conducted at multiple levels:
    - Per-pixel: direct overlay of FS and LCM2000 parcels.
    - Per-segment: FS-dominant segment labels compared to LCM2000 spectral segments.
    - Per-parcel: FS land parcels labeled against corresponding LCM2000 class labels.
  - Thematic levels: BH level, Target class level, and Aggregate class level (for reporting).
  - Confidence estimation: Bootstrapping used to derive 95% confidence limits for correspondence measures.
  - Regions: Separate summaries for Great Britain (GB), England/Wales, and Scotland.

- Key findings on correspondence and accuracy
  - Per-pixel correspondence (GB): ~54% overall (England/Wales ~60%, Scotland ~44%).
  - Per-segment correspondence (BH level): GB ~58% (England/Wales ~64%, Scotland ~47%).
  - Per-parcel correspondence: GB ~62% (England/Wales ~69%, Scotland ~48%).
  - At Target class level (parcel-based): GB ~65% (England/Wales ~73%, Scotland ~51%).
  - Overall conclusion: FS captures higher detail than LCM2000’s 1 km resolution; differences arise from resolution, timing, class definitions, and mapping methodologies.
  - Notable causes of discrepancies:
    - FS finer spatial resolution and year differences vs LCM2000 timing.
    - 0.5 ha minimum mapping unit (MMU) for LCM2000 vs 0.04 ha FS parcels leading to small features being missed or misrepresented.
    - Classification differences between BH definitions and LCM2000 target/aggregate schemes.
    - Specific challenges in distinguishing semi-natural vs improved grasslands, neutral/calcareous/acid grasslands, bogs, fens, montane habitats, bracken, and peat depth considerations.
    - Built-up areas vs vegetation within urban contexts, and coastal BHs (supra-, littoral) with limited representation at 1 km resolution.
    - Boundary and linear features (Rivers/streams) excluded from LCM2000 calibration due to resolution constraints.

- Class-level insights and notable distortions
  - Woodland and arable/horticulture: general agreement on area, but small woodlands and field boundaries are often misrepresented due to MMU and resolution; arable vs. improved grassland and urban confusion contribute to misclassifications.
  - Grasslands: substantial ambiguity between improved, semi-natural, neutral, calcareous, and acid grasslands; spectral data alone struggle to separate these, necessitating contextual and soil information (e.g., pH) for corrections.
  - Wetlands and bogs: peat-depth criteria used to distinguish bogs; FS often identifies more fen, marsh, and swamp than LCM2000, prompting reconsideration of peatland mapping and future data integration.
  - Montane, inland rock, and coastal habitats: underrepresented or simplified in LCM2000; context and altitude-based rules can misclassify certain montane or bare-ground areas.
  - Water and urban areas: inland water and standing water have near-identical totals but differ in MMU thresholds and detection; urban areas are treated as a mix of built and vegetated surfaces, differing from FS treatment of urban land as continuous.

- Change detection and future work
  - Changes between 1990 and 2000 are generally small and often within error margins of satellite mapping; precise change detection requires more than satellite data alone.
  - An intelligent, pattern-based approach could combine FS baseline data with LCM2000 results to identify probable real changes and distinguish them from classification or resolution errors.
  - Recommendations for improvement:
    - Re-examine bogs and heath classifications and integrate FS with external datasets (peat depth, soil maps) for refined BH distinctions.
    - Explore direct calibration of Broad Habitat statistics using FS to enhance consistency across datasets.
    - Improve change detection workflows by leveraging known error patterns and historical baselines (FS 1990/1998 data).

- Appendix and technical context
  - Appendix I provides detailed distinctions and limitations of Broad Habitats and the challenges of mapping with remote sensing, including the difficulty in differentiating certain semi-natural swards, peat-related bogs, and coastal habitats.
  - The document emphasizes that LCM2000’s accuracy is best judged at the Target class level rather than BH level, due to inherent resolution and definitional differences.

- Governance and data handling implications for Data Stewards
  - Provenance and provenance trail: FS calibration data and LCM2000 classification workflow must be preserved to document the basis for BH statistics and change analyses.
  - Uncertainty management: Quantified via bootstrapped confidence limits; per-pixel results are less reliable than per-parcel or per-segment assessments.
  - Data interoperability: Requires explicit mapping between BHs, Target classes, and Aggregates; maintain clear crosswalks and metadata to enable reuse across systems and any future reclassification.
  - Temporal alignment: Acknowledge timing differences between FS (1998–1999) and LCM2000 imagery (mostly 1998–2001); document potential time-induced discrepancies.
  - Usage guidance: Treat FS as calibration data rather than ground truth; use the calibration results to inform change detection, BH statistics, and integration efforts with auxiliary datasets (soil, peat depth, urban masks).
  - Future integration plan: Develop iterative calibration workflows that incorporate additional external data sources (e.g., peatland maps, soil pH) to improve discrimination of sensitive classes and to strengthen harmonization across datasets for governance and discovery.