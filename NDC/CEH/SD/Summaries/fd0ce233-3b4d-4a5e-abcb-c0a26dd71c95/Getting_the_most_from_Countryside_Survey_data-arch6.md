# Notes on the downloadable data

## Overview
- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and detailed measurements are made (e.g., quadrats laid out, vegetation, soils).
- Measurements occur at two levels: whole square and within-square, including binary and continuous variables.
- The data are not a random subset; the sampling is stratified by land classification, affecting representativeness and variance.

## Sampling design and classifications
- Land Classification stratification drives square selection; original 32 classes expanded to 42 in 1998 (Scotland reporting), and 45 classes in 2007 (Wales reporting adjustments).
- Each country has its own classification: England (21 classes), Wales (8), Scotland (16).
- Some GB squares were excluded from field survey based on area criteria: squares >90% sea or >75% urban (from 1:250,000 OS maps).
- Official GB estimates assume excluded squares have vegetation similar in composition to sampled squares; bias is considered small unless a region has a high proportion of sea/urban squares.

## Representativeness and analysis implications
- Because the sample is stratified and not random across all GB squares, estimates must account for stratification to avoid biased results.
- Ratios by land class are used, weighting estimates by the vegetative land area within each land class.

## Data structure and types
- Data include both:
  - Square-level measurements (characterising the overall square)
  - Within-square measurements (e.g., quadrats for details on vegetation, soils)
- Variables range from binary (yes/no) to continuous (areas, lengths).

## Estimation and uncertainty
- Estimates are produced using ratio estimation (Cochran, 1963) for each land class, with weights reflecting vegetative land area.
- Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) from 1998 onward.

## Practical notes for data users
- Location privacy: the precise locations of CS survey squares are kept confidential by CEH; external users cannot identify square locations with precision finer than 100 square kilometers.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.