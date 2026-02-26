# Notes on the downloadable data

- Confidentiality and spatial precision: The exact locations of Countryside Survey (CS) field squares are kept confidential by UKCEH. External users will not be provided with precision better than 100 square kilometres, so you cannot determine whether a survey square falls within defined areas below this threshold.

- CS data structure and sampling levels: CS field data come from a sample of 1 km squares in Great Britain. Each square is mapped and measured at two levels: the square level (characterising the whole square) and within-square features (e.g., quadrats for vegetation, soils). Measurements range from binary to continuous variables (areas, lengths).

- Sampling design and stratification: The CS sample squares are not a random subset; they are stratified with sub-samples within strata. Strata are defined by the ITE Land Classification. Classification changes over time:
  - Original: 32 land classes
  - 1998: revised to 42 classes ( Scotland reporting prompted changes)
  - 2007: Wales-only reporting led to 45 classes
  - England, Wales, and Scotland each have separate classifications (23? per country: England 21 classes, Wales 8 classes, Scotland 16 classes are stated in the document).
  Estimation that ignores stratification may be unrepresentative.

- Exclusions and representativeness: Not all GB squares are surveyed. Squares with land area >90% sea or >75% urban were excluded. Field survey estimates are representative of the included squares. In practice, GB estimates assume vegetative land in excluded squares is similar to that in sampled squares; bias is typically negligible unless a region has a high proportion of sea or urban squares.

- Estimation method and uncertainty: Official estimates are produced using ratio estimates for each land class, weighting by the vegetative land area in each class. Since 1998, standard errors and confidence intervals are estimated using bootstrapping to accommodate skewness in some features.

- References: 
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.