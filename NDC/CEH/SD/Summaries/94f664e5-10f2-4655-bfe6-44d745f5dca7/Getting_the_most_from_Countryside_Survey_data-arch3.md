# Notes on the downloadable data

- To preserve representativeness of the wider countryside, precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH. External users are limited to identifying squares with no greater precision than 100 square km, making it impossible to determine whether specific survey squares fall within defined areas.

## Sampling considerations in the Countryside Survey Data

- CS field survey data come from a sample of 1 km squares across Great Britain. Each selected square is mapped and detailed measurements are taken for features within the square; measurements are made at two levels: across the whole square and within-square, using a variety of variable types (binary and continuous).

- The CS sample squares are not a random subset of all GB squares. Instead, the sample is stratified, with sub-samples drawn within designated strata defined by the ITE Land Classification. Country-specific classifications have evolved:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
  These classifications were adjusted over time to accommodate separate country reporting (originally 32 classes, expanded to 42 in 1998, and further changes by 2007).

- Estimates for GB or regional scales are derived using ratio estimates for each land class, weighted by the area of vegetative land within each land class.

## Representativeness and exclusions

- Not all GB squares were considered for field survey. Squares with more than 90% sea or more than 75% urban area were excluded. Official GB estimates assume that vegetative land in excluded squares is similar in composition to sampled squares; biases are expected to be small unless a region has a high proportion of sea or urban squares.

- In practice, if a region contains a large share of sea/urban squares, the assumption may be more problematic.

## Uncertainty and statistical methods

- From 1998 onward, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some feature estimates (Cochran, 1963).

- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron and Tibshirani (1993). An Introduction to the Bootstrap.