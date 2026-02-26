# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies

## Overview
- A dataset accompanying a study on whether the SR-drive chromosome in Teleopsis dalmanni reduces egg-to-adult viability and whether fitness effects are recessive or sex-limited.
- Two CSV data files are provided: raw data at the offspring level and processed data summarized by genotype within cages.
- Aims: test viability loss due to drive, infer selection coefficients against drive in both sexes.
- Publication and contact: Finnegan et al. 2019, Proc. R. Soc. B. DOI: 10.1098/rspb.2019.1414. Contact: a.pomiankowski@ucl.ac.uk

## Data Files and Structure
- Data files
  - Egg-to-adult_viability_raw_data.csv: per-offspring records.
  - Egg-to-adult_viability_processed_data.csv: per-genotype-per-cage summaries.
- Data types
  - Genotype categories include X/X, SR/X, SR/SR, ST/Y, SR/Y (identified by microsatellite marker comp162710).
  - Food_condition uses categorical codes: H (75% corn), M (50% corn), L (25% corn).
  - Cage-based aggregation in processed data to enable genotype-specific fitness estimates.

## Key Data Columns

### Egg-to-adult_viability_raw_data.csv
- ID: Unique offspring identifier.
- Sex: Offspring sex.
- Food_Condition: Diet treatment during egg laying (H/M/L).
- Genotype: Offspring genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y); NG = not genotyped, NA = not amplified.
- Collection_Date: Date eggs were collected.
- Cage: Cage ID (nested within collection date).

### Egg-to-adult_viability_processed_data.csv
- Cage_ID: Unique cage identifier.
- Food_condition: Diet treatment in the cage (H/M/L).
- Collection_Date: Date eggs were collected.
- Tot_No: Total offspring in the cage.
- F_No: Total females in the cage.
- M_No: Total males in the cage.
- Males_Genod: Number of males genotyped in the cage.
- Females_Genod: Number of females genotyped in the cage.
- Geno_No: Total offspring genotyped in the cage.
- Sex: Sex of the genotype (as in raw data).
- Genotype: Genotype category (X/X, SR/X, SR/SR, ST/Y, SR/Y).
- W: Fitness of each genotype by cage (per-cage fitness measure).

## Data Provenance and Collection Methods
- Experimental design: Controlled crosses to produce all possible SR and ST male and female genotypes.
- Genotyping: Offspring were genotyped at adult eclosion to obtain observed genotype ratios for estimating selection against drive in both sexes.
- Processing: Processed data summarize raw data by cage and genotype, yielding one row per genotype per cage with aggregated counts and a fitness metric.

## Data Use and Analytical Potential
- Use raw data to reproduce genotype frequencies, mating designs, and per-offspring viability calculations.
- Use processed data to estimate genotype-specific fitness (W) and infer selection coefficients against the SR-drive in different sexes and conditions.
- Enables exploration of how diet (food condition) and cage-level factors affect genotype viability and observed fitness.

## Data Quality, Standards, and Governance Considerations
- Metadata completeness:
  - Clear field definitions and allowed values for Genotype, Food_Condition, and Cage_ID.
  - Note: NG and NA values indicate incomplete genotyping for certain offspring in the raw data; must be accounted for in analyses.
- Data standardization:
  - Consistent coding for food conditions (H, M, L) and genotype categories; ensure uniform interpretation across datasets and catalogues.
- Provenance and traceability:
  - Link raw and processed data via Cage_ID, Collection_Date, and Genotype to support end-to-end reproducibility.
- System and format considerations:
  - Two CSV files with related but distinct granularity; ensure data catalogues capture both raw and processed layers and their relationship.
- Update and curation:
  - Processed data is derived from raw data; any updates to raw data should propagate to the processed dataset with clear reconciliation of Tot_No, Geno_No, and W values.
- Accessibility and citation:
  - Data published with a peer-reviewed article; practitioners should cite the original publication and the dataset DOI when reused.
  - Primary contact for data questions: a.pomiankowski@ucl.ac.uk.

## Practical Considerations for Data Stewards
- Validate that Cage_ID uniquely identifies cage instances and remains stable across raw and processed files.
- Ensure that Genotype values are consistently encoded and that NG/NA flags are properly handled during analysis.
- Maintain clear mapping between Diet codes (H/M/L) and corresponding actual food conditions for reproducibility.
- Provide lineage information or processing scripts if possible to reproduce W (fitness) calculations from raw data.

## Access and Citation
- Source: Meiotic drive reduced egg-to-adult viability in stalk-eyed flies.
- Publication: Proc. R. Soc. B. 2019. DOI: 10.1098/rspb.2019.1414.
- Contact for data: a.pomiankowski@ucl.ac.uk