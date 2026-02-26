# Notes on the downloadable data

- Privacy and location confidentiality
  - Precise locations of Countryside Survey squares are kept confidential by UKCEH.
  - External users cannot identify whether survey squares fall within defined areas with precision finer than 100 square kilometers.
  - This limits exact geo-identification for analyses requiring precise spatial tagging.

- Data structure and sampling framework
  - Field data come from a sample of 1-km squares across Great Britain (GB).
  - Each square is mapped and measurements are taken at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils).
  - Data include a mix of binary and continuous variables (e.g., area, length).

- Not a simple random sample; stratified design
  - Squares are not a random subset of all GB 1-km squares.
  - The sample is stratified by land classification (ITE Land Classification), which has evolved over time and between countries:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Analyses must account for stratification; ignoring it can yield unrepresentative estimates and incorrect variation estimates.
  - Some squares were excluded from field survey if their area was largely sea (>90%) or urban (>75%).

- Representativeness and extrapolation
  - Field survey data are representative only of the included squares.
  - Extrapolation to all GB or regions assumes vegetative land in excluded squares is similar to sampled squares.
  - This assumption is generally reasonable due to the small total area involved, but can be problematic for regions with high sea/urban square proportions.

- Estimation methods and uncertainty
  - Official estimates are produced using ratio estimates for each land class, weighting by the vegetative land area within each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.

- References and methodological context
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Cochran (1963): Sampling techniques
  - Efron & Tibshirani (1993): Bootstrap methods

- Practical implications for analysts
  - Use stratification-aware weighting (land-class-based) when deriving estimates.
  - Apply bootstrap-based uncertainty measures to capture skewness and variation.
  - Be cautious with extrapolation beyond sampled squares, especially in regions with high sea/urban coverage.
  - Maintain awareness of privacy constraints limiting precise geographic tagging.