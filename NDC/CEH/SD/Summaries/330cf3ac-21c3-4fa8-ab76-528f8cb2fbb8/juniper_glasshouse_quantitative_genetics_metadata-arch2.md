# 2020 juniper glasshouse quantitative genetics metadata Created 20/6/24 by Baker, J.

## Aim and context
- Describes a juniper glasshouse trial (2015–2020) at UKCEH Edinburgh, part of a conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
- Contains trait measurements from 289 plants from 16 populations, measured in 2020; analyzed for publication on the EIDC.
- Objective: evaluate standing phenotypic diversity of remnant juniper stands and assess their adaptive potential.

## Data provenance and seed collection
- Seeds collected from 19 natural populations in late summer/fall 2015; each collection recorded by population and family (mother tree or open-pollinated half-siblings).
- Seeds subjected to warm then cold stratification; germinated in a greenhouse at UKCEH.
- Emergence from Oct 2016 to Aug 2018; seedlings assigned an age class (1 oldest to 4 youngest) based on when they were potted up.

## Experimental design and sampling
- In Dec 2018, 89 families with at least 3 surviving individuals were repotted into 13x13x13 cm pots and placed in a 12-block randomized design.
- Populations CD, DH and HD excluded due to insufficient survivors.
- Some families had seedlings represented across multiple age classes; most families represented by one individual per block.
- Overall: 289 plants from 89 families across 16 populations; first three blocks used for trait measurements to ensure full representation.

## Traits and data structure
- Traits measured include:
  - Stem and leaf metrics: mean main stem length (Mean_ld_len), main stem diameter (Mean_ld_diam), leading stem angle (Mean_ld_ang), internode distance near tip (Ld_in), number of branches near tip (Ld_brn), mean internode length (Mean_in_len), mean leaf length (Mean_lf_len), mean leaf width (Mean_lf_wid), Branch_no, Mean_spread, Extension.
  - Metadata: Order_all, Order_block, Pop (population abbreviation), Fam (family code), Block, Age_class.
- Needle morphology measured only for blocks 2–3.
- Data file: Juniper_glasshouse_trait_data.csv with variables described in Table 2 (definitions and units provided).

## Data quality, cleaning and analysis
- Data graphed as boxplots; outliers visually inspected; extreme outliers removed; Grubbs outlier tests and Shapiro-Wilks normality tests conducted.
- Branch-related traits had additional outliers removed; Branch_no square-root transformed to correct right-skew.
- Variation analysis: general linear models with:
  - Region as a fixed effect
  - Population nested within region as a fixed effect
  - Family nested within population as a random effect
  - Age_class as a fixed effect
  - Block as a random effect
- Multiple-test correction: Bonferroni-corrected significance level for 11 traits to p = 0.0045.

## Output, accessibility and provenance
- Data prepared for publication on the Environmental Information Data Centre (EIDC).
- Analysis conducted using Minitab 2019 (Version 21.4.3); results referenced with standard boxplots and GLMs.
- Works cited: Minitab 19. In. (2024). Minitab LLC.