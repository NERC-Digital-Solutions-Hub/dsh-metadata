# 2020 juniper glasshouse quantitative genetics metadata

- Overview
  - Metadata and accompanying CSV describe a juniper glasshouse trial (2015–2020) at the UKCEH in Edinburgh.
  - Part of a larger conservation project funded by UKCEH, Forest Research, Scottish Forestry, and the Botanist Foundation.
  - Goal: evaluate standing phenotypic diversity of remnant juniper stands and assess adaptive potential.
  - Data measured in 2020 by ERJ; dataset prepared for publication on the EIDC by JB.

- Seed collection and plant material
  - Seeds collected from 19 natural populations in 2015; populations and families recorded (family = seeds from the same mother tree; open-pollinated half-siblings possible).
  - Seeds stratified (warm then cold) and germinated in greenhouse; emergence from Oct 2016 to Aug 2018.
  - Plants assigned an age class (1 = oldest, 4 = youngest) based on potting order.
  - Final dataset includes 289 plants from 89 families across 16 populations (Table 1: population names, abbreviations, coordinates, and counts).
  - Populations include locations in Scotland and England; coordinates provided (latitude/longitude).
  - In Dec 2018, 89 families with at least 3 surviving individuals were repotted into 13x13x13 cm pots and arranged in a 12-block randomized design.
  - Exclusions: populations CD, DH, and HD excluded at repotting due to insufficient surviving families.
  - Some families (six) were represented across multiple age classes due to dual emergence waves.

- Experimental design
  - 89 families represented by single plant per block (except six families across multiple age classes; some blocks contained more plants).
  - 13x13x13 cm pots; 12-block randomized design.
  - Blocks and age class treated as factors in analyses.

- Dataset structure and contents
  - Single data file: Juniper_glasshouse_trait_data.csv
  - Key fields (examples):
    - Order_all: overall order in randomized block design
    - Order_block: order within its block
    - Pop: population abbreviation
    - Fam: family designation (population abbreviation + number)
    - Block: block number (three blocks used in certain measurements)
    - Age_class: plant age class (1 oldest to 4 youngest)
    - Trait measurements (mean values across leaders or defined segments), including:
      - Mean_ld_len: mean main stem length (cm)
      - Mean_ld_diam: mean main stem diameter just above soil (mm)
      - Mean_ld_ang: mean leading stem angle (degrees; 0–90)
      - Ld_in: number of internodes within 15 cm of tip
      - Ld_brn: number of branches within 15 cm of tip
      - Mean_in_len: mean internode length (cm)
      - Mean_lf_len: mean length of three needles from attachment to tip (mm)
      - Mean_lf_wid: mean width of three needles at widest point (mm)
      - Branch_no: count of branches >50% main stem diameter plus main stem
      - Mean_spread: average horizontal spread (cm)
      - Extension: length of new growth on main stem (mm)
  - Notes: data may contain NA values for missing measurements.

- Measured traits and measurement units
  - Trajectory and morphological traits were measured on leaves, stems, buds, and needles as described above.
  - Units include cm, mm, and degrees (0–90), with some traits derived as means across multiple measurements.

- Data analyses and quality control
  - Statistical software: Minitab 2019 (Version 21.4.3).
  - Data handling: boxplots used to identify outliers; extreme outliers removed; Grubbs outlier tests and Shapiro-Wilks normality tests performed on all traits.
  - Specific outlier handling: branch number and branch spread outliers removed; branch number transformed via square-root to reduce right-skew.
  - Normality assessment used on transformed data; appropriate transformation retained if normality improved.
  - Variation analysis: general linear models with:
    - Region as fixed effect
    - Population nested within region (fixed effect)
    - Family nested within population (random effect)
    - Age_class as fixed effect
    - Block as random effect
  - Multiple testing correction: Bonferroni correction for 11 traits, significance threshold set to p = 0.0045.

- Access, provenance, and preparation
  - Data prepared for publication on the EIDC by JB.
  - Dataset designed to enable cross-population and cross-family comparisons for adaptive potential assessments.

- References and tools
  - Analyses referenced Minitab 19 (version 21.4.3) as the statistical tool.
  - No external datasets cited beyond the described field and lab measurements.