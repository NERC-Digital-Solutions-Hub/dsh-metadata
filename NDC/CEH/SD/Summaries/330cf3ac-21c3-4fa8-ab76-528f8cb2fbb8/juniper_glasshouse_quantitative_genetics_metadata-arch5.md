# 2020 juniper glasshouse quantitative genetics metadata

- Overview
  - Metadata file and accompanying CSV describe a juniper glasshouse trial (2015–2020) at UKCEH, Edinburgh.
  - Part of a larger conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
  - Traits measured on 289 plants from 89 families across 16 populations; data prepared for publication on the EIDC.
  - Goal: evaluate standing phenotypic diversity and adaptive potential of remnant juniper stands.

- Seed collection and populations
  - Seeds collected from 19 natural populations in late summer/fall 2015.
  - Population and family information recorded; seeds stored at 4°C and stratified (warm then cold) before germination.
  - Seedlings emerged 2016–2018; assigned an age_class (1 oldest to 4 youngest) based on potting time.
  - Table 1 lists populations (e.g., Argyll, Gleann Dubh, Blowick Fell, etc.) with abbreviations, coordinates, and counts of families/individuals.
  - In Dec 2018, 89 families with ≥3 surviving individuals re-potted in a 12-block design (13x13x13 cm pots); some populations excluded (CD, DH, HD) due to no surviving individuals.
  - Some families represented by multiple age classes due to staggered emergence; most others by a single individual per block.

- Experimental design and sampling
  - 289 plants from 89 families across 16 populations.
  - Block design: 12 blocks; first 3 blocks include all 89 families; remaining blocks vary by seedling availability.
  - Some families (e.g., AG7, LM14) represented by two individuals due to differential survival; otherwise one individual per block.
  - Needle morphology measurements (length/width) primarily in blocks 2 and 3.

- Traits measured and data structure
  - Trait categories include:
    - Plant architecture and growth: mean main stem length (Mean_ld_len), main stem diameter above soil (Mean_ld_diam), leading stem angle (Mean_ld_ang), internodes near tip (Ld_in), branches near tip (Ld_brn), mean internode distance (Mean_in_len), mean needle length (Mean_lf_len), mean needle width (Mean_lf_wid).
    - Branch and canopy metrics: branch_no (count of branches >50% main stem diameter plus main stem), mean_spread, Extension (new growth).
  - Units:
    - Lengths in cm or mm, angles in degrees, counts as integers, Extension in mm.
  - Data gaps:
    - NA indicates not recorded.

- Data file structure
  - Single data file: Juniper_glasshouse_trait_data.csv.
  - Key columns:
    - Order_all, Order_block (batch/positioning in design)
    - Pop (population abbreviation)
    - Fam (family identifier)
    - Block (block number)
    - Age_class (potted-up age)
    - Trait measurements: Mean_ld_len, Mean_ld_diam, Mean_ld_ang, Ld_in, Ld_brn, Mean_in_len, Mean_lf_len, Mean_lf_wid, Branch_no, Mean_spread, Extension
  - Table 2 provides definitions, descriptions, and units for each trait.

- Analyses and quality control
  - Analyses conducted in Minitab 2019.
  - Data visualization via boxplots; outliers identified and removed; Grubbs tests and Shapiro-Wilks normality tests applied.
  - Specific outliers removed for branch-related traits; a square-root transformation applied to branch number to address right-skewness.
  - Statistical modelling: general linear models with
    - Fixed effects: region, population nested within region, age_class
    - Random effects: family nested within population, block
  - Bonferroni correction for 11 traits (significance threshold p = 0.0045) to control for multiple testing.

- Provenance, publication, and governance notes
  - Data collected 2015–2020; analyses and preparation for publication conducted by J. Baker and colleagues; dataset prepared for publication on the EIDC.
  - Data intended to enable discovery and reuse for studies on phenotypic diversity and adaptive potential of juniper populations.
  - Data quality considerations include explicit handling of missing data (NA) and documentation of populations/families excluded due to insufficient surviving individuals.

- Limitations and considerations for Data Stewards
  - Some populations were excluded from certain analyses due to zero surviving individuals after re-potting.
  - Variation in representation across families and populations due to seedling availability and survival.
  - Comprehensive metadata available (populations, families, blocks, age_class) to support traceability, discovery, and reproducibility.