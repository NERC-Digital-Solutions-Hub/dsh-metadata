# Soil sampling

## Overview
- Sampling date: 1 April 2015.
- Climate treatments had been inactive for 6 months.
- To minimize destructive sampling, only a single 8 cm diameter core (0–8 cm depth) per plot was used, yielding 3 replicates per treatment (control, drought, warming).
- Cores collected near the base of Calluna vulgaris shrubs; samples sealed, stored at 4°C until processing.

## Root extraction and identification
- C. vulgaris roots isolated by cutting cores into 1 cm subsections, soaking in tap water, and manual removal with forceps.
- Large roots (>1 mm) identified by dark, woody, kinked morphology; fine roots (reddish, non-woody) verified as C. vulgaris by tracing to larger identifiable roots.
- Necrotic/rotting roots discarded; cleaned roots stored in deionised water at 4°C for measurements.

## Root measurements
- Measurements: root length, diameter, and number of root tips using WinRHIZO v3.2.
- Procedure: roots scanned on a flatbed scanner submerged in 5 mm tap water; parameters set via TWAIN in professional mode (positive film, 24 bit, 300 dpi); fine roots (≤1 mm) analyzed; larger roots (>2 mm) oven-dried at 70°C for 24 h to obtain dry weight data.
- Data focus: detailed analysis of fine roots for microscopy; broader metrics captured for larger roots.

## Fungal colonisation measurements
- Fine root fragments treated with 10% KOH, rinsed, then stained with 5% vinegar-ink solution and heated to enhance visibility.
- Direct counting of coils unreliable; Ericoid mycorrhizal (ErM) colonisation assessed by confirming presence of hyphal coils within cells using a compound microscope with a scale bar.
- Root segments (2 mm) prepared on slides; 40× magnification; evaluation across root length to determine ErM colonisation level (presence/absence across cells).
- Also recorded Dark Septate Endophytes (DSE) colonisation.

## Quality control
- Tested root bleaching at different KOH concentrations (10% and 2.5%) and durations (10, 20, 30 minutes) to confirm no difference in results.
- Preliminary testing and example photographs produced for colonisation scores to prevent measurement drift.
- Data screened for outliers and improbable values.

## Data structure and variables
- Dataset composition: 53 columns, 72 rows.
- Key identifiers and measurements included:
  - A: Entry ID; Plot; Depth (cm); Treatment (warming, control, drought).
  - AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2, AvgDiam_mm, LenPerVol_cm_m3, RootVol_cm3, Tips, DryWeightAll_g, DryWeight2mm_g.
  - Length_Root1 to Length_Root5 (cm) representing multiple root segments.
  - ErM_0_Root1 to ErM_0_Root5, ErM_0_1_Root1 to ErM_0_1_Root5, ErM_1_10_Root1 to ErM_1_10_Root5, ErM_10_50_Root1 to ErM_10_50_Root5, ErM_50_90_Root1 to ErM_50_90_Root5, ErM_90_100_Root1 to ErM_90_100_Root5 (counts of 2 mm root segments by ErM colonisation level).
  - DSE_Root1 to DSE_Root5 (counts of 2 mm root segments with DSE).
- These variables collectively capture: image-derived root metrics, fine vs. coarse root weights, and detailed fungal colonisation statuses across five root segments per sample and multiple colonisation categories.

## Data usage considerations for analysis
- Provides structured, self-serve data for cross-treatment and cross-plot comparisons of root morphology and fungal associations.
- Clear methodological QC and data dictionary facilitate reproducibility and integration with other datasets.