# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Overview
- Dataset of abundance data for invertebrates, pest damage to apples, and yields from an agroforestry system with two understorey treatments: unmown flowering understorey and mown understorey.
- Location and scale: Screveton, Nottinghamshire, UK; 5 experimental blocks over a 5.6 hectare field; coordinates 0° 54' 38" E, 52° 59' 19" N.
- Timeframe: Data collected April–September 2020; collected by Tom Staton (University of Reading).
- Methods: pitfall traps, sticky traps, visual tree searches for natural enemies and pests, flower visitation counts for pollinators, apple yield/quality metrics, and grain yield samples.
- Purpose: compare effects of understorey management on functional invertebrates and associated ecosystem services.
- Data quality note: three pitfall traps were damaged and excluded from the dataset.

## Experimental design
- Field layout: 5 blocks within a 5.6 ha agroforestry site with 3 m wide tree rows (apple trees) and 24 m wide arable alleys (spring barley in 2020).
- Understorey: wildflower mix established in 2014; infrequent mowing prior to sampling to promote flowering.
- Blocks and varieties: Block 1 Lord Derby, Block 2 Spartan, Block 3 King of the Pippins, Block 4 Bramley’s Seedling, Block 5 D’Arcy Spice.
- Treatment split: each block divided into unmown flowering understoreys and mown understoreys.
- Mowing regime: outer thirds cut in winter 2019/2020; main mowing occurred approximately monthly in spring/summer 2020.
- Replication and sampling: each treatment within a block replicated; sampling areas designed to sample adjacent crop effects and to minimize disturbance.

## Sampling techniques
- Visual searches: 8 visits (May–July 2020) for aphid colonies and natural enemies on sample trees.
- Pest/disease assessments: counting apples per tree and damaged apples (various pests and diseases); aphids counted on entire tree; other pests/disease on five branches per tree; one July visit for diseases/pests, September for aphid damage.
- Pollinator visitation: 3-minute timed counts per sample tree; two complete visits plus one partial visit in late April–early May 2020.
- Seed counts and yield estimates: four apples per tree; seed counts as a proxy for pollination; pre-harvest fruit counts to estimate yield; one September 2020 visit.
- Pitfall traps: 70 mm diameter cups with propylene glycol; 7–8 day runs; monthly April–September 2020; 200 traps (3 damaged).
- Sticky traps: yellow traps raised ~250 mm above ground; 7-hour runs; conditions-based timing (May–July 2020).
- Grain samples: 50 × 50 cm quadrats harvested August 2020; weighed after threshing.
- Replication: each technique replicated four times per treatment per block (except arable yield replicated twice); total 40 samples per technique per visit (except yield).
- Placement: traps placed 0.5 m into adjacent crop alley to sample understorey effects on the adjoining crop invertebrate community.
- Processing: specimens stored frozen; identification to functional group as needed; taxonomic resolution chosen to establish functional relevance.

## Data structure
Seven CSV files:
- apple_counts_inv.csv: invertebrate counts from visual searches; 33 columns including Visit, Block, Treatment (M = mown, U = unmown), Position, DistFromBoundary, multiple taxon counts, TotalNEs, TotalAphidCols.
- apple_damage.csv: pest and disease damage to apples; 11 columns (Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, counts by taxon for damage).
- apple_damage_aphids.csv: aphid-damaged apples; 5 columns (Block, Treatment, Position, TotalApples, AphidApples).
- apple_seeds_yield.csv: apple seed counts and yield data; 7 columns (Block, Treatment, Position, DistFromBoundary, Width, Seeds, TotalApples).
- barley_yield.csv: barley grain yield; 5 columns (Block, Treatment, Position, Weight, WeightTpH).
- pitfall_sticky_traps.csv: invertebrate abundance from pitfall and sticky traps; 8 columns (Method, Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary).
- poll_visitation.csv: pollinator visitation counts to apple flowers; 11 columns (Visit, Block, Treatment, Position, DistFromBoundary, counts by pollinator taxa, Total).

Notes:
- DistFromBoundary enables spatial analysis relative to field boundaries and block layout.
- Taxonomic resolution was selected to establish functional groups.

## Quality control
- Standard sense checks: values within feasible ranges, all samples represented, no duplicates.

## GIS-ready considerations and potential map-based data products
- Spatial mapping of abundance, damage, and yields by block and understorey treatment.
- Visualizations by distance from field boundary to explore edge effects.
- Layered maps integrating trap data (pitfall and sticky) with tree-block layout and mowing treatments.
- Linking understorey management regimes to ecosystem services (pollination, pest suppression) across the agroforestry site.