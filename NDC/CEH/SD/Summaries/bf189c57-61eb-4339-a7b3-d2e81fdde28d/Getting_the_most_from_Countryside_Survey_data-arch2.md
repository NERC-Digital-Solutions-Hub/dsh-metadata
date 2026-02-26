# Notes on the downloadable data

- Confidentiality of CS survey square locations: CEH will not share precise locations; external users will not be able to identify squares with precision finer than 100 square km.
- Implication: Users cannot determine whether specific squares fall within defined areas described below.

## Sampling considerations in the Countryside Survey Data

- Data source and structure:
  - Field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Each selected square is mapped; measurements are taken at two levels: at the square level and within-square (e.g., quadrats for vegetation, soils), yielding both binary and continuous variables.

- Sampling design:
  - The sample is not a random subset of GB squares; it is stratified by ITE Land Classification.
  - Land Classification detail changes:
    - Originally 32 classes.
    - 1998: expanded to 42 classes for Scotland reporting needs.
    - 2007: expanded to 45 classes with separate country reporting (England: 21, Wales: 8, Scotland: 16).

- Representativeness and analysis implications:
  - Estimates not accounting for stratification are not necessarily representative and may misstate variation.
  - Official GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares; this assumption is generally reasonable because excluded areas (sea/urban) are small, but regional biases could arise if a region contains a high proportion of sea or urban squares.

- Exclusions and representativeness:
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys.
  - Estimates officially pertain to the included squares; extrapolation to all GB squares requires caution.

- Estimation methods:
  - Estimates are produced as ratio estimates (Cochran 1963), weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are derived using bootstrap methods (Efron & Tibshirani 1993) to address skewness.

- References for methods and data:
  - Barr, Bunce, Clarke, et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.