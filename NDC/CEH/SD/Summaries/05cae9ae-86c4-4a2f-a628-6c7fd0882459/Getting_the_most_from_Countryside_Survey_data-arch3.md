# Notes on the downloadable data

- Confidentiality: The precise locations of Countryside Survey (CS) field survey squares are held in confidence by CEH to preserve representativeness. External users cannot identify squares with precision finer than 100 square km, limiting geographic pinpointing of squares within defined areas.

- Sampling design: CS field data come from a sample of 1 km squares across GB. Each square is mapped and measured at two levels (the whole square and within-square features). Measurements include binary and continuous variables across vegetation, soils, etc. The sample is not a random subset; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16). Since 1998, classifications have been adjusted for country reporting.

- Excluded squares: Squares with >90% sea area or >75% urban area (based on 1:250,000 OS maps) were excluded from field survey. Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible unless a region has a high proportion of sea/urban squares.

- Estimation approach: Because of skewness in some features, estimates are derived as ratio estimates for each land class and combined using the vegetative land area as weights. From 1998 onward, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani).

- Measurement scope: Data include both square-level and within-square measurements, with a range of variable types from binary to continuous (e.g., areas, lengths). The sampling design and weighting are essential for correct interpretation of estimates, particularly when analyzing across land classes or regions.

- Data handling and governance considerations: The design implies careful attention to stratification, weighting, and representativeness when using CS data for monitoring frameworks. The confidentiality constraint and the need to understand the sampling design are important for data access, reproducibility, and appropriate aggregation.

- References: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) Bootstrap.