# Estimated species richness data used in study of UK ecological status

## Overview
- Presents estimated species richness data at 10 km2 hectad scale for 11 taxonomic groups, across two time periods, derived to account for uneven recorder effort and support ecological status assessments.

## Data sources and spatial units
- Primary sources: UK species occurrence data from the Biological Records Centre (BRC) for 11 groups (Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshoppers and Crickets, Vascular plants).
- Birds: data from British Trust for Ornithology (BTO) for two atlas periods (1976 and 2001–2011).
- Spatial unit: hectads (10 km2 grid cells) as the basic unit of analysis.
- Analyses conducted separately for each taxonomic group and each time period.

## Temporal scope
- Two time periods:
  - 1970 to 1990
  - 2000 to 2013
- Bird data aligned to two atlas-based periods: 1976 and 2001–2011.

## Methods and workflow
- Per hectad and taxon/period, compile a species list and calculate observed richness.
- Apply Frescalo (Hill 2012) to estimate true richness by adjusting for recording effort variation.
  - Frescalo concept: uses a neighbourhood of the 100 most similar hectads within the 200 nearest hectads.
  - The proportion of a benchmark set of common species recorded in the neighbourhood is used to scale observed richness toward the neighbourhood maximum.
- Implementation:
  - Frescalo run via Sparta R package (August, Harrower & Isaac 2013) in R.
  - Neighbourhood similarity defined using biological similarity; most datasets use vascular plant weight files embedded in Frescalo.
  - For the vascular plants dataset, biological similarity was defined using land cover type (to avoid circularity) with the 2007 ITE Land Cover Map (Morton et al. 2011).

## Spatial data processing notes
- Data integration involves harmonising multiple datasets with potentially different resolutions and recording efforts.
- Two separate analyses (by time period) were performed for each taxon to reflect temporal changes in richness.

## Outputs and applications
- Estimated species richness per hectad, by taxon and time period, adjusted for recording effort.
- Designed to support large-scale biodiversity indicators and environmental assessments (e.g., impact assessments for shale gas sites as cited in related work).

## References and tools
- Frescalo and Sparta R package (August, Harrower & Isaac 2013)
- Hill (2012) Local frequency methodology
- LCM2007 – UK Land Cover Map (Morton et al. 2011)
- R Core Development Team (R 2011)