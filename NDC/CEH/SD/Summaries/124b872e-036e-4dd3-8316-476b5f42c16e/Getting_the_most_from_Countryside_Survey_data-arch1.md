# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
  - External users will not be given location precision finer than 100 square kilometres; you cannot identify whether specific survey squares fall within defined areas below this threshold.

- Data structure and sampling levels
  - CS Field Survey data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary and continuous variables (areas, lengths, etc.).

- Sampling design and representativeness
  - The CS sample squares are not a random subset of all GB squares; the design is stratified within designated strata.
  - Stratification is defined by the ITE Land Classification, which has evolved:
    - Originally 32 land classes
    - 1998: modified to 42 classes for Scotland reporting
    - 2007: Wales reporting led to 45 classes
  - Each country has its own classification: England (21), Wales (8), Scotland (16).
  - Therefore, estimates that ignore stratification may be unrepresentative or have biased variation estimates.

- Exclusions and implications for inference
  - Squares with area > 90% sea or > 75% urban (as per 1:250,000 OS maps) were excluded from field survey.
  - Official estimates for GB or regions are derived under the assumption that vegetative land in excluded squares is similar to sampled squares.
  - This assumption may be problematic in regions with high sea/urban proportions, though such regions are typically small.

- Estimation methods and uncertainty
  - Estimates by land class are produced using ratio estimation (Cochran, 1963), weighting by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to skewness in some features.

- References
  - Barr, C.J. et al. Countryside Survey 1990 Main Report (1993)
  - Cochran, W.G. Sampling Techniques (2nd ed., 1963)
  - Efron, B. & Tibshirani, R.J. Bootstrap (1993)