# Estimated species richness data used in study of UK ecological status

## Overview
- Describes the estimation of species richness for UK taxa using collated presence data and methods that adjust for uneven recording effort.
- Data are organized by 10 km2 hectads across two time periods: 1970–1990 and 2000–2013, covering 11 taxonomic groups.
- Birds data come from the British Trust for Ornithology (BTO) for corresponding periods.

## Data sources
- UK species occurrence data from the Biological Records Centre (BRC) for 11 taxonomic groups: Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshoppers and Crickets, and Vascular plants.
- Time periods: 1970–1990 and 2000–2013 (two separate datasets per taxon).
- Bird data for breeding birds obtained from BTO, using atlases from 1976 and 2001–2011.

## Methodology
- For each taxon and time period, a species list and raw species richness are compiled per hectad.
- Frescalo (Method to account for variation in recording effort) is applied to estimate corrected species richness.
  - Frescalo uses the neighbourhood concept: the 100 most similar hectads among the 200 nearest hectads.
  - The proportion of a set of common benchmark species recorded in the neighbourhood’s hectads assesses recording intensity and scales raw richness toward the neighbourhood maximum.
- Analyses are conducted separately for each taxon and time period.

## Implementation details
- Frescalo is run using the Sparta R package (August, Harrower & Isaac 2013) within the R statistical environment.
- Neighbourhood similarity is defined using vascular plant data or land cover type:
  - Most analyses use vascular plant weights embedded in Frescalo.
  - For the vascular plants dataset, neighbourhood similarity is defined using land cover type to avoid circularity, employing the 2007 ITE Land Cover Map (Morton et al. 2011).

## Outputs and interpretation
- Produces estimated species richness per hectad for each taxon and time period, adjusted for uneven recording effort.
- Facilitates assessment of biodiversity status at a fine spatial scale and over time, enabling comparisons across periods and taxa.

## Data products and reuse
- The approach provides a reproducible framework for turning unstructured presence-only data into comparable richness estimates across space and time.
- The method is designed to handle patchy data and varied data sources, making the outputs suitable for ecological status assessments and policy-relevant reporting.

## References
- August, T., Harrower, C. & Isaac, N. (2013) Sparta - An R package for estimating trends in species' status from unstructured, presence-only data., http://dx.doi.org/10.6084/m9.figshare.771963
- Dyer, R.J., Gillings, S.G., Pywell, R.F., Roy, D.B. & Oliver, T.H. (in press). Developing an indicator of biodiversity for large-scale environmental assessment: a case study on proposed shale gas extraction sites in Britain. Journal of Applied Ecology
- Hill, M.O. (2012) Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3, 195-205.
- Morton, D., Rowland, C., Wood, C., Meek, L., Marston, C., G, S., Wadsworth, R. & Simpson, I.C. (2011) Final Report for LCM2007 - the New UK Land Cover Map. Countryside Survey Technical Report No 11/07.
- R Core Development Team. (2011) R: a language and environment for statistical computing.