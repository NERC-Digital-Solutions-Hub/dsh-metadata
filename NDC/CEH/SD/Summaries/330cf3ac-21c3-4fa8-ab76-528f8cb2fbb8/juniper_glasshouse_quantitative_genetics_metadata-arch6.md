# 2020 juniper glasshouse quantitative genetics metadata Created 20/6/24 by Baker, J.

## Overview
- Describes a juniper glasshouse trial (2015–2020) at UKCEH Edinburgh, part of a conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
- Contains trait measurements from 289 plants representing 89 families across 16 populations; data analyzed and prepared for publication on the EIDC.
- Aim: evaluate standing phenotypic diversity of remnant juniper stands and assess adaptive potential.

## Experimental design and seed collection
- Seed collection from 19 natural populations in 2015; berries collected, seeds stratified and sown Dec 2015.
- Plants established in a greenhouse with warm then cold stratification; emergence from Oct 2016 to Aug 2018; plants assigned an age class (1 = oldest, 4 = youngest).
- In Dec 2018, 89 families with ≥3 surviving individuals repotted into a 12-block randomized design (13×13×13 cm pots). Populations CD, DH and HD excluded due to no surviving individuals.
- Most families represented by a single plant per block; six families represented by multiple individuals across age classes due to multiple wave emergence.
- Traits measured on plants in the first three blocks; needle morphology measured only on blocks 2–3; NA values present where data were not recorded.

## Dataset structure
- Single data file: Juniper_glasshouse_trait_data.csv.
- Core identifiers: Order_all (overall order in block design), Order_block (order within block), Pop (population abbreviation), Fam (family identifier, e.g., AR5), Block (block number), Age_class (potted-up age).
- Trait data cover a range of morphological measurements (detailed in Table 2 of the metadata).

## Traits measured
- Mean_ld_len: mean length of the main stem(s); units: cm.
- Mean_ld_diam: mean diameter of the main stem(s) just above soil; units: mm.
- Mean_ld_ang: mean angle of leading stem(s) from vertical; units: degrees (0–90°).
- Ld_in: number of internodes within 15 cm of the tip; unit: count.
- Ld_brn: number of branches within 15 cm of the tip; unit: count.
- Mean_in_len: mean length of internode distance on main stems; units: cm.
- Mean_lf_len: mean length of 3 needles from attachment point to tip; units: mm.
- Mean_lf_wid: mean width of 3 needles at widest point; units: mm.
- Branch_no: total number of branches >50% diameter of main stem plus main stem; unit: count.
- Mean_spread: average spread in the growth area; units: cm.
- Extension: length of new growth on the main stem (non-woody growth); units: mm.
- Notes: NA values present where data were not recorded.

## Data processing and quality assurance
- Outlier handling: boxplots and visual checks; extreme outliers removed; Grubbs tests and Shapiro–Wilk normality tests applied to traits.
- Specific corrections: branch number (Ld_brn) outliers removed and square-root transformed to correct right-skewness; Shapiro–Wilk on transformed values became non-significant.
- Statistical analyses: general linear models with region as fixed effect; population nested within region fixed effect; family nested within population random effect; age_class fixed effect; block random effect.
- Multiple testing correction: Bonferroni-adjusted significance level for 11 traits (p = 0.0045).

## Analyses tools and provenance
- Analyses performed in Minitab 19 (Version 21.4.3, 2024).
- Data prepared for publication on the EIDC by JB.

## Potential uses for data support
- Enable cross-population and cross-family comparisons of phenotypic traits to assess diversity and adaptive potential.
- Create self-serve data products (e.g., dashboards, pivot tables) to explore trait variation by population, family, age class, or block.
- Inform conservation and breeding strategies by linking trait variation to geographic and genetic provenance, with clear metadata for reproducibility.

## Limitations and notes
- Some populations have zero survivors and were excluded from certain analyses; NA entries exist where measurements were not recorded.
- Needle morphology data are limited to blocks 2–3; not all traits are measured across all plants.