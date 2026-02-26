# Invertebrate pests, natural enemies, pollinators, pest damage and yields associated with different understorey treatments in an agroforestry system, Nottinghamshire, UK, 2020

## Aim and scope
- A dataset of abundance data for invertebrates, pest damage to apples, and yields from an agroforestry system under two understorey treatments: unmown flowering understorey and mown understorey.
- Collected to compare effects of understorey management on functional invertebrates and related ecosystem services.

## Experimental context
- Location: Screveton, Nottinghamshire, UK; 5.6-hectare field on a working farm.
- Design: five experimental blocks, each containing one apple variety; blocks distributed across four tree rows.
- Treatments: within each block, understorey divided into unmown flowering versus mown vegetation.
- Structure: tree rows 3 m wide; arable alleys 24 m wide with spring barley in 2020.
- Understorey history: seeded with wildflower mix in 2014; infrequent mowing to promote flowering prior to the 2020 season.

## Treatments and management
- Flowering understoreys (unmown) vs mown understoreys (vegetation cut after sampling visits and approximately monthly in spring/summer 2020).
- Some outer sections were mown as part of standard farm operations; inner experimental areas maintained as per treatment.

## Sampling techniques
- Visual searches on sample trees for aphids and natural enemies (May–July 2020).
- Apple pest and disease assessments: counting apples on branches and damaged apples (including aphids, codling moth, winter moth, moth larvae, sawfly) with aphid-focused sampling in July–September 2020.
- Pollinator visitation: 3-minute timed counts on sample trees; conducted during favorable weather (late April–May 2020).
- Apple seed counts and yield estimates: seed counts per fruit and pre-harvest fruit counts to estimate yield (September 2020).
- Pitfall traps: 70 mm diameter cups with glycol solution; monthly sampling April–September 2020; trapped in field alleys near understorey treatments.
- Sticky traps: yellow traps raised above ground; monthly sampling May–July 2020; weather-dependent.
- Grain samples: barley yield samples collected near harvest (August 2020); weighed after threshing.

## Data structure and files
Seven CSV files:
- apple_counts_inv.csv: invertebrate counts from visual searches; fields include Visit, Block, Treatment (M = mown, U = unmown), Position, DistFromBoundary, multiple taxon counts, TotalNEs, TotalAphidCols.
- apple_damage.csv: pest/disease damage counts on apples; includes Block, Treatment, Position, DistFromBoundary, TotalApplesOnBranch, and damage counts by taxon.
- apple_damage_aphids.csv: aphid-damaged apples; includes Block, Treatment, Position, TotalApples, AphidApples.
- apple_seeds_yield.csv: seed counts and yield data for apples; includes Block, Treatment, Position, DistFromBoundary, Width, Seeds, TotalApples.
- barley_yield.csv: barley grain yield samples; includes Block, Treatment, Position, Weight, WeightTpH.
- pitfall_sticky_traps.csv: invertebrate abundance from pitfall and sticky traps; includes Method, Visit, Block, Treatment, Position, Taxon, Count, DistFromBoundary.
- poll_visitation.csv: pollinator visitation counts to apple flowers; includes Visit, Block, Treatment, Position, DistFromBoundary, counts by pollinator taxa, and Total.

## Replication and sampling intensity
- Each sampling technique replicated four times per treatment per block (except arable yield, which was replicated twice).
- Overall, 40 samples per technique per visit (except yield); trap samples collected 0.5 m into adjacent crop alley to capture edge effects.

## Data quality and provenance
- Data quality checks included range validation, ensuring all samples were represented, and no duplicates.
- Three damaged pitfall traps were excluded from the dataset.

## Usage notes and cautions
- Taxonomic resolution was chosen to establish functional groups; data supports analysis of understorey treatment effects on invertebrate communities and associated ecosystem services (pollination, pest control, and yields).
- Some sampling depended on weather (temperature, wind, rain) affecting trap and visitation data.
- DistFromBoundary provides spatial context relative to field boundaries, useful for spatial analyses within and across blocks.