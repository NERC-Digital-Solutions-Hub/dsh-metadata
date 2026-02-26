# Sampling design

- Purpose: Describe the design and methods used for Countryside Survey Soils across multiple years to detect significant changes and inform data collection and analysis for GIS-based mapping and interpretation.
- Scope: Soils were sampled in 1978, 1998, and 2007 with varying square and plot coverage to support power analyses for change detection (Emmett et al. 2008).

## Sampling framework and coverage

- Years and sampling intensity:
  - 1978 and 1998: same 256 squares sampled.
  - 2007: expanded to all 591 CS squares, with not all measurements taken on every sample.
- Power analyses: conducted to determine the number of samples needed to detect significant change.
- Plot structure within squares:
  - Soils are sampled from CS x-plots; each CS square contains 5 x-plots randomly spaced.
  - X-plots within a square are not replicates (they may differ in land use, soil type, etc.).
- Repeat sampling and relocation:
  - Over time, x-plots may be relocated due to land use changes, access, or uncertainty in original locations.
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
  - Samples with the same identifier come from the same location, though exact sampling points are typically ~2–3 m apart around a permanently marked 2 m × 2 m plot.

## Sampling methods and depths

- Depth of sampling:
  - 1998 and 2007: top 15 cm of soil (8 cm depth for invertebrate samples).
  - 1978: top 15 cm sampled from a soil pit rather than a core.
- Sampling technique:
  - 1998 and 2007: multiple cores taken per x-plot; cores hammered into soil and pulled out.
  - 1978: soil pit method used.
- Core documentation:
  - In 2007, core photographs and detailed measurements of core dimensions were made for some cores (2 of the 4 cores).

## Measurements and data collected

- Laboratory measurements (varied by year and core):
  - pH (in water and CaCl2), LOI, bulk density (not by ISO method in 2007), %C, %N, several soil physical/chemical attributes, mineralisable N, soil moisture, Olsen P, metals, texture indicators, depth of organic layer, photographs, and other core-specific measurements.
- Measurement coverage:
  - In 2007, measurements were collected for all 591 squares for several variables, but not all measurements were made on all samples.
  - Some measurements were based on original 256 squares, while others covered all 591 squares.
- Data release notes:
  - Some measurements are indicated as data released only after the Soils Report published in November 2009 (marked with an asterisk in the source tables).

## Data analysis and interpretation guidance

- Statistical considerations:
  - Analyses should account for land class structure; ignoring land classes can bias estimates to stock/change of the population.
  - If land classes are accounted for, results become weighted national estimates of stock and change.
  - Bootstrapping is not always used; a mixed model with square as a random factor is recommended to reflect multiple x-plots per square.
  - In CS design-based contexts where spatial structure is not central, a dispersed set of observations can improve regional precision and coverage.
- Practical guidance:
  - Users should consult CEH prior to analysis and interpretation.
  - Review CS publications and the CS website for related data and analyses.

## Data availability and references

- Data scope and release caveats:
  - Several measurements are tied to specific years or square sets (e.g., original 256 squares vs. all 591 squares) and not all measurements are available for all samples.
  - Some measurements are available only after the 2009 Soils Report.
- Key reference:
  - Emmett, BA et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. CEH project details (Emmett et al. 2008).