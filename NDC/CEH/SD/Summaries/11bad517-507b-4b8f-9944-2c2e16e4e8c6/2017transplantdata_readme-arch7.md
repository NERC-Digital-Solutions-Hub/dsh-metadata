# Data collected on Mt Etna in 2017

## Overview
- Field transplant study on Mt Etna (2017): cuttings from natural populations of two Senecio species were propagated in a glasshouse and transplanted at four elevations.
- Collected data include survival outcomes and leaf morphology measurements.

## Spatial and experimental structure
- Source sites (genotype origins):
  - AE (S. aethnensis): ES = Etna South, EN = Etna North
  - CH (S. chrysanthemifolius): five sites around Mt. Etna base
- Transplant context:
  - TGSite: elevation of transplant sites
  - TGBlock: replicate experimental blocks in the field
  - Grid: plant grid location within each block (genotype randomised to grid locations)
- Data captured to support spatial and temporal analyses of survival and morphology

## Variables (attributes)
- Species: AE = S. aethnensis, CH = S. chrysanthemifolius
- Genotype: genotype ID from natural populations
- Site: source site (defined above for AE and CH)
- Altitude: altitude of the source populations
- TGSite: transplant-site elevation
- TGBlock: transplant block identifier
- Grid: plant grid location within each block
- Survival.09.09: survival status by 9 September
- Survival.April.18: survival status by spring following year
- totaldays: total days survived (for survival analysis)
- Censor: censor day at end of experiment (for survival analysis)
- Height: plant height (mm)
- LeafWeight: total leaf weight (g)
- nleaves: number of leaves measured
- Area: leaf area (mm2)
- P2A: leaf complexity (perimeter^2 / area)
- Nind: number of indents per perimeter
- IndentWidth: width of leaf indentations
- IndentDepth: depth of leaf indentations
- Circularity: leaf circularity proxy
- SLA: specific leaf area (area / weight)

## Notes on data and preparation
- Leaf morphology metrics computed using the software Lamina
- NA values indicate plants for which survival data were collected but leaves were not (died before sampling)

## Potential GIS uses
- Map origin vs. transplant sites to visualize spatial survival and adaptation across elevations
- Create choropleth or point maps of survival probabilities by site, altitude, and species
- Link morphometric data to spatial location for landscape-level trait analyses
- Integrate with other spatial datasets to explore environmental drivers of survival and morphology across Mt Etna<|grid|>