# Experimental design/Sampling regime

- This dataset is a census of heathland and associated vegetation in Dorset, UK, with plots sized 200 m x 200 m (4 ha) aligned to the national OS grid.
- Initial survey of all plots within Dorset containing heathland vegetation (dry heath, humid/wet heath, mire) conducted in 1978; 3110 plots identified.
- Repeat surveys of all plots completed in 1987, 1996, and 2005.

## Sampling design and scope

- All plots within the county boundary that contained heathland vegetation in 1978 were surveyed for major vegetation type cover.
- Plots were combined into larger units called "heaths" using an 8-neighbour rule (adjacent or diagonally adjacent heath-containing plots merged).
- Total heath area within each heath calculated by summing area estimates across land cover types that comprise heathland.

## Collection methods

- Major vegetation types recorded include: dry heath; humid/wet heath; mire; brackish marsh; carr; scrub; hedges/boundaries; woodland; grassland; sand dunes; sand and clay; ditches/streams/pools; arable; urban; other land uses; bare ground.
- Within each plot, cover of each vegetation type estimated on a 3-point abundance scale: 1 = 1–10%, 2 = 11–50%, 3 = >50%.
- Plot locations initially mapped or photographed; fields in later surveys also used hand-held GPS.

## Fieldwork and instrumentation

- Location aided by maps and air photographs; compass used initially; GPS employed in the later two surveys.
- Calibration steps and analytical methods: none applied.

## Data transformation and units

- An algorithm converts 3-point scores into area estimates for the primary vegetation in each plot.
- Key rule: each score-1 contributes 5% of the plot area (0.05 x 4 ha = 0.20 ha); remaining area allocated among scores-2 and -3 according to defined cases (including handling of multiple 2s and 3s, and ensuring at most one 3 per plot).
- Special cases defined for distributions of 2s and 3s (e.g., when N2 > 0 and N3 = 0; when N2 = 0 and N3 = 1; cases with N2 and N3 both present; interpolation across intermediate N1 values).
- Heath areas are summed across true heathland and associated vegetation types (dry heath, humid/wet heath, mire, and related categories).
- Units: hectares (ha) for area estimates.

## Data structure and content

- Format: a single CSV file containing summed area estimates (ha) for each major vegetation type within each heath for each survey year.
- Columns include: Year, Heath Number, Total Heath area, DH (dry heath), WH/HH (humid/wet heath), M (mire), B (brackish marsh), C (carr), S (scrub), H (hedges/boundaries), W (woodland), G (grassland), SD (sand dunes), ST (sand and clay), D (ditches/streams/pools), AR (arable), UR (urban), OT (other land uses), B (bare ground). Note: two entries use the letter B for different categories (brackish marsh and bare ground).

## Quality control and data quality

- Recording teams initially worked together, then in rotating pairs to ensure consistency across surveyors.

## Documentation and appendices

- Appendix 1 provides vegetation descriptions for the major types (e.g., dry heath, humid/wet heath, mire, brackish marsh, carr, scrub, etc.), including dominant species and typical associations.
- Miscellaneous supporting documents: None.

## Data governance and stewardship considerations

- Metadata needs: dataset scope (geographic and temporal), exact variable definitions, and column mappings (noting the potential B duplication issue).
- Provenance and lineage: clearly document the algorithm rules used to convert abundance scores to area estimates to enable reproducibility.
- Versioning and updates: define how future surveys would be incorporated (e.g., new years, revised plot boundaries, reclassification).
- Licensing and access: specify data use terms, any restrictions on redistribution, and contact for data custodians.
- Interoperability: ensure consistent naming conventions and provide a data dictionary to facilitate integration with other datasets.
- Limitations: temporal gaps (survey years spaced 1978, 1987, 1996, 2005); potential ambiguity from the B column naming; reliance on a 3-point scale with a complex area-conversion algorithm that should be documented for reuse.