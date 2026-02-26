# Notes on the downloadable data

- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain (GB), with measurements at two levels: the square as a whole and features within the square.
- Data types include binary variables and continuous measurements (e.g., areas, lengths), and measurements are taken from both levels to characterize the square and its internal features.

- Location confidentiality: The precise locations of CS survey squares are kept by CEH and are not provided to external users with precision finer than 100 square kilometers to preserve representativeness of the wider countryside.

- Sampling design and stratification:
  - The sample squares are not a random subset; they are stratified within the ITE Land Classification.
  - Land classification has changed over time: originally 32 classes, expanded to 42 in 1998 for Scotland, and to 45 in 2007 for Wales. In practice, each country has a separate classification (England: 21 classes, Wales: 8, Scotland: 16).
  - Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

- Exclusion of squares:
  - Squares with more than 90% sea area or more than 75% urban area were excluded from field surveys.
  - Official GB or regional estimates assume excluded vegetative land is similar to that in sampled squares; this is usually a small bias, but could be problematic in regions with high sea/urban proportions.

- Estimation methodology:
  - Official estimates are produced using ratio estimates for each land class, weighted by the vegetative land area in each class.
  - Since some features are skewed, standard errors and confidence intervals have been estimated using bootstrap methods (since 1998).

- Practical considerations:
  - Data users should be aware of potential limitations related to scale, accessibility, and stratification when analysing CS data.
  - The document cites key methodological references: Barr et al. (1993), Cochran (1963), and Efron & Tibshirani (1993).