# Notes on the downloadable data

- Confidentiality of CS survey locations: exact locations are kept confidential by CEH; external users cannot identify whether squares fall within defined areas beyond 100 square km precision.

- Structure of Countryside Survey (CS) data: field survey data come from a sample of 1 km squares in Great Britain; each square is mapped and measured both at the square level and within-square features (e.g., quadrats for vegetation and soils); measurements span binary and continuous variables.

- Sampling design and representativeness: CS squares are not a random subset; sampling is stratified by the ITE Land Classification with country-specific revisions (England: 21 classes; Wales: 8; Scotland: 16; overall classifications have changed over time from 32/42/45 to the current country-specific schemes).

- Implications for analyses: estimates that ignore stratification may be non-representative and have biased variation; proper analyses must account for the stratified design.

- Excluded squares and extrapolation: squares that are >90% sea or >75% urban are excluded from field surveys; official GB estimates are based on the included squares, with extrapolation to GB assuming vegetation in excluded squares is similar to sampled squares; this assumption may introduce bias if regions have high sea/urban proportions, though the impact is generally small.

- Estimation method: GB land-class estimates are produced as ratio estimates that incorporate the area of vegetative land in each sampled square; final estimates are weighted by the vegetative land area within each land class overall.

- Uncertainty assessment: since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani).

- References: Barr et al. (1993); Cochran (1963); Efron and Tibshirani (1993).