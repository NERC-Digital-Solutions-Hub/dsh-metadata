# Notes on the downloadable data

## Overview
- The Countryside Survey (CS) data are sourced from a sample of 1 km squares in Great Britain, with measurements at two levels: whole squares and within-square features.
- Locations of CS survey squares are kept confidential to preserve representativeness; external users cannot pinpoint square locations to better than 100 square kilometers.
- Data include a mix of binary and continuous measurements (e.g., quadrats, vegetation, soils).

## Data structure and sampling
- CS field survey data comprise measurements collected from selected squares and within-square features, enabling both square-level and within-square characterisation.
- The sampling is stratified, not a simple random subsample, using the ITE Land Classification. Country-specific classifications have evolved (England 21 classes, Wales 8, Scotland 16; total changed from 32 to 42 to 45 over time).
- Analyses must account for stratification; estimates ignoring stratification may be biased and misrepresent variation.

## Coverage and representativeness
- Not all GB squares were surveyed: squares with more than 90% sea or more than 75% urban area were excluded from field surveys.
- Official GB/regional estimates assume excluded squares have similar vegetative land composition to sampled squares; this assumption introduces minimal bias unless a region contains a high proportion of sea/urban areas.

## Estimation method
- Estimates are produced using ratio estimates for each land class, incorporating the area of vegetative land within each sample square.
- Land-class Estimates are then combined using weights equal to the vegetative land area of each class across the whole area.
- Since 1998, to address skewness in some features, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani, 1993).

## Implications for data use
- When analysing CS data, consider the stratified sampling design and apply land-class weights.
- Use bootstrap-based confidence intervals for uncertainty where appropriate.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.