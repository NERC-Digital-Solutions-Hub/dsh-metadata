# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Overview
- Abundance data for invertebrates, pest damage to apples, and yields from an agroforestry site in Screveton, Nottinghamshire, UK, collected in 2020.
- Two understorey management treatments: unmown flowering understorey vs mown understorey.
- Five experimental blocks across a field with apple trees intercropped with spring barley; five apple varieties represented.
- Data collected Apr–Sep 2020 using multiple methods to assess functional invertebrates and ecosystem services:
  - Pitfall traps, sticky traps, visual searches for natural enemies and pests, pollinator visitation counts, apple fruit damage and yield metrics, and grain yield samples.
- Data collected by Tom Staton (University of Reading).
- Three pitfall traps were damaged and excluded from the dataset (Visit 1 Block 2 Mown Position 4; Visit 4 Block 2 Mown Position 3; Visit 4 Block 3 Unmown Position 2).

## Experimental design
- Site: 5.6 hectare agroforestry field at a working farm in Screveton, UK (0°54'38" E, 52°59'19" N).
- System: 3 m wide tree rows (mostly apple trees) intercropped with 24 m wide arable alleys containing spring barley (2020).
- Understorey: wildflower mix seeded in 2014; flowering promoted by infrequent mowing, typically two late-season cuts.
- Blocks and treatments: five experimental blocks, each with one apple variety (Block 1 Lord Derby, Block 2 Spartan, Block 3 King of the Pippins, Block 4 Bramley’s Seedling, Block 5 D’Arcy Spice). Blocks distributed across four tree rows; two blocks per row, separated by ~60 m.
- Each block is subdivided into two treatments: unmown flowering understorey (flowering) and mown understorey. Each block/treatment area is 42–60 m long by 3 m wide.
- Mowing regime: mown vegetation cut as short as possible with a petrol strimmer (Nov 2019) and approximately monthly over spring/summer 2020; sampling occurred between cuts to minimize disturbance.
- Farm operations: outer thirds of flowering understoreys and areas outside experimental zones were cut once in winter 2019/2020 as part of standard management.

## Sampling techniques
- Visual searches: inspect sample trees for aphid colonies and natural enemies (within reach); 8 visits between May–July 2020.
- Apple pest and disease assessments: count total apples per tree branch, and count damaged fruits (scab and insect pests including several lepidopteran pests); one July visit for diseases/pests and a September visit for aphid damage.
- Pollinator visitation to apple flowers: 3-minute timed counts per sample tree; conducted during favorable weather; two complete visits plus one partial visit in late Apr/early May 2020.
- Apple seed counts and yield estimates: four apples per tree sampled for width (mm) and seeds; pre-harvest fruit counts to estimate yield; one September 2020 visit.
- Pitfall traps: 70 mm diameter x 100 mm depth cups with glycol solution; monitored for 7–8 days monthly Apr–Sep 2020; 200 traps total (three damaged and excluded).
- Sticky traps: yellow traps sampled for 7 hours monthly May–July 2020; raised ~250 mm above ground; weather conditions required (temp ≥ 13°C, wind < 25 mph, no rain).
- Grain samples: 50 × 50 cm quadrat sampled within one week of harvest in Aug 2020; threshed and weighed.
- Replication: each technique replicated four times per treatment per block (except arable yield, replicated twice per treatment block). This results in 40 samples per sampling technique per visit (unless otherwise noted).
- Trap placements: pitfall/sticky traps positioned 0.5 m into adjacent crop alleys to sample effects on the adjacent crop and its invertebrate community.
- Specimen processing: invertebrate samples stored frozen and identified via optical microscopy; taxonomic resolution chosen to establish functional groups.
- Table 1 provides timing of sampling and management activities (dates/months across the study).

## Data structure
The dataset comprises seven CSV files:
- apple_counts_inv.csv: invertebrate counts from visual searches on apple trees. 33 columns (Visit, Block, Treatment, Position, DistFromBoundary, 28 taxonomic group counts, TotalNEs, TotalAphidCols).
- apple_damage.csv: pest and disease damage to apples. 11 columns (Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, counts by damage taxon).
- apple_damage_aphids.csv: aphid-damaged apple counts. 5 columns (Block, Treatment, Position, TotalApples, AphidApples).
- apple_seeds_yield.csv: apple seed counts and yield metrics. 7 columns (Block, Treatment, Position, DistFromBoundary, Width, Seeds, TotalApples).
- barley_yield.csv: barley grain yield samples. 5 columns (Block, Treatment, Position, Weight, WeightTpH).
- pitfall_sticky_traps.csv: invertebrate abundance from pitfall and sticky traps. 8 columns (Method, Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary).
- poll_visitation.csv: pollinator visitation counts to apple flowers. 11 columns (Visit, Block, Treatment, Position, DistFromBoundary, counts by pollinator taxa, Total).

- Quality control: standard sense checks applied (feasible value ranges, complete sample representation, no duplicates).

## Potential analyses and use
- Assess how unmown flowering versus mown understorey affects:
  - Invertebrate community composition and abundance (functional groups).
  - Pest damage levels on apples and associated yields.
  - Pollinator visitation rates and potential pollination success (seed counts/yield proxy).
  - Arable grain yield in relation to adjacent understorey management.
- Explore correlations and multivariate patterns across sampling methods, blocks, and distances from field boundaries.
- Develop predictive models linking understorey management to ecosystem services and crop performance.
- Leverage metadata (block, treatment, position, distFromBoundary) to control for spatial effects and to generalize findings to similar agroforestry contexts.