# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies

## Overview
- Presents data from a study testing whether the SR-drive chromosome in Teleopsis dalmanni reduces egg-to-adult viability and whether fitness effects are recessive or sex-limited.
- Controlled crosses produced eggs with all possible SR and ST male and female genotypes; offspring were genotyped at adult eclosion to estimate selection against drive in both sexes.
- Data are provided as raw observations and as processed summaries to enable exploration of genotype viability under different food conditions.

## Data files included
- Egg-to-adult_viability_raw_data.csv
- Egg-to-adult_viability_processed_data.csv

## Study context and what the data measure
- Objective: quantify viability loss associated with meiotic drive across genotypes and sexes.
- Measurements: genotype frequencies and viability indicators across cages and food treatments, enabling estimation of fitness coefficients for each genotype.

## Data fields and structure

### Raw data (Egg-to-adult_viability_raw_data.csv)
- ID: Unique offspring identifier
- Sex: Offspring sex
- Food_Condition: Food treatment on egg lay (H = 75% corn, M = 50% corn, L = 25% corn)
- Genotype: Offspring genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) defined by microsatellite marker comp162710
  - NG: not genotyped
  - NA: not amplified
- Collection_Date: Date eggs were collected
- Cage: Cage ID number (nested within collection date)

### Processed data (Egg-to-adult_viability_processed_data.csv)
- Cage_ID: Unique cage identifier
- Food_condition: Food treatment (H, M, L)
- Collection_Date: Date eggs were collected
- Tot_No: Total offspring collected from a cage
- F_No: Total females collected from a cage
- M_No: Total males collected from a cage
- Males_Genod: Males genotyped in a cage
- Females_Genod: Females genotyped in a cage
- Geno_No: Total offspring genotyped in a cage
- Sex: Sex of the genotype
- Genotype: Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y)
- W: Fitness of each genotype, by cage (a summarized measure)

## Data processing and aggregation
- Raw data are aggregated to produce processed data with one row per genotype per cage, summarizing counts and genotyped individuals.
- Processed data includes a fitness indicator (W) by cage for each genotype.

## How to use the data
- Combine raw and processed files by Cage_ID/Collection_Date and Genotype to analyse genotype viability across cages and conditions.
- Explore genotype frequencies and viability by:
  - Food_condition (H, M, L)
  - Sex (where applicable)
  - Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y)
- Compute per-genotype fitness estimates (W) and compare across sexes and food conditions to assess recessivity or sex-limited effects.
- Create dashboards or pivot tables to enable self-service exploration of:
  - Genotype distribution per cage and collection date
  - Viability trends across food treatments
  - Genotype-specific viability contrasts between sexes

## Data quality and notes
- Some records include NG (not genotyped) or NA (not amplified) statuses in raw data.
- Data are organized per cage and per genotype, enabling robust aggregation but requiring careful handling of missing genotyping data when analyzing viability.

## Access and provenance
- Source: Finnegan, S.; White, N.; Koh, D.; Camus, M. F.; Fowler, K.; Pomiankowski, A. (2019). Meiotic drive reduced egg-to-adult viability in stalk-eyed flies. Proc. R. Soc. B. DOI: https://doi.org/10.1098/rspb.2019.1414
- Contact: a.pomiankowski@ucl.ac.uk