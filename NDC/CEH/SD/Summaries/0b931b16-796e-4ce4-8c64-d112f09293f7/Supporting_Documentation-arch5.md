# Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013

## Overview
- A long-term vegetation dataset from Moor House National Nature Reserve (banner site NY730320) covering 1954–2013, focusing on rotational burning and grazing effects.
- Experimental design features four replicate blocks (A–D) with altitude gradient from 594 to 625 m, arranged in randomized split-plot layout to test fenced (excluded grazing) vs unfenced (grazed) conditions and three burning regimes: no burn (N), long-rotation burn (L), and short-rotation burn (S).
- Burning events occurred mainly in winter under suitable weather conditions, with burns in 1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07 (slightly delayed), and 2016/17; the 2006/07 burn occurred two years later than planned.
- Data types evolve over time: initial vegetation recording in 1961 and 1965 using quadrats and the DOMIN cover scale; from 1972 onwards, vegetation is recorded with pin quadrats (height stratification) across repeated sampling campaigns in 1972, 1982, 1992, 2001, and 2013.
- Data are organized into two main CSV datasets (1961/1965 quadrat data and 1972 onwards pin data) with consistent coding (VESPAN species numbers; updated species names) to support discoverability and reuse within the ECN database.

## Experimental design and site details
- Location: Moor House NNR in OS grid NY730320; burnt blanket bog habitat.
- Structure: Four blocks A–D arranged along slope; each block 90 m long and 60 m wide, split into two 90 m × 30 m strips (fenced and unfenced within each block), and each strip subdivided into three 30 m × 30 m cells.
- Treatments:
  - Fenced vs unfenced within each strip (grazed vs grazed-excluded).
  - Within strips, three burning sub-treatments applied randomly to cells: no burn (N), long-rotation burn (L), short-rotation burn (S).
- Management: Burning conducted in winter under suitable weather to remove surface vegetation and litter without deep peat burning.

## Data collection methods

### Quadrats: 1961 and 1965
- Quadrats: 1 m², arranged on a 5 m grid within each plot; 25 quadrats per plot in 1961, reduced to 10 per plot in 1965 (recorded at positions 6–15).
- Assessment: DOMIN cover-abundance scale (1–9 plus negative values for rare) used to score species cover within each quadrat.
- Data organization (1961/1965):
  - Year, Block (A–D), Treatment (N, L, S), Fenced (UF or F), Quadrat (1–25), DOMIN score, Species number (VESPAN), Species name (updated to current nomenclature).
- Data capture: Conducted by experienced botanists, maintaining consistent methods.

### Pin method: 1972 onwards
- Sampling window: 8th growing season in July–August; recorded in 1972, 1982, 1992, 2001, and 2013 (2001 at the 7th season).
- Plot layout: Each 30 m × 30 m cell contains a central sampling plot (14 m across slope, 6 m up slope). Within each plot, 7 transects (starting 1 m from the marker, 2 m apart; left/right side designated A/B). Each transect contains six 1 m quadrats (1–6 along the transect).
- Coverage: 82 one-square-meter quadrats per plot (7 transects × 6 quadrats × 2 sides × 1 plot per cell; scaled to dataset size).
- Pin frame: 1 m long frame with 10 pin positions spaced 10 cm apart; two methods used:
  - Pin positions and height strata recorded to measure vegetation height layers.
  - Strata: 1 (>30 cm), 2 (20–30 cm), 3 (10–20 cm), 4 (0–10 cm); 99 indicates unstratified.
  - For non-vascular plants (bryophytes, lichens) and non-living features (rock, litter, bare soil, peat, water), data are unstratified (99) and only presence/absence or touches are counted where applicable.
- Data organization (1972 onwards):
  - Year (1972, 1982, 1992, 2001, 2013), Block (A–D), Treatment (N, L, S), Fenced (UF or F), Stratified (s) or presence-only (u), Transect (1A–7B), Quadrat (1–6), Frame (1–5), Pin, Strata (1–4 or 99), Score (touch counts for vascular plants in stratified data; 1 for non-vascular or unstratified data in some years), Species number, Species name (updated nomenclature).
- Quality assurance: Surveys conducted by experienced botanical surveyors in pairs with consistent methods and equipment.

## Data structure and dataset schemas

### Quadrat method 1961 and 1965
- Dataset: single CSV
- Columns:
  - Year (1961, 1965)
  - Block (A–D)
  - Treatment (S, L, N)
  - Fenced (UF, F)
  - Quadrat (1–25)
  - DOMIN score (values -1, 1–9)
  - Species number (VESPAN)
  - Species name (updated nomenclature)

### Pin method 1972 onwards
- Dataset: single CSV
- Columns:
  - Year (1972, 1982, 1992, 2001, 2013)
  - Block (A–D)
  - Treatment (S, L, N)
  - Fenced (UF, F)
  - Stratified (s or u)
  - Transect (1A–7B)
  - Quadrat (1–6)
  - Frame (1–5)
  - Pin
  - Strata (1–4 or 99)
  - Score (touch counts or presence/absence rules by year)
  - Species number (VESPAN)
  - Species name (updated nomenclature)

## Quality control, data processing, and standards
- Fieldwork performed by experienced botanists in pairs; standardized recording methods across surveys.
- Two main data collection methods reflect methodological evolution and ensure long-term continuity.
- Use of standardized identifiers:
  - VESPAN species numbers for cross-dataset linkage within the ECN database.
  - Updated species names maintain current nomenclature.
- Data capture differentiates vascular vs non-vascular plants, with corresponding stratified vs unstratified recording rules.
- Records include clear treatment and fencing status to support comparative analyses across management regimes.

## Accessibility, metadata, and governance
- Data are prepared for integration into the Environmental Change Network (ECN) database; consistent metadata and coding facilitate discoverability and re-use.
- Documentation includes explicit field methods, sampling designs, and data schemas to support reproducibility and data provenance.
- Historical methodological notes (e.g., 2006/07 burn timing deviation) are documented to aid interpretation and data quality assessment.

## Limitations, challenges, and considerations for data stewards
- Shifts in methodology over time (quadrats in 1961/1965 vs pin-frame approach from 1972) require careful harmonization for cross-year analyses.
- Some years include presence-absence data instead of full stratified counts (e.g., certain strata coverage in 1992 and 2001), affecting comparability of touch counts across all years.
- Data normalization may be needed for species taxonomy updates; ensure alignment with current nomenclature in downstream use.
- Data availability may be influenced by plan timing of burns and potential gaps (e.g., late 2006/07 burn).
- Large-scale, multi-year, multi-treatment data require robust versioning, clear lineage, and consistent metadata documentation to support governance and reuse.

## Supporting documents and references
- Marrs, R.H., Rawes, M., Robinson, J., & Poppitt, S. (1986). Long-term studies of vegetation change at Moor House NNR: guide to recording methods and the database. Merlewood Research and Development Paper 109.
- Adamson, J.K. & Kahl, J. (2001). Changes in vegetation at Moor House within sheep exclosure plots established between 1953 and 1972. CEH Project C00162.
- www.ecn.ac.uk