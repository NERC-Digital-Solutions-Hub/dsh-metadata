# Notes on the downloadable data

- Confidentiality of locations: To preserve representativeness, precise locations of CS survey squares are kept confidential by UKCEH; external users cannot identify squares with precision finer than 100 square km, limiting geospatial identifyability.

## CS Field Survey design and data structure

- Data come from a sample of 1 km squares across GB; each square is mapped and measured at two levels (whole square and within-square) with a mix of variable types (binary to continuous).

## Sampling design and stratification

- The CS sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification, with country-specific revisions (32 → 42 → 45 classes; England 21, Wales 8, Scotland 16). Analyses ignoring stratification may misrepresent variability.
  
## Exclusions and representativeness

- Squares exceeding 90% sea area or 75% urban were excluded from field survey. Official GB estimates assume similarity between vegetative land in excluded and included squares; bias is generally negligible unless a region has high sea/urban proportions.

## Estimation methods and uncertainty

- Estimates by land class are produced using ratio estimates weighted by vegetative land area within each class. Since some features are skewed, standard errors and confidence intervals are computed via bootstrap methods (from 1998 onward).

## Documentation and references

- Key sources: Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) Bootstrap.

## Data governance and stewardship implications

- When sharing or using CS data, preserve and document the stratification, weighting, and exclusion rules to ensure valid analyses.
- Provide metadata on land-class classifications, country-specific schemes, and any changes over time to support reproducibility.
- Be explicit about limitations due to non-random sampling and location confidentiality, and supply design variables (strata, weights, and bootstrap information) to enable proper uncertainty assessment.