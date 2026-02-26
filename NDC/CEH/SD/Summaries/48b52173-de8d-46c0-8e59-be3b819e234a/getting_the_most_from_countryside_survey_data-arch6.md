# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify exact squares to better than 100 square km.
- CS Field Survey data come from a sample of 1 km squares across Great Britain, with measurements at two levels: the whole square and within-square, covering a variety of data types (binary to continuous).

## Sampling design and representativeness
- The sample is not a random subset of all GB squares; it is stratified by Land Classification (ITE). Country-specific classifications are used: England (21 classes), Wales (8), Scotland (16); classifications have evolved from 32 to 42 to 45 classes due to separate country reporting.
- Not all GB squares were surveyed: squares more than 90% sea or more than 75% urban were excluded. Estimates for GB or regions assume excluded vegetative land is similar in composition to sampled squares; bias is generally small except in regions with high sea/urban proportions.
- Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area within each land class.

## Estimation and uncertainty
- Since 1998, standard errors and confidence intervals are estimated using bootstrapping (Efron & Tibshirani, 1993) due to concerns about skewness in some features.

## Data usage considerations for analysis
- Analyses must account for the stratified sampling design and area-weighted estimation to avoid biased inferences.
- Be mindful of potential biases if region-specific composition differs between included and excluded squares, particularly in areas with substantial sea or urban land.

## Practical implications for data support
- The confidentiality of precise locations limits pinpoint-level analyses; users should work with area- or class-level data and explain the sampling design when sharing outputs.
- When aggregating to regional scales or communicating results, recognize the reliance on ratio estimates and bootstrap-based uncertainty measures.
- Encourage end users to understand the stratification and weighting to improve data interpretation and re-use.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.