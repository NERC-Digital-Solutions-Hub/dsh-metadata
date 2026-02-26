# Notes on the downloadable data

- Location confidentiality and precision
  - The precise locations of Countryside Survey squares are kept confidential by UKCEH to preserve representativeness.
  - External users cannot identify survey squares with precision finer than 100 square kilometers.
  - Consequently, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

- Data structure and sampling design
  - Countryside Survey (CS) field data come from a sample of 1-km squares across Great Britain (GB).
  - Each selected square is mapped, and detailed measurements are taken for features within the square and for the square as a whole (two levels: whole-square and within-square).
  - Measurements include both binary (yes/no) and continuous variables (e.g., areas, lengths).
  - The sample is not a random subset of all 1-km GB squares; it is stratified by the ITE Land Classification.
  - Land Classification has evolved: originally 32 classes, expanded to 42 in 1998 for Scotland reporting, and 45 classes after Wales reporting in 2007.
  - Separate country reporting means England, Wales, and Scotland have distinct classifications (21, 8, and 16 classes, respectively).

- Exclusion criteria and representativeness
  - Squares whose area is more than 90% sea or more than 75% urban (based on 1:250,000 OS maps) were excluded from field survey.
  - Official GB/ region estimates are derived using ratio estimates that account for vegetative land area in each land class.
  - In practice, estimates for GB or regions assume vegetative land in excluded squares is similar to that in sampled squares. This assumption is generally reasonable, but can be problematic if a region has a high proportion of sea or urban squares.

- Estimation methods and uncertainty
  - Land class estimates are produced by ratio estimation, weighted by the vegetative land area of each land class.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

- Practical considerations for analysts
  - When using CS data, account for the stratified sampling design, the exclusion of certain squares, and the weighting by vegetative land area.
  - Be cautious about making inferences at very local scales where the sampling frame or exclusions may affect representativeness.
  - Understand that the precise location limitation may affect alignment with boundaries or areas of interest.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.