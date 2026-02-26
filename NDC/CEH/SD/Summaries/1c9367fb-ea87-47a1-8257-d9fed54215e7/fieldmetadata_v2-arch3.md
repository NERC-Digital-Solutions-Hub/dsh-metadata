# Metadata for 'Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020'

## Overview
- Long-term, multisite field experiment assessing Scots pine phenotypes across Scotland.
- Seed from 21 native populations (10 trees per population) collected in 2007; grown in nurseries and transplanted to three field sites in 2012-2013.
- Aimed at producing environmental health indicators (growth, structure, phenology) to inform policy and management decisions, with an emphasis on data quality, accessibility, and clear metadata.

## Study design and sites
- Populations and families
  - Seeds from 21 populations, representing Scotland’s native range; each population contributes families from a common mother tree (half-siblings within a family).
  - Families represented across sites; some replacements in FS due to insufficient trees.
- Nurseries and field sites
  - Nursery origins: NW, NG, NE (three nurseries).
  - Field sites (transplanted in 2012): Yair (FS, south), Glensaugh (FE, east), Inverewe (FW, west).
  - Distribution of trees per site: FW includes cohorts from all three nurseries; FS and FE predominantly from specific nurseries.
- Experimental design
  - Randomised blocks with 3 m x 3 m spacing; guard row around periphery.
  - Each block contains one tree from each of eight of the 10 populations across 21 populations (168 trees per site).
  - Some population replacements at FS; majority of families represented across sites.

## Data collected and timing
- Traits measured
  - Growth: height and basal stem diameter (seasonal end measurements).
  - Phenology: spring assessments (2015–2019; 2020 not possible due to COVID-19).
- Measurement schedule
  - Height: end of each growing season (FE and FW: 2013–2020; FS: 2014–2020).
  - Basal diameter: end of each growing season (FE and FW; FS measured in 2020 for the end-year value).
  - Phenology: spring assessments (2015–2019).
- Data file
  - FieldTraits.txt consolidates population, family, site, tree identifiers, and a comprehensive set of trait measurements and derived metrics (see Data Structure section).

## Data structure and variables (FieldTraits.txt)
- Identifiers
  - PopulationCode, Description
  - Family, Description
  - FieldSite (FE, FS, FW), Description
  - FieldCode (unique tree code by site; ranges listed per site)
  - Block, Row, Column
- Growth metrics
  - HA13–HA20: Height at end of growing seasons 2013–2020
  - HI13–HI20: Height increment each year (2013–2020)
  - DA13–DA20: Base stem diameter after each season (2013–2020)
  - DI13–DI20: Base stem diameter increment (2013–2020)
- Budburst and phenology
  - BD15–BD18: Duration of budburst (days from stage 4 to 6) for 2015–2018
  - BD15_4, BD15_5, BD15_6 … BD19_6: Days to reach budburst stages 4–6 for multiple years
  - BT15_4, BT15_5, BT15_6 … BT19_6: Days since 31 March to reach budburst stages (4–6) for multiple years
- Notes on data
  - Units: Heights and diameters in millimeters; durations in days.
  - 2013–2020 data span with COVID-related gap in 2020 phenology assessments.
  - Some inconsistencies and substitutions acknowledged (e.g., replacement of trees at FS).

## Data quality, governance and metadata
- Data provenance and transparency
  - Clear documentation of seed origin, nursery provenance, transplantation, and trial layout.
  - Explicit note that trees from the same mother are half-siblings; randomised block structure described.
- Metadata and accessibility
  - Dataset centralized in FieldTraits.txt with comprehensive column descriptions and units.
  - Detailed population, family, site, and tree identifiers to support traceability and reproducibility.
- Data gaps and challenges
  - COVID-19 impacted 2020 phenology data collection.
  - Some populations/families were replaced at one site due to insufficient representation.
  - Data transformation needs may arise from complex field coding (e.g., FieldCode ranges by site).
- Relevance to monitoring frameworks
  - Provides long-term, multisite environmental health indicators (growth, structure, phenology) across diverse genetic backgrounds.
  - Demonstrates governance around data quality, sharing, and metadata richness, essential for policy monitoring and decision-making.

## Access, usage and implications for policy
- Usage emphasis
  - Suitable for evaluating environmental responses and adaptation across populations and environments.
  - Supports analyses of genetic diversity, growth trajectories, and phenological timing under site-specific conditions.
- Implications for monitoring
  - Illustrates the importance of well-documented metadata, consistent measurement protocols, and transparent data governance to enable policymaker-facing reporting and dashboards.