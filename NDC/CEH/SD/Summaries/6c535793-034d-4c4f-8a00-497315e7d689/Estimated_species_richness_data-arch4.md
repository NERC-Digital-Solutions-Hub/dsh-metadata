# Estimated species richness data used in study of UK ecological status

## Data sources
- UK species occurrence data from the Biological Records Centre (BRC).
- 11 taxonomic groups at 10 km2 hectad scale: Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshopper and Crickets, and Vascular plants.
- Time periods: 1970–1990 and 2000–2013 (two separate datasets).
- Bird data for breeding birds sourced from the British Trust for Ornithology (BTO), corresponding to atlases from 1976 and 2001–2011.

## Data processing
- Separate analyses conducted for both time periods within each taxonomic group.
- For each hectad, compile a species list and calculate observed species richness.
- Estimate species richness using Frescalo to account for variation in recorder effort across hectads.

## Frescalo methodology and implementation
- Frescalo estimates within-hectad richness based on the neighbourhood of the 100 most similar hectads from the 200 nearest hectads.
- The proportion of a set of common benchmark species from the neighbourhood that are recorded in the focal hectad is used to assess recording intensity and adjust observed richness toward the neighbourhood maximum.
- Analyses performed in R using the Sparta package (August, Harrower & Isaac 2013).

## Neighbourhoods and data used
- Neighbourhoods defined by biological similarity using either vascular plant data or land cover type.
- All datasets analysed using vascular plant weights embedded in Frescalo, except the vascular plants dataset which used land cover type to define similarity to avoid circularity.
- Land cover data based on the 2007 ITE Land Cover Map (Morton et al. 2011).

## References and tools
- Sparta package for R (August, Harrower & Isaac 2013).
- Dyer et al. (in press) – developing an indicator of biodiversity for large-scale environmental assessment.
- Hill (2012) – local frequency as a key to interpreting species occurrence data with unknown recording effort.
- Morton et al. (2011) – Final Report for LCM2007, UK Land Cover Map.
- R Core Development Team (2011) – R statistical computing environment.