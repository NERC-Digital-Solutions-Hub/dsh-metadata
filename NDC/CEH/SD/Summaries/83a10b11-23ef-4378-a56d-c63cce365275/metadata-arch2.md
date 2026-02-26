# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Aim
- Provide abundance data for invertebrates, pest damage to apples, and yields from an agroforestry system to compare the effects of two understorey management treatments (unmown flowering understorey vs mown understorey) on functional invertebrates and associated ecosystem services.

## Study site and experimental design
- Location: 5.6-hectare agroforestry field at Screveton, Nottinghamshire, UK (0° 54' 38'' E, 52° 59' 19'' N).
- System: 3 m wide tree rows (primarily apples) intercropped with 24 m wide arable alleys with spring barley in 2020.
- Understorey: Wildflower mix sown in 2014; infrequent mowing to promote flowering (two late-season cuts typical).
- Experimental blocks: Five blocks, each containing one apple variety (Block 1 Lord Derby; Block 2 Spartan; Block 3 King of the Pippins; Block 4 Bramley’s Seedling; Block 5 D’Arcy Spice).
- Treatments: Each block divided to two understorey treatments—unmown flowering understoreys and frequently mown understoreys (vegetation cut after sampling visits; outer margins cut in winter as part of standard farm operations).
- Replication and layout: Blocks span four tree rows; blocks 1 and 2 share a tree row (60 m apart); block lengths 42–60 m; each block completely split between treatments.
- Sampling period: April–September 2020.
- Data collected by: Tom Staton (University of Reading).

## Sampling methods and timing
- Visual searches on sample trees for aphids and natural enemies (8 visits May–July 2020; branches within reach).
- Apple pest and disease assessments: counts of apples and damaged apples (scab and pests) with sampling visits, including aphid-specific assessment in Sept 2020.
- Pollinator visitation to apple flowers: timed counts (3 minutes per sample tree) during favorable weather; two complete visits and one partial visit in late April–early May 2020.
- Apple seed counts and yield estimates: four apples per tree sampled for seed counts; pre-harvest fruit counts to estimate yield; one visit in Sept 2020.
- Pitfall traps: plastic cups with glycol solution; runs of 7–8 days; monthly Apr–Sept 2020; traps placed 0.5 m into adjacent crop alley.
- Sticky traps: yellow traps deployed ~250 mm above ground; runs of 7 hours; monthly May–July 2020; weather-dependent sampling.
- Grain samples: 50 × 50 cm quadrat sample taken near harvest in Aug 2020; grains weighed after threshing.
- Replication: Each sampling technique replicated four times within each treatment per block (except arable yield, replicated twice per treatment block), yielding 40 samples per technique per visit (4 locations × 2 treatments × 5 blocks).
- Spatial sampling: Pitfall and sticky traps sited 0.5 m into the adjacent crop alley to capture effects on the understorey treatment and nearby invertebrates.
- Specimen processing: Invertebrates stored frozen and identified to functional group level via optical microscope.
- Note: Three pitfall traps were damaged and excluded from the dataset (details provided).

## Data structure and files
This dataset comprises seven CSV files:

- apple_counts_inv.csv
  - Invertebrate count data from visual searches of apple trees for pests and natural enemies.
  - Columns: Visit, Block, Treatment (M = mown, U = unmown), Position, DistFromBoundary, multiple Taxonomic Group columns, TotalNEs (total natural enemies), TotalAphidCols (aphid colonies).

- apple_damage.csv
  - Pest and disease damage to apples.
  - Columns: Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, Taxon-specific damage counts.

- apple_damage_aphids.csv
  - Aphid-damaged apples counts.
  - Columns: Block, Treatment, Position, TotalApples, AphidApples.

- apple_seeds_yield.csv
  - Apple seed count and yield data.
  - Columns: Block, Treatment, Position, DistFromBoundary, Width (mm), Seeds, TotalApples.

- barley_yield.csv
  - Barley grain yield samples.
  - Columns: Block, Treatment, Position, Weight (g), WeightTpH (tonnes per hectare).

- pitfall_sticky_traps.csv
  - Invertebrate abundance data from pitfall and sticky traps.
  - Columns: Method (PF for pitfall, Sticky for sticky trap), Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary.

- poll_visitation.csv
  - Pollinator visitation counts to apple flowers.
  - Columns: Visit, Block, Treatment, Position, DistFromBoundary, multiple Pollinator taxa columns, Total (sum of taxa counts).

## Quality control and data integrity
- Standard sense checks performed: values within feasible ranges, all samples represented, and no duplicates.
- Notes on data completeness: three noted pitfall traps damaged and excluded; all other sampling proceeded as planned.

## Key considerations for analysts
- Data are organized to compare understorey treatments across multiple blocks and tree varieties, enabling assessment of effects on invertebrate communities, pest/disease pressure, pollination, and yields.
- Taxonomic resolution is selected to establish functional groups sufficient for ecosystem service analyses.
- Data are suitable for integration with other environmental monitoring datasets to evaluate ecosystem health and service provision in agroforestry systems.