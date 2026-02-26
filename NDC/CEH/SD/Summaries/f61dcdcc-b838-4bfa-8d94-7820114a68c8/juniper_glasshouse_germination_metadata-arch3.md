# 2015 juniper glasshouse germination metadata

## Overview
- Describes collection, processing, and analysis of juniper seed germination data to derive environmental health measures and indicators for monitoring policy impacts.
- Focuses on viability assessment, seed weights, counts, and germination outcomes across multiple natural populations.

## Sampling and seed collection
- Collected berries from 19 natural juniper populations in late summer/fall 2015; populations are stands, families are berries from the same maternal tree or open-pollinated half-siblings.
- Berries stored at 4°C until processing; seeds extracted by hand.
- Viability assessed with a float test; nonviable seeds (floaters) verified with a cut test on 10 floating seeds per family to estimate false-negative rate.
- Both viable and nonviable seeds were sowed to account for false negatives; germination rates based on estimated viable seeds.
- Table 1 lists population names, abbreviations, regions, and geographic coordinates.

## Laboratory processing and viability testing
- Weight measurements obtained for 10 berries, 10 viable seeds, and 10 nonviable seeds; three replicates per family, averaged to estimate per-unit weights.
- Estimated numbers for berries and seeds derived by dividing total weights by mean unit weights (for berries, viable seeds, and nonviable seeds).
- Sowing and stratification:
  - Seeds sown in December 2015 in a 1:1 sand:compost mix.
  - Warm stratification (Dec 2015–Mar 2016) at 7.3–14.3°C, then cold stratification (Mar 2016–Oct 2017) at 4°C.
  - Post-stratification, trays moved to greenhouse; first emergence in Oct 2016, continuing through Aug 2018.
- The dataset captures germination outcomes during greenhouse conditions.

## Dataset content and structure
- Single data file: Juniper_glasshouse_germination_data.csv.
- Key columns (examples):
  - Population, Family: identifiers for origin population and maternal family.
  - 10_berry_rep1/rep2/rep3, Mean_weight_10_berries: weights of berries (grams).
  - Berry_number_estimate, Total_berry_collection_weight: estimates and totals for berries.
  - 10_viable_seeds_rep1/rep2/rep3, Mean_weight_10_viable, Mean_viable_seed_weight: weights for viable seeds.
  - Total_viable_collection_weight, Viable_seed_number_estimate: counts of viable seeds.
  - 10_nonviable_seeds_rep1/rep2/rep3, Mean_weight_10_nonviable, Mean_nonviable_seed_weight: weights for nonviable seeds.
  - Total_nonviable_collection_weight, Nonviable_seed_number_estimate: counts of nonviable seeds.
  - Cut_test_viability_nonviable, Number_viable_in_nonviable: outcomes from cut test and estimated viable seeds among floating nonviables.
  - Seeds_per_berry, Viable_seeds_per_berry, Viable_nonviable_ratio: derived seed metrics per berry.
  - Viable_seeds_from_nonideal_berries: viable seeds recovered from non-ideal berries.
  - Total_viable_sown: total viable seeds sown.
  - Germination_rate: proportion of viable seeds that germinated.
- Units are specified for weight measures (grams) and counts are in integers.

## Data processing and derived metrics
- Weights and counts are averaged across three replicates to obtain per-unit estimates (berries and seeds).
- Derived metrics include:
  - Berry_number_estimate and Seed counts derived from weights and mean seed weights.
  - Viable_seed_number_estimate and Nonviable_seed_number_estimate from respective total weights and mean seed weights.
  - Seeds_per_berry, Viable_seeds_per_berry, and Viable_nonviable_ratio.
  - Viable_seeds_from_nonideal_berries to account for imperfect fruit material.
  - Total_viable_sown aggregates viable seeds across sources.
  - Germination_rate computed from viable seeds that germinated during the experiment.

## Analysis approach and modeling
- Software: Minitab 2019 (Version 21.4.3).
- Data quality checks:
  - Box plots to identify extreme outliers.
  - Grubbs outlier tests and Shapiro-Wilk normality tests.
  - Germination rates were right-skewed; applied log transformation to normalize (log-transformed germination rates distributed normally, p = 0.093).
- Statistical models:
  - Nested general linear models to evaluate regional and population differences.
  - Regions defined as Southern England, Lake District, and Scotland.
  - Random effects: families nested in populations; populations nested in regions.
  - Fixed effects: populations and regions.
  - Linear regressions to test relationships between berry/seed weights and germination rates, using the same nesting structure.

## Data quality, provenance, and governance notes
- Metadata present via:
  - Table 1: population names, abbreviations, regions, and coordinates.
  - Table 2: detailed column headers, descriptions, and measurement units (for transparency and reproducibility).
- Methodology is described in detail, enabling traceability from raw berries to final germination metrics.
- Data sharing considerations are not explicitly stated; the dataset emphasizes transparency of measurements, replicates, and processing steps to support reproducibility and future monitoring use.