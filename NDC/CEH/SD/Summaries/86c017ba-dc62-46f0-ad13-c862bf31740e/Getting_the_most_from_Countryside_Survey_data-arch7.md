# Notes on the downloadable data

- Spatial confidentiality: precise locations of Countryside Survey (CS) squares are kept confidential by CEH to preserve representativeness. External users cannot identify whether squares fall within defined areas to finer than 100 square km, limiting precise location-based queries.

- Sampling design and data structure:
  - CS Field Survey data come from a sample of 1 km squares in Great Britain.
  - Each selected square is mapped and detailed measurements are taken, including within-square sampling with quadrats for vegetation, soils, etc.
  - Two levels of sampling: measurements characterise the entire square and measurements within the square; data include both binary and continuous variables.

- Stratification and land classification:
  - Squares are not a random subset; they are stratified by the ITE Land Classification.
  - Land Classification categories vary by country (England 21 classes, Wales 8, Scotland 16) due to separate reporting needs; historically classifications expanded from 32 to 45 classes.
  - Estimates derived from CS data must account for stratification to be representative.

- Exclusions and representativeness:
  - Squares with more than 90% sea or more than 75% urban area (as measured on 1:250,000 OS maps) were excluded from field survey.
  - Official estimates assume vegetative land in excluded squares is similar to that in sampled squares; this introduces potential bias if regional composition differs significantly, though such excluded land is typically small in area.

- Estimation and uncertainty:
  - Estimates are produced as ratio estimates by land class, weighted by the vegetative land area within each land class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features.

- References:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap