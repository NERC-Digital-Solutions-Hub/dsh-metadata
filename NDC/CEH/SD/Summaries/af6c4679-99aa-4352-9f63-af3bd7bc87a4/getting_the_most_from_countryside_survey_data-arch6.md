# Notes on the downloadable data

- The precise locations of Countryside Survey squares are kept confidential to preserve representativeness; external users will not be able to identify square locations with precision finer than 100 square km.
- Consequently, it is not possible for users to determine whether survey squares fall within defined areas below this threshold.

# Sampling Considerations in the use of Countryside Survey Data

- CS field survey data come from a sample of 1-km squares in GB, with two levels of measurement: whole squares and within-square features, including various data types from binary to continuous.
- The sampling is not a random subset but a stratified sample within designated strata defined by the ITE Land Classification; country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16). Estimates ignoring stratification may be non-representative and have biased variation estimates.
- Squares were selected from a subset of all GB squares; squares with area more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded. The survey data are strictly representative of the included squares; estimates for GB or regions assume similar vegetative land composition in excluded squares. This assumption may cause bias only in regions with high proportions of sea or urban squares, and the impact is generally small.
- Official GB estimates are produced by ratio estimation within land classes, weighting by the vegetative land area of each class. Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.
- Practical implications for users: analyses should account for stratification and weighting; be cautious with extrapolations to whole GB or regions, especially where excluded areas (sea/urban) are substantial.
- References: Barr et al. (1993); Cochran (1963); Efron & Tibshirani (1993).