# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

## Overview
- A QA assessment of CS2000 fieldwork to measure consistency, reliability, and mapping accuracy across plots, land cover, boundaries, and changes since CS1990.
- Sub-sample: 38 of 519 squares; one quarter of each square re-surveyed, totaling 234 plots across nine plot types.
- Focus on plot relocation, species concordance, vegetation cover, landcover and boundary coding, and change recording.

## Aims and Scope
- Quantify field recording accuracy and comment on change statistics.
- Examine plot relocation efficiency and observer effects (location, orientation, management/seasonal effects).
- Compare CS2000 results with CS1990 QA and relate findings to mapping accuracy and boundary coding.
- Provide an objective assessment of mapping and change coding alongside the CS2000 survey.

## Methods and Scope Highlights
- Sampling: 38 squares; 34 of these previously included in 1990 CS; 234 plots analyzed across plot types (quadrats, Y-plots, U/X plots, road verges, streamsides, boundaries, arable margins).
- Plate and plot relocation: buried plates used as location markers; relocation effectiveness assessed eight years after burial.
- Data comparison: CS2000 records vs QA assessments; emphasis on land cover mapping, boundary features, and change strings.

## Key Findings

### Plot Relocation and Plate Recovery
- Relocation success: 86.7% recovery for full plot searches (28 of 210 plots not satisfactorily relocated).
- CS2000 relocation vs. CS1990: surveyors accurately relocated 60% of 1990 plots; about 25% relocated more or less adequately; ~15% inadequately relocated. Y-plots showed highest relocation difficulty (23% failure).
- Plate/plot relocation: assessors located 69.3% of plates; total recovery rate potentially around 40–45% when including plots and approximate matches. QA in 1991 achieved 87% adequate relocation for CS1990 plates.
- Overall takeaway: CS2000 plot relocation is feasible eight years on, but accuracy is lower than the QA of CS1990; some misplacements occurred (e.g., wrong bank/side of hedge, wrong boundary feature).

### Species Concordance and Recording Accuracy
- Concordance: about 71% of records confirmed as present in the resurvey; ~2% non-concordances due to management/seasonal changes between original and resurvey.
- Overall initial recording accuracy: ~73%, slightly lower than CS1990 (~78%), largely due to plot relocation errors.
- Species mis-matches and concordance analysis detailed (types cover mis-identifications, overlooked species, and plot-location/orientation issues).

### Vegetation Cover and Frequency Changes
- Comparisons of 30 most frequent species showed several significant differences in cover levels for a minority of species (notably several grasses).
- Overall agreement on cover levels between CS2000 surveyors and QA assessors was moderate to good for many species; some species showed significant differences likely due to seasonality, phenology, or identification challenges.
- The QA found longer species lists per plot than CS2000, with increases broadly similar to previous QA cycles.

### Land Cover, Boundaries, and Mapping
- Primary land cover codes: high concordance between CS2000 and QA (about 88%); BAP codes lower (around 77%).
- Overall primary land cover agreement (excluding BAP): ~87.5%; including BAP: ~83–87% depending on aggregation.
- Primary boundary codes: ~85% concordance; boundary qualifiers ~83%; overall boundary coding concordance ~92% for primary codes; boundary heights ~89% concordance; stockproof condition ~84%.
- Hedge/wall and boundary shapes: limited success with new hedge codes; many hedges could be described using existing code 374 (box-shaped hedge); mis-matches often involved hedge/stockproof changes and occasional mis-identification of boundary features.
- Boundary height and stockproof nature: high reliability; some occasional misinterpretation of stockproof status.

### Change Recording and Change Coding
- Change occurrences: 177 sampled changes; surveyors and assessors disagreed on 51.4% of changes; 33.9% of changes not noted by CS2000; 14.7% change noted by CS2000 but not substantiated by assessors.
- A substantial portion of observed changes since 1990 appears missed or mis-coded; this raises caution for using change strings as sole evidence of land-use or habitat change.
- Some instances show changes that may reflect original coding errors or misinterpretations, rather than real ecological change.

### Arable Plots
- Only five arable margin plots analyzed; concordance was very poor, with many mismatches attributable to seasonality and limited familiarity with ruderal species.
- Recommendation: plan multiple visits when working with arable margins to improve reliability.

### Direction of Vegetation Change and Ordination
- DECORANA ordination (Axis 1) shows axis shifts largely reflecting plot-location/orientation and cover mis-matches rather than true directional change.
- No directional bias detected in mean axis scores between CS2000 and QA overall.

## Data Quality Implications for GIS Specialists
- Spatial accuracy: Plot relocation and plate recovery rates indicate a significant, but manageable, level of spatial uncertainty in historical CS2000 data. GIS workflows should account for potential locational and orientation errors, especially for smaller plots (e.g., Y-plots).
- Coding schemes: Land cover and boundary coding show strong overall concordance but notable discrepancies in certain codes (notably some grasses and hedges). When integrating with other datasets, treat CS2000 codes with awareness of potential misclassifications and seasonality effects.
- Change detection: Change concurrence is modest; many changes are not consistently captured or substantiated. For change analyses, CS2000 change data should be treated as indicative and validated with field notes or higher-resolution data where possible.
- Boundary and hedge data: High agreement in boundary-related attributes supports GIS use for landscape-scale analyses, though some hedge-shape and wall-condition codes require careful interpretation or supplementary sources.
- Arable plots: Very limited data and poor concordance suggest lower reliability for arable-margin components within GIS products; consider excluding or flagging these in mapping products until additional data are collected.
- Temporal comparisons: Comparisons with CS1990 show general methodological consistency; however, eight-year relocation and code-change dynamics require careful alignment when combining CS2000 with earlier datasets.

## Practical Recommendations for GIS Production
- Flag uncertain plots: mark plots with relocation uncertainty or orientation issues to guide users and future QA work.
- Use code dictionaries: rely on primary land cover and boundary code concordances; corroborate BAP and hedge/wall codes with ancillary data where possible.
- Document changes with uncertainty: for change analyses, include confidence estimates or a checklist of which changes are substantiated.
- Plan targeted QA for arable margins: anticipate seasonality and species identification challenges; schedule multiple visits if these are critical to mapping outputs.
- Preserve metadata: ensure QA provenance, survey dates, plot types, and QA outcomes are captured with GIS records to support traceability and reproducibility.

## Annex and Protocol References
- Annex A: QA protocol details for locating plots, boundaries, and comparative coding.
- Annex B: Dates of survey and measures of surveyor efficiency; square-by-square efficiency and agreement metrics.
- Annex C and other coding annexes: CS2000 primary/secondary/cov er codes and BAP classifications; used for mapping accuracy assessments.

## Conclusion
- CS2000 QA demonstrates generally solid map-based data quality with strong concordance in land cover and boundary coding, and acceptable plot relocation performance for GIS applications.
- While overall accuracy is high in many components, notable limitations exist in plot relocation, change recording, arable plots, and some vegetation-cover codings.
- For GIS specialists, CS2000 provides a reliable but nuanced dataset requiring careful documentation of uncertainty, with opportunities to refine data integration, change detection, and heat-map generation through targeted QA-informed workflows.