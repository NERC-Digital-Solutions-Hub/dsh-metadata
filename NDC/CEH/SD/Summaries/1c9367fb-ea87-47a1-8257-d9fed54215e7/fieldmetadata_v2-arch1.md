# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

- Overview
  - A long-term field trial of Scots pine across three Scottish field sites to study growth and phenology across 21 native populations.
  - Seeds collected from 21 populations (10 trees per population) in 2007, germinated and grown in nurseries, then transplanted to field in 2012.
  - Aims to analyze genetic and environmental effects on growth (height, stem diameter) and phenology, enabling assessments of local adaptation and performance of seed sources.

- Experimental design
  - Seed and nursery phase
    - Seeds collected March 2007; germination at James Hutton Institute, Aberdeen (coordinates provided).
    - Seedlings grown in three nurseries (NW, NG, NE) before field transplantation.
    - Populations chosen to cover native range; three populations per seed zone (seven seed zones total).
  - Field phase
    - Field sites: Yair (FS, south Scotland), Glensaugh (FE, east Scotland), Inverewe (FW, west Scotland).
    - Transplanted to fields in 2012; randomised block design with a guard row around blocks.
    - Each block contains one tree from eight of the 10 families per population (total 168 trees per block).
    - Site-specific block counts: FS and FE have four blocks each; FW has three blocks.
    - Representation: most families (N=159) represented at all three sites; nine families were replaced at FS due to insufficient trees.

- Data collected and timeline
  - Growth measurements
    - Height: end of each growing season (FE and FW: 2013–2020; FS: 2014–2020).
    - Basal stem diameter: end of each growing season (FE and FW: 2013–2020; FS: 2020).
  - Phenology measurements
    - Spring assessments: 2015–2019 (2020 not possible due to COVID-19).
  - Data file
    - FieldTraits.txt contains per-tree measurements and metadata (see Variables below).

- Field and sampling structure
  - Populations and family structure
    - 21 populations, 10 trees per population; family refers to half-siblings from the same mother tree.
    - Population code and description included; seed zones represented.
  - Field site details
    - FE: Glensaugh (east Scotland) – coordinates provided.
    - FS: Yair (south Scotland) – coordinates provided.
    - FW: Inverewe (west Scotland) – coordinates provided.
  - Per-tree identifiers
    - FieldCode: unique code per tree (ranges differ by site; not transplanted: NA).
    - Block, Row, Column: spatial layout within field sites.

- Data structure and schema (FieldTraits.txt)
  - Core identifiers
    - PopulationCode, Description
    - Family (mother-tree lineage)
    - FieldSite (FE, FS, FW)
    - FieldCode (tree identifier)
    - Block, Row, Column
  - Growth metrics
    - HA13–HA20: Height after 7th to 14th growing seasons (mm)
    - HI13–HI20: Height increment between consecutive years (mm)
    - DA13–DA20: Base stem diameter after 7th to 14th growing seasons (mm)
    - DI13–DI20: Base stem diameter increment between consecutive years (mm)
  - Budburst phenology
    - BD15–BD19: Duration of budburst (days from stage 4 to stage 6) for 2015–2019
    - BT15_4, BT15_5, BT15_6, BT16_4, BT16_5, BT16_6, BT17_4, BT17_5, BT17_6, BT18_4, BT18_5, BT18_6, BT19_4, BT19_5, BT19_6: Days since 31 March to reach budburst stages 4, 5, and 6 across multiple years (2015–2019) with yearly markers
  - Notes
    - Many measurements are year-specific; data allow longitudinal growth and phenology analyses.
    - Some fields are year-tagged (e.g., 2013–2020) and site-specific.

- Sites, coordinates, and context
  - Field sites with geographic coordinates
    - FS (Yair, south Scotland): 55.603625, -2.893025
    - FE (Glensaugh, east Scotland): 56.893567, -2.535736
    - FW (Inverewe, west Scotland): 57.775714, -5.597181
  - Nursery origins
    - NW, NG, NE (locations not specified in detail here)

- Data quality, accessibility, and structure
  - Data are organized at the tree level with hierarchical structure: population → family → tree → repeated measures across years.
  - A single main data file (FieldTraits.txt) consolidates identifiers, growth metrics, and phenology metrics.
  - Gaps and caveats
    - COVID-19 limited 2020 phenology data collection.
    - FS site had 9 families replaced due to insufficient trees, potentially affecting cross-site comparability for those families.
    - Full origin metadata for seed zones and nursery provenance is present but may require careful alignment with field data for certain analyses.

- Potential analyses and use cases
  - Growth trajectories and age-related growth (height and diameter) across three sites and nursery origins.
  - Genotype-by-environment interactions: how populations/families perform differently across FE, FS, FW.
  - Relationships between growth metrics (height/diameter) and phenology timing (budburst duration and timing) across years.
  - Assessments of local adaptation and seed-zone representation by comparing phenotypic responses among populations.
  - Hierarchical modelling leveraging population, family, site, and block structure to partition genetic and environmental effects.