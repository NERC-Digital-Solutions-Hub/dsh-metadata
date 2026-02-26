# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Overview
- A dataset describing abundance of invertebrates, pest damage to apples, and yields from an agroforestry system under two understorey management treatments: unmown flowering understorey vs mown understorey.
- Collected at Screveton, Nottinghamshire, UK on a 5.6-hectare field with intercropped apple-arable layout.
- Experimental design includes five blocks, each with two treatments, across four tree rows; understorey established with a wildflower mix since 2014.
- Data collection period: April–September 2020; collected by Tom Staton (University of Reading).
- Purpose: compare understorey management effects on functional invertebrates and related ecosystem services (pollination, pest control, and yields).

## Experimental design
- Field setup: 5 blocks, each containing one apple tree variety (Block 1 Lord Derby, Block 2 Spartan, Block 3 King of the Pippins, Block 4 Bramley’s Seedling, Block 5 D’Arcy Spice); blocks distributed across four tree rows.
- Treatments: within each block, half the area has unmown flowering understorey to promote flowering, and half has mown understorey to suppress flowering.
- Layout: blocks 42–60 m long, 3 m wide tree rows; understorey disturbance minimized by mowing after sampling visits.
- Understorey history: wildflower mix planted in 2014; infrequent mowing prior to data collection (two late-season cuts).
- Replication: each sampling technique replicated four times per treatment per block; arable yield samples replicated twice per treatment block.
- Distances: measurements include distance from nearest field boundary (DistFromBoundary) and sampling locations within blocks.

## Sampling techniques
- Visual searches: tree-side surveys for aphid colonies and natural enemies; eight visits May–July 2020; focus on leaf undersides and branch ends.
- Apple pest and disease assessments: count apples, assess damage by pests/disease (e.g., aphids, codling moth, scab); one July and one September assessment.
- Pollinator visitation: 3-minute counts per sample tree; favourable weather; two complete visits plus one partial visit in late April–May 2020.
- Apple seed counts and yield estimates: seed counts from four apples per tree; fruit counts per tree pre-harvest to estimate yield.
- Pitfall traps: 70 mm diameter cups with glycol solution; monthly traps April–September 2020; 7–8 days per run; three traps damaged and excluded.
- Sticky traps: yellow traps set above ground; monthly runs May–July 2020; weather-dependent conditions.
- Grain samples: barley yield samples collected August 2020, threshed and weighed.
- Each technique: four replicates per treatment per block (except arable yield), resulting in 40 samples per technique per visit.
- Traps positioned 0.5 m into adjacent crop alleys to sample understorey treatment effects on adjacent crop invertebrates.
- Specimens stored for identification; taxonomic resolution chosen to establish functional groups.

## Data structure
- Seven CSV files model the dataset:
  - apple_counts_inv.csv: invertebrate counts from visual searches (33 columns; includes Visit, Block, Treatment, Position, DistFromBoundary, taxon counts, TotalNEs, TotalAphidCols).
  - apple_damage.csv: pest/damage data on apples (11 columns; Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, damage by taxon).
  - apple_damage_aphids.csv: aphid-damaged apples counts (5 columns; Block, Treatment, Position, TotalApples, AphidApples).
  - apple_seeds_yield.csv: seed counts and yield (7 columns; Block, Treatment, Position, DistFromBoundary, Width, Seeds, TotalApples).
  - barley_yield.csv: barley grain yield (5 columns; Block, Treatment, Position, Weight, WeightTpH).
  - pitfall_sticky_traps.csv: invertebrate abundance from pitfall and sticky traps (8 columns; Method, Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary).
  - poll_visitation.csv: pollinator visitation to apple flowers (11 columns; Visit, Block, Treatment, Position, DistFromBoundary, taxa counts, Total).
- Common fields include Block, Treatment (M = mown, U = unmown flowering), Position, DistFromBoundary; data are arranged to support comparisons between understorey treatments and aggregation across blocks.
- Data are organized to enable taxon-level and functional-group analyses, with explicit replication and sampling metadata.

## Quality control
- Standard sense checks applied: values fall within feasible ranges, all samples represented, and no duplicates.
- Noted data losses: three damaged pitfall traps excluded from the dataset.

## Practical notes for data leadership and reuse
- Rich, multi-technique dataset supports evaluation of understorey management on invertebrate communities and ecosystem services (pollination, natural enemies) and on crop yields.
- Well-documented experimental design, sampling schedule, and file-level metadata facilitate replication, cross-site comparison, and integration with broader agroforestry or agricultural biodiversity data.
- Data management considerations include explicit replication counts, boundary distances, and taxonomic-to-functional-group resolution, which aid standardization and interoperability for future analyses and governance discussions.