# 2015 juniper glasshouse germination metadata

## Overview
- Dataset arising from germination work on juniper seeds collected from 19 natural populations in 2015.
- Records population, family, weights (berries and seeds), viability testing results, and germination outcomes from a glasshouse experiment.
- Designed to enable estimation of viable seed numbers and germination rates, with data cleaned and structured for downstream analysis and self-service use.

## Dataset contents and structure
- Primary data file: Juniper_glasshouse_germination_data.csv
- Key data columns (examples):
  - Population, Family: identifiers for berry source population and maternal family
  - Weights: 10_berry_rep1/rep2/rep3, 10_viable_seeds_rep1/rep2/rep3, 10_nonviable_seeds_rep1/rep2/rep3
  - Means: Mean_weight_10_berries, Mean_berry_weight, Mean_weight_10_viable, Mean_viable_seed_weight, Mean_weight_10_nonviable, Mean_nonviable_seed_weight
  - Totals and estimates: Total_berry_collection_weight, Berry_number_estimate, Total_viable_collection_weight, Viable_seed_number_estimate, Total_nonviable_collection_weight, Nonviable_seed_number_estimate
  - Viability tests: Cut_test_viability_nonviable, Number_viable_in_nonviable
  - Recovered outputs: Seeds_per_berry, Viable_seeds_per_berry, Viable_nonviable_ratio, Viable_seeds_from_nonideal_berries, Total_viable_sown, Germination_rate
  - Subset indicators and NA entries to handle partial collections
- Supporting context: Table 1 lists population names and coordinates; Table 2 describes column headers, descriptions, and units.

## Methods and data processing
- Seed collection and tracking
  - 19 populations sampled in late summer/fall 2015; each berry tied to population and family.
  - Berries stored at 4°C; seeds extracted by hand.
  - Viability assessed by float test; 10 floating (presumed nonviable) seeds per family examined with cut test to estimate false-negative rate.
  - Germination rates derived from estimated viable seed numbers, accounting for viability outcomes and nonideal berries.
- Weight measurements and conversions
  - Weights recorded for 10 berries, 10 viable seeds, and 10 nonviable seeds, each in triplicate per family.
  - Weights averaged across replicates and converted to per-berry or per-seed estimates.
  - Used to estimate numbers of berries and seeds per family (berry_number_estimate, viable_seed_number_estimate, nonviable_seed_number_estimate).
- Sowing, stratification, and greenhouse handling
  - Seeds sown Dec 2015 in sand:compost, with warm stratification (Dec 2015–Mar 2016) and cold stratification (Mar 2016–Oct 2017) at 4°C.
  - Post-stratification growth in a greenhouse (Edinburgh).
  - Emergence began Oct 2016; continued until Aug 2018 when repotted.
- Data analysis context (for interpretation)
  - Data were analyzed in Minitab 2019; outliers checked with boxplots, Grubbs and Shapiro–Wilk tests.
  - Germination rates were right-skewed; log transformation applied to meet normality assumptions.
  - Nested general linear models used to test effects of region and population (families nested within populations, populations nested within regions); region and population treated as fixed effects.
  - Linear regressions tested relationships between berry/seed weights and germination, with the same nesting structure.

## Data quality, notes, and limitations
- Multiple replicates and cross-checks (float test and cut test) used to estimate viability and false negatives.
- Data include NA and Subset fields to reflect partial collections and varying data availability.
- Germination rates are analyzed after log transformation due to skewness observed across families.

## Potential data products and usage (for data support perspective)
- Self-serve dashboards or queries by: population, region, or family; seed/berry weight metrics; viability outcomes; and germination rates.
- Comparative analyses across regions (Scotland, Lake District, South England) to explore regional effects on germination.
- Data products to facilitate replication or meta-analysis: CSV extracts of weight metrics, viability estimates, and germination outcomes.
- Documentation and lineage tracing: link Table 1 (population metadata) and Table 2 (column descriptions) to the main dataset for clarity and auditability.

## File, provenance, and access
- File: Juniper_glasshouse_germination_data.csv
- Created: January 24, 2024 (Baker, J.)
- Analysis tool reference: Minitab 19 (Version 21.4.3) used for statistical processing.