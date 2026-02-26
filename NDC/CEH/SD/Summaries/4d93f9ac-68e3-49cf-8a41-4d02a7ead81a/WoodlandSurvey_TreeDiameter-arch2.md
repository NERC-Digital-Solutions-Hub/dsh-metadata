# Woodlands Survey tree diameter data 1971-2001

## Purpose and scope
- Long-term ecological dataset capturing site-level ecological information and detailed plot-level data from 103 broadleaved woodlands across Britain (1971), with resampling in 2000s (referred to as 2001) using identical field methods.
- Aimed at assessing ecological change over time and identifying principal drivers of change (e.g., atmospheric deposition of sulfur and nitrogen, climate, canopy changes, woodland management).

## Dataset contents and structure
- Site and plot identifiers:
  - Site: code 1–103
  - Plot: code 1–16
- Species and counts:
  - BRC_number and BRC_names: scientific species codes and names
  - Amalgams and Amalgam_names: grouped taxa where data were inconsistently recorded
  - Status: Live or Dead
- Measurements:
  - DBHclass: 5 cm diameter-at-breast-height interval bands (coded 1–32)
  - Count: number of individuals in each DBH class (saplings/shrubs counted with a doubling factor)
  - Final_count: corrected count per DBH class per plot
- Temporal and categorical fields:
  - Yr: 1 = 1971, 2 = 2000s
  - Woody: 'w' if woody species
  - Field_sheet: original data sheet type
- DBH ranges and class mapping are predefined (multiple 5 cm intervals)

## Sampling design and methods
- Stratified sampling across the entire area.
- Survey conducted according to Bunce & Shaw (1973) standardized methods.
- Field handbook included in supporting documentation.
- Re-surveys were carried out in 2000/2001 using the same methods to ensure comparability.

## Temporal coverage and key analyses
- Baseline data collected in 1971 with follow-up in 2000s (2001), enabling analysis of long-term ecological change.
- Analyses (published in 2004/2005) examined drivers of change using both survey data and external explanatory variables (e.g., deposition, climate, canopy structure, management).

## Related datasets and publications
- Related dataset: Countryside Survey.
- Key publications:
  - Corney et al. (2004) on landscape-scale drivers of vegetation composition.
  - Kirby et al. (2005) Measuring Long Term Ecological Change in British Woodlands (1971-2001): re-survey and change analysis.
  - Supporting references include Avery (1973) and Haines-Young et al. (2003).

## Originators and data custodians
- 1971 originators: R.G.H. Bunce and M.W. Shaw (Nature Conservancy Merlewood)
- 2001–03 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH Lancaster; English Nature; University of Liverpool)
- Data structure and metadata maintained to support broad reuse and cross-site comparisons

## Data usage, quality, and storage
- Data intended for verification, quality assurance, cleansing, transformation, and standardised analysis to produce outputs (e.g., site-level summaries, plots, charts).
- Datasets are designed for storage and upload to appropriate portals; field handbook and supporting documentation facilitate reproducibility and methodological transparency.

## Access and interpretation considerations
- Data are structured for cross-temporal comparison of DBH distributions and species composition within and across sites.
- Interpret with awareness of:
  - The 5 cm DBH interval coding and sapling/shrub counting adjustments
  - The cross-year comparability ensured by identical field methods and sampling design
  - Historical context on drivers (atmospheric deposition, climate, canopy changes, management) as reported in associated publications