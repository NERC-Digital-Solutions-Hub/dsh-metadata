# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies

## Overview
- Dataset from a 2019 study testing SR-drive chromosome effects on egg-to-adult viability in Teleopsis dalmanni.
- Controlled crosses produced all possible SR/ST genotypes; offspring genotyped at adult eclosion to estimate selection against drive in both sexes.
- Data provided as two CSV files: raw per-offspring data and cage-level processed summaries.

## Data Files and Structure
- Egg-to-adult_viability_raw_data.csv
  - Per-offspring records with fields:
    - ID (unique offspring identifier)
    - Sex
    - Food_Condition (H = 75% corn, M = 50%, L = 25%)
    - Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) via microsatellite comp162710
    - Collection_Date
    - Cage (cage ID, nested within collection date)
    - NG (not genotyped) or NA (not amplified)
- Egg-to-adult_viability_processed_data.csv
  - Cage-level summaries, one row per genotype per cage with fields:
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

## Variables and Coding
- Genotypes: X/X, SR/X, SR/SR, ST/Y, SR/Y; designated by microsatellite marker comp162710.
- Food_condition: H, M, L corresponding to corn content.
- Collection_Date: date eggs were collected; Cage is nested within this date.
- NG/NA: indicate missing genotype data (not genotyped / not amplified).
- W: fitness score for each genotype within a cage.

## Research Aims and Analyses
- Objective: estimate selection coefficients against the drive in both sexes; determine if fitness effects are recessive or sex-limited.
- Data enable assessment of genotype frequencies and viability across environmental conditions (food levels) and over time (collection date), via raw and cage-level aggregated data.

## GIS Visualization Considerations
- Although data are not spatially explicit, they can be prepared for map-like visualization by treating Cage_ID (and collection date) as spatial-temporal units.
- Potential visualizations:
  - Fitness (W) by Cage_ID and Genotype, colored by Genotype and by Food_condition.
  - Temporal trends of genotype frequencies across Collection_Date.
  - Faceted views by Food_condition to compare environmental effects.
- Data preparation steps:
  - Join raw and processed data on Cage_ID and Genotype.
  - Normalize Tot_No and Geno_No to derive per-genotype viability by cage.
  - If cage coordinates become available, create spatial maps showing genotype distribution and fitness across locations.

## Data Quality and Provenance
- Data originate from a published study (2019) with DOI provided in the full text.
- Data include explicit environmental treatment (Food_condition) and clear genotype categories.
- Metadata notes:
  - NG/NA codes indicate incomplete genotyping or data amplification issues.
  - Processed data summarize raw data by genotype and cage for higher-level analyses.

## Source
- Authors: Finnegan, White, Koh, Camus, Fowler, Pomiankowski (2019)
- Title: Meiotic drive reduced egg-to-adult viability in stalk-eyed flies
- Publication: Proceedings of the Royal Society B
- Contact: a.pomiankowski@ucl.ac.uk