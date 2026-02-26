# Notes on the downloadable data

- Data confidentiality: precise locations of CS survey squares are kept confidential by CEH; external users cannot identify whether squares fall within defined areas below a threshold of 100 square km. This preserves representativeness but limits precise geolocation use.

- Sampling design and data structure:
  - CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels: the square level and within-square (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include binary and continuous variables, collected both at square level and within-square features.
  - The sample is not a random subset; it is a stratified sample with sub-samples within designated strata.

- Stratification and land classification:
  - Strata are defined by the ITE Land Classification. The system has evolved:
    - Originally 32 land classes.
    - In 1998, Scotland-specific reporting increased to 42 classes.
    - In 2007, Wales-specific reporting raised to 45 classes.
  - Each country effectively has its own classification (England: 21 classes, Wales: 8, Scotland: 16).
  - Analyses that ignore stratification may yield non-representative estimates and incorrect variation.

- Exclusions and representativeness:
  - Squares with >90% sea or >75% urban area (as measured from 1:250,000 OS maps) were excluded from field survey.
  - Official GB estimates are derived by assuming excluded vegetative land is similar to sampled squares; this is generally acceptable since the excluded land is small, but regional biases may occur if an area has a high sea/urban proportion.

- Estimation and inference:
  - Land class estimates are produced as ratio estimates, weighting by the vegetative land area of each class.
  - Because of skewness in some features, standard errors and confidence intervals have been estimated using bootstrap methods since 1998 (Efron & Tibshirani).

- Practical implications for analysts:
  - When analyzing CS data, account for stratification by land class to obtain valid estimates and uncertainty.
  - Be aware of potential biases from excluded squares, especially in regions with substantial sea or urban areas.
  - Use bootstrap-based standard errors for skewed features and apply area-based weights when aggregating across land classes.

- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.