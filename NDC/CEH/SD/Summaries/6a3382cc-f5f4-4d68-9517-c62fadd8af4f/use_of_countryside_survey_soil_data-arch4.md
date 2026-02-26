# Sampling design

## Overview
- Countryside Survey soils are collected in a rolling program to measure changes over time, with historic rounds in 1978, 1998, 2007 and 2019, and a pilot in 2018 followed by a rolling survey from 2019 aiming to sample ~100 squares per year for five years before repeating.
- Earlier rounds used fixed square sets (1978 and 1998: 256 squares; 2007 added all 591 CS squares but not all measurements on every sample). The rolling survey adapts sampling frequency and coverage.

## Sample locations and plot structure
- Samples come from CS X-plots within CS squares; each square contains 5 randomly spaced X-plots.
- X-plots within a square are not replicates; they can differ in land use and soil type.
- Over time X-plots may be relocated if a plot is destroyed, access is denied, or certainty about location changes. Each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
- Samples with the same identifier are from the same location, but exact sampling spots are typically 2–3 m apart around a permanently marked 2 m x 2 m plot corners.

## Sampling methods
- Soils are sampled from the top 15 cm of the profile (8 cm for the invertebrate sample).
- 1998 and 2007 used core sampling; 2019 rolling survey continued core-based sampling. 1978 used a soil pit to access the top 15 cm.
- In some soils, full 15 cm cores could not be collected due to stones or shallow soils.
- Core measurement details were partially recorded in 2007 (photographs and dimensions for two of the four cores; black cores and N mineralization cores). The rolling CS survey adopted that approach.

## Measurements and laboratory analyses
- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1998, 2007, and rolling survey: multiple cores per X-plot; cores may receive different measurements; samples are homogenised before pH and LOI analyses.
- Bulk density was measured in 2007 and again in 2018/19–2023, but not using ISO bulk density methods (which would require a full core).
- No chemical analyses are performed by soil horizon; the analysis protocol and implications are described in Emmett et al. 2008.

## Data handling and statistical considerations
- Analyses should account for land class structure; ignoring land classes yields stock-and-change estimates for the population, while including land classes yields weighted national estimates.
- Bootstrapping is not always used; CS’s design emphasizes the spatial structure. A mixed-effects model with square as a random factor is recommended to account for multiple X-plots (up to 5) within each square.
- CS adopts a design-based approach: dispersed, widespread sampling improves regional precision and coverage.
- For analysis and interpretation, users should consult UKCEH and review CS publications listed on the CS website to understand prior analyses and findings.

## Data governance, access, and usability
- The sampling framework ensures longitudinal comparability through repeat identifiers, even when plots are relocated.
- Documentation and methodological details (including power analyses and protocols) are available in Emmett et al. 2008 and related CS reports.
- Researchers should coordinate with UKCEH and review CS publications to ensure appropriate analysis and interpretation.

## Key caveats and limitations for users
- Not all measurements were taken on all samples in every year (e.g., 2007 had partial measurement coverage).
- The non-replicate nature of X-plots within squares and potential plot relocations can affect within-square comparability.
- Some measurements diverge from ISO-standard methods (e.g., bulk density), which should be considered in cross-year comparisons.

## References
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.