# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies

## Overview
- Study aim: Test whether the SR-drive chromosome in Teleopsis dalmanni reduces egg-to-adult viability and whether fitness effects are recessive or sex-limited.
- Experimental design: Controlled crosses to produce eggs with all SR and ST male and female genotypes; offspring were genotyped at adult eclosion to estimate selection coefficients against drive in both sexes.
- Data format: Provided as two CSV files—raw data and processed data.

## Data assets
- Egg-to-adult_viability_raw_data.csv: Offspring-level data from the experiment.
- Egg-to-adult_viability_processed_data.csv: Cage- and genotype-level summaries derived from the raw data.

## Data structure and content

### Raw data (Egg-to-adult_viability_raw_data.csv)
- ID: Unique offspring identifier.
- Sex: Offspring sex.
- Food_Condition: Food treatment during egg lay (H = 75% corn, M = 50% corn, L = 25% corn).
- Genotype: Offspring genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) designated by microsatellite marker comp162710; NG = not genotyped; NA = not amplified.
- Collection_Date: Date eggs were collected.
- Cage: Cage ID number, nested within collection date.

### Processed data (Egg-to-adult_viability_processed_data.csv)
- Cage_ID: Unique cage identifier.
- Food_condition: Food treatment during egg lays in the cage (H, M, L).
- Collection_Date: Date eggs were collected.
- Tot_No: Total number of offspring collected from a cage.
- F_No: Total number of females collected from a cage.
- M_No: Total number of males collected from a cage.
- Males_Genod: Total number of males genotyped from a cage.
- Females_Genod: Total number of females genotyped from a cage.
- Geno_No: Total number of offspring genotyped from a cage.
- Sex: Sex of the genotype.
- Genotype: Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) designated by marker comp162710.
- W: Fitness of each genotype, by cage.

## Key variables and coding
- Genotype categories include X/X, SR/X, SR/SR, ST/Y, SR/Y, with genotype designation tied to a microsatellite marker (comp162710).
- NG indicates offspring not genotyped; NA indicates not amplified.
- W represents genotype-specific fitness estimates at the cage level.

## Data quality and limitations
- Raw data provide per-offspring records; processed data summarize by genotype and cage.
- Potential gaps include incomplete genotyping (Geno_No vs Tot_No) and missing or unbalanced counts by cage or sex.
- Aggregation in processed data is one row per genotype per cage, enabling per-cage fitness analyses but requiring careful handling of unequal genotype sampling across cages.

## Implications for data strategy and use
- Supports replication and re-analysis to estimate selection coefficients against the drive in both sexes.
- Enables assessment of how experimental design (crossing scheme, genotyping, and feeding conditions) affects viability outcomes.
- Useful for planning data collection and metadata standards in future studies, ensuring clear linkage between raw offspring data and cage-level summaries.
- Highlights the importance of documenting data provenance (raw to processed transformation) and metadata completeness (dates, cage IDs, food conditions) to improve discoverability and re-use.