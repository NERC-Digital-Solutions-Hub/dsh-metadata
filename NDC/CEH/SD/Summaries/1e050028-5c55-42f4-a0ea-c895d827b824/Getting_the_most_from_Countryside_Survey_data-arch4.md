# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field squares are kept confidential by CEH to preserve representativeness; external users cannot identify squares with precision better than 100 square km.
- As a result, users cannot determine whether specific survey squares fall within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- CS field survey data come from a sample of 1 km squares in Great Britain (GB). Each selected square is mapped and detailed measurements are taken at two levels: the square level (characterising the whole square) and within-square measurements (characterising features inside the square). Measurements range from binary to continuous variables (e.g., areas, lengths).
- The CS sample squares are not a random subset of all GB squares. It is a stratified sample with sub-samples within designated strata, defined by the ITE Land Classification.
  - The land classification has evolved: originally 32 classes; revised to 42 classes in 1998 for Scotland reporting; further revised to 45 classes in 2007 for Wales reporting. Each country now has a separate classification (England: 21, Wales: 8, Scotland: 16).
- Some squares are excluded from field survey: those with area > 90% sea or > 75% urban (based on 1:250,000 OS maps). Consequently, CS field survey data are strictly representative of squares meeting these criteria. Extrapolation to GB or regional scales assumes excluded squares have similar vegetative land composition to sampled squares; this is generally reasonable given the small total area of excluded land, but problems may arise in regions with high proportions of sea/urban squares.
- Since the sampling design is not purely random, official GB estimates are produced using ratio estimates by land class, incorporating the vegetative land area of each sample square as weights. From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.
- Two-stage sampling design considerations: both square-level and within-square measurements feed into analyses; some features describe the square as a whole, others describe within-square variation.

## Implications for data practitioners (Data Leaders)

- When analysing CS data, account for stratification by ITE Land Classification and the weighting by vegetative land area to obtain unbiased estimates and correct uncertainty measures.
- Be mindful of the exclusion criteria and the potential biases when applying GB-wide or regional inferences, especially in areas with many excluded squares.
- Use appropriate statistical methods (e.g., ratio estimation with class-specific weights; bootstrap-based standard errors) rather than simple, unweighted analyses.
- Ensure thorough documentation of the sampling design, classification scheme (country-specific land classes), exclusion criteria, and data limitations in any data product or policy briefing.
- Recognize confidentiality constraints on precise locations and plan data access and metadata accordingly to maintain representativeness while safeguarding sensitive information.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., Fuller, R.M., Furse, M.T., Gillespie, M.K., Groom, G.B., Hallam, C.J., Hornung, M., Howard, D.C., and Ness, M.J. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.