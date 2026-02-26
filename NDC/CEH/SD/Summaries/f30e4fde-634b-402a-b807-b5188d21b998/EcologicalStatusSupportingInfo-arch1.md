# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK, derived from species occurrence records across 11 taxonomic groups.
- Data compiled at 10 km grid squares (hectads) and split into two time periods to assess changes in richness and ecological status.

## Data sources
- Species occurrence data collated from the Biological Records Centre (BRC) for 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants.
- Bird occurrence data for breeding birds from the British Trust for Ornithology (BTO) using atlases from 1976 and 2001-2011.

## Spatial and temporal scope
- Spatial unit: Ordnance Survey National Grid 10 km grid squares (hectads).
- Time periods: 1970–1990 and 2000–2013 (two separate analyses per taxonomic group).

## Data processing and methodology
- For each hectad and taxonomic group:
  - Compile a species list and calculate species richness.
  - Use the FRESCALO method to adjust for variation in recording effort across hectads.
- Ecological status assignment:
  - Classify hectads into environmental zones defined by land cover, climate, geology, and topography.
  - Environmental zones determined using the 2007 ITE land classification (45 classes) based on the dominant land class per hectad.
  - Create a reference list of potential species for each environmental zone; compute relative richness by comparing observed richness to the zone’s potential richness.
  - Compute mean ecological status across all taxonomic groups for 2000–2013, relative to the maximum potential richness observed in 1970–1990.
- The methodology and related details are described further in the manuscript under preparation; key methodological references include Hill (2012) for FRESCALO and Bunce et al. (2007) for the land classification scheme.

## Data product and structure
- Primary dataset: EcologicalStatusMap.csv
- Key columns:
  - gridSquare: Ordnance Survey National Grid 10 km grid reference
  - Easting: x-coordinate (metres) of the grid square’s southwest corner (British National Grid)
  - Northing: y-coordinate (metres) of the grid square’s southwest corner (British National Grid)
  - dominantLandClass: Dominant 2007 ITE land class for the hectad
  - ecologicalStatus: Mean ecological status for the hectad

## Land classification 2007
- Uses the 2007 ITE land classification (Bunce et al. 2007) to define 45 environmental zones that represent areas with similar abiotic conditions.
- Provides summary names and regional groupings for England, Scotland, and Wales to contextualize zone classifications.

## References
- Bunce, R. G. H., Barr, C. J., Clarke, R. T., Howard, D. C., & Scott, W. A. (2007). ITE Land Classification of Great Britain 2007. NERC-Environmental Information Data Centre. doi:10.5285/5f0605e4aa2a-48ab-b47c-bf5510823e8f
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195-205. doi:10.1111/j.2041-210X.2011.00146.x