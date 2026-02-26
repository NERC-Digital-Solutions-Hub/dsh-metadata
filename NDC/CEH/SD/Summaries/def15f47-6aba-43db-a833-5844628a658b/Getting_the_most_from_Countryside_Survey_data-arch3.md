# Notes on the downloadable data

- To preserve representativeness of the wider countryside, the precise locations of Countryside Survey (CS) field squares are kept confidential by CEH. External users cannot identify whether any survey squares fall within defined areas below a precision finer than 100 square kilometers.

- CS field survey data are collected from a sample of 1 km squares across Great Britain. Each selected square is mapped and measured at two levels: the square as a whole and features within the square. Measurements vary from binary to continuous variables.

- The sampling design is not a random subset of all GB squares. It is stratified, with sub-samples drawn within designated strata defined by the ITE Land Classification. The classification has evolved (32 -> 42 -> 45 classes) to accommodate separate country reporting, yielding England, Wales, and Scotland with 21, 8, and 16 classes respectively.

- Some squares are excluded from field survey if, on 1:250,000 scale OS maps, their area is more than 90% sea or more than 75% urban. Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; this assumption introduces potential bias, typically small because the excluded land area is minor, except in regions with high sea/urban proportions.

- Estimation approach uses ratio estimates for each land class, weighted by the vegetative land area within each class. Since some features are skewed, standard errors and confidence intervals have been estimated using bootstrap methods since 1998.

- The document references key sources: Barr et al. (1993) for the CS 1990 Main Report, Cochran (1963) on sampling techniques, and Efron & Tibshirani (1993) on the bootstrap.

## Sampling Considerations in the use of Countryside Survey Data

- The two-tier sampling (whole square and within-square measurements) requires careful handling to avoid biased inferences, as not all GB squares are surveyed and stratification must be accounted for in analyses.

- The changing land-class classifications across years and differing country reporting necessitate attention to how estimates are formed and interpreted for England, Wales, and Scotland.

- Because of confidentiality and the non-random, stratified design, users should explicitly incorporate stratification, weighting by vegetative land area, and the potential non-representativeness of excluded areas when conducting analyses or making regional or national inferences.