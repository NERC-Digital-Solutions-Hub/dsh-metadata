# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify whether squares fall within defined areas to better than 100 square km.

- Consequently, users cannot determine if survey squares fall inside specific study areas below this precision threshold.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares across Great Britain; for each selected square, the whole square is mapped and detailed measurements are taken, with additional measurements within the square (two levels: square-level and within-square).

- Measurements include a mix of binary (yes/no) and continuous variables (e.g., areas, lengths).

- The dataset is not a random subset of GB squares; it is a stratified sample with sub-samples within designated strata.

## Stratification and country classifications

- Strata are defined by the ITE Land Classification. Classifications have evolved:
  - Originally 32 land classes
  - 1998: Scotland-specific changes expanded to 42 classes
  - 2007: Wales-specific reporting increased to 45 classes
- Each country effectively has its own classification (England 21 classes, Wales 8, Scotland 16).

- Estimates must account for stratification; ignoring it can yield non-representative results or inaccurate variation estimates.

## Exclusions and representativeness

- Not all GB squares were considered for field survey; squares with 1:250,000-scale area > 90% sea or > 75% urban were excluded.

- Official GB or regional estimates assume excluded land is similar in vegetative composition to sampled land; this introduces potential bias mainly if a region has a large share of sea/urban squares, though such bias is expected to be small overall.

## Estimation methods and uncertainty

- Official land-class estimates are produced using ratio estimates, weighted by the vegetative land area within each land class.

- Because some features can be skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).

## References

- Barr et al. (1993) Countryside Survey 1990 Main Report
- Cochran (1963) Sampling Techniques
- Efron & Tibshirani (1993) An Introduction to the Bootstrap

Notes for data leaders:
- When analyzing CS data, implement stratification-aware methods and appropriate weighting.
- Be mindful of the confidentiality constraints on square locations when defining study areas.
- Use bootstrap-based uncertainty measures to reflect potential skewness in features.