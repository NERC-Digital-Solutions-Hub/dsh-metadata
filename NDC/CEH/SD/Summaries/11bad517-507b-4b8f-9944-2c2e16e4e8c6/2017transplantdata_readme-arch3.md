# Data collected on Mt Etna in 2017

- Objective and design
  - Field transplant study conducted in 2017
  - Cuttings sampled from genotypes in natural populations
  - Propagated in a glasshouse, then transplanted at four elevations
  - Collected survival data and leaf morphology data

- Subjects and study system
  - Species: AE = S. aethnensis; CH = S. chrysanthemifolius
  - Genotype: genotype ID from individuals in natural populations
  - Source sites: AE from Etna South (ES) and Etna North (EN); CH from five sites around Mt. Etna base
  - Source elevation: Altitude of the sampled source populations

- Experimental design and metadata
  - TGSite: Transplant site elevation
  - TGBlock: Replicate experimental blocks in the field
  - Grid: Plant grid location within each block (genotype randomized to grid locations)

- Measurements and timing
  - Survival data
    - Survival.09.09: Survival after Summer (to 9 September)
    - Survival.April.18: Survival after winter (to spring following year)
    - totaldays: Total days each plant survived (for survival analysis)
    - Censor: Censor day at end of experiment (used in survival analysis)
  - Morphology and growth
    - Height: Plant height (mm)
    - LeafWeight: Total leaf weight (g)
    - nleaves: Number of leaves measured
    - Area: Leaf area (mm2)
    - P2A: Leaf complexity (perimeter squared divided by area)
    - Nind: Number of indents divided by perimeter
    - IndentWidth: Width of leaf indentations
    - IndentDepth: Depth of leaf indentations
    - Circularity: How close the leaf shape is to a circle
    - SLA: Specific leaf area (area divided by weight)

- Data processing notes
  - Leaf morphology calculated using the software Lamina
  - NA entries indicate plants for which survival data existed but leaves were not sampled because of death

- Data quality and governance considerations (context for monitoring frameworks)
  - Data encompass multi-level design (species, genotype, site, altitude, block), enabling assessment of environmental gradients and genotype-by-environment interactions
  - Clear temporal data points (two survival checks) plus continuous growth metrics support survival analysis and growth-morphology relationships
  - Metadata fields (Site, Altitude, TGSite, TGBlock, Grid) support traceability, replication, and data governance
  - Public availability of underlying data is implied by the need to share data used, though this document notes that data processing steps (e.g., Lamina-derived metrics) and data completeness (NA cases) are explicitly documented
  - Potential data quality considerations include: completeness of survival and morphology data, alignment between source and transplant sites, and transformation/standardization requirements for cross-site comparisons