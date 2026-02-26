# Metadata for 'Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020'

## Overview
- A long-term, multisite field experiment of Scots pine (Pinus sylvestris) conducted across three field sites in Scotland (Yair/FS, Glensaugh/FE, Inverewe/FW).
- Seed from 21 native populations (10 trees from each) collected in 2007; three populations from each of seven seed zones.
- Seedlings grown in one of three nurseries (NW, NG, NE) before transplanting to field sites in 2012.
- The study design includes randomised blocks, multiple families per site, and guards around perimeters. Most families (N=159) are represented at all three sites; a few were replaced due to insufficient trees.
- Measurements span 2013–2020 for growth traits and phenology, with 2020 phenology data not collected due to COVID-19 restrictions.

## Data Structure and Content
- Dataset consists of a single file: FieldTraits.txt.
- Core variables and descriptors:
  - PopulationCode, Description: population identity
  - Family: family code (half-siblings from the same mother tree)
  - FieldSite: site code (FE = Glensaugh, FS = Yair, FW = Inverewe)
  - FieldCode: unique tree identifier; ranges differ by field site (Inverewe: 5001–5672, 6001–6004, 7001–7672; NA if not transplanted)
  - Block: randomized block code (A, B, C, D for FW; FS/FE have 4 blocks; FW has 3 blocks)
  - Growth and phenology traits recorded across years, including:
    - HA13–HA20: height after 7th–14th growing seasons (mm)
    - HI13–HI20: height increments (mm)
    - DA13–DA20: base stem diameter after 7th–14th growing seasons (mm)
    - DI13–DI20: base stem diameter increments (mm)
    - BD15–BD20: duration of budburst (days to progress between stages)
    - BT15_4, BT15_5, BT15_6; BT16_4, BT16_5, BT16_6; BT17_4, BT17_5, BT17_6; BT18_4, BT18_5, BT18_6; BT19_4, BT19_5, BT19_6: time or days to reach budburst stages (days since 31 March or duration)
- Units are specified in the metadata (e.g., mm for height/diameter, days for budburst timing).
- Data include NA values where not applicable (e.g., non-transplanted trees).

## Study Design and Provenance
- Seed collection in 2007; germination and nursery growth prior to field planting.
- Field transplant in 2012 to three sites with 3 m x 3 m spacing; four blocks at FS/FE and three blocks at FW; guard row around plot perimeters.
- Each block contains one tree from each of eight of the ten populations (168 trees per block across sites). Most populations are represented at all sites; a minority replaced at FS due to insufficient trees.
- Field measurements taken at end of each growing season (2013–2020 for FE and FW; 2014–2020 for FS). Phenology assessments conducted spring 2015–2019; 2020 assessments not possible due to COVID-19.

## Temporal and Spatial Coverage
- Temporal: seed collection 2007; nursery growth; field planting 2012; growth/phenology measurements 2013–2020.
- Spatial: three field sites in Scotland with precise coordinates provided for the seed origin and field sites; site codes FE (Glensaugh), FS (Yair), FW (Inverewe).

## Data Quality, Documentation, and Limitations
- Highly detailed metadata describing each variable, units, and data collection context.
- 2020 phenology data unavailable due to COVID-19 restrictions; users should account for missing data in time-series analyses.
- Some fields contain NA or are conditionally applicable (e.g., FieldCode NA for non-transplanted trees), requiring careful handling during data processing.

## Governance, Reuse, and Access Considerations
- Metadata-rich dataset supports discoverability, reproducibility, and appropriate data governance.
- Single-file dataset (FieldTraits.txt) with explicit variable definitions and year-by-year measurements facilitates standardized use across sites.
- Licensing, data access policy, and redistribution terms are not specified in the provided metadata; consider adding a data usage license and citation guidance.
- For Data Stewards: ensure ongoing stewardship by maintaining a clear data dictionary, crosswalks for FieldCode and site mappings, and an update plan for new years or revised measurements; confirm interoperability and consistency of units across sites and years.