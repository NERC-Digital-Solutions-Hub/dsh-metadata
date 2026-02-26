# Countryside Survey Soils 2007: Method development, power analyses and protocols

## Overview
- Document describes sampling design, measurement methods, and statistical considerations for CS soils across the years 1978, 1998, and 2007.
- Goal: detect significant change over time through power analyses and robust protocols.
- Key scope shift: 1978 and 1998 used 256 squares; 2007 expanded to sample all 591 CS squares, with measurements not always made on every sample.
- Sampling hierarchy: CS x-plots (5 per CS square) containing non-replicate locations; each location has a unique repeat identifier (e.g., 2RPT1).

## Sampling design and scope
- Sampling years and coverage:
  - 1978 and 1998: same 256 squares sampled.
  - 2007: all 591 CS squares sampled; not all measurements on all samples.
- Power analyses conducted to determine sample numbers needed to detect significant change (Emmett et al. 2008).

## Sample location and replication
- Soils sampled from CS x-plots within each CS square.
- x-plots are not replicates due to potential differences in land use, soil type, etc.
- Relocation occur for practical reasons (destruction, access, uncertainty); each location has a repeat identifier.
- Sampling location accuracy: typically within ~2–3 m of the intended 2 m x 2 m marked plot corners.

## Sampling procedures
- Depth and method:
  - 1998 and 2007: top 15 cm sampled using a soil core hammered into the soil; removed as a core.
  - 1978: soil pit dug with top 15 cm sampled from pit side.
  - In some soils, full core collection is not possible due to stones or shallow soils.
  - In 2007, core photographs and detailed core dimension measurements were recorded for two of the four cores (black cores and N mineralization cores).
- Invertebrate sampling depth: 8 cm.

## Measurements and measurements detail
- 1978: limited laboratory measurements (pH and LOI only).
- 1990s onward: multiple cores per x-plot; different cores had different measurements (see Table 1 reference).
- General measurement approach:
  - Samples homogenised before pH and LOI measurements (no chemical analyses by soil horizons).
  - Bulk density measured in 2007 (not via ISO whole-core method).
  - Some measurements (e.g., metals, Olsen P, mineralisable N) were performed only for subsets of plots/cores.
- Variables recorded (examples from Table 1):
  - LOI, pH (in water and CaCl2), %C, %N, bulk density, core dimensions, photograph, depth of organic layer, hand texture, soil moisture, Olsen P, metals.
  - Measurements and sample counts varied by core type and year (e.g., original 256 squares vs. all 591 squares in 2007).
- Data release notes:
  - Some data marked with an asterisk were released only after the Soils Report published in November 2009.

## Data structure and accessibility considerations
- Data are tied to the CS square and the repeat location within each square; multiple x-plots per square.
- Not all measurements were taken for all cores or all years; users should reference the CS website and Emmett et al. (2008) for full protocols and the data release specifics.
- Table 1 in the document enumerates the different measurements and the number of samples per category (e.g., which measurements were available for all 591 squares vs. only original 256 squares).

## Statistical analysis guidance
- Important to account for land class structure:
  - If land classes are ignored, results reflect stock/change of the population rather than national estimates.
  - If land classes are included, results are weighted toward national estimates.
- Bootstrapping is not consistently used; recommended analytic approach often requires a mixed-model framework.
- Suggested model specification:
  - Use a mixed model with square as a random factor to account for multiple x-plots within each square.
- Design considerations:
  - CS uses a dispersed set of observations, which is efficient for broad regional estimates.
  - When regional estimates are desired, wider spatial coverage improves precision.
- Advisory notes:
  - Users should consult CEH before analysis and interpretation.
  - Review publications exploiting CS data that are listed on the CS website.

## Practical implications and caveats
- Data coverage is year- and measurement-specific; careful alignment of years, squares, and cores is required for trend analysis.
- Some data are only released post-2009; researchers should verify data availability and any usage restrictions.
- Measurement methods evolved over time (e.g., depth, cores, bulk density methodology), which should be harmonized or accounted for in analyses.

## Reference
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.