# Notes on the downloadable data

- Confidentiality of locations: CEH holds precise CS survey square locations; external users will not be able to identify square locations with precision finer than 100 square km to preserve representativeness.

- Data structure and measurements: Countryside Survey (CS) field data come from a sample of 1 km squares in GB. Each square is mapped; measurements are taken at two levels (the whole square and within-square features). Data types range from binary to continuous (e.g., areas, lengths).

- Sampling design: The CS sample squares are not a random subset of all GB squares but a stratified sample with sub-samples within designated strata. Strata are defined by the ITE Land Classification, which has evolved from 32 classes (original) to 42 (1998) to 45 (2007) due to separate country reporting. England has 21 classes, Wales 8, Scotland 16.

- Representativeness and inference: Estimates derived from CS data without accounting for stratification may be unrepresentative and have inaccurate variation estimates. Proper analysis requires incorporating the stratified design.

- Excluded squares: Squares with more than 90% sea area or more than 75% urban area (as measured on 1:250000 OS maps) were excluded from field survey. Official GB or regional estimates assume similarity in vegetative land between excluded and included squares; bias is generally negligible unless a region has a high proportion of sea or urban squares.

- Estimation and weighting: Official estimates are produced using ratio estimates (Cochran, 1963) for each land class, incorporating the area of vegetative land in each sample square. Land-class estimates are then combined using weights proportional to the vegetative land area of each land class.

- Uncertainty assessment: Since 1998, standard errors and confidence intervals have been estimated via bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

- References: Barr, Bunce, Clarke, et al. (1993); Cochran (1963); Efron and Tibshirani (1993).