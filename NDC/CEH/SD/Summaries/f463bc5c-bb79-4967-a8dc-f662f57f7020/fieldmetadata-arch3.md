# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- A long-term, multi-site field trial of Scots pine (Pinus sylvestris) across three field sites in Scotland (Yair/South: FS, Glensaugh/East: FE, Inverewe/West: FW).
- Seed material from 21 native Scottish populations (10 trees per population) collected in 2007; seeds germinated and grown in three nurseries (NW, NG, NE) before field planting in 2012.
- Aims to monitor growth and phenology traits over time to understand environmental and genetic influences.
- Data are captured in a single file, FieldTraits.txt, covering measurements from 2013 to 2020 (phenology 2015–2019; 2020 phenology not collected due to COVID-19).

## Study design and data collection
- Population and family structure:
  - 21 populations; 10 trees per population, with offspring grouped into families by mother tree (assumed half-siblings within a family).
- Nursery and field deployment:
  - Seedlings raised in three nurseries (NW, NG, NE) and transplanted to three field sites (FS, FE, FW) in 2012.
  - At least one site (FW) contains cohorts from all three nurseries; other sites mix origins.
- Experimental layout:
  - Randomised blocks with 3 m x 3 m spacing; guard row around blocks.
  - FS and FE: 4 blocks each; FW: 3 blocks.
  - Each block includes one tree from eight of the ten families per population (168 trees per block); some replacements occurred when insufficient trees were available.
- Measurements and timing:
  - Height: end of each growing season (FE and FW: 2013–2020; FS: 2014–2020).
  - Basal stem diameter: end of each growing season (FE and FW: 2013–2020; FS: 2020 only).
  - Phenology: spring assessments 2015–2019 (2020 data not collected due to COVID-19).
- Data file and structure:
  - FieldTraits.txt contains per-tree measurements with columns for population, family, field site, field code, block, and repeated measures of height (HA), height increment (HI), base diameter (DA), diameter increment (DI), and budburst timing (BD/BT variables) across years.
  - Units primarily in millimeters for growth metrics; BD/BT variables capture timing in days relative to defined dates (e.g., days to budburst stages).

## Data structure and fields (FieldTraits.txt)
- Key fields:
  - PopulationCode, Family, FieldSite, FieldCode, Block.
  - HA13–HA20: height after each growing season (mm).
  - HI13–HI20: height increment per year (mm).
  - DA13–DA20: base stem diameter after each season (mm).
  - DI13–DI20: base diameter increment per year (mm).
  - BD15–BD19: duration of budburst (days) in 2015–2019.
  - BT15_4, BT15_5, BT15_6, etc.: days since 31 March 2015 to reach budburst stages 4, 5, 6; similar variables for 2016–2019.
- Notes on data quality:
  - Some NA values where not applicable (e.g., not transplanted or missing measurements).
  - Replacements of families in FS to maintain population representation.
  - 2020 phenology not collected due to COVID-19.
- Provenance and representation:
  - Seeds and families are designed to represent the species’ native range in Scotland.
  - Clear documentation of planting scheme, spacing, and randomised-block design supports reproducibility and cross-site comparability.

## Data quality, metadata, and governance considerations
- Metadata richness:
  - Detailed description of seed provenance, nursery origins, field site coordinates, planting design, and measurement protocols.
  - Explicit labeling of units and field code conventions, enabling cross-study integration.
- Data availability and openness:
  - The dataset emphasizes transparent data usage, with explicit notes on data provenance and measurement methods; however, practical sharing constraints (as highlighted in the archetype) may apply to broader data dissemination and metadata completeness.
- Data integration and standardisation:
  - Multi-site design and genotype-by-environment potential require harmonised units and consistent measurement timing to enable robust comparative analyses.
  - Some data gaps due to COVID-19 and site-specific replacements may introduce biases if not properly documented and accounted for in analyses.
- Data governance implications for monitoring frameworks:
  - This dataset exemplifies long-term environmental health monitoring across diverse sites and genetic backgrounds.
  - Highlights the importance of fixing metadata gaps, ensuring timely data sharing, and maintaining data lineage from seed collection through field measurements.
  - Demonstrates the need for level-appropriate data transformations to standardize measurements across sites and years.

## Relevance for monitoring frameworks
- Demonstrates how long-term, multi-site phenotypic monitoring can quantify environmental and genetic influences on tree growth and phenology.
- Provides a model for:
  - Designing monitoring campaigns with clear sampling (populations, families), randomised layouts, and repeated annual measurements.
  - Capturing a broad set of traits (growth metrics and phenology) to inform climate resilience and forestry policy decisions.
  - Documenting data provenance and metadata to support transparency, reuse, and governance.
- Practical considerations for policy monitoring:
  - Ensure access to high-quality metadata and data sharing to enable policy evaluation.
  - Anticipate and mitigate data gaps (e.g., pandemic-related disruptions) in long-term monitoring plans.
  - Align variable definitions and measurement protocols across sites to facilitate integration into environmental health dashboards and decision-support tools.