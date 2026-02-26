# Notes on the downloadable data

- Location confidentiality: The precise locations of Countryside Survey (CS) survey squares are held in confidence by CEH. External users cannot identify whether squares fall within defined areas with any precision better than 100 square km, limiting fine-grained location queries.

- Structure of CS Field Survey data: Based on a sample of 1 km squares in Great Britain. Each selected square is mapped and measured at two levels (the whole square and within-square features). Measurements vary from binary to continuous (e.g., areas, lengths). The sample is not a random subset; it is stratified by Land Classification with implications for representativeness.

- Land Classification and country specifics: The Land Classification has evolved from 32 classes to 42, then 45 classes to accommodate separate country reporting. England uses 21 classes, Wales 8, Scotland 16. Estimates ignoring stratification may be unrepresentative or have incorrect variation estimates.

- Exclusions from survey: Squares with more than 90% sea or more than 75% urban area are excluded from field survey. Official GB estimates assume excluded squares have vegetative land similar in composition to sampled squares; this introduces potential bias mainly where a region has a high proportion of sea or urban squares, though such bias is generally small.

- Estimation methodology: GB land class estimates are computed as ratio estimates weighted by the area of vegetative land within each land class. From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods due to skewness concerns.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.