# Notes on the downloadable data

## Overview
- The document describes how Countryside Survey (CS) data are collected, stored, and used, with attention to representativeness, privacy, and statistical methods.
- It emphasizes the two-level sampling (whole 1 km squares and within-square measurements), the stratified design, and the need for appropriate analysis to avoid biased inferences.

## Privacy and representativeness
- Precise locations of CS survey squares are confidential to preserve representativeness; external users cannot identify squares with precision finer than 100 square km.
- This confidentiality limits locating whether specific squares fall within defined areas.

## Sampling design and data structure
- Field data come from a sample of GB 1 km squares; each square is mapped and measured at the square level and within-square level (e.g., quadrats for vegetation, soils, etc.).
- Measurements include both binary and continuous variables (e.g., areas, lengths).
- The sample is not a random subset; it is stratified within designated land classification strata defined by the ITE Land Classification.
- Land Classification classifications have evolved: originally 32 classes, then 42 (1998) for Scotland, and 45 (2007) for Wales; England, Wales, and Scotland have country-specific classifications.

## Exclusions and regional implications
- Squares with >90% sea or >75% urban area were excluded from field surveys.
- Official GB estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally negligible unless a region contains a high proportion of sea or urban squares.

## Estimation methods and uncertainty
- Estimates by land class are produced using ratio estimation techniques that account for the area of vegetative land within each class.
- Land-class estimates are combined using weights equal to the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals are estimated with bootstrap methods due to skewness in some features.

## Data quality, usage, and implications for analysis
- Analysts must account for stratification; ignoring it can lead to non-representative estimates and incorrect variation.
- The sampling design and exclusions constrain how results can be generalized to the whole GB and to regional contexts.

## Metadata, provenance, and references
- References include Barr et al. (1993) for the 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on the bootstrap.

## Takeaways for data leadership and governance
- Privacy constraints and precision limits should be documented as part of data governance.
- Analytic workflows must incorporate stratification, weighting by vegetative land area, and bootstrap-derived uncertainty.
- Be aware of non-random, stratified sampling and regional exclusions when planning analyses, reporting, and data product development.
- Maintain clear metadata on land classifications, their country-specific variants, and updates to classifications across time.