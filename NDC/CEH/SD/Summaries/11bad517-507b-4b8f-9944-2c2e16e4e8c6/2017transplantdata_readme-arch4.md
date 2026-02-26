# Data collected on Mt Etna in 2017

## Study design and scope
- Field transplant experiment across four transplant elevations on Mt Etna.
- Cuttings sampled from genotypes in natural populations of two Senecio species (AE = S. aethnensis; CH = S. chrysanthemifolius).
- Propagated in the glasshouse, then transplanted; survival and leaf morphology data recorded.

## Data variables and data types
- Identity and origin
  - Species: AE (S. aethnensis) or CH (S. chrysanthemifolius)
  - Genotype: genotype ID from source natural populations
  - Site: source site of genotypes (AE: ES Etna South, EN Etna North; CH: five base-area sites)
  - Altitude: source population elevation
- Experiment design and location
  - TGSite: transplant site elevation
  - TGBlock: replicate field blocks
  - Grid: plant grid location within each block (genotype randomized to grid)
- Survival data
  - Survival.09.09: survival by summer (9 September)
  - Survival.April.18: survival by following spring
  - totaldays: total days survived (for survival analysis)
  - Censor: censor day at end of experiment (survival analysis)
- Morphology and growth measurements
  - Height: plant height (mm)
  - LeafWeight: total leaf weight (g)
  - nleaves: number of leaves measured
  - Area: leaf area (mm2)
  - P2A: leaf complexity (perimeter^2 divided by area)
  - Nind: number of leaf indentations divided by perimeter
  - IndentWidth: width of leaf indentations
  - IndentDepth: depth of leaf indentations
  - Circularity: how close leaf is to a circle
  - SLA: specific leaf area (leaf area divided by weight)

## Data collection process and tools
- Leaf morphology calculated using the Lamina software.
- Notes: NA entries indicate plants with recorded survival data but that died before leaf sampling.

## Data quality, metadata, and provenance
- Clear, structured fields capturing species, origin, transplant location, and timing.
- Derived metrics (P2A, SLA) calculated from primary measurements.
- Metadata considerations: units (mm, g, mm2), treatment of censored data, and labeling of transplant blocks and grid positions.
- Data gaps: some plants have survival data but no leaf measurements due to mortality before sampling.

## Accessibility, usage, and governance considerations for data leaders
- Potential analyses: compare survival across species, sites, and elevations; relate genotype origin to survival; assess leaf morphology trait variation by environment.
- Data integration opportunities: pair with environmental/climate data from transplant sites; combine with other phenotypic datasets for cross-study synthesis.
- Data management actions to support discovery and reuse
  - Maintain consistent unit conventions and clear provenance (source site, transplant site, block, grid).
  - Preserve distinctions between source-site altitude and transplant-site altitude.
  - Ensure clear documentation of censoring rules and survival-time calculations.
  - Retain metadata indicating which plants lack leaf data due to early mortality (NA cases).
  - Confirm software-derived metrics (Lamina) and any versioning or parameter details for reproducibility.