# Notes on the downloadable data

## Confidentiality and data precision
- The exact locations of Countryside Survey (CS) survey squares are confidential; CEH restricts precision to 100 square km for external users.
- Users cannot identify whether any square falls within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares across Great Britain (GB), with measurements at two levels: the whole square and within-square features.
- Data types include binary and continuous variables (e.g., areas, lengths).
- The sample squares are not a random subset; they are stratified by the ITE Land Classification. Country reporting has led to different classifications: originally 32 classes; 1998 update to 42; 2007 update to 45, resulting in England (21), Wales (8), and Scotland (16) classes.

## Representativeness and bias considerations
- Analyses must account for stratification; estimates ignoring stratification may be biased.
- Not all GB squares were considered for field survey; exclusions were based on OS map-derived area criteria (>90% sea or >75% urban).
- When estimating for GB or regions, it is assumed vegetation in excluded squares resembles that in sampled squares; biases are generally small unless a region has a high proportion of sea/urban land.

## Statistical estimation and uncertainty
- Official estimates are produced using ratio estimates by land class, weighted by the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap due to skewness in some features.

## Data usage implications for data stewards
- Document the sampling design, stratification, exclusions, and estimation procedures in metadata.
- Provide clear guidance on appropriate analyses that respect the stratified design and weighting.
- Ensure confidentiality constraints (100 km2 precision) are communicated to data users and that provenance references are maintained.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.