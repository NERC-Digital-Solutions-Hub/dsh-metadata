# Data collected on Mt Etna in 2017

## Overview
- Field transplant study conducted in 2017 on Mt Etna.
- Cuttings sampled from natural populations of two Senecio species: S. aethnensis (AE) and S. chrysanthemifolius (CH).
- Propagated in glasshouse, then transplanted at four elevations.
- Collected data on plant survival (across seasons) and leaf morphology/size metrics.

## Experimental design and scope
- Species and genotypes:
  - AE: Genotypes from Etna South (ES) and Etna North (EN).
  - CH: Genotypes from five sites around Mt. Etna’s base.
- Source/site information:
  - Altitude: Elevation of source populations (for AE and CH).
- Transplant design:
  - Transplants at four transplant elevations (TGSite).
  - Experimental layout includes TGBlock (replicate blocks) and Grid (plant location within each block; genotype randomized to grid locations).
- Survival measurements:
  - Survival.09.09: Survival by 9 September.
  - Survival.April.18: Survival by spring (following year).
  - totaldays: Total days survived (used for survival analyses).
  - Censor: Censor day at end of experiment (for survival analyses).
- Morphology measurements:
  - Height (mm), LeafWeight (g), nleaves (count of leaves measured), Area (leaf area in mm2).
  - P2A (perimeter squared divided by Area), Nind (indentations divided by perimeter), IndentWidth, IndentDepth, Circularity, SLA (leaf area divided by weight).
- Data processing:
  - Leaf morphology calculated using the Lamina software.
  - NA entries indicate plants with survival data collected but leaves not collected because of death prior to sampling.

## Data quality, metadata, and processing notes
- Variable naming and units are explicit (e.g., Area in mm2, Height in mm, SLA as area/weight).
- Morphology data depend on Lamina-derived calculations; consistent methodology is implied.
- NA handling explained: some plants have survival data but no leaf measurements due to early death.
- Data ready for integration into data portals and catalogue systems with clear field definitions.

## Key considerations for data stewardship
- Standards and interoperability:
  - Ensure consistent coding for Species (AE, CH) and Sites, with clear mapping of source sites to each species.
  - Maintain uniform units and calculation methods (e.g., Lamina-derived morphology metrics).
- Data availability and updates:
  - Prepare dataset for sharing with metadata detailing experimental design, variables, and processing steps.
  - Track any updates to genotype provenance, site classifications, or measurement protocols.
- Accessibility and discoverability:
  - Include sufficient metadata for discoverability (site elevations, TGSite, TGBlock, Grid, and variable definitions).
- Potential challenges:
  - Harmonizing data across sites and populations, given multiple source sites and transplant elevations.
  - Maintaining data integrity when integrating survival data with morphology data (timing of measurements relative to survival status).
  - Handling legacy or outdated formats if integrating with older databases or systems.
- Use cases:
  - Survival analysis across species and environmental gradient.
  - Comparative leaf morphology and allometry under different transplant elevations.