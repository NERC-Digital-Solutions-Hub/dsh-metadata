# Coccinellidae competition

## Overview
- Study of interactions among the invasive Harmonia axyridis (predator) and two UK native coccinellids, Coccinella septempunctata and Adalia bipunctata (prey).
- Specimens collected in Oxfordshire (May 2013); reared in controlled conditions (20 ± 1°C, 16 h photoperiod) with Acyrthosiphon pisum as diet.
- Aimed to assess prey-stage preferences and competitive effects on feeding using laboratory experiments; prey supply and experimental conditions standardized to enable comparison.

## Experimental design

Experiment 1: prey-stage preferences
- Purpose: identify coccinellid larval stage preferences for the aphid Amphorophora idaei (raspberry aphid).
- Setup: circular arena with 50 aphids (10 apterous adults + 10 each of nymphal stages I–IV); one larval stage introduced, observed for 1 h.
- Replication: 120 bioassays (3 coccinellid species × 4 larval stages × 10 replicates per stage), randomized across 12 temporal blocks.

Experiment 2: competition on shared prey
- Purpose: evaluate impact of interspecific and intraspecific competition on consumption, using cadaver-prey to identify aphid stage eaten.
- Setup: 25 aphids arranged around arena; two larval stage IV coccinellids placed center in focal pairs; one larva marked for ID; 1 h trials with video recording.
- Designs: hetero- and conspecific pairings, plus a no-competing-control; each pairing repeated with reversed focal species; total 90 bioassays.
- Data collection: video analysis to count aphid stages consumed by focal and competing larvae.

## Data and metadata

- Experiment1.csv includes: id, individual coccinellid ID, block, ladybird_stage, Coccinellid lifestage, aphid_stage, aphid_lifestage, number_eaten, species, max (initial aphid count).
- Experiment2.csv includes: arena, unit (arena descriptor), aphid_lifestage, focal_species, pred_species, eaten, painted (ID mark), eaten_comp, total_aphid.
- Data provenance: field-collected prey and lab-reared bugs; mixing field and supplier sources for a single laboratory generation to reduce source bias.
- Supporting documentation is archived in the NERC Environmental Information Data Centre.

## Data quality, methods, and analysis

- Quality control: datasets manually checked for errors; no further QC required.
- Analytical approach: performed in R 3.0.2 using the gamm4 package for statistical analysis.
- Data handling: prey were sometimes pre-killed (-20°C) to facilitate rapid identification of consumed stages; larvae were starved briefly (24 h) before experiments.

## Data accessibility and governance

- Data described and stored as Experiment1.csv and Experiment2.csv; access through NERC EIDC with DOI link provided in the documentation.
- Data sharing and openness facilitated by explicit experimental metadata, standardized data fields, and clear provenance, though the broader document notes general barriers to sharing datasets in some monitoring contexts.

## Relevance to monitoring frameworks

- Demonstrates a complete data lifecycle relevant to monitoring: careful experimental design, detailed metadata, quality assurance, data sharing, and transparent analysis.
- Highlights practical monitoring challenges: ensuring data availability, rich metadata, standardization across datasets, and governance to support data sharing and reuse.
- Provides concrete data structures (CSV formats) and field definitions that support replication, validation, and integration into broader environmental monitoring assessments.