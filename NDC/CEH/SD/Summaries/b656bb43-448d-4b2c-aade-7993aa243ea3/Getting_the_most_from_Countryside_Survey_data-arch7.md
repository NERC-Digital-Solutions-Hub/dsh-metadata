# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness of the wider countryside; external users cannot identify whether squares fall within defined areas below a 100 square km precision.
- CS field survey data come from a sample of 1 km squares in Great Britain, with measurements taken at two levels: for the whole square and for features within the square. Measurements vary from binary to continuous variables.

## Sampling design and representativeness

- The sample is not a random subset of all GB squares; it is stratified by the ITE Land Classification. The land-class classification has evolved:
  - Original 32 classes
  - 1998 update to 42 classes (Scotland reporting)
  - 2007 update to 45 classes (Wales reporting)
  - Separate classifications per country: England (21), Wales (8), Scotland (16)
- Some squares were excluded from field survey based on their area (as measured on 1:250,000 OS maps): more than 90% sea or more than 75% urban. Official estimates assume vegetative land in excluded squares is similar to sampled squares; bias is expected to be small but can be problematic in regions with high sea/urban proportions.
- Estimates derived from CS data use ratio estimation by land class, weighting by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness concerns.

## Data structure and content

- Two levels of data:
  - Square-level data: information characterising the entire 1 km square.
  - Within-square data: measurements describing features inside each square (e.g., vegetation, soils).
- Variables range from binary to continuous (e.g., areas, lengths), requiring careful aggregation and interpretation in GIS analyses.
- Location precision for mapping remains intentionally coarse to protect confidentiality.

## Estimation, uncertainty, and caveats for GIS work

- Estimates are stratified by land class with weights based on vegetative land area; direct unstratified estimates may misrepresent variation.
- Bootstrap-based standard errors (since 1998) provide uncertainty estimates, which should be incorporated into map symbology and decision-making.
- Because the sampling is not random and is stratified, users should account for stratification in analyses to avoid misinterpreting variation and representation.

## Practical implications for GIS mapping and analysis

- When mapping CS-derived metrics, incorporate land-class stratification and area-based weights.
- Exercise caution in interpreting estimates for regions with high proportions of excluded squares (sea/urban) or limited vegetative land.
- Ensure alignment with the country-specific land-class classifications when aggregating or comparing across England, Wales, and Scotland.
- Be mindful of data confidentiality constraints that limit precise geolocations, which may affect fine-scale spatial analyses but not broader regional patterns.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.