# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

## Overview
- A QA exercise to assess consistency and reliability of CS2000 fieldwork across 38 of 519 squares (sampled from 1998) with resurvey of 234 species plots across nine plot types.
- Aims included measuring plot relocation efficiency, species concordance, accuracy of percent cover, bias in habitat change analyses, comparability with CS1990, land-use mapping accuracy, and recording changes.

## Methodology and Scope
- QA sample: 38 squares; in each, one quarter resurveyed; seven main plot types analyzed as quadrats and linear plots; 234 plots per square assessed.
- Plot types include quadrats of different sizes, road verges, streamsides, boundaries, arable margins, etc. New plots (e.g., arable margins) discussed but small in sample.
- Plate and plot relocation focus: buried plates marking quadrats; relocation effectiveness compared to 1990 and 1991 QA exercises.
- Change assessment: comparison of 1990 CS data with 1998 CS2000 data, and QA results to separate real change from recording changes.

## Key Findings

### Plot Relocation and Plate Recovery
- Relocation success: 86.7% of 210 plots relocated satisfactorily; similar to earlier QA results.
- CS2000 surveyors: precisely relocated 60% of 1990 plots; ~25% relocated acceptably; ~15% inadequately relocated.
- Plate recovery: assessors located 69.3% of plates; 23.3% of plates could not be precisely recovered but plots were near original location; overall recovery rate region estimated around 40–45% (accounting for uncertainties).
- Implication: eight years after burial, maintaining precise relocation is feasible but more challenging than after one year; some mislocation issues noted (e.g., wrong side of a hedge/stream).

### Species Concordance
- Across ~6000 records in 210 plots, 71% of species were confirmed present by assessors; 2% non-concordances due to real changes.
- Initial recording efficiency estimated around 73%, slightly lower than CS1990 (c. 78%), largely due to plot location errors in 1998.
- QA suggests similar efficiency to CS1990 when plot location issues are accounted for.

### Vegetation Cover and Frequency
- For the 30 most frequent, several species showed significant differences in cover between CS2000 and QA (e.g., Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum, Elymus repens, etc.), with some seasonal effects likely contributing.
- Overall, QA produced longer species lists per plot; the frequency rankings of common species remained broadly similar to prior surveys.
- Cover measurements showed reasonable agreement overall, with some species-specific discrepancies.

### Change Direction and DECORANA Axis
- DECORANA analysis showed overall axis shift between time one (CS2000) and time two (QA) was insignificant, indicating no directional bias in the direction of change across plot types and land classes.
- Variation in axis scores generally related to location/orientation, cover-mismatch, and overlooked species rather than systematic bias.

### Landcover Mapping and Codes
- Landcover coding evaluated at multiple levels: primary landcover codes, secondary descriptive codes, and cover codes, including boundary features.
- Concordance (CS2000 vs QA):
  - Primary landcover codes: 88% agreement
  - BAP codes: 77% agreement
  - Primary boundary codes: 85% agreement
  - Principal qualifying landcover codes: 73% agreement
  - Species awarded cover: 63% agreement
  - Species cover codes: 74% agreement
- Including BAP codes, overall primary landcover agreement: about 87.5% (with 91.6% concordance excluding BAP in some tables).
- The mapping of BAP codes showed particular difficulties in differentiating certain habitat types; boundaries between some BAP classes were not always updated to reflect true distributions.

### Change in Landuse and Boundary Features
- Change recording concordance overall: 51.4% (CS2000 changes matched by QA); 33.9% of changes not noted by CS2000; 14.7% changes recorded but not substantiated by QA.
- Many changes since 1990 appear missed or under-recorded; suggests plot data are more reliable for evaluating change.
- Hedge/wall boundary coding: boundary-related codes showed 67.5% concordance; omissions around 14.8%.
- Boundary height coding: high concordance (around 89–92% when considering code concordance), stockproof status around 83–89%.
- Changes in hedge types and boundary features were noted, with some inconsistencies likely due to observer interpretation at boundary features.

### Hedge Diversity and Arable Plots
- Hedge diversity plots: total species 124; common species 92; overall concordance 74.2%; surveyor efficiency 77.4%; mean species per plot CS2000 5.16 vs QA 5.89.
- Arable margins: only five plots; very poor concordance; seasonality and unfamiliarity with ruderal species likely contributed; recommendation for multiple visits for future arable margins.

## Data Quality Metrics and GIS Implications

- Overall data reliability indicators:
  - Plot relocation: ~60% precise relocation, ~25% approximate, ~15% poor; plate recovery ~69% located; total plotting reliability around 40–45% when accounting for uncertainties.
  - Species concordance: ~73% initial recording accuracy; ~71% confirmed at QA; about 2% changes attributed to management between surveys.
  - Landcover and boundary mapping: primary landcover codes ~88% concordance; boundary codes high concordance (~85–92% depending on type); BAP and certain land-use qualifiers show more variability.
  The QA indicates strong overall mapping reliability but notable uncertainties in some habitats, seasonal effects, and boundary classifications.
- No directional bias detected in axis changes between CS2000 and QA.
- Data integration implications:
  - When combining CS2000 with QA results, treat location/orientation errors as key uncertainty drivers in GIS analyses.
  - Use QA-derived concordance and omissions to quantify uncertainty in land-cover transitions and boundary changes.
  - Be cautious with arable margins due to limited sample; seasonal timing significantly affects species presence/absence and cover estimates.
  - Mapping components (primary codes, BAPs, boundaries) show robust agreement overall but require careful review where boundary updates or rare codes are involved.

## Recommendations for GIS Practice

- Incorporate QA metrics to quantify reliability in spatial analyses:
  - Use relocation success rates to model uncertainty in plot positions and to flag plots with higher positional uncertainty.
  - Apply species concordance and cover-code agreement statistics to weight vegetation-change analyses and time-series maps.
- For landcover mapping:
  - Prioritize verification of BAP and boundary changes; update classical maps to reflect known changes where QA indicated discrepancies.
  - Treat instances of "overlooked" species as potential gaps in biodiversity layers and adjust richness layers accordingly.
- For temporal change analyses:
  - Consider that a substantial portion of observed change may be due to recording changes rather than true ecological change; where possible, cross-validate with QA-like procedures.
- Data collection guidance for future GIS projects:
  - Use enhanced measurement protocols for boundary features, hedge types, and wall integrity to improve code concordance.
  - Plan for multiple, seasonally spread visits for arable margins and other seasonally variable habitats to improve species capture and reduce mis-matches.
  - Maintain clear documentation of plot orientation and location reasoning to minimize orientation-related errors.

## Accessibility of Results

- The report provides quantified metrics that can feed uncertainty models in GIS workflows and help communicate confidence levels in map-based products derived from CS2000 data and QA assessments.