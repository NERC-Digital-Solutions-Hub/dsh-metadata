# Notes on the downloadable data

## Overview
- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness; external users cannot identify squares with precision finer than 100 square km.
- This confidentiality means users cannot determine whether specific survey squares fall within defined areas below the 100 sq km threshold.

## Sampling design
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped, with detailed measurements made for features within the square (two levels: the square as a whole and features within the square).
- Data types include both binary (yes/no) and continuous measurements (areas, lengths, etc.).
- The sampling is not a simple random subset; it is stratified by the ITE Land Classification.
- Land Classification details have evolved:
  - Originally 32 classes.
  - 1998: increased to 42 classes to support Scotland-only reporting.
  - 2007: 45 classes to support Wales-only reporting.
  - Each country has its own classification: England (21), Wales (8), Scotland (16).
  
## Representativeness and limitations
- Not all GB squares were considered for field survey; excluded if:
  - The square's land area is more than 90% sea, or
  - More than 75% urban.
- Official GB or regional estimates are derived under the assumption that vegetative land in excluded squares is similar to that in sampled squares. This is generally unlikely to be exact, but the overall land area covered by excluded squares is small, so bias is typically negligible. Exceptions may occur for regions with high sea/urban proportions.

## Estimation and uncertainty
- Estimates are produced as ratio estimates for each land class, incorporating the vegetative land area within each sampled square.
- Land class estimates are combined using weights based on vegetative land area for the land class as a whole.
- Since 1998, standard errors and confidence intervals are estimated using the bootstrap method.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.