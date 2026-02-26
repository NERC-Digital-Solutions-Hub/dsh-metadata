# Notes on the downloadable data

- To preserve representativeness, precise locations of Countryside Survey (CS) squares are confidential; external users cannot identify square locations with better than 100 square km precision.
- Consequently, users cannot determine whether any survey squares fall within defined areas below this threshold.

## Sampling Considerations in the use of Countryside Survey Data

- CS field survey data come from a sample of 1 km squares in GB, with two sampling levels: whole squares and within-square measurements. Measurements include a mix of binary and continuous variables (e.g., vegetation, soils, quadrats).
- The 1 km square sample is not a random subset; it is stratified by the ITE Land Classification. Land classifications have evolved: originally 32 classes; 1998 broadened to 42 classes; 2007 expanded to 45 classes. England has 21 classes, Wales 8, Scotland 16.
- Estimates that do not account for stratification may be unrepresentative, and variation estimates may be inaccurate.
- Some GB squares were excluded from field surveys if their area was more than 90% sea or more than 75% urban (per 1:250,000 OS maps). Official estimates are representative only of squares meeting these criteria.
- For GB-wide estimates, vegetative land in excluded squares is assumed similar to sampled squares; bias is expected to be small except in regions with high sea/urban proportions.
- Official estimates are produced using ratio estimation (Cochran, 1963) for each land class, weighted by the vegetative land area of that class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness.

## Implications for GIS mapping and analysis

- Treat location information as coarse (100 km2 scale) and avoid precise pinpointing in maps.
- Estimates are stratified and area-weighted by land class; when aggregating, preserve the underlying stratification logic.
- When integrating with other datasets, account for differences in land-class schemes across England, Wales, and Scotland and changes over time.

## References

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report. DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.