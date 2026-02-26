# Notes on the downloadable data

## Data confidentiality and access
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH.
- External users will not be identified to a precision finer than 100 square kilometres.
- This confidentiality constraint affects the ability to determine whether specific squares fall within defined areas.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and measured at two levels: the square level and within-square features.
- Measurements span various data types, from binary to continuous (e.g., areas, lengths).

## Stratification and classifications
- The sample is not a simple random subset; it is stratified by the ITE Land Classification.
- Land classification has evolved by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Estimates ignoring stratification may be biased; proper analysis requires accounting for this stratification.

## Exclusions and representativeness
- Squares excluded from field survey if their area is >90% sea or >75% urban (based on 1:250,000 OS maps).
- Official GB or regional estimates assume excluded squares have vegetation similar to sampled squares; this introduces potential bias, particularly if a region contains many sea or urban areas. Overall bias is expected to be small unless regional composition is extreme.

## Estimation methods and uncertainty
- GB land class estimates are derived using ratio estimates weighted by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods.

## Data use guidance
- Analyses should incorporate the stratification and area-based weights.
- Do not treat CS data as a simple random sample of all GB squares.
- Consider the potential biases arising from excluded squares and the evolving land classifications.
- Refer to the cited methodological references for detailed procedures (Cochran 1963; Efron & Tibshirani 1993).

## References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.

## Data governance considerations for data stewards
- Document and communicate the sampling design, stratification, classifications, and exclusion criteria in metadata.
- Record any updates to land classifications and their implications for comparability over time.
- Ensure confidentiality constraints (location precision) are enforced in data sharing and portals.
- Provide guidance on appropriate analysis methods (weights, stratification, bootstrap SEs) to users.