# Sampling design

## Overview
- Describes how soils were sampled in Countryside Survey (CS) across 1978, 1998, 2007 and 2019 rolling survey, including pilot in 2018.
- Rolling survey aims to measure approximately 100 CS squares per year for five years before repeating.
- Emphasizes data structure, sampling depth, measurements, and implications for statistical analyses and GIS mapping.

## Sampling framework and locations
- Soils are sampled from CS X-plots within each square; there are 5 X-plots randomly spaced in a square.
- X-plots are not replicates; they may differ in land use, soil type, etc.
- Each sampling location has a unique repeat identifier (e.g., 2RPT1), enabling cross-year linkage.
- Actual sampling location within a square may shift by ~2–3 m between years due to plot destruction, access issues, or relocation uncertainty.
- Within a square, up to five X-plots are used; plots are spread around a permanently marked 2 m × 2 m sampling area.

## Temporal design
- 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares with some measurements missing.
- 2018/2019–2023 rolling survey adopts ongoing sampling to build a time-series.

## Sampling depth and methods
- Top 15 cm sampled in 1998, 2007, and rolling survey (8 cm depth for invertebrate samples).
- 1978 used a soil pit and sampled the top 15 cm from the pit side.
- Some cores cannot reach full 15 cm due to stones or shallow soils.
- In 2007, core photographs and measurements of core dimensions were taken for a subset of cores (black cores and N mineralization cores).
- Rolling CS survey continued with the core-based approach.

## Measurements and laboratory work
- 1978: pH and loss-on-ignition (LOI) only.
- 1998 onward: multiple cores per X-plot; different cores may have different measurements.
- Bulk density measured in 2007 and again in 2018/19–2023, though not using ISO bulk density methods (which would require a full core).
- No chemical analyses by soil horizon; samples are homogenised before pH and LOI measurements.
- A full description and implications are documented in Emmett et al. (2008).

## Data structure and limitations
- Not all measurements are made on every sample; data can be incomplete.
- Design and analysis considerations emphasize accounting for land class structure to avoid biased estimates.
- Bootstrapping is not consistently used in analyses.
- The CS structure (multiple X-plots per square) warrants models with square as a random factor to reflect nesting.

## Statistical considerations for GIS analyses
- When land class structure is ignored, outputs reflect stock and change of the population rather than national estimates.
- At minimum, use a mixed model with square as a random factor to account for multiple X-plots per square.
- Dispersed, widespread sampling enhances regional precision and coverage when spatial structure is not the primary interest.

## Practical guidance for GIS workflows
- Capture and maintain: square geometry, X-plot locations, repeat identifiers, year of sampling, depth, and measured variables (pH, LOI, bulk density).
- Track relocations and offsets to preserve cross-year traceability via repeat identifiers.
- Represent sampling design in GIS with layers for squares, X-plots, and time-series points.
- Annotate data with method notes (e.g., non-ISO bulk density method) and incomplete measurements.

## References
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.