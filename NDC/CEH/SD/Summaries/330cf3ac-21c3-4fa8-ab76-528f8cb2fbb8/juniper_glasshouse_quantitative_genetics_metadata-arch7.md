# 2020 juniper glasshouse quantitative genetics metadata

## Overview
- Metadata and accompanying CSV describe a juniper glasshouse trial (2015–2020) at UKCEH, Edinburgh.
- Part of a conservation project funded by UKCEH, Forest Research, Scottish Forestry and the Botanist Foundation.
- Contains trait measurements from 289 plants across 16 populations (from 89 families) to evaluate standing phenotypic diversity and adaptive potential.
- Data analyzed and prepared for publication on the EIDC.

## Spatial and Population Context
- Populations originate from natural stands across the UK (e.g., Argyll, Arran, Lake District, S. England, etc.).
- Table 1 lists full names, abbreviations, latitude, longitude, number of families, and number of individuals per population.
- Geographic coordinates enable spatial understanding of population sources and potential environmental associations, even though the trial is in a single glasshouse.

## Seed Collection and Experimental Design
- Seeds collected in late summer/fall 2015 from 19 natural populations; populations and maternal families recorded.
- Seeds stratified (warm then cold) and grown in UKCEH Edinburgh greenhouse; emergence began in Oct 2016 and continued to Aug 2018.
- In Dec 2018, 89 families with at least 3 surviving individuals were repotted into a 12-block randomized design (13x13x13 cm pots).
- Excluded populations: CD, DH, HD due to insufficient surviving individuals.
- Some families represented by multiple age classes due to staggered emergence; most families represented by a single plant per block.
- Final dataset: 289 plants from 89 families representing 16 populations.

## Data Structure and Variables
- Dataset file: Juniper_glasshouse_trait_data.csv
- Metadata describes the data fields (Table 2):
  - Design and identifiers: Order_all, Order_block, Pop, Fam, Block, Age_class
  - Population ancestry: Pop = population abbreviation; Fam = family code (e.g., AR5)
  - Trait measurements: Mean_ld_len, Mean_ld_diam, Mean_ld_ang, Ld_in, Ld_brn, Mean_in_len, Mean_spread, Extension, Mean_lf_len, Mean_lf_wid, Branch_no
  - Units and descriptions are specified for each field; some values are NA
- Populations and families are tied to the geographic table (Table 1) via the Pop/Age_class/Block fields.

## Measured Traits
- Main stem and architecture:
  - Mean_ld_len (cm): mean length of the main stem leaders
  - Mean_ld_diam (mm): diameter just above soil
  - Mean_ld_ang (degrees): angle of leading stem(s)
  - Ld_in: internodes within 15 cm of the tip
  - Ld_brn: number of branches within 15 cm of the tip
  - Mean_in_len (cm): mean length of internodes on main stems
  - Mean_spread (cm): growth spread
  - Branch_no: count of branches >50% main stem diameter
  - Extension (mm): new growth on the main stem
- Needle morphology:
  - Mean_lf_len (mm): mean length of 3 needles
  - Mean_lf_wid (mm): mean width of 3 needles
- Sampling and layout:
  - Order_all, Order_block, Block, Age_class, Pop, Fam describe the experimental setup and population lineage

## Data Processing and Analysis
- Analyses performed in Minitab 2019 (Minitab 19, 2024).
- Quality checks: boxplots, outlier screening, visual assessment of skewness.
- Outliers removed for most traits; branch-related traits subjected to additional outlier removal and square-root transformation to address right-skewness.
- Normality tests (Shapiro-Wilks) conducted; transformations applied as needed.
- Variation analysis: general linear models with region as fixed effect, population nested within region, and family nested within population; age_class as fixed effect; block as random effect.
- Multiple testing correction: Bonferroni-adjusted significance level to p = 0.0045 for 11 traits.

## Data Provenance and Publication
- Data collected and prepared for publication on the EIDC.
- Seed collection and trial conducted 2015–2020; trait data finalized and analysed by project researchers.
- References: Minitab 19 for statistical analyses.

## GIS-Relevance and Potential Visualisations
- Geospatial value lies in linking population origin coordinates (Table 1) to trait variation across populations.
- Potential map-based products:
  - Spatial distribution of trait means by population with uncertainty
  - Spatial-genetic/allocation visuals correlating phenotypic traits with geographic origins
  - Overlay of population coordinates with environmental layers to explore landscape adaptation signals
- Considerations for GIS use:
  - The glasshouse trial is a controlled environment; coordinates reflect source populations rather than trial locations.
  - Data are at the population-family level, not per-plot geolocated measurements; integration with other spatial datasets may require careful alignment of population-level geography.
  - Missing data and excluded populations should be accounted for in spatial analyses.