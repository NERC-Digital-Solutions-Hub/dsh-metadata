# 2015 juniper glasshouse germination metadata

## Overview
- Metadata and dataset describing juniper seed germination from 19 natural populations collected in 2015.
- Includes methods for seed viability assessment (float test, cut test) and adjustments for false negatives.
- Sowing, stratification, and greenhouse growth described; dataset comprises a single file: Juniper_glasshouse_germination_data.csv.

## Provenance and collection details
- Seed source: berries collected from 19 populations, with population and family identifiers recorded.
- Population data include abbreviations and geographic coordinates (Table 1).
- Storage and processing: berries stored at 4°C; seeds extracted by hand; viability assessed via float test; false-negative correction using cut test on a subset.
- Post-collection handling: seeds sown in December 2015; stratification phases (warm Dec 2015–Mar 2016; cold Mar 2016–Oct 2017) followed by greenhouse growth in Edinburgh.
- Emergence observed from Oct 2016 to Aug 2018; plants eventually potted up.

## Dataset structure and metadata details
- File: Juniper_glasshouse_germination_data.csv.
- Key columns and data types:
  - Population, Family: identifiers for berry source and maternal lineage.
  - 10_berry_rep1 to 10_berry_rep3: weights of 10 berries (grams), replicates.
  - Mean_weight_10_berries: mean berry weight (grams).
  - Mean_berry_weight: estimated weight of a single berry (grams).
  - Total_berry_collection_weight: total weight of berries collected (grams).
  - Berry_number_estimate: estimated number of berries (count).
  - 10_viable_seeds_rep1 to rep3; Mean_weight_10_viable; Mean_viable_seed_weight; Total_viable_collection_weight; Viable_seed_number_estimate (count).
  - 10_nonviable_seeds_rep1 to rep3; Mean_weight_10_nonviable; Mean_nonviable_seed_weight; Total_nonviable_collection_weight; Nonviable_seed_number_estimate (count).
  - Cut_test_viability_nonviable: number of nonviable seeds deemed viable by cut test (NA for some entries).
  - Number_viable_in_nonviable: estimated viable seeds among nonviable fraction.
  - Seeds_per_berry, Viable_seeds_per_berry, Viable_nonviable_ratio: derived metrics.
  - Viable_seeds_from_nonideal_berries: viable seeds recovered from non-ideal berries.
  - Total_viable_sown: total viable seeds sown.
  - Germination_rate: proportion of viable seeds that germinated.
- Derived calculations rely on weight-based estimates to infer counts (e.g., viable/nonviable seed counts, berries per collection).
- Units: grams for weights; counts for numbers; NA where not applicable.

## Data processing, quality assurance, and analysis
- Data quality checks: outlier screening via box plots, Grubbs tests, and Shapiro-Wilk normality tests.
- Distribution: germination rates highly right-skewed; log transformation applied to normalize for analyses.
- Statistical approach: nested general linear models to test region, population, and family effects (regions nested within and populations nested within regions; families nested within populations); random effects for families; fixed effects for populations and regions.
- Additional analyses: linear regressions to examine relationships between berry/seed weights and germination, using the same nesting structure.
- Software: Mintab 2019 (Minitab 19).

## Data availability and sharing considerations
- Dataset comprises a single file with both raw measurements and derived metrics.
- Comprehensive metadata included to enable reuse, replication, and downstream analyses (e.g., germination expectations by region/population, and relationships with seed/berry weights).
- Clear lineage from field collection to laboratory processing to statistical analysis, supporting data provenance and reproducibility.

## Governance, stewardship considerations, and recommendations
- Ensure metadata completeness and consistency across related datasets (clear definitions for all columns and units).
- Maintain explicit data provenance: link population abbreviations to full names and coordinates (Table 1 reference).
- Preserve data lineage: document all transformation steps used to derive counts (e.g., Berry_number_estimate, Seed counts from weights).
- Establish data versioning and a stable storage location or repository to support discoverability and long-term access.
- Consider providing accompanying data dictionary and code/scripts used for calculations and analyses to enhance reproducibility.
- Monitor and document any updates or corrections to measurements (e.g., handling NA values for certain test results).