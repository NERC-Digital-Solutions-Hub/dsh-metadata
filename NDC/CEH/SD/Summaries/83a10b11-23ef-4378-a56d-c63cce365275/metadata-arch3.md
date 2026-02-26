# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Overview
- Abundance data for invertebrates, pest damage to apples, and yields from an agroforestry system under two understorey treatments: unmown flowering understorey vs mown understorey.
- Location: Screveton, Nottinghamshire, UK; five experimental blocks; each block split between treatments.
- Field period: April–September 2020.
- Data collected to compare effects of understorey management on functional invertebrates and associated ecosystem services.
- Collection methods: pitfall traps, sticky traps, visual tree assessments (pests and natural enemies), pollinator flower visitation counts, apple yield/quality metrics, and grain yield samples.
- Three damaged pitfall traps were excluded from the dataset.

## Experimental design
- Site: 5.6 ha working farm agroforestry field; three-meter-wide tree rows intercropped with 24 m-wide arable alleys (spring barley in 2020).
- Understorey history: wildflower seed mix established in 2014; infrequent mowing to promote flowering, with ~two late-season cuts prior to 2020.
- Blocks and treatments: five experimental blocks, each containing one apple variety (Block 1 Lord Derby; Block 2 Spartan; Block 3 King of the Pippins; Block 4 Bramley’s Seedling; Block 5 D’Arcy Spice); blocks distributed across four tree rows; each block split into unmown (flowering) and mown understoreys.
- Management timing: mown understorey cut after sampling visits to minimize disturbance; outer thirds of flowering understoreys and outside experimental areas cut once in winter 2019/2020 as standard farm operation but not during 2020 growing season.

## Sampling techniques
- Visual searches: eight visits May–July 2020; insects on sample trees focusing on aphid colonies and natural enemies (ends of branches and leaf undersides).
- Apple pest and disease assessments: total apples per tree and damaged fruits assessed; aphid counts via entire tree plus five branches sampled; one July 2020 (diseases/pests) and one September 2020 (aphid damage) visit.
- Pollinator visitation to apple flowers: 3-minute timed counts per sample tree; two complete visits plus one partial with favorable weather; avoid counting duplicates; late April/early May 2020.
- Apple seed counts and yield estimates: four apples per sample tree; width and seed count per fruit; pre-harvest fruit counts to estimate yield; one September 2020 visit.
- Pitfall traps: 70 mm diameter, 100 mm depth cups with glycol-based solution; 7–8 days trapping, monthly Apr–Sep 2020; three traps damaged and excluded.
- Sticky traps: yellow traps (100 mm × 250 mm), raised ~250 mm; 7 hours trapping, monthly May–July 2020; weather-conditioned as required.
- Grain samples: 50 × 50 cm quadrat sampled around harvest; thresh and weigh; August 2020.
- Replication: each technique replicated four times per treatment per block (except barley yield, replicated twice); total 40 samples per technique per visit; pitfall/sticky traps placed 0.5 m into adjacent crop alley.
- Specimen handling: invertebrates stored frozen and identified to functional group; taxonomic resolution sufficient for ecological grouping.

## Data structure
- Seven CSV files:
  - apple_counts_inv.csv: invertebrate counts from visual searches; 33 columns (Visit, Block, Treatment M/U, Position, DistFromBoundary, taxa counts, TotalNEs, TotalAphidCols).
  - apple_damage.csv: pest/disease damage to apples; 11 columns (Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, damage by taxon).
  - apple_damage_aphids.csv: aphid-damaged apples; 5 columns (Block, Treatment, Position, TotalApples, AphidApples).
  - apple_seeds_yield.csv: seed counts and yield data; 7 columns (Block, Treatment, Position, DistFromBoundary, Width, Seeds, TotalApples).
  - barley_yield.csv: barley grain yield; 5 columns (Block, Treatment, Position, Weight, WeightTpH).
  - pitfall_sticky_traps.csv: invertebrate abundance from pitfall and sticky traps; 8 columns (Method PF/Sticky, Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary).
  - poll_visitation.csv: pollinator visitation counts to apple flowers; 11 columns (Visit, Block, Treatment, Position, DistFromBoundary, Pollinator taxa counts, Total).
- Experimental design context: data collected across five blocks with two treatments, including spatial context (distance from boundary) and replication details.

## Quality control
- Standard sense checks performed: values within feasible ranges; all intended samples represented; no duplicate samples.

## Relevance for monitoring frameworks
- Provides a multi-taxa, multi-metric basis for evaluating how understorey management affects ecosystem services such as pest regulation (natural enemies), pollination, pest damage, and crop yields in agroforestry systems.
- Useful for policy decisions on sustainable farming practices that integrate biodiversity with agricultural productivity.
- Demonstrates a structured, replicable data collection and management approach across ecological indicators, enabling monitoring, evaluation, and potential data governance considerations for openness and interoperability.