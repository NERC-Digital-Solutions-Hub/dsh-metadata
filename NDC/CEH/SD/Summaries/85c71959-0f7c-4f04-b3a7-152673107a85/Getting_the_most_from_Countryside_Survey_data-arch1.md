# Notes on the downloadable data

- Countryside Survey (CS) Field Survey data come from a sample of 1 km squares across Great Britain, with measurements at two levels: the square as a unit and features within the square. Measurements include binary (yes/no) variables and continuous variables (e.g., areas, lengths).
- The sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific revisions over time (32 classes originally; 42 in 1998; 45 in 2007; England, Wales, and Scotland each have their own classifications).
- Not all GB squares were considered for field survey. Squares more than 90% sea or more than 75% urban (per 1:250,000 OS maps) were excluded. Estimates for GB or regions assume excluded squares are similar to sampled ones, with bias likely negligible unless a region has a high proportion of sea or urban squares.
- Estimates are produced using ratio estimators for each land class, weighting by the vegetative land area of each class. From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.
- Location confidentiality: precise locations of CS survey squares are kept confidential by CEH. External users cannot identify whether squares fall within defined areas with precision finer than 100 square km.
- Implications for analysis:
  - Analyses must account for stratification and area-based weighting; simple random-sample assumptions are inappropriate.
  - When using data at regional or local scales, be mindful of the potential for bias from excluded squares and from the non-random sampling design.
  - Bootstrap-derived uncertainty should be used to reflect sampling variability and skewness in the data.
- Key references:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap