# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users only have location precision to 100 square km, making it impossible to identify whether squares fall within defined areas below this threshold.
- CS field survey data come from a sample of 1 km squares in Great Britain (GB), with two sampling levels: whole squares (mapped) and within-square measurements (e.g., quadrats for vegetation, soils, etc.). Measurements include binary and continuous variables.
- The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification. Country-specific classifications exist: England (21 classes), Wales (8), Scotland (16). Estimates ignoring stratification may be biased.

## Sampling design and representativeness
- Not all GB squares are surveyed; exclusions include squares where at least 90% of area is sea or at least 75% urban. Estimates for GB or regional levels assume excluded squares are similar in vegetative land composition to sampled squares; bias is generally small but may be an issue in regions with many sea/urban squares.
- Official GB estimates are produced using ratio estimates that account for the vegetative land area within each land class, with weights based on land area in each land class.

## Uncertainty and analysis considerations
- Since some features are skewed, from 1998 onward standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).
- When analyzing CS data, it is important to account for stratification, sampling design, and area-based weighting to obtain valid estimates and uncertainties.

## Practical implications for use
- Be mindful of the two-level sampling (square and within-square) when summarising or modelling data; some measurements are square-level while others are within-square.
- Use land-class weights and the stratified design to compute representative estimates; avoid analyses that ignore stratification.
- Consider the confidentiality constraint when discussing locations or attempting to map precise square-level information.
- Use bootstrap-derived standard errors and confidence intervals for uncertainty reporting, especially for skewed features.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.