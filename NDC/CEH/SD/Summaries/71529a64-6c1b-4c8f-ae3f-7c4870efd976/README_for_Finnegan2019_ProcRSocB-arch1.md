# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies

## Aim and study design
- Tests whether the SR-drive chromosome in Teleopsis dalmanni reduces egg-to-adult viability.
- Investigates whether fitness effects are recessive or sex-limited.
- Experimental crosses produced eggs with all possible SR and ST male and female genotypes.
- Offspring were genotyped at adult eclosion to estimate selection coefficients against drive in both sexes.

## Data files and structure
- Two CSV datasets:
  - Egg-to-adult_viability_raw_data.csv
  - Egg-to-adult_viability_processed_data.csv
- Raw data fields:
  - ID (unique offspring identifier)
  - Sex (offspring sex)
  - Food_Condition (H = 75% corn, M = 50% corn, L = 25% corn)
  - Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y; NG/NA if not genotyped or amplified)
  - Collection_Date
  - Cage (cage ID, nested within collection date)
- Processed data fields (one row per genotype per cage):
  - Cage_ID
  - Food_condition
  - Collection_Date
  - Tot_No (total offspring)
  - F_No (females)
  - M_No (males)
  - Males_Genod (males genotyped)
  - Females_Genod (females genotyped)
  - Geno_No (offspring genotyped)
  - Sex
  - Genotype
  - W (fitness of each genotype by cage)

## Genotypes and markers
- Genotypes defined by microsatellite marker comp162710:
  - X/X, SR/X, SR/SR, ST/Y, SR/Y

## Environment and treatment
- Food_condition levels:
  - H: 75% corn
  - M: 50% corn
  - L: 25% corn

## What is measured
- Egg-to-adult viability as genotype-specific fitness.
- W in the processed data represents fitness by cage for each genotype.

## How to analyse
- Use raw data for individual-level analyses; processed data for cage-level analyses.
- Estimate selection coefficients against the SR drive in both sexes.
- Test for recessive vs. sex-limited effects by comparing fitness across genotypic classes.
- Assess potential interactions with food_condition (diet effects).
- Compare observed genotype frequencies to Mendelian expectations to detect viability differences.

## Data quality and caveats
- Some entries are NG (not genotyped) or NA (not amplified); account for missing data.
- Cage-level aggregation in processed data aids robust cross-cage analysis; ensure proper alignment by Cage_ID and Collection_Date.

## Metadata and access
- Source: Finnegan, S.; White, N.; Koh, D.; Camus, M. F.; Fowler, K.; Pomiankowski, A. 2019. Meiotic drive reduced egg-to-adult viability in stalk-eyed flies. Proc. R. Soc. B. DOI: https://doi.org/10.1098/rspb.2019.1414
- Contact: a.pomiankowski@ucl.ac.uk