# Notes on the downloadable data

## Key confidentiality constraint
- Precise locations of Countryside Survey (CS) survey squares are confidential; external users cannot identify squares with precision finer than 100 square km.

## Sampling design and levels
- CS field survey data come from a stratified sample of 1 km squares in Great Britain.
- Each selected square is mapped and measured at two levels: the whole square and within-square features.
- Measurements vary from binary to continuous (e.g., areas, lengths).

## Stratification and representativeness
- The sample is not a random subset of GB squares; it is stratified by the ITE Land Classification.
- National classifications vary by country: England (21 classes), Wales (8), Scotland (16).
- Estimates derived from CS data must account for stratification; ignoring it can yield unrepresentative estimates and incorrect variation.

## Exclusions and implications for representativeness
- Squares with >90% sea or >75% urban areas were excluded from field surveys.
- Official GB estimates assume that vegetative land in excluded squares is similar to that in sampled squares. This is usually acceptable given the small total area involved, but regions with high sea/urban proportions may experience bias.

## Estimation methods and inference
- Land-class estimates are calculated using ratio estimates, weighted by the vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated via bootstrap methods due to skewness in some features.

## Practical implications for data use
- Analyses should account for the stratified sampling design to avoid biased results.
- Users should be aware of non-random sampling and the extrapolation assumptions for regions containing many excluded squares.
- Location confidentiality limits precise mapping, which may affect fine-scale geographic analyses.

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.