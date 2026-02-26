# Notes on the downloadable data

- Location privacy: The precise locations of Countryside Survey (CS) survey squares are confidential to CEH. External users will not be provided with precise locations beyond 100 square kilometers.
- Implication: It is therefore not possible to determine whether survey squares fall within defined areas smaller than 100 km².

## Sampling considerations in the Countryside Survey Data

- Data structure: CS Field Survey data come from a sample of 1 km squares in Great Britain. Each selected square is mapped and measured at two levels (the square as a whole and features within the square). Measurements include a mix of binary and continuous variables (e.g., areas, lengths).
- Non-random, stratified design: The sample squares are not a random subset of all GB squares; sampling is stratified with sub-samples within designated strata.
- Stratification by land classification: Strata are defined by the ITE Land Classification. Classifications have evolved over time:
  - Original: 32 land classes
  - 1998 (Scotland reporting needs): 42 classes
  - 2007 (Wales reporting needs): 45 classes
  - Result: Each country effectively has its own classification (England 21, Wales 8, Scotland 16).
- Representativeness and analysis: Estimates that do not account for stratification may not be representative and can misstate variation. Official estimates use ratio techniques (Cochran, 1963) for each land class, weighted by the vegetative land area of each class.
- Exclusion of certain squares: Squares with more than 90% sea or more than 75% urban area (as measured on 1:250,000 OS maps) were excluded from field survey. Thus, the data are representative of the included squares; extrapolations to the whole GB assume similarity in vegetative land composition in excluded squares. This bias is likely negligible except in regions with high sea/urban proportions.
- Uncertainty estimation: Since 1998, because of skewness concerns, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).

References
- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.