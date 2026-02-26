# Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013. Rose, R.J., Marrs, R.H., O'Reilly, J. & Furness, M.

## Overview
- A long-term dataset of vegetation responses to rotational burning and grazing at Moor House National Nature Reserve (OS grid NY730320), spanning 1954–2013.
- Experimental design comprises four replicate blocks (A, B, C, D) with fenced (grazed only by grouse/small mammals) and unfenced (grazed by sheep) strip treatments.
- Three burning sub-treatments applied within strips: no burning (N), short rotation burn (S, 10-year intervals), and long rotation burn (L, 20-year intervals).
- Data collected via two main methods across time: Quadrat method (1961, 1965) and Pin method (1972 onwards), enabling assessment of plant cover, height stratification, and species presence/abundance under different management scenarios.

## Experimental design
- Location: Moor House NNR, 1954 onward.
- Blocks: A (lowest altitude, 594 m) to D (highest altitude, 625 m); blocks oriented to slope.
- Split-plot design: within each block, fenced vs unfenced strips; each strip divided into 3 sub-cells (30 m × 30 m), and each cell subdivided into 30 m × 30 m cells treated with N, S, or L in random allocation.
- Burning history: plots burned at multiple timepoints (1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07, 2016/17); 2006/07 burn occurred two years later than planned.

## Data collection methods

### Quadrat method (1961 and 1965)
- Timing: Initial post-burn vegetation surveys in 1961 (25 quadrats per block) and 1965 (reduced to 10 quadrats per plot; 6–15 recording points within plots).
- Method: 1 m × 1 m quadrats with Domin scale for cover estimation.
- Layout: Quadrats positioned on a 5 m grid across plots; quadrat numbering 1–25 in 1961 (and 4 × 1–4 grid references listed for 1965).
- DOMIN scale: 9 to 1 (cover-abundance 91–100% down to <4% rare/occasional) with -1 used for very rare occurrences.
- Output: Dataset includes Year, Block, Treatment (N, S, L), Fenced (UF or F), Quadrat, DOMIN score, Species number (VESpan code), Species name.

### Pin method (1972 onwards)
- Timing: Surveys conducted in 1972, 1982, 1992, 2001, and 2013 (8th growing season, July–August; 2001 recorded in 7th season).
- Plot layout: Each 30 m × 30 m cell contains a central 14 m × 6 m vegetation recording plot; within each plot, 7 transects with 1 m × 1 m quadrats along transects (positions 1A–7B).
- Data collection: Pin frame (1 m long) with 10 pins spaced 10 cm apart; two measurement modes:
  - Absolute counts: number of touches per species in four height strata.
  - Presence/absence: for non-vascular species and unstratified data.
- Strata for vascular plants: >30 cm, 20–30 cm, 10–20 cm, 0–10 cm (coded as 1–4); 99 used for unstratified data or non-vascular/bryophytes/lichens.
- Non-vascular data and physical features (litter, bare soil, rock, peat) recorded as unstratified (99) with touches not counted.
- Data capture per quadrat: 5 frame positions (1, 2, 3, 4, 5) representing distance from origin; pins allocated randomly; 7 transects with left/right sides (A/B) and 82 1 m² quadrats per plot.
- Output: Dataset fields include Year, Block, Treatment (N, S, L), Fenced (UF, F), Stratified (s or u), Transect, Quadrat, Frame, Pin, Strata, Score (touch counts for vascular taxa in stratified data; presence counts for non-vascular and unstratified data), Species number, Species name.

## Data structure and fields

- Quadrat method dataset (1961 and 1965)
  - Year
  - Block (A, B, C, D)
  - Treatment (S = short rotation burn, L = long rotation burn, N = no burning)
  - Fenced (UF = unfenced; F = fenced)
  - Quadrat (1–25)
  - DOMIN score (integer values corresponding to cover estimates)
  - Species number (VESpan code in ECN database)
  - Species name (nomenclature updated over time)

- Pin method dataset (1972, 1982, 1992, 2001, 2013)
  - Year
  - Block (A, B, C, D)
  - Treatment (S, L, N)
  - Fenced (UF, F)
  - Stratified (s = stratified, u = unstratified/presence only)
  - Transect (1A–7B)
  - Quadrat (1–6 along transect)
  - Frame (1–5)
  - Pin (position along the frame)
  - Strata (1 = >30 cm, 2 = 20–30 cm, 3 = 10–20 cm, 4 = 0–10 cm, 99 = unstratified)
  - Score (touch counts for vascular taxa in stratified data; presence counts for non-vascular and unstratified data; ranges and applicability vary by year)
  - Species number (VESpan)
  - Species name

## Data quality, standardization, and provenance
- Fieldwork conducted by experienced botanical surveyors in pairs to ensure consistency.
- Data collection methods remained aligned with documented protocols across time, enabling cross-year comparisons.
- Nomenclature updates applied to species names to align with current standards.
- Supporting documentation and context available in related reports and the Environmental Change Network (ECN) database.

## Temporal coverage and burning events
- Burning history across years: 1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07 (two years late), 2016/17.
- Vegetation data points spanning:
  -  Agricultural quadrat data: 1961 and 1965 (quadrats per block; DOMIN scores)
  -  Pin data: 1972, 1982, 1992, 2001, 2013 (height-stratified and presence/absence data)

## Applications for data use and product development
- Potential data products:
  - Time-series dashboards by block, treatment, and fencing status to track vegetation changes under different burning and grazing regimes.
  - Stratified vs. unstratified comparisons of vascular plant abundance and height distribution.
  - Cross-method integration that merges DOMIN-based quadrat data (1961/1965) with pin-based height-stratified data (1972–2013) for holistic vegetation change analysis.
- Considerations for data use:
  - Harmonize treatment coding (N, S, L) and fencing status across datasets.
  - Manage differences in measurement units and data granularity between quadrat (DOMIN scale) and pin (touch counts or presence/absence) methods.
  - Be mindful of changes in sampling intensity (e.g., 25 → 10 quadrats in 1965; variable frame/pin-based sampling years).

## Miscellaneous supporting documents
- Marrs, R.H., Rawes, M., Robinson, J., & Poppitt, S. (1986). Long-term studies of vegetation change at Moor House NNR: guide to recording methods and the database.
- Adamson, J.K. & Kahl, J. (2001). Changes in vegetation at Moor House within sheep exclosure plots established between 1953 and 1972.
- www.ecn.ac.uk