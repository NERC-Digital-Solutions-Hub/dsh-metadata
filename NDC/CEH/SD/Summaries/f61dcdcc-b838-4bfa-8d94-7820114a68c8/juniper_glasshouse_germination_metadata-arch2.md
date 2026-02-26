# 2015 juniper glasshouse germination metadata

## Overview
- Metadata and methodology describing germination and viability testing of Juniper seeds collected from 19 natural populations in 2015.
- Data processed to derive estimates (e.g., berry weights, seed weights, viable/nonviable seed counts) and to analyze germination with respect to region and population.
- Data intended to support standardized environmental monitoring and policy-relevant insights about juniper viability and propagation potential.

## Data collection and provenance
- Seed source: 19 natural populations across Scotland and England, with population abbreviations and geographic coordinates recorded (Table 1).
- Family structure: seeds grouped by population, family (same maternal tree or open-pollinated half-siblings).
- Viability assessment: float test to identify potentially nonviable seeds, followed by cut test on 10 floating seeds per family to estimate false-negative rate.
- Data capture: both viable and nonviable seeds collected and germination tracked; viability estimates used to compute viable seed counts.
- Documentation: dataset described in detail with column definitions, units, and calculation steps (Table 2).

## Sowing and stratification procedures
- Sowing: December 2015 in seed trays using a 1:1 sand:compost mix.
- Stratification: warm stratification (Dec 2015–Mar 2016) at 7.3–14.3°C, then cold stratification (Mar 2016–Oct 2017) at 4°C.
- Growing environment: greenhouse at UKCEH, Edinburgh; emergence began Oct 2016 and continued through Aug 2018.
- Purpose: generate germination data across populations under controlled conditions to support comparative analyses.

## Dataset content and key variables
- File: Juniper_glasshouse_germination_data.csv (one dataset file).
- Core variables (examples):
  - Population, Family identifiers; 10_berry_rep1/rep2/rep3 (weights of 10 berries; grams)
  - Mean_weight_10_berries; Mean_berry_weight (weight of a single berry)
  - Total_berry_collection_weight; Berry_number_estimate
  - 10_viable_seeds_rep1/rep2/rep3; Mean_weight_10_viable; Mean_viable_seed_weight
  - Total_viable_collection_weight; Viable_seed_number_estimate
  - 10_nonviable_seeds_rep1/rep2/rep3; Mean_weight_10_nonviable; Mean_nonviable_seed_weight
  - Total_nonviable_collection_weight; Nonviable_seed_number_estimate
  - Cut_test_viability_nonviable; Number_viable_in_nonviable
  - Seeds_per_berry; Viable_seeds_per_berry; Viable_nonviable_ratio
  - Viable_seeds_from_nonideal_berries; Total_viable_sown; Germination_rate
- Units include grams for weights, counts for seed numbers, and proportions for germination rates.

## Data processing and quality assurance
- Wastewater-style QA not applicable; implemented seed-level QA through viability testing and replication.
- Calculations derived from replicated measurements: averaging across three replicates for berries, viable seeds, and nonviable seeds.
- Derived metrics include estimated berry counts, viable/nonviable seed counts, seeds per berry, and germination rate.
- Data provenance notes: explicit descriptions of how each derived column was computed (e.g., using mean weights to estimate totals and counts).

## Analysis approach
- Software: Minitab 19 (Mintab 2019).
- Data exploration: box plots to identify extreme outliers; Grubbs tests and Shapiro–Wilk tests for normality; observed germination rates were heavily right-skewed.
- Data transformation: log transformation of germination rates to achieve near-normal distribution (p ≈ 0.093 for log-transformed data).
- Statistical models: nested general linear models to assess region and population differences, with:
  - Random effects: family nested in population
  - Fixed effects: region and population (regions defined as Southern England, Lake District, Scotland)
  - Additional analyses: linear regression to test relationships between berry/viable seed weights and germination rates, using the same nesting structure.

## Data access and stewardship
- The dataset is structured for storage and upload to appropriate data portals in environmental monitoring contexts.
- Emphasis on making underlying data accessible to support transparency, re-use, and monitoring across time.

## Key takeaways for monitoring and policy
- Standardised collection and processing steps enable cross-population comparisons of germination and viability.
- Viability estimation includes correction for false negatives via a cut test, improving accuracy of viable seed counts.
- Germination analyses account for non-normal distributions by applying log transformations and using hierarchical models to partition variance by region, population, and family.
- The dataset supports ongoing monitoring of juniper propagation potential across regions, informing conservation and restoration planning; highlights the importance of linking raw observation data with derived metrics to enable broader data reuse and policy scrutiny.