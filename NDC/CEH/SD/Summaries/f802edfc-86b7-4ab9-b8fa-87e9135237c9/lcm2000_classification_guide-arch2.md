# CSLCM/Final

## Overview
- Purpose: Support the UK Biodiversity Action Plan by framing Broad Habitats (BHs) and using LCM2000 (a satellite-derived, 1 km spectral classification) to map terrestrial, freshwater, and coastal BHs, with external data to refine classifications.
- Structure: BHs are described via Target classes, Subclasses, and Variants; map displays use aggregated BHs for reporting; effort aims to calibrate LCM2000 outputs against field data for robust BH statistics.

## Data and Methods
- Field data: CS2000 field survey (FS) conducted in Britain across 569 one-kilometre squares (1998–1999; NI data not digitally testable yet); 88% repeatability for primary FS codes; not true ground truth due to resolution and boundary challenges.
- Remote sensing data: LCM2000 classified from 1990s imagery (primarily 1998–2001); 25 m pixels; minimum mappable unit (MMU) of >0.5 ha; no direct mapping of BHs, but linking to BHs via Target classes, Subclasses, and Variants; multiple aggregation levels for reporting.
- GIS and calibration: ARC/Info workflows; produced 569 FS-to-LCM2000 correspondence matrices; three main comparison modes (per-pixel, per-segment, per-parcel); analyses across 40 National Land Classes; bootstrapping used to estimate 95% confidence intervals.
- Calibration focus: inter-comparison (calibration) rather than full validation; aims to derive BH cover statistics from LCM2000 that align with FS.

## Calibration Results (Key Findings)
- Overall correspondence (GB):
  - Per-pixel: 54% (95% CI 53–56)
  - Per-segment: 58% (95% CI 57–60)
  - Per-parcel: 62% (95% CI 60–64)
- England & Wales:
  - Per-pixel: 60% (95% CI 58–62)
  - Per-parcel: 69% (95% CI 67–72)
  - Per-segment: 64% (95% CI 62–66)
- Scotland:
  - Per-pixel: 44% (95% CI 40–47)
  - Per-parcel: 48% (95% CI 44–52)
  - Per-segment: 47% (95% CI 43–50)
- Target-class level (parcels, base GB-wide):
  - GB: ~65% (England & Wales ~73%, Scotland ~51%)
- Interpretive points:
  - Mismatches largely reflect:
    - FS’s higher native resolution and different timing (FS around 1998) vs LCM2000 (1998–2001)
    - Differences in class definitions and how urban/rural features are generalized
    - The MMU discrepancy (FS ~0.04 ha vs LCM2000 >0.5 ha)
  - Per-pixel results show the greatest discrepancy due to minor spatial differences; parcel and segment levels improve alignment.

## Interpretations by Habitat Type (Key Observations)
- Woodlands:
  - Broadleaved/mixed woodland: similar total cover, but many small woodlands in FS are not captured by LCM2000’s 0.5 ha MMU, causing underestimation; coniferous woodland shows higher direct correspondence (~70%).
- Arable and horticultural land:
  - LCM2000 often overestimates relative to FS; misclassifications between arable and improved grassland contribute to errors; ~70% of LCM2000 arable overlaps FS arable.
- Grasslands:
  - Improved grassland vs semi-natural: FS often maps improvements not always captured by LCM2000; roughly 20% of FS improved grassland appears as semi-natural in LCM2000.
  - Neutral, Calcareous, and Acid grasslands are difficult to separate spectrally; spectral data plus soil pH context used to distinguish but remains imperfect.
- Bracken, Heath, Bogs, Fen/Marsh/Swamp:
  - Bog mapping is sensitive to peat depth; FS and peat masks diverge; FS records more fen/marsh and bog in some years; peat depth (>0.5 m) used to reclassify bog on deep peat, but this yields conservative bog estimates.
  - Dwarf shrub heath, montane, and inland rock/inland bare ground differences arise from distinct BH definitions and thresholds; montane mappings are hampered by accessibility and altitude-based criteria.
- Water and coastal:
  - Inland water bodies (>0.5 ha) tracked; standing water and canals align reasonably with FS for larger water bodies; coastal BHs are small, often below resolution, and partially aggregated for reporting.
- Built-up areas:
  - LCM2000 differentiates urban and suburban development (including vegetated parks) more explicitly than FS; FS tends to record urban land as a continuous block, which blends with other land-cover types in LCM2000.
- Boundary and linear features:
  - Not targeted as BHs in LCM2000; FS maps these separately; this contributes to mismatches in calibration.

## Change Detection
- Detecting landscape change between 1990 and 2000 is challenging with satellite data alone; changes are likely modest and can be confounded by resolution and data differences.
- An intelligent approach is proposed: use historical FS data (Haines-Young et al. 2000) and calibration results to guide interpretation of apparent changes, identifying patterns of real change versus classification error.
- Future work (beyond production phase) includes combining LCM2000 with FS and external datasets to improve detection of genuine changes.

## Accuracy and Limitations
- FS is not ground truth; differences reflect resolution, data models, and survey timing.
- Estimated accuracy at the Target class level suggests around 85% potential alignment, with overall practical accuracy around 72% when accounting for FS limits and MMU mismatches.
- Key limitations include:
  - 0.5 ha MMU for LCM2000 vs 0.04 ha FS
  - Timing differences between field and satellite data
  - Difficulty in distinguishing closely related BHs spectrally (e.g., neutral vs calcareous vs acid grasslands)
  - Underrepresentation of small or narrow features (boundaries, rivers) in LCM2000

## Next Steps and Implications for Analysts
- Use direct calibration to generate Broad Habitat statistics that reflect FS precision while retaining LCM2000’s comprehensive coverage.
- Improve integration of peatland/bog classifications with external peat maps and FS data; review peat-depth-based reclassifications.
- Develop and apply intelligent change-detection approaches that incorporate known calibration patterns and potential error sources.
- Recognize which BHs and aggregates are robust at 1 km scale and which require caution or supplementary data for accurate interpretation.

## Appendix and Additional Context
- Appendix I outlines distinguishing features of BHs and notes on specific habitat classes; Table 2 provides mapping of LCM2000 Variants to BHs and associated color codes for display.
- The document emphasizes calibration over validation and discusses the implications of data timing, resolution, and classification schemes for environmental monitoring and policy evaluation.