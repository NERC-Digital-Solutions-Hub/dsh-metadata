# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements at both the square level and within-square features.
- The dataset supports analyses of vegetation, soils, and related features, using various measurement types from binary to continuous.

## Confidentiality and geographic precision
- To preserve representativeness of the wider countryside, precise locations of CS survey squares are kept confidential by CEH.
- External users will not be able to identify exact square locations with precision finer than 100 square kilometres.
- This ensures the privacy of site locations while still enabling broad-area analysis.

## Sampling design and structure
- Two levels of sampling:
  - Whole-square level provides general square-wide characteristics.
  - Within-square level provides detailed measurements inside each square (e.g., quadrats, plots).
- Squares are not a random subset of all GB squares; sampling is stratified by land classification (ITE Land Classification).
- The land classification has evolved by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Classification changes reflect country-specific reporting requirements (e.g., Scotland in 1998, Wales in 2007).

## Exclusions and representativeness
- Some squares were excluded from field surveys:
  - Squares with more than 90% sea area
  - Squares with more than 75% urban area
- Official GB estimates assume that vegetative land in excluded squares is similar in composition to sampled squares. This assumption is generally reasonable due to the small total area involved but can be problematic if a region has a high proportion of sea or urban squares.

## Estimation methods and uncertainty
- Estimates by land class are produced using ratio estimates that account for vegetative land area within each class.
- Land-class estimates are then combined using weights based on the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness in certain features.

## Implications for analysis and use
- Analyses must account for the stratified sampling design to obtain representative estimates and accurate uncertainty measures.
- Ignoring stratification can lead to biased estimates of variation.
- Users should be aware of the confidentiality constraints on location data and rely on aggregated or generalized outputs (e.g., 100 km2 precision) for spatial analyses.
- When interpreting GB-wide or regional estimates, consider potential biases from excluded squares, especially in regions with substantial sea or urban coverage.

## Documentation and references
- Key references for methodology:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.