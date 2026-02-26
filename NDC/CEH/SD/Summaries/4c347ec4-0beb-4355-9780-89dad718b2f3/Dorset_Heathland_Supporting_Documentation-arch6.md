# Census of the heathland and associated vegetation from Dorset, UK

## Overview
- A census dataset documenting heathland and associated vegetation within Dorset, UK.
- Based on a 4 ha (200 m x 200 m) plot grid, identifying plots in 1978 that contained heathland vegetation; repeat surveys conducted in 1987, 1996, and 2005.
- Provides summed area estimates (in hectares) for major vegetation types across each heath and year.

## Study design and sampling
- 3110 plots identified in 1978 within the Dorset county boundary that contained heathland vegetation (dry heath, humid/wet heath, mire).
- Plots joined into larger “heaths” using an 8-neighbour rule (adjacent or diagonally adjacent plots with heathland vegetation).
- The total heath area is the sum of all included vegetation types within each heath.

## Data collection and measurements
- Major vegetation types recorded per plot: dry heath; humid heath/wet heath; mire; brackish marsh; carr; scrub; hedges and boundaries; woodland; grassland; sand dunes; sand and clay; ditches, streams, rivers, pools, ponds; arable; urban; other land uses; bare ground.
- Within each plot, the cover of each vegetation type was estimated on a 3-point scale:
  - 1 = 1-10% cover
  - 2 = 11-50% cover
  - 3 = >50% cover
- Fieldwork used maps, air photographs, compasses; later surveys (1987 onward) incorporated hand-held GPS for location.

## Data processing and estimation
- An algorithm converts 3-point abundance scores to area estimates for each vegetation type within a plot.
- Key steps:
  - Plot area T = 4 ha; count scores N1 (score 1), N2 (score 2), N3 (score 3; at most one).
  - Score 1 areas (A1) set to 5% of the plot (0.05 T).
  - Remaining area R allocated to scores 2 and 3 according to specified rules, including special cases when N2 or N3 are present.
  - For cases with N2 > 0 and N3 = 0, distribute R among score-2 types; when N2 = 0 and N3 = 1, assign all R to the 3-score type; else interpolate between extremes for mixed cases.
  - In complex cases, area allocations (A2, A3) follow defined relationships to N1, N2, N3.
- Individual plots are aggregated into heaths; total heath area sums across true heathland and associated vegetation types.
- Vegetation types are aggregated into a single set of area estimates per heath per year.

## Data structure and contents
- File format: a single CSV with summed area estimates (hectares) for each major vegetation type in each heath for each survey year.
- Columns include: Year, Heath Number, Total Heath area, and abbreviations for each vegetation type:
  - DH (dry heath); WH/HH (humid/wet heath); M (mire); B (brackish marsh); C (carr); S (scrub); H (hedges and boundaries); W (woodland); G (grassland); SD (sand dunes); ST (sand and clay); D (ditches, streams, rivers, pools, ponds); AR (arable); UR (urban); OT (other land uses); B (bare ground).

## Temporal coverage and repeats
- Survey years: 1978 (baseline), 1987, 1996, and 2005.
- Repeated measurements enable assessment of changes in heathland extent and vegetation composition over time.

## Quality assurance
- Early surveys conducted as a group, later rotated in pairs to maintain consistency and standardization across surveyors.

## Output and potential uses
- Enables analysis of spatial and temporal dynamics of heathland vegetation in Dorset.
- Outputs can support dashboards, reports, or self-serve exploration of trends by heath and vegetation type.
- Appendix 1 provides detailed vegetation descriptions to support interpretation of categories and transitions between heath types.

## Appendix: vegetation descriptions (summary)
- Detailed, species-level descriptions for each vegetation type (e.g., dry heath dominated by Calluna vulgaris; humid/wet heath with Calluna and Erica spp.; mire with Sphagnum and ericaceous species; various transitions to scrub, carr, marsh, and woodland).
- Descriptions clarify definitions and boundaries between related vegetation communities used in the dataset.