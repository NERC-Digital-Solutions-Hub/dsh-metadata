# Data collected on Mt Etna in 2017

## Overview
- In 2017, a field transplant experiment was conducted on Mt Etna.
- Cuttings were sampled from genotypes in natural populations, propagated in a glasshouse, and transplanted at four elevations.
- Survival and leaf morphology data were collected for analysis.

## Dataset structure and scope
- Two Senecio species were studied:
  - AE: S. aethnensis
  - CH: S. chrysanthemifolius
- Genotype: identifier of the source individual from natural populations.
- Source site (Site): origin of the genotypes
  - AE: ES = Etna South, EN = Etna North
  - CH: five sites around Mt. Etna base
- Altitude: elevation of the source population (where the cuttings came from)
- TGSite: elevation of the transplant site
- TGBlock: replicate blocks in the field
- Grid: plant location within each block (genotype randomized to different grid locations)

## Measured variables
- Survival data (time-to-event):
  - Survival.09.09: survival after Summer (to 9 September)
  - Survival.April.18: survival after winter (to following spring)
  - totaldays: total days survived (for survival analysis)
  - Censor: censor day at end of experiment (for survival analysis)
- Growth/morphology (measured traits):
  - Height: plant height (mm)
  - LeafWeight: total leaf weight (g)
  - nleaves: number of leaves measured
  - Area: leaf area (mm2)
  - P2A: leaf complexity (perimeter squared divided by area)
  - Nind: number of indentations divided by perimeter
  - IndentWidth: width of leaf indentations
  - IndentDepth: depth of leaf indentations
  - Circularity: how close the leaf is to a circle
  - SLA: specific leaf area (area divided by weight)

## Notes on data collection and processing
- Leaf morphology metrics were calculated using the software Lamina.
- NA entries indicate plants for which survival data were collected, but the plant died before leaves could be sampled.

## Data quality and interpretation considerations
- Data capture spans multiple sites, species, and transplant elevations, enabling cross-site and cross-species comparisons of survival and leaf morphology.
- Survival analyses rely on totaldays and censoring information; careful handling of censored data is required.
- Morphological measures may have missing values (NA) for plants that did not have leaf samples due to early mortality; consider imputation or analysis that accommodates missing traits.

## Potential uses
- Compare survival outcomes across species, genotypes, source sites, and transplant elevations.
- Explore relationships between leaf morphology traits and survival or environmental conditions.
- Create self-serve data products (dashboards, charts) to enable stakeholders to explore survival and leaf trait patterns.