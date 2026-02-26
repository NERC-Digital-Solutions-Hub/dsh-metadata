# Experimental design/Sampling regime

- This dataset is a census of heathland and associated vegetation from Dorset, UK.
- Plot size: 4 ha (200 m x 200 m) on the national OS mapping grid; surveys include all plots within Dorset that contained heathland vegetation in 1978.
- Sample scope: 3110 plots identified in 1978.
- Temporal coverage: repeat surveys in 1987, 1996, and 2005.

# Collection Methods

- Major vegetation types recorded include: dry heath; humid heath/wet heath; mire; brackish marsh; carr; scrub; hedges and boundaries; woodland; grassland; sand dunes; sand and clay; ditches, streams, rivers, pools, ponds; arable; urban; other land uses; bare ground.
- Within each plot, cover of each vegetation type estimated on a 3-point abundance scale:
  - 1 = 1-10% cover
  - 2 = 11-50% cover
  - 3 = >50% cover

# Fieldwork and Instrumentation

- Plots located in the field using maps, air photographs, and a compass; GPS used in the latter two surveys to aid location.

# Calibration and Analytical Methods

- Calibration steps and analytical methods: None reported.

# Nature and Units of Recorded Values

- An algorithm converts 3-point scores into area estimates for each vegetation type within a plot.
- Plot-level details:
  - Plot area T = 4 ha with primary vegetation scores N1 (score 1), N2 (score 2), N3 (score 3, at most one per plot).
  - A1, A2, A3 are estimated areas corresponding to scores 1, 2, 3.
  - Rules define how to allocate the 4 ha among vegetation types based on score patterns, including cases with only scores 2, cases with score 3, and cases with mixed 2s and 3s.
  - In total, the algorithm yields area estimates for each vegetation type represented in a plot.
- Post-processing: Individual plots are joined into 'heaths' using an 8-neighbour rule (horizontal, vertical, or diagonal adjacency) to form contiguous heath units.
- Heath-level calculations: Total heath area is the sum of true heathland and associated vegetation types (across all included land-cover types in each heath).

# Quality Control

- Recording consistency maintained by initial group work and then regular rotation in pairs.

# Details of data structure

- File format: single CSV.
- Contents: summed area estimates (in hectares) for each major vegetation type in each heath for each survey year.
- Columns:
  - Year, Heath Number, Total Heath area
  - DH (dry heath); WH/HH (humid/wet heath)
  - M (mire)
  - B (brackish marsh)
  - C (carr)
  - S (scrub)
  - H (hedges and boundaries)
  - W (woodland)
  - G (grassland)
  - SD (sand dunes)
  - ST (sand and clay)
  - D (ditches, streams, rivers, pools, ponds)
  - AR (arable)
  - UR (urban)
  - OT (other land uses)
  - B (bare ground)

# Appendix 1. Vegetation descriptions

- Dry heath: dominated by Calluna vulgaris with Erica cinerea, Ulex minor/gallii; typical associated species listed; mosses and lichens common in older stands.
- Humid heath/Wet heath: combined category; occurs with poor drainage and gley soils; key species include Calluna vulgaris and Erica tetralix; wet heath may include Sphagnum spp. and Molinia caerulea; dry-to-wet transition forms exist.
- Mire: peatland with variable composition; Sphagnum spp. important; Calluna vulgaris and Erica spp. often present but not dominant; other typical associates listed.
- Brackish marsh: transitional area between mire and true salt-marsh; often dominated by Phragmites australis or Spartina anglica with some heath/mire species.
- Carr: woodland on organic soils; closed canopy with species like Salix and Betula; ground water remains waterlogged.
- Scrub: seral stage toward woodland; >50% cover by scrub species; includes Betula, Pinus, Ulex spp., Salix, with other typical heathland shrubs; certain ground covers (Pteridium aquilinum, Ulex galli, Gaultheria shallon) also recorded as scrub.
- Hedges and boundaries: included to complete total plot cover.
- Woodland: trees (>5 m tall) with closed canopies or >50% ground cover.
- Grasslands: semi-natural/unimproved grasses; dry grasslands dominated by Agrostis spp. and Festuca spp.; wet Molinia caerulea grassland included when dwarf shrub cover is <25%.
- Sand dunes: coastal systems dominated by Marram grass (Ammophila arenaria); transitional forms to heathland exist.
- Sand and clay: records natural sand exposures or man-made features like pits/spoil heaps.
- Ditches, streams, etc.: all open water areas recorded; pools defined as <3 m diameter.
- Arable: recently cultivated land with/without crops.
- Urban: housing, parks, roads, etc.
- Bare ground: natural or semi-natural bare ground, recently burnt heath, or similar.
- Other land uses: miscellaneous land-cover types not represented above (industrial, development, cleared land, etc.).