# Estimated species richness data used in study of UK ecological status

## Overview
- Describes how UK species occurrence data were used to estimate species richness for ecological status assessment.
- Aims to account for variation in recorder effort and enable comparison across time and space.

## Data sources and scope
- Data from the Biological Records Centre (BRC) for 11 taxonomic groups (Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshoppers and Crickets, Vascular plants).
- Spatial scale: 10 km2 hectads.
- Time periods: 1970–1990 and 2000–2013 (two separate datasets per taxon/period).
- Bird data from the British Trust for Ornithology (BTO) for two atlases: 1976 and 2001–2011.
- Separate analyses conducted for each taxon and time period.

## Methodology for estimating richness
- For each hectad, a species list is compiled and raw richness is calculated.
- Frescalo (Hill 2012) used to estimate true richness by correcting for uneven recording effort.
- Frescalo concept: richness is estimated based on the neighbourhood of the 200 nearest hectads, using the 100 most similar to the focal hectad to gauge recording intensity and scale toward the neighbourhood maximum.
- Analysis performed using the Sparta R package (August, Harrower & Isaac 2013) in R.

## Neighbourhoods and similarity benchmarks
- Neighbourhoods defined by biological similarity; used to determine recording intensity.
- For most datasets: vascular plant weights from Frescalo embedded in Sparta.
- For the vascular plants dataset: similarity defined using land cover type to avoid circularity.
- Land cover reference: 2007 ITE Land Cover Map (Morton et al. 2011).

## Data processing and outputs
- Separate analyses by time period and taxonomic group.
- Outputs: estimated species richness per hectad, adjusted for recording effort, enabling more comparable indicators across space and time.

## Tools, replication, and governance
- Software: Frescalo (R-based method), Sparta R package, R programming language.
- Emphasizes reproducibility and methodological transparency for monitoring purposes.

## Implications for monitoring frameworks
- Demonstrates a robust approach to derive biodiversity indicators from presence-only/unstructured data by correcting for sampling effort.
- Facilitates comparability of biodiversity indicators across different years and regions.
- Highlights the importance of metadata, data provenance, and standardized benchmarks to enable replication and policy use.
- Addresses practical challenges in monitoring data: data gaps, variable access, and need for consistent data governance and sharing.

## References (key sources)
- Frescalo method: Hill (2012)
- Sparta R package: August, Harrower & Isaac (2013)
- Dyer et al. (in press) on biodiversity indicators
- LCM2007: Morton et al. (2011)
- R Core Development Team (2011)