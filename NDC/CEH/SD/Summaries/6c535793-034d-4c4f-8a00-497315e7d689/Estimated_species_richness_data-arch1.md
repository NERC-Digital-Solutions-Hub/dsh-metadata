# Estimated species richness data used in study of UK ecological status

- Purpose and scope
  - Compile and estimate species richness to support assessment of UK ecological status.
  - Utilizes data from multiple taxonomic groups across two historical timeframes.

- Data sources and timeframes
  - UK species occurrence data from the Biological Records Centre (BRC) covering 11 taxonomic groups (Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshoppers and Crickets, Vascular plants).
  - Spatial resolution: 10 km2 hectads.
  - Time periods:
    - 1970–1990 and 2000–2013 (two separate datasets per taxonomic group).
  - Bird data specifics: breeding birds of the UK from the British Trust for Ornithology (BTO) atlases for 1976 and 2001–2011.

- Methodology
  - For each hectad, compile a species list and calculate observed richness.
  - Estimate true species richness using Frescalo (frequency-sensitive estimator) to account for variation in recorder effort.
    - Frescalo uses the neighbourhood concept: richness is estimated based on the 100 most similar hectads among the 200 nearest hectads.
    - The proportion of a set of common benchmark species recorded in the neighbourhood’s focal hectad assesses recording intensity and scales observed richness toward the neighbourhood maximum.
  - Implementation details
    - Analysis conducted separately for each time period within each taxonomic group.
    - Software: R (R Core Development Team 2011) with the Sparta package (August, Harrower & Isaac 2013).
    - Neighbourhood definitions and similarity
      - Defined by biological similarity using either vascular plant data or land cover type.
      - Most datasets analyzed with vascular plant weights from Frescalo; for the vascular plants dataset itself, similarity was defined using land cover type (to avoid circularity). The 2007 LCM2007 land cover map (Morton et al. 2011) was used for this purpose.

- Outputs and interpretation
  - Estimated species richness per hectad, adjusted for uneven recording effort, enabling comparisons across time periods and spatial locations.
  - Analyses provide a basis for biodiversity indicators and evaluations of ecological status at a large UK scale.