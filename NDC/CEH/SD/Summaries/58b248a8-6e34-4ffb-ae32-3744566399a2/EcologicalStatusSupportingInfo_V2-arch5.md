# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- A spatial indicator of UK ecological status based on species occurrence data across 11 taxonomic groups.
- Generated at the 10 km grid (hectad) scale for two time periods: 1970–1990 and 2000–2013.
- Data compiled from UK sources and processed to account for uneven recording effort; ecological status is relative to potential species richness in environmental zones.

## Data sources and scope
- Taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants (non-native species excluded for vascular plants).
- Primary data providers: Biological Records Centre (BRC) and British Trust for Ornithology (BTO) for birds.
- Geographic scope: United Kingdom.
- Data coverage periods: two distinct periods per group (1970–1990 and 2000–2013).

## Methods and processing
- Richness estimation: for each hectad, compile species lists and calculate species richness; apply FRESCALO (Hill 2012) to adjust for variable recorder effort.
- Environmental zoning: assign each hectad to an environmental zone defined by land cover, climate, geology, and topography.
- Land classification: allocate zones using the 2007 ITE land classification (Bunce et al. 2007) with 45 classes to represent abiotic conditions.
- Ecological status: compute a relative measure of estimated species richness per hectad by comparing to a reference species list for each environmental zone; derive mean ecological status across all taxonomic groups for 2000–2013 relative to the 1970–1990 maximums.
- Documentation: methodology detailed in Dyer et al. (2016) with supporting references.

## Dataset structure and fields
- gridSquare: Ordnance Survey National Grid reference for the 10 km grid square.
- Easting: x-coordinate (British National Grid, metres) of the grid square’s southwest corner.
- Northing: y-coordinate (British National Grid, metres) of the grid square’s southwest corner.
- dominantLandClass: Dominant land class for the 10 km square (2007 version) from the ITE land classification.
- ecologicalStatus: Mean ecological status for the hectad.

## Land classification 2007
- Based on the 2007 ITE land classification (Bunce et al. 2007), consisting of 45 classes used to define environmental zones.
- Codes include a mixture of landform/types across England, Scotland, and Wales (e.g., coastal plains, upland valley systems, river floodplains, sea cliffs, etc.).
- The classification serves as the basis for comparing potential species richness across zones.

## Data availability and access
- UK ecological status map version 2 is available from the Environmental Information Data Centre (EIDC).
- DOI: 10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2.

## Version history and provenance
- 14/03/2014: Dataset created; versioning initiated.
- 28/04/2014: Name corrections and metadata updates.
- 02/02/2016: Added section on Land Classification 2007.
- 23/05/2016: Updated to version 2 of the dataset.
- 09/01/2017: Added references to Dyer et al. (2016) and data availability section; included supporting documentation.

## Limitations and considerations for data stewards
- Completeness of user needs and timely data provision can affect currency and usefulness.
- Data quality depends on consistent metadata and standardization across many data providers and formats.
- Varying data availability and embargoes may impact shareability and updates.
- Non-native species exclusion (for vascular plants) affects cross-taxa comparability.
- Large, multi-system datasets require careful governance regarding versioning, access controls, and update cycles.

## References
- Bunce, R. G. H., Barr, C. J., Clarke, R. T., Howard, D. C., & Scott, W. A. (2007). ITE Land Classification of Great Britain 2007. NERC- Environmental Information Data Centre. doi:10.5285/5f0605e4-aa2a-48abb47c-bf5510823e8f
- Dyer, R.; Oliver, T. (2016). UK ecological status map version 2. NERC Environmental Information Data Centre. https://doi.org/10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2
- Dyer, R. J., et al. (2016). Developing a biodiversity-based indicator for large-scale environmental assessment: a case study of proposed shale gas extraction sites in Britain. Journal of Applied Ecology. doi:10.1111/1365-2664.12784
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195–205. doi:10.1111/j.2041-210X.2011.00146.x
- Dyer, R.; Oliver, T. (2016). Supporting documentation for UK ecological status map version 2. https://doi.org/10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2