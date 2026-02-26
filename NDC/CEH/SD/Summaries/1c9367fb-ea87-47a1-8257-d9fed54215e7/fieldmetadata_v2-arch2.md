# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- Long-term field trial of Scots pine (Pinus sylvestris) using seed from 21 native Scottish populations, representing the species' native range and three seed zones.
- Purpose: monitor environmental health and policy-relevant phenotypes using standardized trait data across multiple sites and years.

## Experimental design and provenance
- Seed collection: seeds from ten trees per population (210 trees total) collected March 2007; germinated and grown under controlled nursery conditions.
- Nurseries: trees raised in NW, NG, or NE nurseries before field planting.
- Field sites (planted in 2012): Yair (FS, south Scotland), Glensaugh (FE, east Scotland), Inverewe (FW, west Scotland); sites characterized by latitude/longitude coordinates.
- Transplant and layout: randomized blocks at each site with 3 m x 3 m spacing; guard row around blocks.
- Population and family representation: each block contains one tree from eight of the ten families per population (168 trees per block). Most populations represented at all sites (N=159); nine families replaced at FS due to insufficient trees.
- Tree assignment by site: FW included cohorts from all three nurseries; FS and FE primarily from NG or locally grown stocks.

## Measurements and phenotypes
- Growth measurements:
  - Height: recorded annually-end (FE and FW 2013–2020; FS 2014–2020) in millimeters.
  - Basal stem diameter: recorded annually-end (FE and FW 2013–2020; FS 2020) in millimeters.
- Phenology:
  - Spring assessments of phenology at each site (2015–2019); 2020 not possible due to COVID-19.
- Data scope: multiple trait categories captured over time to assess growth trajectories and seasonal timing across genetic populations and environmental contexts.

## Data file and structure
- File: FieldTraits.txt
- Core fields:
  - PopulationCode, Description; Family; FieldSite (FE, FS, FW); FieldCode (unique tree code per site); Block; Row; Column.
  - Growth traits: HA13–HA20 (Height after 7th–14th seasons; 2013–2020), HI13–HI20 (Height increment per year), DA13–DA20 (Base stem diameter; 2013–2020), DI14–DI20 (Base stem diameter increment; 2014–2020).
  - Budburst traits: BD15–BD20 (Duration of budburst by year); BT15_4, BT15_5, BT15_6, etc. (Days since 31 March for budburst stages 4–6; year-specific).
- Units: Height and diameter in millimeters; duration and days in days.

## Data quality, storage and access
- Data provenance: clearly documents seed origin, nursery history, transplantation, and site-level experimental design.
- Standardised outputs: measured as time-series growth and phenology across sites and populations for consistent environmental health interpretation.
- Data management: dataset designed for storage and upload to appropriate data portals; supports reproducibility and cross-site comparisons.

## Potential uses for environmental health and policy monitoring
- Compare long-term growth and phenology across environmental gradients and genetic origins.
- Assess adaptation potential and environmental sensitivity of Scots pine populations.
- Integrate with other environmental datasets to enhance value beyond single-use analyses (as a key challenge and objective for data interoperability).
- Map and chart spatial-temporal trends in forest phenotypes to inform conservation and management decisions.