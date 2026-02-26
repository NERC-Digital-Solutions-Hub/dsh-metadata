# LCM2000: A Broad Habitat Classification of Great Britain—Calibration against CS2000 Field Survey

- Objective and scope
  - Develop a UK-wide framework of Broad Habitats (BHs) to support Biodiversity Action Plan reporting.
  - Use LCM2000 as a satellite-derived, thematic classification to map terrestrial, freshwater, and coastal BHs, with external data to refine spectral classes.
  - Produce map displays and data products (targets, subclasses, variants) to support non-expert users and enable broad data use.

- Data sources and classification
  - LCM2000: Thematic classification of spectral data from satellite imagery, with external context to improve classification.
  - BHs, Target classes, Subclasses, and Variants: hierarchical structure used to describe landscapes; aggregate/10-class level used for reporting.
  - CS2000 field survey: Ground-based data for calibration, covering 569 one-kilometre squares in Great Britain (549 in 1998, rest in 1999); higher detail than LCM2000 but not a strict ground truth.
  - Additional notes: Northern Ireland data not yet digital; field data show 88% repeatability for primary codes; upland boundary mapping is problematic.

- Calibration and methodology
  - GIS workflow: ARC/Info-based mapping with BH-labeled coverage; created 569 correspondences (one per 1 km square) between CS2000 and LCM2000.
  - Calibration vs validation: treated as calibration, not ground-truth validation, due to resolution and timing differences.
  - Three main correspondence tests:
    - Per-pixel comparisons (overlay analysis, limited by resolution differences and MMU)
    - Per-segment comparisons (dominant FS class within LCM2000 segments)
    - Per-parcel comparisons (FS parcels vs LCM2000 labels)
  - Thematic levels of assessment:
    - BH level (excluding some features)
    - Target class level
    - Aggregate class level (simplified 10-class level)
  - Confidence estimates: bootstrapping to derive 95% confidence limits for correspondence; results stratified by GB, England/Wales, Scotland, and National Land Classes.
  - Several factors drive mismatch:
    - FS higher spatial resolution and time differences
    - Class-definition differences between FS and LCM2000
    - Differences in data structures (parcels vs segments vs pixels)
  - Accuracy interpretation: not a direct measure of LCM2000 accuracy; best viewed at Target class level.

- Key findings: correspondence and accuracy
  - Per-pixel correspondence (BH level):
    - Great Britain: 54% (95% CI 53–56%)
    - England & Wales: 60% (95% CI 58–62%)
    - Scotland: 44% (95% CI 40–47%)
  - Per-segment correspondence:
    - Great Britain: 58% (95% CI 57–60%)
    - England & Wales: 64% (95% CI 62–66%)
    - Scotland: 47% (95% CI 43–50%)
  - Per-parcel correspondence:
    - Great Britain: 62% (95% CI 60–64%)
    - England & Wales: 69% (95% CI 67–72%)
    - Scotland: 48% (95% CI 44–52%)
  - Target-class level (weighted correspondence, parcel-based):
    - GB: 65% (overall)
    - England & Wales: 73%
    - Scotland: 51%
  - Overall interpretation:
    - FS repeatability (~88%) is an upper bound; LCM2000 performance is around 72% of that potential.
    - Major sources of error: resolution differences (25 m pixels vs FS finer parcels), MMU differences (>0.5 ha in LCM2000 vs >0.04 ha in FS), time gaps between datasets, and classification differences.
    - Realistic target-class accuracy around 85% could be achievable; 65–73% at the parcel/target level is typical for broader analyses.

- Class-level insights and notable challenges
  - Woodland (broadleaved/mixed vs coniferous):
    - Broadleaved/mixed woodland coverage similar in LCM2000 and FS, but per-square agreement lower due to small woodlands often below LCM2000’s 0.5 ha minimum.
    - Coniferous woodland shows higher direct correspondence (~70%) and similar cover, typically in larger blocks.
  - Arable and horticulture:
    - LCM2000 often overestimates in part due to small features; misclassification with grassland and built-up areas remains an issue.
  - Grasslands and swards:
    - Distinguishing improved vs semi-natural grassland is challenging; FS often records improved grassland while LCM2000 may classify as neutral grassland.
    - Rough grasslands (some derelict or set-aside) are hard to separate spectrally; LCM2000 tends to group them with Neutral grassland.
    - The spectral signature of semi-natural swards is difficult to distinguish from other grasslands; context maps (soil acidity) help but are not perfect.
  - Fen, marsh, swamp, bog, and peat:
    - FS shows more fen/marsh/swamp than LCM2000; peat depth and context significantly influence bog classification.
    - LCM2000 peat-based bog mapping is conservative; ongoing work to re-examine bogs/heaths with additional data.
  - Montane and inland rock / urban and coastal:
    - Montane and inland bare ground (rock) have notable misalignments with FS; context-based rules (altitude, peat maps) used to adjust classifications.
    - Coastal BHs are small and often near-resolution limits; intertidal areas are variably represented.
  - Built-up areas and gardens:
    - LCM2000 separates urban components (suburban/rural development and continuous urban) and captures vegetation in parks/gardens more detail than FS, which treated urban areas more schematically.
  - Boundary and linear features:
    - Not targeted by LCM2000; FS captures many linear features (e.g., roads, rivers). This contributes to calibration differences, especially for boundary/rivers/streams.

- Data products, display and reporting
  - Map displays use cartographic conventions to balance reliability and pattern visibility; some rare classes are aggregated for national/regional plots.
  - Outputs include BHs, Target classes, Subclasses, Variants, and aggregated 10-class maps for reporting compatibility.
  - Table 2 and Appendix I provide crosswalks between LCM2000 variants and BHs, including color codes for map displays.
  - The goal is to enable “self-serve” use by end users and support broader data sharing and feedback.

- Change detection and future work
  - Detecting landscape change (1990–2000) with satellite data alone is difficult due to similar error sources; an intelligent, pattern-based approach combining FS-change expectations is proposed.
  - Calibration results identify locations where LCM2000 under- or overestimates; these insights will inform change analyses.
  - Future work includes re-examining bogs/heaths, integrating FS with external data, and producing Broad Habitat statistics directly calibrated to field data.

- Implications for data use and decision support
  - LCM2000 provides broad, nationwide BH mapping with substantial coverage and a framework to generate BH statistics by direct calibration against field survey data.
  - Useful for policy support, planning, and monitoring across broad habitat types, while acknowledging limitations in resolution, timing, and complex habitat distinctions.
  - Users should account for 25 m MMU constraints, mismatches in urban and boundary features, and the need for supplementary data sources for precise habitat delineation.

- Appendix I: key considerations for broad habitats in LCM2000 context
  - Distinguishing тонally between broadleaved/mixed vs coniferous woodland is difficult spectrally; training and context help classification.
  - Boundaries and linear features are not primary targets for LCM2000; field data remain the best source for these features.
  - Setaside and semi-natural grasslands require contextual correction; spectral data alone may not reliably separate these categories.
  - Neutral, calcareous, and acid grasslands present spectral ambiguity; soil acidity maps are useful but not definitive.
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bog, peat depth, montane habitats, inland rock, built-up areas, and coastal habitats each present distinctive challenges requiring supplementary data, context, or iterative refinement.
  - Coastal and intertidal zones are difficult to map consistently at the 1 km/25 m scale; both surveys have limitations in these areas.

- Release and documentation
  - Full methodology, image selection, pre-processing, classification, and calibration details are documented in the final report and forthcoming materials, including how Broad Habitat statistics will be generated through direct calibration against field data.