# Notes on the downloadable data

- The precise locations of Countryside Survey squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.
- Countryside Survey (CS) field data come from a sample of 1-km squares in Great Britain, with measurements at two levels: the square as a whole and features within the square.
- Measurements vary from binary to continuous (e.g., areas, lengths).

## Sampling design and selection

- CS samples are not a random subset of all 1-km GB squares; they are stratified within designated strata.
- Strata are defined by the ITE Land Classification, which has evolved into country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16) due to separate reporting requirements.
- Estimates derived from CS data must account for stratification to be representative and to accurately estimate variation.
- Not all GB squares were considered for field survey; squares with more than 90% sea or more than 75% urban area were excluded from survey.
- In practice, estimates for GB or regions assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small except where a region has a high proportion of sea/urban squares.

## Representativeness and estimation

- Official GB estimates are produced using ratio estimates for each land class, weighted by the vegetative land area of each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods.

## Practical implications for analysts

- When using CS data, account for stratification and weighting by vegetative land area to obtain representative estimates.
- Be aware of potential biases if a region has unusual proportions of sea or urban areas; the sampling design aims to mitigate this, but limitations remain.
- Use bootstrap-based standard errors and CIs to reflect sampling variability.

## Data privacy and access

- Location data are restricted to protect confidentiality; exact square locations are not disclosed beyond the 100 square km precision threshold.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.