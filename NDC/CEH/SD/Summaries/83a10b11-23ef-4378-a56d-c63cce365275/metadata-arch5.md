# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Overview
- Dataset of abundance data for invertebrates, pest/disease damage to apples, and yields from an agroforestry system with two understorey treatments (unmown flowering vs mown understorey) collected in Screveton, Nottinghamshire, UK, in 2020.
- Collected across five experimental blocks (each block with one apple variety) from April to September 2020.
- Data collected using multiple methods: pitfall traps, sticky traps, visual searches of trees for natural enemies and pests, pollinator visitation counts, apple fruit damage, seed counts, and grain yield.
- Principal investigator: Tom Staton (University of Reading).
- Note: three pitfall traps were damaged and excluded (specific Visit/Block/Treatment/Position details provided).

## Experimental design
- Site: 5.6-hectare agroforestry field with 3 m wide tree rows (apple trees) intercropped with 24 m wide arable alleys containing spring barley; understorey sown with a wildflower mix in 2014, traditionally mowed infrequently to promote flowering.
- Blocks and treatments: five experimental blocks, each containing one of five apple varieties (Block 1 Lord Derby, Block 2 Spartan, Block 3 King of the Pippins, Block 4 Bramley’s Seedling, Block 5 D’Arcy Spice). Each block split between two understorey treatments—unmown flowering understorey and frequently mown understorey.
- Replication and sampling: each sampling technique replicated four times per treatment per block (except barley yield, which had two replicates per treatment block), yielding 40 samples per technique per visit. Data were collected across visits spanning 2020, with mowing and sampling coordinated to minimize disturbance.
- Measurements and context: DistFromBoundary recorded; mowing consisted of late-season cuts with additional seasonal mowing; outer thirds of flowering understoreys cut during winter as part of standard farm operations.

## Sampling techniques
- Visual searches: Tree-level inspections for aphid colonies and natural enemies; eight visits May–July 2020; targeted ends of branches and undersides of leaves.
- Apple pest and disease assessments: Count of apples per tree and damaged apples due to scab or pests; multiple pests/diseases recorded; one July and one September visit for damages.
- Pollinator visitation to flowers: Timed counts (3 minutes per sample tree); visits conducted under favorable weather; two complete visits and a partial visit in late April/early May 2020.
- Apple seed counts and yield estimates: Seed counts per fruit as a proxy for pollination; estimated yield via counting fruits pre-harvest.
- Pitfall traps: 200 traps (70 mm x 100 mm) with propylene glycol solution; deployed April–September 2020; some traps damaged and excluded; 7–8 day runs monthly.
- Sticky traps: Yellow traps (100 mm x 250 mm) raised ~250 mm; deployed May–July 2020 under suitable weather; run for about 7 hours monthly.
- Grain samples: Barley yield samples collected in August 2020; samples weighed after threshing.
- Replication and placement: All techniques replicated four times per treatment per block; traps placed 0.5 m into adjacent crop alley to capture effects on the adjacent crop community.
- Specimen handling: Invertebrate samples stored in a freezer and identified to the functional group level; taxonomic resolution chosen to support functional insights.

## Data structure and files
The dataset comprises seven CSV files:
- apple_counts_inv.csv: Invertebrate counts from visual searches; columns include Visit, Block, Treatment (M = mown, U = unmown), Position, DistFromBoundary, counts for multiple taxonomic groups, TotalNEs (total natural enemies), TotalAphidCols (total aphid colonies).
- apple_damage.csv: Pest/disease damage to apples; includes Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, and counts of damaged fruits by taxon.
- apple_damage_aphids.csv: Aphid-damaged apples; includes Block, Treatment, Position, TotalApples, AphidApples.
- apple_seeds_yield.csv: Apple seed counts and yield data; includes Block, Treatment, Position, DistFromBoundary, Width (mm), Seeds, TotalApples.
- barley_yield.csv: Barley grain yield samples; includes Block, Treatment, Position, Weight (g), WeightTpH (tonnes per hectare).
- pitfall_sticky_traps.csv: Invertebrate abundance from traps; columns: Method (PF or Sticky), Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary.
- poll_visitation.csv: Pollinator visitation counts to apple flowers; columns: Visit, Block, Treatment, Position, DistFromBoundary, counts for pollinator taxa, Total.

## Data quality and provenance
- Quality control: standard sense checks performed (feasibility of values, representation of all samples, avoidance of duplicates).
- Data integrity considerations: three pivot/trap samples were damaged and excluded from the dataset (specifics noted in the data description).

## Governance, reuse, and documentation considerations
- The dataset is organized to enable comparative analyses of understorey management effects on invertebrates, pests, pollinators, and yield within an agroforestry system.
- To ensure discoverability and reusability, accompany the seven CSVs with comprehensive metadata and a data dictionary detailing:
  - Definitions for each variable and taxonomic group
  - Measurement units and calculation methods (e.g., seed counts, weight, WeightTpH)
  - Sampling schedule and replication structure
  - Spatial context (DistFromBoundary, block-row layout, and understorey treatments)
  - Any data exclusions (e.g., damaged traps) and rationale
- Consider versioning and clear provenance to support updates or corrections; align with data stewardship practices for large, multi-method ecological datasets.
- Potential use cases include meta-analyses of understorey management on ecosystem services, association between invertebrate communities and yield, and pollination biology in agroforestry contexts.