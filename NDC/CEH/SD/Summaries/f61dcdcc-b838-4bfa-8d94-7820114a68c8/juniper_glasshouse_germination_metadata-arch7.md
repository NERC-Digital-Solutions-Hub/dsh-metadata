# 2015 juniper glasshouse germination metadata

## Overview
- A dataset detailing seed collection from 19 juniper populations in late summer/fall 2015 and subsequent glasshouse germination experiments (2016–2018) at UKCEH, Edinburgh.
- Includes seed weight measurements, viability assessments, and derived counts of viable/nonviable seeds and seeds per berry.
- One primary data file: Juniper_glasshouse_germination_data.csv, with supporting population metadata (locations and regions) described in Table 1 and column definitions in Table 2.
- Germination rates were analyzed statistically (log-transformed due to right-skew) using nested general linear models; data analysis performed in Minitab 19.

## Dataset and structure
- File: Juniper_glasshouse_germination_data.csv
- Key variables (examples):
  - Population, Family
  - 10_berry_rep1/rep2/rep3 (weight of 10 berries; grams)
  - Mean_weight_10_berries, Mean_berry_weight (average weights; grams)
  - Total_berry_collection_weight, Berry_number_estimate
  - 10_viable_seeds_rep1/rep2/rep3, Mean_weight_10_viable, Mean_viable_seed_weight
  - Total_viable_collection_weight, Viable_seed_number_estimate
  - 10_nonviable_seeds_rep1/rep2/rep3, Mean_weight_10_nonviable, Mean_nonviable_seed_weight
  - Total_nonviable_collection_weight, Nonviable_seed_number_estimate
  - Cut_test_viability_nonviable, Number_viable_in_nonviable
  - Seeds_per_berry, Viable_seeds_per_berry, Viable_nonviable_ratio
  - Viable_seeds_from_nonideal_berries, Total_viable_sown
  - Germination_rate
  - Subset (whether data are from entire collection or a subset)
- Table 1 provides population names, regions, and coordinates (latitude and longitude) for all sampled populations.
- Table 2 documents column headers, descriptions, and measurement units (including notes on replication and derived calculations).

## Geospatial components
- Population coordinates (lat/long) enable GIS mapping of sampling sites.
- Regions defined for analysis: Scotland, Lake District, and Southern England (S England).
- Population-level and regional aggregation can support spatial visualization of germination metrics.

## Key variables and GIS-relevant metrics
- Germination_rate by population/family (derived from viable seeds that germinated).
- Viable_seed_number_estimate, Nonviable_seed_number_estimate, Seeds_per_berry, Viable_seeds_per_berry, and Viable_nonviable_ratio for spatial comparison of seed quality.
- Mean_berry_weight and Mean_weight_10_berries provide physical trait mapping across sites.
- Subset flag indicates whether data come from entire berry collections or subsets, useful for filtering in GIS workflows.

## Data processing and analysis
- Outlier checks and distribution assessments performed in Minitab 19.
- Germination rates exhibited right-skew; log transformation applied for normality prior to analysis.
- Statistical approach: Nested general linear models with:
  - Families nested in populations
  - Populations nested in regions
  - Regions and populations as fixed effects
  - Linear regressions to test relationships between berry/seed weights and germination rates

## Practical GIS use cases
- Visualize spatial distribution of germination rates across 19 populations.
- Create choropleth or point maps of derived metrics (e.g., seeds per berry, viable seed counts) by population.
- Overlay regional boundaries to compare Scotland, Lake District, and S England trends.
- Link CSV data to population coordinates to produce GIS layers for ecological or conservation planning.

## Limitations and considerations for GIS
- Data are greenhouse-based and may not reflect natural field germination conditions.
- Text includes some typographical inconsistencies (e.g., spacing in labels) that should be resolved by inspecting the CSV/Table 2 definitions.
- Derived metrics depend on replicate measurements and averaging; ensure transparent aggregation in GIS analyses.
- Temporal aspects are limited to collection and stratification timelines; the primary GIS use is spatial associations rather than time-series analysis.

## Provenance and access
- Source: 2015 juniper glasshouse germination metadata.
- Created: 24/1/2024 by J. Baker.
- Dataset analyzed with Minitab 19; includes detailed methodology for seed viability, weight calculations, and germination assessment.