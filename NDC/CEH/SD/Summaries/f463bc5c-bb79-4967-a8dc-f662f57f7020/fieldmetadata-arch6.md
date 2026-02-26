# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- Multi-site, long-term dataset of field phenotypes for Pinus sylvestris across three field sites in Scotland (Yair/FS, Glensaugh/FE, Inverewe/FW) from 2013 to 2020.
- Seeds sourced from 21 native Scottish populations (10 mother trees per population; families described as half-siblings).
- Data collected include growth metrics and phenology at tree level, enabling cross-population and cross-site comparisons.

## Experimental design and plant material
- Seed collection and nursery propagation
  - Seeds from ten trees per population collected in March 2007 and germinated in Aberdeen, 2007.
  - Seedlings transplanted to nurseries (NW, NG, NE) for initial growth.
- Field transplant and layout
  - In 2012, trees transplanted to three field sites: Yair (FS, south), Glensaugh (FE, east), Inverewe (FW, west).
  - Randomised block design with 3 m x 3 m spacing; guard row around blocks.
  - Each block contained one individual from each of eight of the ten families from each of the 21 populations (168 trees per site).
  - Most populations were represented at all three sites; nine were replaced at FS with alternate families from the same population due to insufficient trees.
- Nursery origins at field sites
  - FS and FE: most trees raised in NG or NE; FW included cohorts raised from all three nurseries (NW, NG, NE).

## Measurements and data collection timeline
- Growth measurements
  - Tree height measured at end of each growing season (2013–2020 at FE and FW; 2014–2020 at FS).
  - Basal stem diameter measured at end of each season (2013–2020 at FE and FW; 2020 at FS).
- Phenology assessments
  - Spring phenology assessments conducted annually at each site from 2015 to 2019; 2020 assessments not possible due to COVID-19 restrictions.
- Data file
  - FieldTraits.txt contains per-tree records with identifiers and measured traits across years.

## Data fields and structure (FieldTraits.txt)
- Key identifiers
  - PopulationCode, Description
  - Family (shared mother-tree line; treated as half-siblings)
  - FieldSite (FE: Glensaugh; FS: Yair; FW: Inverewe)
  - FieldCode (unique tree code; ranges by site; NA if not transplanted)
  - Block (randomised block code)
- Measured traits (variables across years)
  - Height related: HA13–HA20 (height after 7th–14th growing seasons; units: mm)
  - Height increments: HI13–HI20 (incremental height; mm)
  - Base stem diameter: DA13–DA20 (mm)
  - Base diameter increments: DI13–DI20 (mm)
  - Budburst timing and duration: BD15–BD20 (duration in days; 2015–2020)
  - Budburst timing (days to reach stages): BT15_4/5/6, BT16_4/5/6, BT17_4/5/6, BT18_4/5/6, BT19_4/5/6 (days since 31 March 2015; multiple stage-specific fields)
- Units and notes
  - Height and diameter in millimetres (mm)
  - Durations and days to budburst in days
  - FieldCode ranges specified per site; some entries may be NA if not transplanted

## Site and data collection specifics
- Field sites
  - FS: Yair, southern Scotland (coordinates provided in metadata)
  - FE: Glensaugh, eastern Scotland
  - FW: Inverewe, western Scotland
- Plot design
  - Blocks: 4 at FS/FE; 3 at FW
  - Each block includes one tree from each of eight of the ten families per population
  - Data capture spans 2013–2020 for growth; 2015–2019 for phenology (COVID-19 affected 2020)

## Data quality, handling, and caveats
- Data compiled from multiple nurseries and sites; potential patchiness and missing entries.
- Most populations represented at each site (N ≈ 159 of 168 trees per site); nine replacements at FS to maintain population representation.
- COVID-19 limited 2020 phenology assessments, affecting complete year coverage.
- FieldCode and NA entries indicate non-transplanted individuals; careful alignment with site metadata is required for cross-site analyses.

## Potential data products and use cases for data support
- Cross-site growth and phenology comparisons by population, seed zone, or nursery origin.
- Longitudinal analysis of height and diameter development across years and sites.
- Evaluation of budburst timing and duration in relation to site conditions and genetic background.
- Creation of dashboards or self-serve reports for stakeholders to explore growth trajectories and phenology patterns.
- Informing conservation, breeding, or adaptation studies using multi-population long-term phenotypic data.

## Accessibility and usage notes
- Primary data file: FieldTraits.txt
- Metadata and variable definitions accompany the dataset to aid interpretation and integration with other datasets.
- Users should account for site-specific measurement timelines, year coverage differences, and any missing data when performing analyses.