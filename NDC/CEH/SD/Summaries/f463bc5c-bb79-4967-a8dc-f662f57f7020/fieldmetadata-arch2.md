# Metadata for 'Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020'

## Overview
- Long-term, multisite field trial of Scots pine (Pinus sylvestris) across three field sites in Scotland to monitor growth and phenology over time.
- Seed collection in March 2007 from ten trees per population across 21 native Scottish populations (3 populations per seed zone; 7 seed zones).
- Seed handling includes dormancy breaking, cold storage, germination, and transplanting to controlled nurseries before field establishment.
- Phenotypic data cover growth traits and phenology from 2013/2014 to 2020, enabling longitudinal analysis of environmental health and policy-related performance.

## Experimental design and sites
- Populations and families
  - 21 populations, 10 mother-tree families per population (families treated as half-sib groups).
  - Seeds represent the species’ native range in Scotland; three populations per seed zone.
- Nurseries
  - Seedlings grew in three nurseries: NW, NG, NE.
- Field sites (established 2012)
  - Yair, Scottish Borders (FS) – south Scotland
  - Glensaugh (FE) – east Scotland
  - Inverewe (FW) – west Scotland
- Planting design
  - Randomised blocks: 3 m x 3 m spacing; four blocks at FS and FE, three blocks at FW; guard row around periphery.
  - Each block contains one tree from each of eight of the 10 families from 21 populations (168 trees per site).
  - Minor substitutions: 9 families replaced at FS with alternatives from the same population due to insufficient trees.
- Transplant origins
  - FS: trees raised in NG; FE: most locally raised in NE; FW: cohorts from all three nurseries (NW, NG, NE) represented.

## Data collection and traits
- Growth measurements
  - Height measured annually end of growing season: FE and FW (2013–2020); FS (2014–2020).
  - Basal stem diameter measured annually end of growing season: FE and FW (2013–2020); FS only in 2020.
- Phenology assessments
  - Spring assessments conducted 2015–2019 at all sites; 2020 data not collected due to COVID-19 restrictions.
- Data file
  - Single file: FieldTraits.txt
  - Core fields include: PopulationCode, Family, FieldSite, FieldCode, Block, annual heights (HA13–HA20), height increments (HI13–HI20), base diameters (DA13–DA20), base diameter increments (DI14–DI20), budburst duration metrics (BD15–BD20), and days to budburst stages (BT15_4, BT15_5, BT15_6, etc. for 2015–2019).
  - Units: heights and diameters in millimeters; durations in days.
  - NA indicates missing or not transplanted (e.g., some FieldCode values).

## Data structure and provenance
- FieldTraits.txt includes standardized codes:
  - PopulationCode and Description
  - Family and NA for non-applicable
  - FieldSite codes: FE (Glensaugh), FS (Yair), FW (Inverewe)
  - FieldCode: unique tree identifiers per site; not transplanted entries are NA
- Temporal span: phenotypes collected 2013–2020 (with phenology 2015–2019; 2020 omitted due to pandemic).

## Data quality, limitations, and notes
- Randomised design and multi-site layout enhance comparability and reduce bias in environmental monitoring.
- Some populations/families were replaced at one site due to sample constraints; site-level representation adjusted accordingly.
- COVID-19 disrupted 2020 phenology data collection, resulting in incomplete final-year phenology records.

## Applications for environmental monitoring and analytics
- Enables long-term assessment of growth, structure, and phenology responses across multiple populations and environments.
- Supports evaluation of genetic-by-environment interactions and adaptation over time.
- Provides standardized, repeatable outputs suitable for cross-site comparisons, policy performance evaluation, and environmental health monitoring.
- Data management aligns with standard monitoring practice, with an emphasis on transparency and reproducibility (data stored with appropriate portals).