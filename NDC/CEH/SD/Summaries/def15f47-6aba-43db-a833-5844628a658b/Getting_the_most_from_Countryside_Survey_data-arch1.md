# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot identify squares with precision better than 100 square km.

- CS field survey data come from a sample of 1 km squares across GB, with two levels of measurement: across the whole square and within-square (e.g., quadrats within each square). Measurements include binary and continuous variables.

- The sampling is not a random subset; it is stratified by the ITE Land Classification. The land classification has evolved from 32 to 42 to 45 classes due to country-specific reporting, resulting in England (21 classes), Wales (8 classes), and Scotland (16 classes).

- Estimates that ignore stratification may be unrepresentative. Official GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares; exclusions are small in area but could matter in regions with high sea or urban proportions.

- Some squares were excluded from field survey: those with area more than 90% sea or more than 75% urban on 1:250000 OS maps. The practical effect is on representativeness, with the assumption that excluded areas do not bias the overall estimates significantly.

- The estimation approach uses ratio estimates for land class, weighting by the vegetative land area within each land class. From 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness (Efron and Tibshirani, 1993).

- Implications for analyses:
  - Analyses must respect the stratified sampling design and apply appropriate weights.
  - Be mindful of potential bias if stratification and exclusions are ignored.
  Use bootstrap-derived uncertainty measures when assessing variability.

- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.