# Experimental design/Sampling regime

- This document describes a census of heathland and associated vegetation in Dorset, UK.
- Plot framework: 4 hectares per plot (200 m x 200 m), aligned to the national OS grid; include all plots within Dorset known to contain heathland vegetation in 1978.
- Sampling scope: 3110 plots identified in 1978; repeat surveys conducted in 1987, 1996, and 2005.

- Vegetation types recorded: dry heath; humid/wet heath; mire; brackish marsh; carr; scrub; hedges and boundaries; woodland; grassland; sand dunes; sand and clay; ditches/streams/rivers/pools/ponds; arable; urban; other land uses; bare ground. Humid and wet heath are combined for this dataset.

- Abundance measurement: within each plot, the cover of each vegetation type is estimated on a 3-point scale (1 = 1–10%, 2 = 11–50%, 3 = >50%).

- Fieldwork: plots located using maps and air photos; compass navigation; hand-held GPS used in later surveys to aid location.

- Calibration and analysis: no calibration values or analytical methods were documented; data processing relies on a specific algorithm to convert 3-point scores into area estimates.

- Data processing: an algorithm converts 3-point abundance scores to hectares within each 4 ha plot:
  - A1, A2, A3 represent estimated areas corresponding to scores 1, 2, and 3.
  - Rules determine how area is allocated among vegetation types within each plot, including constraints (e.g., at most one score of 3 per plot) and multiple case-based allocations depending on N1, N2, N3 counts.
  - The total area for a plot is 4 ha; the algorithm distributes residual area among invigorated categories based on defined cases and interpolation.

- Heath delineation and total area:
  - Individual plots are joined into broader “heaths” using an 8-neighbour rule (adjacent horizontally, vertically, or diagonally).
  - Total heath area is the sum of true heathland and associated vegetation types (including dry/wet/humid heath, mire, brackish marsh, carr, scrub, hedges/boundaries, and other land uses as relevant).

- Quality control: initial group-based recording followed by regular rotation of two-person pairs to ensure consistency.

- Data structure:
  - A single CSV file with summed area estimates (hectares) for each major vegetation type within each heath and year.
  - Columns include: Year, Heath Number, Total Heath area, DH (dry heath), WH/HH (humid/wet heath), M (mire), B (brackish marsh), C (carr), S (scrub), H (hedges and boundaries), W (woodland), G (grassland), SD (sand dunes), ST (sand and clay), D (ditches/pools), AR (arable), UR (urban), OT (other land uses), B (bare ground).

- Miscellaneous supporting documents: none.

- Appendix 1: Vegetation descriptions for major types (definitions and characteristic species provided to contextualise classifications).