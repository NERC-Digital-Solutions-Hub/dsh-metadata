# LCM2000 Final Report

## Overview
- Purpose: Support UK Biodiversity Action Plan with a standard framework of Broad Habitats (BHs) to monitor environmental health and policy performance over time.
- Context: LCM2000 is a thematic, satellite-derived classification linked to BHs, with external data used to refine spectral classifications. Aims to distinguish BHs where possible and provide usable target and aggregate classifications for reporting.
- Classification structure:
  - BHs: Broad Habitats (e.g., Broad-leaved woodland, Bracken, Fen, marsh, bog, Coastal, Built up areas).
  - Target classes: more specific, spectrally-defined classes aligned to BHs.
  - Subclasses and Variants: finer distinctions where feasible (e.g., coniferous woodland, arable crops, improved vs semi-natural grassland).
  - Aggregate classes: simplified 10-class level for reporting where FS (field survey) and LCM2000 maps align closely.
- Display: Map displays use cartographic conventions to emphasize patterns and maintain reliability at national/regional scales; some rare or small BHs are aggregated for clarity.

## Data and Methods
- Data sources:
  - LCM2000: satellite-derived spectral classifications mapped to BH framework.
  - CS2000 field survey: detailed ground truth data used to calibrate LCM2000 mappings.
- Calibration approach:
  - Inter-comparison (calibration) rather than strict validation due to resolution differences and survey timing.
  - 569 CS2000 squares (1 km each) examined (Britain; NI data not digitally ready).
- Evaluation methods:
  - Per-pixel: direct overlay comparisons between FS and LCM2000.
  - Per-segment: LCM2000 segment labels vs FS-dominant class.
  - Per-parcel: FS parcels vs LCM2000 parcel labels.
- Confidence assessment:
  - Bootstrapping to estimate 95% confidence limits for correspondence across GB, England/Wales, and Scotland.
  - Analyses performed at BH level (excluding some linear features), Target class level, and Aggregate class level.
- Key data details:
  - LCM2000 MMU: >0.5 ha (parcels typically mapped at 25 m pixels); FS parcels >0.04 ha.
  - Time difference: FS data largely from 1998; LCM2000 mostly 1998–2001 imagery.
  - Data processing: ARC/Info GIS workflows; 569 correspondence matrices created for the squares.

## Key Findings
- Overall correspondence by level (GB-wide):
  - BH level: ~58% match (range 57–60%); England & Wales ~64%; Scotland ~47%.
  - Per-pixel generally lowest due to pixel-level differences (54% GB; 60% England/Wales; 44% Scotland).
  - Per-segment: ~58% GB; ~64% England/Wales; ~47% Scotland.
  - Per-parcel: ~62% GB; ~69% England/Wales; ~48% Scotland.
  - Target class level (parcel-based): ~65% GB; ~73% England/Wales; ~51% Scotland.
- By Habitat type (highlights of interpretation):
  - Broadleaved/mixed woodland and Coniferous woodland: similar gross cover between LCM2000 and FS, but direct agreement is modest (often due to 0.5 ha MMU in LCM2000 excluding many small woods; openings in woodland also misclassified).
  - Arable and horticultural land: LCM2000 ~23.4% vs FS ~21.5%; misclassifications with grassland and improvements cause notable errors.
  - Improved grassland vs Semi-natural: FS often records improvements differently; ~20% FS-improved grassland labeled as semi-natural by LCM2000.
  - Neutral/Calcareous/Acid grasslands: distinguishing spectral signals is difficult; peat depth and soil acidity complicate separation; significant discrepancies.
  - Bracken, Dwarf shrub heath, Bogs, Fen/marsh/swamp, Montane, Inland bare ground: substantial differences due to definitions, spectral resolution, and contextual data (peat depth, altitude, urban context).
  - Coastal BHs: small, often below resolution; aggregate reporting used; inter-tidal areas pose modeling challenges.
  - Water and rivers/streams: Inland water bodies >0.5 ha captured similarly, but narrow, seasonal, or smaller features vary; standing water vs. running water not always distinguished.
  - Built up areas and gardens: LCM2000 differentiates urban components (Suburban/rural development vs Continuous urban) more detail than FS, which treated urban land as a single category.
- Accuracy interpretation:
  - The correspondence figures are not a direct accuracy measure for LCM2000; limitations in resolution, timing, and definitions mean FS is not ground truth.
  - Estimated reality: LCM2000 may achieve around 87% accuracy at the Target class level when considering the best achievable alignment with FS; FS repeatability is about 88%, suggesting an upper bound close to this value.
  - About 5% of mismatches are attributable to the 25 m MMU grid vs the finer field survey; other mismatches come from time differences and classification differences.
- Change detection insights:
  - Between 1990 and 2000, landscape changes are likely small (a few percent) and often within error margins of mapping.
  - Full, reliable change detection is difficult with satellite data alone; an integrated approach using FS data (1990/1998) and intelligent analysis is recommended to identify true changes versus artifacts.
- Data products and calibration:
  - The study provides a framework to generate Broad Habitat statistics by direct calibration against field surveys, enabling robust, wide-coverage statistics aligned with high-precision field data.

## Limitations and Challenges
- Not ground-truth: CS2000 does not provide a definitive ground truth; multiple sources of error and resolution differences complicate interpretation.
- Mismatches arise from:
  - Differences in spatial resolution (25 m parcels vs 1 km FS squares).
  - Timing differences between field surveys and satellite imagery.
  - Varied definitions and mapping rules for BHs, Target classes, and Aggregates.
- Specific classification difficulties:
  - Neutral/Calcareous/Acid grasslands due to spectral ambiguity and soil acidity masking.
  - Peat depth control for bogs leading to underestimation in LCM2000 relative to FS.
  - Montane and Inland bare ground definitions may reflect context limitations and data gaps.
- Coastal and linear features: these are either aggregated or not targeted by LCM2000; FS captures many such features that are not fully represented in LCM2000.

## Implications for Monitoring and Data Use
- LCM2000 provides broad, geographically comprehensive habitat mapping that can be calibrated to field data to produce BH statistics for policy monitoring.
- The approach supports standardized reporting across GB, England/Wales, and Scotland, with quantifiable confidence bounds.
- For improved monitoring:
  - Integrate LCM2000 with FS and external data (peat maps, soil pH, urban context) to refine habitat delineations.
  - Use the Target class and Aggregate class outputs for routine reporting while preserving Subclass/Variant detail where needed.
  - Develop intelligent change-detection workflows that leverage historical FS data to distinguish real change from classification error.
- Data accessibility: emphasis on storing and sharing calibrated datasets through appropriate portals to enable broader access and reuse.

## Appendix and Technical Notes
- Appendix I outlines distinguishing features of Broad Habitats and the limitations of remote sensing in resolving fine-scale habitat distinctions (e.g., woodland types, grassland improvements, bogs vs. dwarf shrub heath).
- Practical mapping notes:
  - Spectral vs. contextual distinctions: many semi-natural and drifted classifications require contextual corrections (soil maps, peat depth, land-use history).
  - Some BHs are better represented as aggregates for reporting due to resolution limits and mapping challenges.
  - The coordinate between BHs and LCM2000 Target classes involves read-across rules, with variants provided where possible for specialist use.