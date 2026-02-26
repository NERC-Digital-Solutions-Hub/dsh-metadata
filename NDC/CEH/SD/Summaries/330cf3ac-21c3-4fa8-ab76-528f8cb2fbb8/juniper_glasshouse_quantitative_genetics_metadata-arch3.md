# 2020 juniper glasshouse quantitative genetics metadata

## Overview
- Metadata and dataset describing a juniper glasshouse trial (2015-2020) at the UKCEH, Edinburgh.
- Part of a larger conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
- Objective: evaluate standing phenotypic diversity of remnant juniper stands and assess their adaptive potential.
- Data prepared for publication on the EIDC (Environment and Information Data Centre).

## Seed collection and experimental setup
- Seeds collected from 19 natural populations in late summer/fall 2015; population and family records retained.
- Seeds germinated in December 2015; subjected to warm stratification (Dec 2015–Mar 2016) then cold stratification (Mar 2016–Oct 2017).
- Seedlings germinated progressively (Oct 2016–Aug 2018); plants age-classified by potting wave (1 = oldest, 4 = youngest).
- December 2018: 89 families with at least 3 surviving individuals repotted into 13x13x13 cm pots, arranged in a 12-block randomized design.
- Excluded populations CD, DH, HD after repotting due to insufficient survivors.
- Some seedling families represented in multiple age classes due to staggered emergence; others represented by a single individual per block.

## Populations and sampling
- 16 populations represented in the final dataset.
- Table 1 provides population names, abbreviations, geographic coordinates, number of families and individuals per population.
- Total: 289 plants from 89 families across 16 populations.
- Needle morphology measurements were limited to blocks 2 and 3.

## Trait measurements
- Traits measured on plants from the first three blocks (to ensure full family representation).
- Measured traits include:
  - Main stem length (Mean_ld_len) and main stem diameter (Mean_ld_diam) near soil level
  - Lead stem angle (Mean_ld_ang)
  - Internode features (Ld_in, Ld_brn, Mean_in_len)
  - Needle traits (Mean_lf_len, Mean_lf_wid)
  - Branch count (Branch_no) and canopy spread (Mean_spread)
  - New growth extension (Extension)
- Data include NA entries where measurements were not recorded.

## Data file structure and metadata
- Data file: Juniper_glasshouse_trait_data.csv
- Key fields:
  - Order_all: overall plant position in the randomized design
  - Order_block: position within its block
  - Pop: population abbreviation
  - Fam: family identifier (population abbreviation + number)
  - Block: block designation (three blocks contained all populations)
  - Age_class: age of plant (1 = oldest, 4 = youngest)
  - Trait columns: Mean_ld_len, Mean_ld_diam, Mean_ld_ang, Ld_in, Ld_brn, Mean_in_len, Mean_lf_len, Mean_lf_wid, Branch_no, Mean_spread, Extension
- Table 2 provides abbreviations, trait descriptions, and measurement units.

## Analyses and statistical methods
- Software: Minitab 2019 (Minitab 19, 2024).
- Data handling and quality checks:
  - Visual boxplots to identify outliers and skewness.
  - Extreme outliers removed; Grubbs tests and Shapiro-Wilks normality tests performed on all traits.
  - Branch-related traits had additional outliers removed; branch number underwent square-root transformation to address right-skew.
- Variation analyses:
  - General linear models with:
    - Region as a fixed effect
    - Population nested within region as a fixed effect
    - Family nested within population as a random effect
    - Age_class as a fixed effect
    - Block as a random effect
  - Bonferroni-adjusted significance level for 11 traits: p = 0.0045
- Notes:
  - Needle morphology data were limited to certain blocks; other traits were measured more broadly.
  - Data prepared and aligned for publication at the EIDC.

## Data provenance and references
- Seed collection and trial details are described within the metadata to support traceability and data governance.
- Works cited: Minitab 19 (Version 21.4.3) for statistical analyses.