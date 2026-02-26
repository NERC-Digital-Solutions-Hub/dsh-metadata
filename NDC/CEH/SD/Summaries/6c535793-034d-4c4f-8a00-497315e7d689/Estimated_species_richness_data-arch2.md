# Estimated species richness data used in study of UK ecological status

- Scope of data
  - UK species occurrence data from the Biological Records Centre (BRC) for 11 taxonomic groups: Bees, Birds, Bryophytes, Butterflies, Carabidae, Hoverflies, Isopoda, Ladybirds, Moths, Grasshoppers and Crickets, and Vascular plants.
  - Spatial scale: 10 km2 hectads.
  - Time periods: 1970–1990 and 2000–2013 (two separate datasets per taxon).
  - Bird data specifically from the British Trust for Ornithology (BTO) atlases for 1976 and 2001–2011.

- Data processing and quality control
  - For each hectad and time period, a species list was compiled and raw richness calculated.
  - To account for uneven recording effort, richness was estimated using Frescalo (Hill 2012) via the Sparta R package (August, Harrower & Isaac 2013).

- Frescalo methodology
  - Estimates local richness based on the neighbourhood of the 100 most similar hectads within the 200 nearest hectads.
  - The neighbourhood list’s proportion of a suite of common benchmark species recorded in the focal hectad gauges recording intensity; this scales the raw richness toward the neighbourhood maximum.
  - Analyses run separately for each taxon and each time period.

- Neighbourhood definition and similarity measures
  - Biological similarity used to define neighbourhoods:
    - Typically based on vascular plant data or land cover type.
  - All datasets analyzed using vascular plant weights; for the vascular plants dataset itself, land cover type was used to define similarity to avoid circularity.
  - Land cover reference: 2007 ITE Land Cover Map (Morton et al. 2011).

- Outputs and application
  - Generated estimated species richness values for each hectad, taxon, and time period.
  - Intended as indicators of biodiversity status for large-scale environmental assessment (e.g., case study on shale gas sites in Britain as per Dyer et al., in press).

- Tools and references
  - Frescalo implemented via Sparta package in R.
  - Key references: August et al. 2013 (Sparta), Hill 2012 (local frequency and recording effort), Morton et al. 2011 (LCM2007), Dyer et al. (in press) for biodiversity indicators.