# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK.
- Based on species occurrence records across 11 taxonomic groups and two time periods.
- Uses a relative measure of estimated species richness to assign ecological status to 10 km grid squares (hectads).

## Data sources and scope
- Collated UK species occurrence data from the Biological Records Centre (BRC).
- Taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants.
- Spatial unit: 10 km × 10 km hectads (grid squares).
- Time periods: 1970–1990 and 2000–2013.
- For vascular plants, non-native species were excluded.
- Bird occurrence data for breeding birds obtained from the British Trust for Ornithology (BTO), for two atlases (1976 and 2001–2011).

## Methodology and indicators
- For each time period and each taxonomic group, compile a species list per hectad and calculate species richness.
- Apply FRESCALO (Hill 2012) to account for variation in recorder effort across hectads.
- Assign each hectad to an environmental zone based on land cover type, climate, geology, and topography.
- Environmental zones are derived from the 2007 ITE land classification (45 classes in total).
- For each environmental zone, compile a reference list of potential species; compare hectad richness to the zone’s potential richness to estimate ecological status.
- Ecological status for each hectad is the mean of relative richness (proportion to potential richness) across all taxonomic groups for the 2000–2013 period.
- Final comparative benchmark: ecological status is measured relative to the maximum potential richness observed in the 1970–1990 period.
- See Dyer et al. (2016) for detailed methodology.

## Data structure and key columns
- gridSquare: Ordnance Survey National Grid reference for the 10 km square.
- Easting: x-coordinate (metres) of the southwest corner in British National Grid.
- Northing: y-coordinate (metres) of the southwest corner in British National Grid.
- dominantLandClass: Dominant 2007 ITE land class for the 10 km square (45 classes).
- ecologicalStatus: Mean ecological status for the hectad (relative richness measure).

## Land classification 2007 and environmental zones
- 45 ITE land classes used to define environmental zones indicative of similar abiotic conditions.
- Classifications include a range of landscapes (e.g., flood plains, coastal plains, upland valleys, sea cliffs, river floodplains, various hills and ridges, coastal/mountain combinations across England, Scotland, and Wales).
- These zones enable the comparison of observed richness to a zone-specific potential species list.

## Data availability
- UK ecological status map version 2 is available from the Environmental Information Data Centre (EIDC).
- DOI: 10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2

## References and notes
- Bunce et al. 2007. ITE Land Classification of Great Britain 2007.
- Dyer, R.; Oliver, T. (2016). UK ecological status map version 2. NERC EIDC.
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution.