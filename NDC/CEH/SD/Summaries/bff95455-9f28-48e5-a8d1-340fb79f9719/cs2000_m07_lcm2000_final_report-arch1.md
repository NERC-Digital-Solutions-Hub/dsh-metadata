# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours)

## Overview of the document
- Presents mapping between LCM2000 broad habitats and LCM Target classes, Subclasses, and Variants (with Suclasses shown by map colors).
- Includes UK-wide and country-level breakdowns of habitat coverage (LCM2000) and comparisons with field survey data (FS/CS2000) across multiple tables.
- Documents the extent of agreement and discrepancies between LCM2000 classifications and field-based CS2000 data, including patterns related to urban generalisation and coastal variation.

## Data sources, scale, and limitations
- LCM2000 statistics come from a full count of cover on a 25 m grid.
- FS statistics come from Haines-Young et al. 2000; CS2000 used for field survey comparisons.
- Coastal coverage is variable due to tidal states and inclusion/exclusion of offshore inter-tidal areas.
- Differences between datasets arise from scale, classification mapping, and definitions of the FS population (e.g., NI exclusions).
- Tables include notes on generalising urban areas and how some habitat classes are aggregated or split across schemes.

## UK-wide habitat coverage (LCM2000 vs. FS) – Table 5 (km²)
- UK total LCM2000 coverage: 246,688 km²; UK FS coverage is not consistently tabulated in total here.
- Country totals (LCM2000):
  - England: 130,362
  - Wales: 20,689
  - Scotland: 77,898
  - Northern Ireland: 17,739
- Key aggregated habitat groups (LCM2000, UK):
  - Arable & Horticultural: 57,630
  - Improved grassland: 59,073
  - Semi-natural grass & bracken: 41,600
  - Mountain, heath & bog: 38,892
  - Broadleaved/coniferous woodland: combined ~43,? (England ~10,?; Scotland ~8,?; UK total ~?; see table for exact country splits)
  - Built-up areas and gardens: 16,637
  - Other notable groupings include Neutral, Calcareous, Acid grasslands, fen/brackens, and various aquatic/rock/coastal categories.
- Overall pattern: Large portions of the UK land area are in grassland, woodland, arable/horticulture, and built-up/urban areas, with regional variation in dominance of each class.

## LCM2000 vs CS2000: calibration and key differences – Table 6
- Table 6 presents uncalibrated LCM2000 BH cover (UK, GB, and constituent countries) alongside field-survey estimates with 95% confidence intervals (Low/High) where available.
- Examples (England):
  - Broadleaved, mixed and yew woodland: LCM2000 = 10,963 km²; FS Low = 8,460; FS High = 11,480.
  - Coniferous woodland: LCM2000 = 2,990; FS Low = 1,802; FS High = 4,158.
  - Arable & horticulture (GB total): LCM2000 = 56,638; FS Low = 47,944; FS High = 57,036.
  - Improved grassland: LCM2000 = 50,024; FS Low = 50,536; FS High = 59,104.
- Wales, Scotland, NI show similar patterns of agreement but with notable regional differences and instance-specific higher or lower FS bounds compared with LCM2000.
- Overall takeaway: There is substantial general alignment in scale between LCM2000 and field survey estimates for major classes, but several categories show meaningful differences in absolute area and across countries, reflecting classification nuances and scale effects.

## Summary correspondence matrices: GB and England & Wales – Tables 8–10
- Table 8: GB-wide summary correspondences (per 1000) comparing LCM2000 vs CS2000 across Broad Habitats, Target Class, and Aggregate levels; uses bootstrap-based confidence intervals with 40 Land Classes for stratification.
- Table 9: England & Wales subset of the correspondence matrix (per 1000); similarly uses bootstrapped confidence intervals and notes urban generalisation effects.
- Table 10: Scotland-specific correspondences (per 1000); shows how CS2000 categories map to LCM2000 targets/classes and highlights cross-walks between habitat concepts across schemes.
- Key patterns:
  - There is a measurable correspondence for major habitat groups (Broad Habitats and Target Classes) at aggregate levels.
  - Urban areas require generalisation in CS2000/LCM2000 mappings, reducing precision in urban-dominated classes.
  - Some habitat mappings show misclassification or reclassification across schemes (e.g., arable/grassland blends, woodland types, bog/fen categories) depending on country and scale.
  - The matrices are designed to quantify how well LCM2000 categories predict or correspond to field-survey squares (CS2000) with country- and region-specific nuances.

## Footnotes and methodological caveats
- LCM2000 vs FS differences are influenced by grid resolution, classification schemes, and boundary definitions.
- Coastal and urban generalisation issues can bias cross-walk results.
- NI field survey data may exclude certain BHs, affecting UK-wide totals.
- The summary correspondences are weighted estimates and rely on bootstrapping to derive confidence intervals.

## Practical implications for analysts
- When using LCM2000 data to infer field-survey outcomes (CS2000), expect good alignment for broad habitat categories but be cautious at finer scales, especially in urban and coastal zones.
- For local-scale decision-making, incorporate uncertainty ranges from FS comparisons and consider cross-walk adjustments between LCM2000 Target Classes/Subclasses/Variants and CS2000 categories.
- Data harmonisation and transparent documentation of classification mappings are essential to improve predictability and reproducibility in applied analyses.
- Be mindful of country-specific differences in habitat classification and coverage when aggregating to UK-wide analyses.