# Notes on the downloadable data

- Purpose and confidentiality
  - To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) field survey squares are kept confidential by UKCEH.
  - External users cannot identify whether squares fall within defined areas to a finer precision than 100 square km.

- Sampling framework and data structure
  - Data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped, with detailed measurements taken for selected features; multiple quadrats are used within squares.
  - Two levels of sampling: whole square and within-square measurements (covering both square-level and within-square features).
  - Measurements include a mix of binary (yes/no) and continuous variables (areas, lengths, etc.).
  - The CS sample is not random; it is stratified by land classification. Countries use different classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Land classification has evolved:
    - Original 32 classes
    - 1998: increased to 42 classes (to accommodate Scotland reporting)
    - 2007: increased to 45 classes (to accommodate Wales reporting)

- Representativeness and limitations
  - Estimates derived from CS data must account for stratification; analyses that ignore stratification may be unrepresentative.
  - Not all GB squares were surveyed; exclusions were based on 1:250,000 OS maps:
    - Excluded if >90% sea or >75% urban.
  - In practice, GB-wide estimates assume vegetative land in excluded squares is similar to sampled squares; bias is generally small unless a region has a high proportion of sea/urban areas.

- Estimation methods and uncertainty
  - Official estimates are produced using ratio estimation (Cochran, 1963) by land class, weighted by vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

- Data handling and governance implications
  - Some data handling considerations arise from representativeness and confidentiality:
    - Location confidentiality can affect cross-boundary analyses and fine-scale mapping.
    - Data users may need to work with aggregated or stratified outputs and appropriate weighting to obtain valid inferences.

- References
  - Barr, C.J. et al. Countryside Survey 1990 Main Report (1993)
  - Cochran, W.G. Sampling Techniques (2nd ed.) (1963)
  - Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993)