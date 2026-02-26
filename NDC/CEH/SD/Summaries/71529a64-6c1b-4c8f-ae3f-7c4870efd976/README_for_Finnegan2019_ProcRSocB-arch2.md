# Meiotic drive reduced egg-to-adult viability in stalk-eyed flies.

## Overview
- Presents data from a genetic experiment testing if the SR-drive chromosome reduces egg-to-adult viability in Teleopsis dalmanni and whether fitness effects are recessive or sex-limited.
- Data support estimating selection coefficients against drive in both sexes.

## Data files included
- Egg-to-adult_viability_raw_data.csv: raw offspring data with individual records.
- Egg-to-adult_viability_processed_data.csv: aggregated data summarised by genotype and cage.

## Experimental design
- Controlled crosses to produce eggs with all possible SR and ST male and female genotypes.
- Offspring were genotyped at adult eclosion to obtain observed genotype ratios used to estimate selection against drive.
  
## Raw data structure (Egg-to-adult_viability_raw_data.csv)
- ID: Unique offspring identifier.
- Sex: Offspring sex.
- Food_Condition: Egg-laying food treatment (H = 75% corn, M = 50% corn, L = 25% corn).
- Genotype: Offspring genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) determined by microsatellite marker comp162710; NG = not genotyped, NA = not amplified.
- Collection_Date: Date eggs were collected.
- Cage: Cage ID (nested within collection date).

## Processed data structure (Egg-to-adult_viability_processed_data.csv)
- Cage_ID: Unique cage identifier.
- Food_condition: Food treatment for eggs in the cage.
- Collection_Date: Date eggs were collected.
- Tot_No: Total offspring in the cage.
- F_No: Total females in the cage.
- M_No: Total males in the cage.
- Males_Genod: Males genotyped in the cage.
- Females_Genod: Females genotyped in the cage.
- Geno_No: Total offspring genotyped in the cage.
- Sex: Sex of the genotype entry.
- Genotype: Genotype (X/X, SR/X, SR/SR, ST/Y, SR/Y) as designated by marker comp162710.
- W: Fitness estimate for each genotype within the cage.

## Data provenance and quality
- Sourced from the study by Finnegan et al. 2019 (Meiotic drive reduced egg-to-adult viability in stalk-eyed flies).
- Data include explicit identifiers, standardised categorical fields (food condition, genotype), and per-cage fitness values.
- Uses microsatellite marker-based genotype designation and notes on incomplete genotyping (NG/NA).

## Relevance for environmental monitoring and analysis
- Demonstrates how genotype- and environment-related fitness (via food condition) can be captured in a consistent dataset.
- Enables calculation of selection coefficients against drive across sexes and environmental conditions.
- Structured to support data quality assurance, reproducibility, and re-use alongside other datasets or environmental metadata.

## Data use and sharing considerations
- Clear, per-cage aggregation facilitates integration with broader environmental datasets.
- Standardised formats and metadata support accessibility and potential uploading to data portals.