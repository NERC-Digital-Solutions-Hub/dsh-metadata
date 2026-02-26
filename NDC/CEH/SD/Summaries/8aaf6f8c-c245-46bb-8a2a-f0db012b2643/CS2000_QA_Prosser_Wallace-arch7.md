COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

## Overview
- QA assessment of CS2000 fieldwork across 38 squares (one quarter per square) to measure consistency, accuracy, and reliability of plot relocation, species records, vegetation cover, landcover mapping, and boundary features.
- Aim: quantify field recording accuracy, assess changes vs. CS1990, and evaluate mapping/data-product reliability for GIS uses.

## Key QA findings

### Plot relocation and plate recovery
- Plot relocation efficiency:
  - 60% of CS2000 surveyors’ plots accurately relocated; ~25% relocated approximately; ~15% inadequately relocated.
  - X- plots (habitat-type) hardest to relocate (4 m plots) with higher failure rate.
- Plate/plot recovery:
  - Assessors satisfactorily located 69.3% of plates (comparable to 65.2% in 1991 QA for CS1990).
  - Overall recovery rate of plates plus plots around 40–45% ( variability due to marking conventions and reuse of boundary plates).
- Implications: eight-year relocation is feasible but with notable location/orientation risks that affect data alignment for GIS products.

### Species concordance and recording accuracy
- Overall species concordance:
  - CS2000 vs QA showed lower initial concordance (~73% correct presence in plots) when considering plot location errors; after accounting for relocation errors, efficiency aligns with CS1990 levels.
  - 234 plots across 38 squares analyzed; ~6000 records analyzed; ≈71% of records confirmed by QA; mis-matches largely due to plot location/orientation (types 7–9) and overlooked species (type 4) contributing most to errors.
- Change in species lists:
  - QA generally produced longer species lists per plot; mean species per plot increased from CS2000 (17.9) to QA (20.4) overall, with similar patterns across land classes.
- Frequency of prevalent species:
  - Ranking of common species largely similar between survey and QA, but notable discrepancies for mosses (under-recorded) and several grasses (over- or mis-recorded due to seasonal/identification issues).
  - Common mis-identifications often involve Poa spp., Ranunculus spp., and others; some confusion between closely related grasses.

### Vegetation cover estimates
- Overall, cover estimates between CS2000 and QA were broadly similar but with several significant differences for a subset of species (primarily grasses and grass-like taxa).
  - Examples of significant differences (CS2000 vs QA):
    - Holcus lanatus: 10.2% vs 7.2% (p ≈ 0.029)
    - Dactylis glomerata: 9.3% vs 5.9% (p ≈ 0.005)
    - Anthoxanthum odoratum: 6.7% vs 3.6% (p ≈ 0.040)
    - Eriophorum vaginatum: notable discrepancy (p ≈ 0.018)
- Implication: observer/seasonal effects influence cover bands; caution needed when using fine-grained cover data from QA vs original surveys.

### Change detection and ordination (DECORANA)
- Axis 1 shifts between CS2000 and QA were generally insignificant, indicating no directional bias in the total change pattern.
- When broken down by plot type and landclass, no consistent directional bias found; differences mainly reflect location/orientation and cover mis-matches rather than systematic bias.

### Landcover mapping and codes
- Primary landcover codes:
  - High concordance between CS2000 and QA; excluding BAP codes, total concordance ~91.6%.
  - Including BAP codes, overall primary land cover agreement ~87.5% (improved ease of BAP coding vs earlier surveys; still some mismatches reflecting boundaries and lens-type habitats).
- Land-use change codes:
  - Change concordance relatively low: overall change concurrence ~51.4%; 33.9% of changes not noted by CS2000; 14.7% changes recorded but not substantiated by assessors.
  - Indication that many real changes since 1990 may have been missed; but plot-based data remain essential for evaluating change over time.
- Boundary features:
  - Primary boundary features: high concordance (total ~85%; code concordance ~92.8% for boundary height and stockproof condition around mid-80s to 90s).
  - Hedge/wall codes (secondary boundary qualifiers): lower concordance (~67.5%), with notable mis-matches in hedge shapes and wall condition coding; new hedge codes had limited uptake.
- Boundary height and stockproof status generally reliable; some inconsistencies in hedge-type coding and wall condition codes noted.

### Hedge diversity and arable plots
- Hedge diversity plots:
  - 124 total species across 19 hedge samples; overall agreement ~74.2%, surveyor efficiency ~77.4%.
  - Mean number of species per hedge plot: CS2000 5.16 vs QA 5.89.
- Arable plots:
  - Only five plots; concordance extremely poor (~30.6% agreement).
  - Seasonality and difficulty identifying ruderal species likely contributed to low reliability; two visits per arable margin suggested for future work.

### Overall effects of species change
- No systematic directional bias between CS2000 and QA in the overall vegetation-change gradient (Axis 1); mean axis scores not significantly different (p ≈ 0.847).
- When examining plot-type landclasses, changes are variable and largely tied to location/orientation and mis-matches rather than a uniform bias in change detection.
- Implication: while individual plot records vary, the aggregate signal across time is not biased in the QA sample.

## Data quality implications for GIS specialists
- Mapping products (landcover, boundary features) show strong reliability:
  - Primary landcover coding and boundary feature data are largely dependable; high concordance supports use in map-based data products.
  - Landcover change data show notable inconsistencies; caution advised when using change metrics across time without QA refinement.
- Location-based data are a key source of error:
  - Plot relocation/orientation errors contribute substantially to mismatches; robust GIS analyses should incorporate positional uncertainty or re-marking protocols.
- Vegetation cover and species presence data:
  - Substantial agreement overall, but persistent discrepancies in grass/dominant species and some annuals; seasonal effects and observer differences can affect fine-grained data layers.
  - Arable margins and hedge diversity data show larger uncertainties; treat as lower-confidence layers or require additional validation.
- Change detection and boundary codes:
  - Change recording shows limited concordance; this data should be treated with caution for time-series analyses unless corroborated.
  - Hedge/wall boundary coding requires careful interpretation due to lower code concordance; consider standardizing codes and training to improve consistency.

## Notable limitations and data gaps
- Small sample for arable margins reduces confidence in those data.
- Seven types of mis-matches identified; many arise from location/orientation errors, highlighting the need for precise plotting and location documentation.
- New coding schemes (e.g., hedge codes) had limited uptake, limiting their usefulness without further training and coding standardization.
- Seasonal timing of QA vs CS2000 can influence species cover data, complicating direct temporal comparisons.

## Takeaways for GIS-focused workflows
- Use CS2000 and QA data with explicit consideration of location accuracy and potential orientation errors.
- Treat landcover mapping as a reliable backbone; exercise caution with change and boundary-change layers.
- Incorporate uncertainty estimates for plots where relocation was uncertain or where boundary plates were missing or disturbed.
- For time-series analyses, corroborate changes with plot-level evidence and consider additional field verification, especially for hedgerows, arable margins, and grass-dominated plots.
- Invest in standardized data entry, consistent boundary marking, and clearer documentation of plate locations to improve future GIS data products.