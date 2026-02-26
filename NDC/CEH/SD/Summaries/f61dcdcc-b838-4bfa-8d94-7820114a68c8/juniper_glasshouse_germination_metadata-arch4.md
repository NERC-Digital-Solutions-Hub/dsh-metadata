# 2015 juniper glasshouse germination metadata

## Overview
- Dataset documenting juniper seed germination from 19 natural populations collected in 2015.
- Includes viability assessment, seed/berry weight metrics, and germination outcomes from a glasshouse experiment.
- Data collection period spans 2015 (collection) to 2018 (germination observations); metadata created 24/1/24 by J. Baker.
- File provided: Juniper_glasshouse_germination_data.csv.

## Data collection and sample design
- Population-level sampling: 19 named populations across Scotland, England/Lake District, with explicit latitude/longitude coordinates (Table 1).
- Family structure: seeds collected from maternal trees, with family identifiers; berries stored at 4°C before processing.
- Viability assessment: float test to classify seeds as viable/nonviable, supplemented by cut test on 10 floating seeds per family to estimate false-negative rate.
- Experimental handling: both viable and nonviable seeds sown to account for float-test errors; germination rates based on estimated viable seeds.
- Sowing/stratification timeline: warm stratification (Dec 2015–Mar 2016) followed by cold stratification (Mar 2016–Oct 2017) at 4°C, then greenhouse growth (Edinburgh) with emergence from Oct 2016 to Aug 2018.

## Dataset structure and key variables
- One main file: Juniper_glasshouse_germination_data.csv.
- Core columns and derived metrics (examples):
  - Population, Family: identifiers linking to Table 1 (population abbreviations, maternal tree/family).
  - 10_berry_rep1/rep2/rep3: dry weight of 10 berries (grams) per replicate.
  - Mean_weight_10_berries: average berry weight across replicates.
  - Mean_berry_weight: estimated weight of a single berry.
  - Total_berry_collection_weight: total weight of all collected berries for the subset analyzed.
  - Berry_number_estimate: estimated number of berries from the total weight.
  - 10_viable_seeds_rep1/rep2/rep3: dry weight of 10 viable seeds per replicate.
  - Mean_weight_10_viable, Mean_viable_seed_weight: average viable seed weights; mean per-seed weight.
  - Total_viable_collection_weight: total weight of viable seeds extracted.
  - Viable_seed_number_estimate: estimated number of viable seeds extracted.
  - 10_nonviable_seeds_rep1/rep2/rep3: dry weight of 10 nonviable seeds per replicate.
  - Mean_weight_10_nonviable, Mean_nonviable_seed_weight: average nonviable seed weights.
  - Total_nonviable_collection_weight: total weight of nonviable seeds extracted.
  - Nonviable_seed_number_estimate: estimated number of nonviable seeds.
  - Cut_test_viability_nonviable: number of seeds considered viable based on the cut test among floating seeds.
  - Number_viable_in_nonviable: estimated viable seeds among nonviable seeds.
  - Seeds_per_berry, Viable_seeds_per_berry: derived counts per berry.
  - Viable_nonviable_ratio: ratio of viable to nonviable seeds.
  - Viable_seeds_from_nonideal_berries: viable seeds recovered from ripened/less-ripe berries.
  - Total_viable_sown: sum of viable seeds sown (including corrections).
  - Germination_rate: proportion of viable seeds that germinated.
- Data processing details: three replicates per measurement, averages computed, and various derived metrics calculated to support germination analysis.

## Data analysis approach
- Software: Minitab 19 (Mintab 2019) used for analysis.
- Exploratory checks: box plots for germination rates and seed weights; Grubbs outlier tests; Shapiro-Wilks normality tests.
- Transformation: germination rates were right-skewed; log transformation applied to achieve normality (log-transformed rates used in further analyses; p = 0.093 for normality test).
- Modeling: nested general linear models to compare regions and populations; random effects for family nested in population, population nested in region; fixed effects for region and population as appropriate.
- Additional analyses: linear regressions to examine relationships between berry/seed weights and germination rates using the same nesting structure.
- Data provenance for analysis remains tied to the provided column definitions and derivations (Table 2 describes column headers, descriptions, and units).

## Data quality and governance
- Viability estimation acknowledges potential false negatives in float tests; the cut test provides an estimate of this error per family.
- Data include explicit replication, averaging, and derived metrics to support robust interpretation of germination outcomes.
- Metadata encompasses population coordinates, sampling design, and processing steps to aid discoverability and reuse.

## Availability and provenance
- Created by J. Baker; metadata/document created 24 January 2024.
- Cited data analysis tool: Minitab 19; provides version details in references.
- Documentation includes tables listing population details (Table 1) and detailed column descriptions (Table 2) for traceability and reuse.

## Relevance for data leaders
- Strengths:
  - Comprehensive metadata, including population structure, replication, and processing steps.
  - Clear provenance and derived metrics enabling cross-population germination analyses.
  - Nested modeling approach aligns with hierarchical data structures common in ecological datasets.
- Considerations for future data strategy:
  - Potential data standardization needs across similar datasets (e.g., consistent viability testing metadata).
  - Managing uncertainties in viability estimates due to float-test limitations (documented via Cut_test_viability_nonviable).
  - Ensuring discoverability by maintaining detailed column definitions and population mappings (Table 2 and Table 1 references).