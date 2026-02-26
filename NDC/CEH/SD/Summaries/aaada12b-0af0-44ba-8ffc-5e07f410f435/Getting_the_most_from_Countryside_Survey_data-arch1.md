# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by UKCEH to preserve representativeness; external users cannot identify whether squares fall within defined areas with precision finer than 100 square km.

## What the data are

- CS Field Survey data come from a sample of 1 km squares in Great Britain (GB). Each selected square is mapped and measured, with some data collected at the square level and additional information collected within squares (e.g., quadrats for vegetation, soils).
- Measurements vary in type, from binary (yes/no) variables to continuous metrics such as areas or lengths.

## Sampling design and representativeness

- The CS sample squares are not a random subset of all GB squares; they are stratified within designated strata defined by the ITE Land Classification.
- Land Classification details have evolved by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Up to 1998, the classification had more classes and changed to accommodate separate country reporting (ultimately 45 classes across countries).
- Not all GB squares were surveyed. Squares more than 90% sea or more than 75% urban in area were excluded from field survey.
- Official CS estimates for GB or regions assume similar vegetative land composition in excluded squares, which may introduce minor bias, particularly where a region has a high proportion of sea or urban squares.

## Estimation and uncertainty

- Estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighted by the vegetative land area of each class.
- Because of concerns about skewness in some features, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) starting from 1998.

## Implications for analysis

- Analyses must account for stratified sampling and weights by vegetative land area within land classes to obtain representative estimates.
- Ignoring stratification can lead to biased estimates and incorrect assessments of variation.
- The sampling design implies careful interpretation when extrapolating to whole GB or to regions, particularly if excluded squares differ systematically in vegetation or land cover.

## Access notes and references

- Data access is governed by confidentiality to protect representativeness (locations known only within 100 square km precision externally).
- Key references:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron and Tibshirani (1993) An Introduction to the Bootstrap