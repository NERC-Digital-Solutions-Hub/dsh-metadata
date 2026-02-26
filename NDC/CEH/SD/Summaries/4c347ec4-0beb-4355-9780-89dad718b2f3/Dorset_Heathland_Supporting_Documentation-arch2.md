# Census of the heathland and associated vegetation from Dorset, UK

- Purpose and scope
  - A dataset census of heathland and associated vegetation in Dorset, UK, covering major vegetation types and their area estimates over time.
  - Humid heath and wet heath are combined into a single category in this dataset.
  - Designed to support environmental monitoring and policy assessment through standardized, comparable outputs.

- Experimental design and sampling regime
  - Plot size: 200 m x 200 m plots (4 hectares per plot) aligned to the national Ordnance Survey grid.
  - Target population: all plots within Dorset known to contain heathland vegetation (dry heath, humid/wet heath, mire) in 1978.
  - Sampling frame: 3110 plots identified in 1978.
  - Repeated measures: repeat surveys conducted in 1987, 1996, and 2005.

- Data collection methods
  - Major vegetation types recorded: dry heath; humid heath/wet heath; mire; brackish marsh; carr; scrub; hedges and boundaries; woodland; grassland; sand dunes; sand and clay; ditches, streams, rivers, pools, ponds; arable; urban; other land uses; bare ground.
  - Within each plot, the cover of each vegetation type estimated on a 3-point abundance scale: 1 = 1-10%, 2 = 11-50%, 3 = >50%.
  - Plot location aided by maps, air photos, compass; later surveys used handheld GPS.

- Data processing and transformation
  - An algorithm converts the 3-point scores into area estimates for each vegetation type within a plot (plot total = 4 ha).
  - Plots joined into “heaths” using an 8-neighbour rule (adjacent or diagonally connected heathland cells).
  - Total heath area is the sum of the areas of heath-related vegetation types (including true heathland and associated vegetation).

- Quality control
  - Consistency checks carried out by group work and rotating pairs of surveyors.

- Data structure and contents
  - Format: a single CSV file with summed area estimates (hectares) for each major vegetation type in each heath for each survey year.
  - Columns include: Year, Heath Number, Total Heath area, DH (dry heath); WH/HH (humid/wet heath); M (mire); B (brackish marsh); C (carr); S (scrub); H (hedges and boundaries); W (woodland); G (grassland); SD (sand dunes); ST (sand and clay); D (ditches, streams, rivers, pools, ponds); AR (arable); UR (urban); OT (other land uses); B (bare ground).

- Miscellaneous
  - No additional supporting documents listed.

- Appendix 1: Vegetation descriptions (overview)
  - Dry heath: dwarf shrub-dominated with Calluna vulgaris and associated species; characterized by well-drained soils.
  - Humid/wet heath: combined category; features Calluna vulgaris and Erica spp. with varying drainage; wet heath may include Sphagnum spp. and Erica tetralix.
  - Mire: peatland with Sphagnum spp. and diverse associated species; water table and soil conditions strongly influence composition.
  - Brackish marsh, carr, scrub, hedges/boundaries, woodland, grassland, sand dunes, sand and clay, ditches/pools, arable, urban, bare ground, and other land uses: defined with characteristic species, structure, and land-use context.