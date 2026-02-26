# Notes on the downloadable data

- Purpose and context
  - Countryside Survey (CS) field data come from a structured sample of GB 1-km squares, with measurements at both the square level and within-square features (e.g., quadrats, vegetation, soils).
  - Data are intended for map-based analysis and GIS visualisations, reflecting spatial patterns across the countryside.

- Confidentiality and spatial precision
  - Precise locations of Countryside Survey squares are confidential.
  - External users cannot identify whether squares fall within defined areas with precision finer than 100 square kilometres.
  - This limitation affects ability to map or verify exact square-by-square placements for very small areas.

- Sampling design: two levels and data types
  - Two levels of sampling: whole square level and within-square level.
  - Measurements range from binary to continuous (e.g., areas, lengths), enabling both square-wide and inside-square characterisation.

- Non-random, stratified sampling
  - CS squares are not a random subset of all 1-km GB squares.
  - Sampling is stratified by the ITE Land Classification (land classes), with country-specific classifications:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Estimates missing stratification adjustments may be biased; weighting uses land-class area to derive representative estimates.

- Exclusions and representativeness
  - Some squares were excluded from field survey: those where area > 90% sea or >75% urban (per 1:250k OS maps).
  - Official GB estimates assume vegetative land in excluded squares mirrors that of sampled squares; bias is considered small unless a region has a high proportion of sea/urban squares.

- Estimation, weighting and uncertainty
  - Estimates by land class are calculated using ratio estimation techniques that incorporate vegetative land area per class.
  - Since 1998, standard errors and confidence intervals are estimated with bootstrap methods (Efron & Tibshirani).

- Implications for GIS work
  - When creating map-based products, account for:
    - Stratification by land class and area weights
    - The non-random sampling design
    - Spatial confidentiality constraints limiting fine-grain location accuracy
    - Potential biases if applying region-wide extrapolations or using excluded-square areas
  - Use provided weights and bootstrap-based uncertainty measures to inform map visuals and uncertainty representation.

- References
  - Barr, C.J. et al. 1993. Countryside Survey 1990 Main Report
  - Cochran, W.G. 1963. Sampling Techniques
  - Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap