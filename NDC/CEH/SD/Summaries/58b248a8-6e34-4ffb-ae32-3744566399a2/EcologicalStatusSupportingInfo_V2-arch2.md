# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK, based on species occurrence records.

## Data sources and scope
- Data collated from the Biological Records Centre (BRC) for 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera and vascular plants.
- Spatial scale: 10 km2 hectads.
- Time periods: 1970–1990 and 2000–2013.
- Vascular plants: non-native species excluded due to high proportions of non-natives in GB.
- Bird data for breeding birds drawn from the British Trust for Ornithology (BTO) atlases (1976 and 2001–2011).

## Methods
- For each hectad and time period, compile a species list and calculate species richness.
- Apply FRESCALO (Hill 2012) to account for variation in recorder effort across hectads.
- Ecological status is a relative measure of estimated species richness.
- Assign each hectad to an environmental zone defined by land cover, climate, geology and topography.
- Environmental zones are based on the 2007 ITE land classification (45 classes) using the dominant ITE land class in the hectad.
- Develop a zone-specific reference list of potential species; compare observed richness to potential richness.
- Compute mean ecological status across all taxonomic groups for 2000–2013, relative to the maximum richness observed in 1970–1990.
- Further methodological details are provided in Dyer et al. (2016).

## Data structure and columns
- gridSquare: Ordnance Survey National Grid 10 km reference.
- Easting: x-coordinate (metres) of the southwest corner (British National Grid).
- Northing: y-coordinate (metres) of the southwest corner (British National Grid).
- dominantLandClass: Dominant land class for the 10 km square (2007 version) from ITE classification.
- ecologicalStatus: Mean ecological status for the hectad.

## Land Classification 2007
- Based on the 2007 ITE land classification (Bunce et al. 2007) with 45 classes used to define environmental zones.
- The 45 classes cover diverse landforms, including flood plains, hills, plains, coasts, valleys, upland areas, and regional distinctions across England, Scotland, Wales.
- Examples include classifications for flood plains, low calcareous hills, flat plains, coastal plains, upland valleys, and various coastal and mountain environments.

## Outputs and interpretation
- Spatially explicit ecological status values at the 10 km hectad level for the 2000–2013 period.
- Status is a relative measure, benchmarked against potential species richness per environmental zone and against the 1970–1990 baseline.
- Useful for national biodiversity valuation and monitoring environmental health over time.

## Data availability
- UK ecological status map version 2 is available from the Environmental Information Data Centre (EIDC): https://doi.org/10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2
- Supporting documentation and references include Dyer & Oliver (2016) and Dyer et al. (2016).

## References
- Bunce, R. G. H. et al. (2007). ITE Land Classification of Great Britain 2007. NERC-EIDC. doi:10.5285/5f0605e4-aa2a-48abb47c-bf5510823e8f
- Dyer, R.; Oliver, T. (2016). UK ecological status map version 2. NERC EIDC. https://doi.org/10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2
- Dyer, R. J. et al. (2016). Developing a biodiversity-based indicator for large-scale environmental assessment: a case study of proposed shale gas extraction sites in Britain. Journal of Applied Ecology. doi:10.1111/1365-2664.12784
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195-205. doi:10.1111/j.2041-210X.2011.00146.x