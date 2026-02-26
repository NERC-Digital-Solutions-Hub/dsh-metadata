# Census of the heathland and associated vegetation from Dorset, UK

## Overview
- A census dataset of heathland and associated vegetation in Dorset, UK.
- Plot design: 4 ha plots (200 m x 200 m) aligned to the national OS grid; 3110 plots identified in 1978.
- Repeated surveys: 1987, 1996, 2005.
- Major vegetation types recorded with definitions in Appendix 1.
- Output: a single CSV file with summed area estimates (hectares) for each vegetation type in each heath and year.

## Sampling design and plot assembly
- Within each plot, the cover of all vegetation types was estimated on a 3-point abundance scale (1 = 1-10%, 2 = 11-50%, 3 = >50%).
- Plots were joined into larger units called heaths using an 8-neighbour rule (adjacent or diagonally-adjacent heath plots merged).
- Total heath area is computed by summing areas of all relevant land cover types within each heath (including heath-related and other land uses).

## Data collection methods
- Major vegetation types recorded include: dry heath; humid/wet heath; mire; brackish marsh; carr; scrub; hedges/boundaries; woodland; grassland; sand dunes; sand and clay; ditches, streams, rivers, pools, ponds; arable; urban; other land uses; bare ground.
- Field location relied on maps, air photographs, compass; later surveys used handheld GPS.
- Calibration steps: none.
- Analytical methods: none.

## Data processing and area estimation
- An algorithm converts 3-point abundance scores into area estimates for each vegetation type within a plot.
- Key rules (illustrative):
  - Each score-1 is treated as 5% of plot area (0.05 x 4 ha = 0.2 ha).
  - Remaining area is allocated to scores 2 and 3 according to several case-based rules depending on N1, N2, N3 (counts of scores 1, 2, and 3).
  - Special cases handle distributions when multiple 2s or a single 3 occur, with interpolation between extremes.
  - In cases with multiple 2s, a fixed proportion for 3s may be used (e.g., 0.55 x T for A3 in certain scenarios).
- The results yield per-vegetation-type area estimates per heath per year.
- The individual plots are aggregated into heaths; the total heath area sums inclusive of associated vegetation types.

## Quality control
- Surveyors initially worked as a group, then in rotating pairs to maintain consistency across surveys.

## Data structure and schema
- Format: a single CSV file.
- Core columns: Year, Heath Number, Total Heath area, followed by area estimates for major vegetation types:
  - DH - dry heath; WH/HH - humid heath/wet heath; M - mire; B - brackish marsh;
  - C - carr; S - scrub; H - hedges and boundaries; W - woodland; G - grassland;
  - SD - sand dunes; ST - sand and clay; D - ditches, streams, rivers, pools, ponds;
  - AR - arable; UR - urban; OT - other land uses; B - bare ground.
- Note: The dataset uses B for brackish marsh in the main list, and B for bare ground in a later note, indicating a potential naming ambiguity.

## Appendix 1. Vegetation descriptions
- Detailed definitions for each vegetation type (e.g., Dry heath dominated by Calluna vulgaris with associated species; Humid/Wet heath characteristics; Mire/peatland composition; Brackish marsh; Carr; Scrub; Hedges/boundaries; Woodland; Grasslands; Sand dunes; Sand and clay; Wetland water features).
- Humid and dry heath are distinguished by drainage and soil conditions; mire emphasizes Sphagnum and associated species; other categories cover transitions and ancillary land uses.
- This appendix provides species-level context used to interpret the vegetation categories.

## Miscellaneous notes
- Supporting documents: none.
- Data scope covers four survey years (1978 baseline with 1987, 1996, 2005 repeats).
- Aimed at enabling longitudinal analysis of heathland change and vegetation composition over time.

## Implications for Data Leaders
- Strengths for data strategy:
  - Longitudinal, geographically-grounded census with a clear sampling frame and repeat design.
  - Explicit methodology for converting categorical cover to quantitative area estimates, enabling comparability over time.
  - Comprehensive data structure capturing a wide range of land cover types and their spatial aggregation into heaths.
  - Built-in quality control and documented data processing steps.
- Key considerations for governance and improvements:
  - Clarify data provenance and reproducibility of the area-estimation algorithm (document any available code or provide a reference implementation).
  - Address potential metadata gaps and ensure consistent terminology (e.g., potential naming conflict between bare ground and brackish marsh).
  - Assess data standardization and interoperability with other datasets (GIS formats, coordinate systems, unit conventions).
  - Consider data publication practices (data licensing, access, and versioning for future updates).
  - Ensure continued documentation of definitions (Appendix 1) to support cross-project interpretation and re-use.