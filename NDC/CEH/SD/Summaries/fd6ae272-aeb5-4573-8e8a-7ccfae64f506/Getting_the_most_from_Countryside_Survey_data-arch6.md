# Notes on the downloadable data

## Key confidentiality and data precision
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by UKCEH.
- External users receive location precision no finer than 100 square kilometers; you cannot identify whether squares fall within defined areas below this threshold.

## Sampling design and data structure
- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: the square as a whole and features within the square.
- Measurements vary from binary to continuous (e.g., areas, lengths).
- The squares are not a random subset; sampling is stratified by ITE Land Classification.
- Land classification has evolved:
  - Original: 32 classes
  - 1998: 42 classes (Scotland reporting prompted change)
  - 2007: 45 classes (Wales reporting prompted change)
- England, Wales, and Scotland have country-specific class counts (England 21, Wales 8, Scotland 16).
- Some squares are excluded from field survey: if area from 1:250,000 OS maps is >90% sea or >75% urban.
- Official GB estimates are based on the included squares; extrapolation assumes excluded squares have similar vegetative land composition to included squares. This assumption minimizes bias overall but can be problematic if a region contains many sea/urban squares.

## Representation and analysis considerations
- Estimates are produced as ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area within that class.
- From 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) due to concerns about skewness in some features.

## Practical guidance for data users
- When analyzing CS data, account for the stratified sampling design rather than treating it as a simple random sample.
- Use land-class-based weights to produce GB-wide or regional estimates; be mindful of the impact of excluded squares.
- Rely on bootstrap-derived standard errors and confidence intervals to assess uncertainty.
- Be cautious when generalizing results to regions with high proportions of sea or urban squares; consider potential biases if regional composition differs from the sampled squares.
- The outputs are suited for self-service exploration, dashboards, and reports; integrating with other datasets may enhance interpretability but must respect the sampling design.

## References
- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.