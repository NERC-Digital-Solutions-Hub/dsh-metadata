# 2015 juniper glasshouse germination metadata

## Overview
- A dataset describing juniper seed germination from 19 natural populations collected in 2015, processed under controlled greenhouse conditions at UKCEH Edinburgh.
- Includes seed viability assessments, seed and berry weight measurements, propagation details, and germination outcomes used to explore region/population effects and weight correlations.

## Seed collection and viability assessment
- Seed sources: 19 natural populations, with population and family assignments for each berry.
- Processing: berries stored at 4°C, seeds extracted by hand.
- Viability testing:
  - Float test to identify nonviable (float) seeds.
  - Cut test on 10 floating seeds per family to estimate false-negative rate.
  - Germination calculations based on estimated viable seed counts, accounting for false negatives.
- Sowing strategy: both viable and nonviable seeds were sown to account for false negatives, but germination analyses used the estimated number of viable seeds.
- Population details: table lists full names, abbreviations, and geographic coordinates.

## Weight and seed estimation
- Measurements: weight of 10 berries, 10 viable seeds, and 10 nonviable seeds recorded as triplicates.
- Derived metrics (per family):
  - Mean weights: 10 berries, 10 viable seeds, 10 nonviable seeds.
  - Mean weights converted to per-item weights (berry weight, viable seed weight, nonviable seed weight).
  - Estimates of total counts: total weights yield estimated number of berries, viable seeds, and nonviable seeds.
  - Seed counts per berry: viable seeds per berry, nonviable seeds per berry, and the viable/nonviable ratio.
  - Viable seeds recovered from non-ideal berries and total viable seeds sown.
  - Germination rate calculated as the proportion of viable seeds that germinated.

## Sowing, stratification, and germination timeline
- Sowing: December 2015 in a 1:1 sand:compost mix.
- Stratification:
  - Warm stratification: December 2015–March 2016 (7.3–14.3°C).
  - Cold stratification: March 2016–October 2017 (4°C).
- Post-stratification: seed trays moved to greenhouse at UKCEH.
- Emergence: first emergence observed October 2016; continued through August 2018 when all remaining plants were potted.

## Dataset structure and contents
- File: Juniper_glasshouse_germination_data.csv
- Table 2 columns (summary of key fields):
  - Population: berry source population abbreviation.
  - Family: numeric family identifier.
  - 10_berry_rep1/rep2/rep3: weight of 10 berries (grams) in each replicate.
  - Mean_weight_10_berries: mean weight of 10 berries across replicates (grams).
  - Mean_berry_weight: estimated weight of a single berry (grams).
  - Total_berry_collection_weight: total weight of all collected berries (grams).
  - Berry_number_estimate: estimated number of berries (counts).
  - 10_viable_seeds_rep1/rep2/rep3: dry weight of 10 viable seeds (grams) per replicate.
  - Mean_weight_10_viable: mean weight of 10 viable seeds (grams).
  - Mean_viable_seed_weight: estimated weight of a single viable seed (grams).
  - Total_viable_collection_weight (and corresponding Viable_seed_number_estimate): total viable seed weight and estimated seed count.
  - 10_nonviable_seeds_rep1/rep2/rep3: dry weight of 10 nonviable seeds (grams) per replicate.
  - Mean_weight_10_nonviable: mean weight of 10 nonviable seeds (grams).
  - Mean_nonviable_seed_weight: estimated weight of a single nonviable seed (grams).
  - Total_nonviable_collection_weight: total weight of nonviable seeds (grams).
  - Nonviable_seed_number_estimate: estimated nonviable seed count.
  - Cut_test_viability_nonviable: number of seeds deemed viable by cut test among floated seeds.
  - Number_viable_in_nonviable: estimated viable seeds among nonviable seeds.
  - Seeds_per_berry: total viable seeds per berry.
  - Viable_seeds_per_berry: viable seeds per berry (ratio/integer).
  - Viable_nonviable_ratio: ratio of viable to nonviable seeds.
  - Viable_seeds_from_nonideal_berries: viable seeds recovered from shriveled/older berries.
  - Total_viable_sown: total number of viable seeds sown.
  - Germination_rate: proportion of viable seeds that germinated.

## Data processing and analysis
- Software: Mintab 2019 (Minitab 19, 2024).
- Data checks:
  - Box plots to identify extreme outliers.
  - Grubbs outlier test and Shapiro-Wilk normality test.
- Transformation and modeling:
  - Germination rates were right-skewed; applied log transformation to achieve normality (log-transformed germination rates distributed normally, p = 0.093).
  - All subsequent analyses used log-transformed germination rates.
  - Nested general linear models:
    - Regions (South England, Lake District, Scotland) defined based on neutral-marker genetics and geographic distribution.
    - Random effects: family nested within population.
    - Fixed effects: population nested within region, and region as a fixed effect.
  - Linear regression tested relationships between germination and berry/viable seed weights within the same nested structure.

## Key notes and interpretation guidance
- The study emphasizes careful handling of viability estimates, accounting for false negatives via the cut test.
- Data are structured to enable analysis of regional and population-level differences in germination, as well as the influence of seed/berry weight on germination.
- Results reported in this document focus on data processing and modeling approach; germination results were found to be log-normally distributed after transformation and analyzed accordingly.