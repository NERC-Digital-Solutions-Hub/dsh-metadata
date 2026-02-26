# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify square locations with precision finer than 100 square km.

## Sampling design
- CS field survey data come from a sample of 1 km squares across Great Britain, with measurements at two levels: whole squares and within-square features.
- The sampling is stratified rather than random, using the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). The classification has evolved (32 → 42 → 45 classes) for country reporting purposes.
- Not all GB squares are surveyed: squares more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded.
- Estimates are derived using ratio estimates by land class, weighting by the vegetative land area within each land class.

## Representativeness and bias
- Official GB or regional estimates assume excluded squares have vegetative land compositions similar to sampled squares; bias is generally considered negligible unless a region has a high proportion of sea or urban squares.

## Estimation and uncertainty
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods to address skewness in some features.

## Data governance considerations for data leaders
- Metadata and documentation detail stratification, land classes, and weighting schemes essential for correct analysis and interpretation.
- Analyses must account for the stratified sampling design and use ratio estimates with appropriate weights to avoid biased conclusions.
- Access constraints (location confidentiality) should be considered when planning spatial analyses or data sharing.

## References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Cochran (1963). Sampling Techniques.
- Efron & Tibshirani (1993). An Introduction to the Bootstrap.