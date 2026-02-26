# Experimental design/Sampling regime

- A census of heathland and associated vegetation in Dorset, UK, using 4-hectare plots (200 m x 200 m) aligned to the national Ordnance Survey grid.
- All plots within Dorset known to contain heathland vegetation in 1978 were surveyed for major vegetation types.
- Total plots identified: 3110 in 1978; repeat surveys conducted in 1987, 1996, and 2005.

## Dataset scope

- Covers major vegetation types including dry heath, humid/wet heath, mire, brackish marsh, carr, scrub, hedges and boundaries, woodland, grassland, sand dunes, sand and clay, ditches/streams/pools, arable, urban, other land uses, and bare ground.
- Data structured to enable comparisons across time (1978, 1987, 1996, 2005).

# Collection Methods

- Within each 4 ha plot, the cover of all vegetation types was estimated and recorded on a 3-point abundance scale:
  - 1 = 1–10% cover
  - 2 = 11–50% cover
  - 3 = >50% cover
- Definitions of vegetation types are provided in Appendix 1.

## Plot location and navigation

- Plots located in the field using maps and aerial photographs, with a compass.
- In the latter two surveys, a hand-held GPS was used to aid location.

# Calibration steps and values

- No calibration steps or values are described.

# Analytical Methods

- No explicit analytical methods are described beyond the area-estimation algorithm that converts 3-point scores to area estimates (see below).

# Nature and Units of recorded values

- An algorithm converts 3-point abundance scores into area estimates for each vegetation type within each plot.
- Key points of the algorithm:
  - Plot area T = 4 ha.
  - For a primary vegetation type, counts N1 (score 1), N2 (score 2), N3 (score 3, with at most one such score per plot).
  - A1, A2, A3 are area estimates corresponding to scores 1, 2, 3 respectively.
  - A1 is fixed at 5% of the plot (A1 = 0.05 × T).
  - Remaining area R is distributed among types with scores 2 or 3 according to a series of rules depending on N1, N2, N3 (seven detailed cases), including a rule that a score of 3 represents at least ~55% of the plot in certain configurations.
  - When N2 > 1, A3 is set to 0.55 × T and A2 is allocated from the remaining area.
- These rules allocate the per-plot area for each vegetation type based on the observed abundance scores.

## Heaths and aggregation

- Individual plots are joined into larger “heaths” using an 8-neighbour rule (horizontal, vertical, or diagonal adjacency).
- Heaths with any presence of dwarf shrub heathland (at least one of dry heath, humid/wet heath, or mire) are combined into larger heath units.
- The total heath area for heathland vegetation within each heath is calculated by summing the areas of all constituent vegetation types (including dry heath, humid/wet heath, mire, and associated types such as brackish marsh, carr, scrub, hedges/boundaries, woodland, grassland, sands, ditches, arable, urban, and other uses).

# Quality Control

- Surveyors initially worked as a group, then in pairs, with regular rotation to ensure consistency.

# Details of data structure

- One CSV file containing summed area estimates (hectares) for each major vegetation type in each heath for each year.
- Columns include: Year, Heath Number, Total Heath area, DH (dry heath), WH/HH (humid/wet heath), M (mire), B (brackish marsh), C (carr), S (scrub), H (hedges and boundaries), W (woodland), G (grassland), SD (sand dunes), ST (sand and clay), D (ditches/streams/rivers/pools), AR (arable), UR (urban), OT (other land uses), B (bare ground).

# Miscellaneous supporting documents

- None.

# Appendix 1. Vegetation descriptions

- Detailed descriptions for each vegetation category:
  - Dry heath: dominance by Calluna vulgaris with associated species; notes on mosses and lichens in older stands.
  - Humid/Wet heath: combined with humid and wet variants in this dataset; typical species include Calluna vulgaris, Erica tetralix, and others; differences based on drainage and water table.
  - Mire: peatland with Sphagnum spp. and Calluna vulgaris; species composition varies with water table and chemistry.
  - Brackish marsh: transitional vegetation between mire and true salt-marsh; often Phragmites australis or Spartina anglica.
  - Carr: woodland on organic soils with open canopy development; often Salix and Betula.
  - Scrub: seral stage between heath and woodland; typically Betula, Pinus, Ulex, Salix, with exclusions for taller trees.
  - Hedges and boundaries: included to complete the plot-wide cover.
  - Woodland: trees >5 m tall with canopy cover; semi-natural or planted.
  - Grasslands: semi-natural or unimproved, dominated by dry grasses; correlations with heather/gorse presence noted.
  - Sand dunes: coastal vegetation dominated by Marram grass (Ammophila arenaria).
  - Sand and clay: recording of natural sand exposures or man-made features.
  - Ditches, streams, rivers, pools: all open water bodies recorded (pools defined as <3 m diameter).
  - Arable: recently cultivated land with or without crop.
  - Urban: housing, parks, roads, etc.
  - Bare ground: natural or semi-natural bare substrates; also includes recently burnt heath.
  - Other land uses: encompasses unclassifiable or miscellaneous land cover (industrial, cleared land, etc.).