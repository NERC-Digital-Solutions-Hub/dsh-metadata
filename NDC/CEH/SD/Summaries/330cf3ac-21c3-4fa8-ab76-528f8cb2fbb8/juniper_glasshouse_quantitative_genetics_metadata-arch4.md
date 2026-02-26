# 2020 juniper glasshouse quantitative genetics metadata

## Overview
- Metadata file and accompanying CSV describe a juniper glasshouse trial (2015–2020) conducted at UKCEH, Edinburgh.
- Part of a larger conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
- Contains trait measurements from 289 plants representing 89 families across 16 populations, measured in 2020.
- Data analyzed and prepared for publication on the EIDC by JB; aims to evaluate standing phenotypic diversity of remnant juniper stands and their adaptive potential.

## Sampling and seed collection
- Seeds collected from 19 natural populations in late summer/fall 2015; both population and family recorded.
- Seeds stratified (warm then cold) and sown in 2015; germination occurred from 2016–2018.
- Plants assigned an age_class (1 oldest to 4 youngest) based on potting sequence.
- Table 1 lists population names, coordinates, number of families and individuals.
- In Dec 2018, 89 families with at least 3 surviving individuals were repotted into a 12-block randomized design (13x13x13 cm pots).
- Exclusions: populations CD, DH, HD excluded due to insufficient survivors; some families represented by multiple age classes across waves.
- Measurements: needle morphology only recorded on blocks 2 and 3; some data unavailable (NA).

## Dataset file structure
- Single data file: Juniper_glasshouse_trait_data.csv.
- Table 2 defines variables:
  - Order_all, Order_block: positional identifiers in the experimental layout.
  - Pop, Fam: population abbreviation and family identifier (Pop-Fam, e.g., AR5).
  - Block: block assignment (3 blocks used for analysis).
  - Age_class: 1–4 representing age of transplant.
  - Trait measurements include:
    - Mean_ld_len: mean length of main stems (cm)
    - Mean_ld_diam: diameter of main stems (mm)
    - Mean_ld_ang: leading stem angle (degrees)
    - Ld_in: internodes within 15 cm of tip
    - Ld_brn: number of branches within 15 cm of tip
    - Mean_in_len: mean internode length (cm)
    - Mean_lf_len: mean needle length (mm)
    - Mean_lf_wid: mean needle width (mm)
    - Branch_no: branch count (≥50% main stem diameter)
    - Mean_spread: canopy spread (cm)
    - Extension: new growth length (mm)
- Data structure notes:
  - 289 plants from 89 families across 16 populations.
  - Needle morphology measured only on blocks 2–3.
  - Some blocks/families partially represented due to seedling availability.
  - NA entries indicate unrecorded data.

## Experimental design
- 89 families from 16 populations arranged in a 12-block randomized design.
- Three blocks used for trait measurements; remaining blocks not fully represented for all families.
- Some populations excluded due to insufficient survivors; multiple age classes recorded for a few families.

## Analyses and quality control
- Analyses performed with Minitab 19.
- Data checks: boxplots, outlier inspection; extreme outliers removed.
- Outlier handling: additional removal for branch number and spread; branch number transformed (square-root) to address right-skewness.
- Statistical modeling:
  - General linear models with:
    - Region as fixed effect
    - Population nested within region (fixed)
    - Family nested within population (random)
    - Age_class as fixed effect
    - Block as random effect
- Multiple testing: Bonferroni correction across 11 traits, significance threshold p = 0.0045.

## Data provenance and publication
- Trait data prepared for publication on the EIDC (European Investment/Data Infrastructure for Conservation or equivalent platform).
- Measurements carried out by specified researchers (ERJ; publication preparation by JB).
- Source materials include measurements and population metadata that enable traceability and re-use.

## Implications for data strategy and reuse
- Demonstrates end-to-end data lifecycle: collection, labeling of populations/families, controlled glasshouse experiment, rigorous data curation, and publication-ready formatting.
- Rich metadata supports reproducibility: explicit sampling timeline, stratification scheme, potting history, age_class, and block design.
- Data leadership considerations:
  - Clear articulation of data scope, structure, and quality checks aids discoverability and re-use across related studies.
  - Metadata supports integration with larger phenotypic diversity and adaptive potential assessments.
  - Accessibility via EIDC enhances discoverability for researchers and policy partners.
  - Detailed trait definitions and units support cross-study comparability and meta-analyses.